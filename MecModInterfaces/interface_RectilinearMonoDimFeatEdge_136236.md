# RectilinearMonoDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is one dimensional, the boundary having a rectilinear geometry._**
**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, in a part containing a Sketch which is made up of a line segment and a spline, the line segment. You will create a RectilinearMonoDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [Hole.SetDirection](../PartInterfaces/interface_Hole_3612.htm#SetDirection) ). The lifetime of a RectilinearMonoDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:** see the [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) example

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

Returns the direction of the rectilinear edge

**Parameters:**

` oDirection[0]`      The X Coordinate of the direction
` oDirection[1]`      The Y Coordinate of the direction
` oDirection[2]`      The Z Coordinate of the direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

Returns the origin of the the rectilinear edge.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the rectilinear edge origin
` oOrigin[1]`      The Y Coordinate of the rectilinear edge origin
` oOrigin[2]`      The Z Coordinate of the rectilinear edge origin