# HybridShapePointOnPlane (Object)

**_Point on a plane._**
**Role** : Allows to access data of the point feature created on a plane with a reference point or not.

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md), [Reference](../InfInterfaces/interface_Reference_17481.md), [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md), [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FirstDirection**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the first direction on the plane to compute the point (for stability).

Example
:      This example retrieves in `oDirection` the direction of the `PointOnPlane` feature.

```VBScript
Dim oDirection As CATIAHybridShapeDirection
Set oDirection = PointOnPlane.FirstDirection

```

### Property **Plane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

Example
:      This example retrieves in `oPlane` the supporting Plane for `PointOnPlane` feature.

```VBScript
Dim oPlane As CATIAReference
Set oPlane  = PointOnPlane.Plane

```

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference point.
This data is not mandatory, if Point is
null, the projection of the origin point on the plane is taken.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

Example
:      This example retrieves in `oPoint` the reference point for `PointOnPlane` feature.

```VBScript
Dim oPoint As CATIAReference
Set oPoint  = PointOnPlane.Point

```

### Property **ProjectionSurface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the projection surface to compute the point.

Example
:      This example retrieves in `oProjSur` the projection surface of the `PointOnPlane` feature.

```VBScript
Dim oProjSur As CATIAReference
Set oProjSur = PointOnPlane.ProjectionSurface

```

### Property **XOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the X cartesian coordinate in the plane.

Example
:      This example retrieves in `oX` the X coordinate for `PointOnPlane` feature.

```VBScript
Dim oX As  CATIALength
Set oX  = PointOnPlane.XOffset

```

### Property **YOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the Y cartesian coordinate in the plane.

Example
:      This example retrieves in `oY` the Y coordinate for `PointOnPlane` feature.

```VBScript
Dim oY As  CATIALength
Set oY  = PointOnPlane.YOffset

```

Methods

### Sub **GetSecondDirection**( double  `oDirX`,  double  `oDirY`,  double  `oDirZ`)

Gets the second direction on the plane to compute the point (for stability).
This direction has to be kept perpendicular to the first direction

**Parameters:**

` oDir`      second direction
**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) 
### Sub **SetSecondDirection**( double  `iDirX`,  double  `iDirY`,  double  `iDirZ`)

Sets the second direction on the plane to compute the point (for stability).
This direction has to be kept perpendicular to the first direction

**Parameters:**

` iDir`      second direction
**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)