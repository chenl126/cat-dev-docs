# HybridShapePlaneMean (Object)

**_Represents the hybrid shape mean plane feature object._**
**Role** : To access the data of the hybrid shape mean plane feature object. This data includes:

  * The list of points

Use the CATIAHybridShapeFactory to create a HybridShapePlaneMean object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Sub **AddPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassingPoint`)

Adds a point to the mean plane.

**Parameters:**

` iPassingPoint`      The point to add

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Sub **GetPoint**( long  `iRank`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oPassingPoint`)

Retrieves the point at a given position.

**Parameters:**

` iRank`      The rank of the point to retrieve
` oPassingPoint`      The point retrieved at this rank

### Func **GetPos**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`) As long

Gets the position of an element in the list.

**Parameters:**

` iPoint`      point
` oPos`      position of point

### Func **GetSize**( ) As long

Gets the size of the list (number of points).

**Parameters:**

` oSize`      position of point

### Sub **RemoveAll**( )

Removes all elements in the list of points.  
### Sub **RemoveElement**( long  `iRank`)

Removes a point in the list.

**Parameters:**

` iRank`      The rank of the point to remove

### Sub **ReplacePointAtPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  long  `iPos`)

Replaces a point in the list at the given position.

**Parameters:**

` oPoint`      point
` iPos`      position of point