# HybridShapePointTangent (Object)

**_Point Tangent._**
**Role** : Allows to access data of the point feature created as follow :
The tangent to the curve at this point is colinear to a given direction.
Note: The resulting feature can contain several points.

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Curve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Gets the supporting curve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Edge](../MecModInterfaces/interface_Edge_3456.md).

Example
:      This example retrieves in `oCurve` the supporting Curve for the `PointTangent` feature.

```VBScript
Dim oCurve As CATIAReference
Set oCurve  = PointTangent.Curve

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or Sets the direction.

Example
:      This example retrieves in `oDirection` the tangent direction use to compute on supporting curve the `PointTangent` feature.

```VBScript
Dim oDirection As CATIAHybridShapeDirection
Set oDirection  = PointTangent.Direction

```