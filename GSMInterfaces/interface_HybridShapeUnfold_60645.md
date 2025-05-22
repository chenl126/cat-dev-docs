# HybridShapeUnfold (Object)

**_Represents the hybrid shape Unfold feature object._**
**Role** : To access the data of the hybrid shape Unfold feature object. This data includes:

  * The shell to unfold
  * The edges to tear

Use the CATIAHybridShapeFactory to create a HybridShapeUnfold object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **DirectionToUnfold**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the direction to unfold.  
### Property **EdgeToTearPositioningOrientation**( ) As long

Returns or sets the positioning orientation when the reference origin is located on an edge to tear.

  * 0= The orientation is undefined
  * 1= The orientation is the default one
  * 2= The orientation is inversed

### Property **OriginToUnfold**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the origin to unfold.  
### Property **SurfaceToUnfold**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the surface to unfold.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Property **SurfaceType**( ) As long

Returns or sets the type of surface to unfold.

  * 0= The type of surface is not defined
  * 1= The type of surface is ruled
  * 2= The type of surface is all

### Property **TargetOrientationMode**( ) As long

Returns or sets the mode for target surface orientation.

  * 0= No axis inversion
  * 1= U inversion axis
  * 2= V inversion axis
  * 3= U inversion axis and V inversion axis
  * 4= U inversion axis and swap U and V axis
  * 5= V inversion axis and swap U and V axis
  * 6= U inversion axis, V inversion axis and swap U and V axis
  * 7= Swap U and V axis

### Property **TargetPlane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the target plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object):  Methods

### Sub **AddEdgeToTear**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`)

Adds an edge to tear.

**Parameters:**

` iEdge`      The edge to tear to add to the hybrid shape feature object.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Edge](../MecModInterfaces/interface_Edge_3456.md) **Examples** :      The following example adds the `iElement` feature object to the `HybridShapeUnfold` object.

```VBScript
HybridShapeUnfold.AddEdgeToTear iElement

```

### Func **GetEdgeToTear**( long  `iRank`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves an element used by the hybrid shape unfold feature object.

**Parameters:**

` iRank`      The rank of the element to read.  **Examples** :      The following example gets the `oElement` feature object of the `HybridShapeUnfold` object at the position `iRank`.

```VBScript
Dim oElement As Reference
Set oElement = HybridShapeUnfold.GetEdgeToTear (iRank).

```

### Sub **RemoveEdgeToTear**( long  `iRank`)

Removes an element used by the hybrid shape unfold feature object.

**Parameters:**

` iRank`      The rank of the element to remove.  **Examples** :      The following example removes the feature object from the `HybridShapeUnfold` object at the position `iRank`.

```VBScript
HybridShapeUnfold.RemoveEdgeToTear iRank.

```