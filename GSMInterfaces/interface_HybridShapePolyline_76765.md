# HybridShapePolyline (Object)

**_Represents the hybrid shape polyline curve object._**
**Role** : To access or set the data of the hybrid shape polyline object. This data includes:

  * Elements
  * Radius
  * Support
  * Closure

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) object to create a HybridShapePolyline object.

## Properties

### Property **Closure**( ) As boolean

Returns or sets the flag to decide closure of the polyline.

**Parameters:**

` Closure`      (For get_Closure) Returns or sets the closure property

**Example** :      This example retrieves the closure property of the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
Dim HybShpPolClosure As  boolean
HybShpPolClosure = HybShpPolyline.Closure

```

### Property **NumberOfElements**( ) As long (Read Only)

Returns the number of elements of the polyline.

**Parameters:**

` NumberOfElements`      Number of elements in the polyline.

**Example** :      This example retrieves the number of elements in the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
Dim HybShpPolNoOfEle As  long
HybShpPolNoOfEle = HybShpPolyline.NumberOfElements

```

Methods

### Sub **GetElement**( long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oElement`,  [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `oRadius`)

Returns the element of the polyline.

**Parameters:**

` iPosition`      Position at which the element is to be retrieved.
` oElement`      Reference to the element.
` ioRadius`      Length to the radius.

**Example** :      This example retrieves the element and radius of the polyline at specified position of the `HybShpPolyline` hybrid shape polyline.

```VBScript
Dim HybShpPolylineElement As Reference
Dim HybShpPolylineRadius As Reference
HybShpPolyline.GetElement 1, HybShpPolylineElement,HybShpPolylineRadius

```

### Sub **InsertElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  long  `iPosition`)

Inserts the element at a specified position in the polyline.

**Parameters:**

` iPoint`      Reference of the point object to be inserted.
` iPosition`      Position at which the element should be inserted.

**Example** :      This example inserts the element in the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
HybShpPolyline.InsertElement PointReference,1

```

### Sub **RemoveElement**( long  `iPosition`)

Removes the element at a specified position in the polyline.

**Parameters:**

` iPosition`      Position from which the element should be should be removed.

**Example** :      This example removes the element in the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
HybShpPolyline.RemoveElement 1

```

### Sub **ReplaceElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  long  `iPosition`)

Replaces the element at a specified position in the polyline.

**Parameters:**

` iPoint`      Reference of the point object that will replace the old element.
` iPosition`      Position at which the element should be inserted.

**Example** :      This example replaces the element in the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
HybShpPolyline.ReplaceElement PointReference, 1

```

### Sub **SetRadius**( long  `iPosition`,  double  `iRadius`)

Sets the radius at specified position of the polyline.

**Parameters:**

` iPosition`      Position at which radius should be set
` iRadius`      Value of the radius to be set.

**Example** :      This example sets the radius at the specific position of the polyline of the `HybShpPolyline` hybrid shape polyline.

```VBScript
HybShpPolyline.SetRadius 1, 10

```