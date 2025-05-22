# DrawingDimensions (Collection)

**_A collection of all the drawing dimensions currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**( [CatDimType](../DraftingInterfaces/enum_CatDimType_21068.md)  `iTypeDim`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iGeomElem`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPtCoordElem`,  [CatDimLineRep](../DraftingInterfaces/enum_CatDimLineRep_34241.md)  `iLineRep`) As [CATIADrawingDimension](../DraftingInterfaces/interface_DrawingDimension_55138.md)

Creates a drawing dimension and adds it to the DrawingDimensions collection.

**Parameters:**

` iTypeDim`      Dimension type
` iGeomElem`      Parent geometrical element(s) of dimension
` iPtCoordElem`      Array of pointers on the selection points of each element of iGeomElem
` iLineRep`      Basic representation mode
**Returns:**      The created drawing dimension  **Example:**      The following example creates a drawing angle dimension between two lines and a partial curvilinear length dimension on an ellipse and retrieved in `MyDimension1` and `MyDimension2` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
Dim MyView As DrawingView
Set MyView = MySheet.Views.ActiveView
Dim Fact2D  As Factory2D
Set Fact2D = MyView.Factory2D
Dim Line1 As Line2D
Dim Line2 As Line2D
Set Line1 = Fact2D.CreateLine(50, 10, 150, 10)
Set Line2 = Fact2D.CreateLine(50, 10, 120, 100)
Dim Ellipse1 As Ellipse2D
Set Ellipse1 = Fact2D.CreateEllipse(-40, 100, 120, 180,120,90,0, 3)
Dim Point1 As Point2D
Dim Point2 As Point2D
Set Point1 = Fact2D.CreatePoint(-10,190)
Set Point2 = Fact2D.CreatePoint(-120,90)
Dim iType As catDimType
iType = catDimAngle
Dim myElements1(1)
myElements1(1) = Array(Line1,Line2)
Dim selpoints(3)
selpoints(3) = Array(150, 10, 120, 100)
Dim MyDimension1 As DrawingDimension
Set MyDimension1 = MyView.Dimensions.Add(iType, myElements1(1), selpoints(3),catDimAuto)
iType = catDimLengthCurvilinear
Dim myElements2(2)
myElements2(2) = Array(Point1,Point2,Ellipse1)
selpoints(3) = Array(0, 0, 0, 0)
Dim MyDimension2 As DrawingDimension
Set MyDimension2 = MyView.Dimensions.Add(iType, myElements2(1), selpoints(3),catDimOffset)

```

### Func **Add2**( [CatDimType](../DraftingInterfaces/enum_CatDimType_21068.md)  `iTypeDim`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iGeomElem`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPtCoordElem`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iLDCRefElem`,  long  `iLDCRefAngle`) As [CATIADrawingDimension](../DraftingInterfaces/interface_DrawingDimension_55138.md)

Creates a drawing dimension along a direction and adds it to the DrawingDimensions collection.

**Parameters:**

` iTypeDim`      Dimension type (available types : catDimDistance, catDimLength, catDimRadiusTangent and catDimDiameterTangent)
` iGeomElem`      Parent geometorical element(s) of dimension
` iPtCoordElem`      Array of pointers on the selection points of each element of iGeomElem
` iLDCRefElem`      Reference geometrical element for the direction of the dimension line .iLDCRefElem can be null: in this case, the view is the reference element
` iLDCRefAngle`      Angle between the reference element and the direction of the dimension line
**Returns:**      The created drawing dimension (The property CATDimLineRep of the dimension line of the created dimension is set to catDimUserDefined)  **Example:**      The following example creates a drawing distance dimension between two points along the direction of a line and retrieved in `MyDimension` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
Dim MyView As DrawingView
Set MyView = MySheet.Views.ActiveView
Dim Fact2D  As Factory2D
Set Fact2D = MyView.Factory2D
Dim Point1 As Point2D
Dim Point2 As Point2D
Set Point1 = Fact2D.CreatePoint(40, 230)
Set Point2 = Fact2D.CreatePoint(80, 210)
Dim Line1 As Line2D
Set Line1 = Fact2D.CreateLine(50, 10, 150, 10)
Dim iType As catDimType
iType = catDimDistance
Dim myElements(1)
myElements(1) = Array(Point1,Point2)
Dim selpoints(3)
selpoints(3) = Array(0, 0, 0, 0)
Dim MyDimension As DrawingDimension
Set MyDimension = MyView.Dimensions.Add2(iType, myElements(1), selpoints(3), Line1, 0)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADrawingDimension](../DraftingInterfaces/interface_DrawingDimension_55138.md)

Returns a drawing dimension using its index or its name from the DrawingDimensions collection.

**Parameters:**

` iIndex`      The index or the name of the drawing dimension to retrieve from the collection of drawing dimensions. As a numerics, this index is the rank of the drawing dimension in the collection. The index of the first drawing dimension in the collection is 1, and the index of the last drawing dimension is Count. As a string, it is the name you assigned to the drawing dimension using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved drawing dimension  **Example:**      This example retrieves in `ThisDrawingDimension` the second drawing dimension, and in `ThatDrawingDimension` the drawing dimension named `MyDimension` in the drawing dimension collection of the active view.

```VBScript
Dim MyView As DrawingView
Set MyView  = MySheet.Views.ActiveView
Dim ThisDrawingDimension As DrawingDimension
Set ThisDrawingDimension = MyView.Dimensions.Item(2)
Dim ThatDrawingDimension As DrawingDimension
Set ThatDrawingDimension = MyView.Dimensions.Item("MyDimension")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a drawing dimension from the DrawingDimensions collection.

**Parameters:**

` iIndex`      The index of the drawing dimension to remove from the collection of drawing dimensions. As a numerics, this index is the rank of the drawing dimension in the collection. The index of the first drawing dimension in the collection is 1, and the index of the last drawing dimension is Count.  **Example:**      The following example removes the third drawing dimension in the drawing dimension collection of the active view of the active document, supposed to be a drawing document.

```VBScript
Dim MyView As DrawingView
Set MyView  = MySheet.Views.ActiveView
MyView.Dimensions.Remove(3)

```