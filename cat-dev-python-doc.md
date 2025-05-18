# 使用Python对CATIA进行二次开发

要驱动CATIA，您可以使用Python与CATIA的COM接口进行交互。通过pywin32库，可以实现Python与Windows COM接口的通信，从而控制CATIA执行各种建模和自动化任务。安装pywin32库、连接到CATIA应用程序、获取和操作CATIA文档。其中，安装pywin32库是第一步，确保您的Python环境能够与Windows COM接口交互。

## 一、安装pywin32库
首先确保您的Python环境能够与Windows COM接口交互，可以通过以下命令安装pywin32库：
```bash
pip install pywin32
```

## 二、连接到CATIA应用程序
安装完pywin32库后，可以通过编写Python脚本连接到CATIA应用程序。首先，需要导入win32com.client模块并创建一个CATIA应用程序对象：
```
import win32com.client
catia = win32com.client.Dispatch("CATIA.Application")
```
这段代码创建了一个CATIA应用程序对象，允许您与CATIA进行交互。

## 三、获取和操作CATIA文档
### 创建新零件文档并添加几何体
通过这段代码，您可以创建一个新的零件文档，并在其中添加一个点几何体。
```
#创建新零件文档
documents = catia.Documents
part_document = documents.Add("Part")

#获取Part对象
part = part_document.Part

#创建一个几何体工厂对象
hybrid_shape_factory = part.HybridShapeFactory

#创建一个点
point = hybrid_shape_factory.AddNewPointCoord(0, 0, 0)

#添加几何体到零件中
part.HybridBodies.Item("Geometrical Set.1").AppendHybridShape(point)

#更新Part
part.Update()
```

## 四、操作实例
### 打开现有文档并获取几何体
这段代码演示了如何打开一个现有的CATIA文档并获取其中的几何体。您可以根据需要对几何体进行操作。
```
#定义要处理的文件路径
file_Path = "C:\\path\\to\\your\\part.CATPart"

# 打开现有文档
part_document = documents.Open(file_Path)

#获取Part对象
part = part_document.Part
bodies = part.Bodies

#获取几何体
body = bodies.Item("PartBody")
shapes = body.Shapes

#遍历几何体
for i in range(1, shapes.Count + 1):
    shape = shapes.Item(i)
    print(shape.Name)
```

### 创建草图并添加几何元素
如果您想在零件中创建草图并添加几何元素，可以使用以下代码：
```
# 创建一个草图
hybrid_bodies = part.HybridBodies
geometrical_set = hybrid_bodies.Item("Geometrical Set.1")
sketches = geometrical_set.HybridSketches
origin_elements = part.OriginElements
xy_plane = origin_elements.PlaneXY
sketch = sketches.Add(xy_plane)

#添加几何元素到草图中
factory_2d = sketch.OpenEdition()
point1 = factory_2d.CreatePoint(0, 0)
point2 = factory_2d.CreatePoint(100, 0)
line = factory_2d.CreateLine(0, 0, 100, 0)
line.StartPoint = point1
line.EndPoint = point2
sketch.CloseEdition()
part.Update()
```
## 五、自动化任务

通过Python脚本，您可以自动化许多CATIA任务，例如批量处理文件、生成报告、执行复杂的几何操作等。例如，您可以编写一个脚本来批量打开多个CATIA文档并提取其中的几何信息：
```
import os
#定义要处理的文件夹路径
folder_path = "C:\\path\\to\\your\\folder"
#遍历文件夹中的所有CATIA文档
for file_name in os.listdir(folder_path):
    if file_name.endswith(".CATPart"):
        file_path = os.path.join(folder_path, file_name)
        part_document = documents.Open(file_path)
        part = part_document.Part
		
		# 获取几何信息
        bodies = part.Bodies
        body = bodies.Item("PartBody")
        shapes = body.Shapes
        for i in range(1, shapes.Count + 1):
            shape = shapes.Item(i)
            print(f"File: {file_name}, Shape: {shape.Name}")
			
		# 关闭文档
        part_document.Close()
```
## 六、处理装配体

打开装配体文档并遍历其产品：
```
# 打开装配体文档
assembly_document = documents.Open("C:\\path\\to\\your\\assembly.CATProduct")

#获取装配体根产品
product = assembly_document.Product

#遍历装配体中的所有产品
products = product.Products

for i in range(1, products.Count + 1):
    sub_product = products.Item(i)
    print(sub_product.Name)
	
	# 获取子产品的几何体
    part_document = sub_product.ReferenceProduct.Parent
    part = part_document.Part
    bodies = part.Bodies
    body = bodies.Item("PartBody")
    shapes = body.Shapes
    for j in range(1, shapes.Count + 1):
        shape = shapes.Item(j)
        print(f"Sub-product: {sub_product.Name}, Shape: {shape.Name}")
```
## 七、处理参数和公式

在CATIA中，您可以使用参数和公式来驱动几何体。以下代码演示了如何创建一个长度参数，并将其应用于几何体的坐标参数。通过参数和公式，您可以实现几何体的参数化设计：
```
# 创建一个长度参数
parameters = part.Parameters
length_param = parameters.CreateDimension("LengthParam", "LENGTH", 100)

#创建一个点并将其位置参数化
hybrid_shape_factory = part.HybridShapeFactory
point = hybrid_shape_factory.AddNewPointCoord(0, 0, 0)
part.HybridBodies.Item("Geometrical Set.1").AppendHybridShape(point)
part.Update()

#获取点的坐标参数
x_param = point.GetCoordinate(1)
y_param = point.GetCoordinate(2)
z_param = point.GetCoordinate(3)

#将点的X坐标与长度参数关联
x_param.Modify("LengthParam")

#更新零件
part.Update()
```

## 八、生成报告

通过Python脚本，您可以生成CATIA模型的报告。例如，您可以生成包含几何体信息的报告：
```
import csv
#定义报告文件路径
report_file = "C:\\path\\to\\your\\report.csv"
#打开报告文件
with open(report_file, mode='w', newline='') as file:
    writer = csv.writer(file)
	
	# 写入报告标题
    writer.writerow(["File Name", "Shape Name"])
	
	# 遍历文件夹中的所有CATIA文档
    for file_name in os.listdir(folder_path):
        if file_name.endswith(".CATPart"):
            file_path = os.path.join(folder_path, file_name)
            part_document = documents.Open(file_path)
            part = part_document.Part
			
			# 获取几何信息
            bodies = part.Bodies
            body = bodies.Item("PartBody")
            shapes = body.Shapes
            for i in range(1, shapes.Count + 1):
                shape = shapes.Item(i)
                writer.writerow([file_name, shape.Name])
				
			# 关闭文档
            part_document.Close()
```