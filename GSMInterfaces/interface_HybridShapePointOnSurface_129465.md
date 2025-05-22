# HybridShapePointOnSurface (Object)

**_Represents the Point on Surface feature objects._**
**Role** : Allows to access data of the point feature created with a geodesic distance in a direction to a reference point on a surface

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or Sets the direction from the reference point in which the point is computed.

Example
:      This example retrieves in `oDirection` the direction from the reference point for `PointOnSurface` feature.

```VBScript
Dim oDirection As CATIAHybridShapeDirection
Set oDirection  = PointOnSurface.Direction

```

### Property **Offset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the geodesic length.

Example
:      This example retrieves in `oGeodesicOffset` the offset (Geodesic Length) from the reference point for `PointOnSurface` feature.

```VBScript
Dim oGeodesicOffset As CATIAReference
Set oGeodesicOffset  = PointOnSurface.GeodesicOffset

```

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the reference point.
This data is not mandatory.
If no point is given, the middle point on the surface is taken.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

Example
:      This example retrieves in `oPointRef` the reference point for `PointOnSurface` feature.

```VBScript
Dim oPointRef As CATIAReference
Set oPointRef  = PointOnSurface.PointRef

```

### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

Example
:      This example retrieves in `oSurface` the supporting surface for `PointOnSurface` feature.

```VBScript
Dim oSurface As CATIAReference
Set oSurface  = PointOnSurface.Surface

```