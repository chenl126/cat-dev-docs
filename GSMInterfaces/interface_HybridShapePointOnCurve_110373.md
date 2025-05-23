# HybridShapePointOnCurve (Object)

**_Represents the hybrid shape point on a curve._**

**Role** : To access the data of the point object created on a curve. This data includes:

  * The curve onto which the point is created
  * The reference point from which the point is created
  * The curvilinear distance from the reference point
  * The ratio of distance with respect to the curve length
  * The distance stored value type, either distance or ratio
  * The curve orientation
  * The distance type, either geodesic or euclidean.

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) to create a HybridShapePointOnCurve object.

## Properties

### Property **Curve**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the curve onto which the point is or should be created.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example:**      This example retrieves in `oCurve` the supporting curve for the `pointOnCurve` hybrid shape point.

```VBScript
     Dim oCurve As CATIAReference
     Set oCurve = pointOnCurve.Curve

```

### Property **DistanceType**( ) As long

   Returns or sets the distance type.

**Legal values** : 1 for geodesic, -1 for euclidean.
Default is geodesic.

  * Geodesic means that the distance is measured with a curvilinear abscissa
  * Euclidean means that the point is created as the intersection between the reference curve and a circle whose radius is the length defined above.

**Example:**      This example retrieves in `oDistanceType` the distance computation type used for the `pointOnCurve` hybrid shape object.

```VBScript
     Dim oDistanceType As  long
     Set oDistanceType = pointOnCurve.DistanceType

```

### Property **Offset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the distance to the reference point.
This distance is a distance in a length unit, The distance can be null.In this case, the reference point is the curve end point defined using the Orientation parameter.

**Example:**      This example retrieves in `oOffset` the distance from the reference point on the supporting curve for the `pointOnCurve` hybrid shape object.

```VBScript
     Dim oOffset As  CATIALength
     Set oOffset = pointOnCurve.Offset

```

### Property **Orientation**( ) As long

   Returns or sets the curve orientation.

**Legal values** : -1 means that the distance (length or ratio) is measured:

  * in the other orientation of the curve, when a reference point has been set
  * in the other orientation of the curve and from the other extremity, when no reference point has been set.

**Example:**      This example retrieves in `oOrientation` curve Orientation use for the `pointOnCurve` hybrid shape feature.

```VBScript
     Dim oOrientation As  long
     Set oOrientation = pointOnCurve.Orientation

```

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the reference point. If the point does not lie on the curve, the point on the curve with the smallest distance to this point is taken. The reference point may not exist. In this case, the extremity of the curve is taken as reference point.

Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example:**      This example retrieves in `oRefPoint` the reference point on the supporting curve for the `pointOnCurve` hybrid shape object.

```VBScript
     Dim oRefPoint As  CATIAReference
     Set oRefPoint = pointOnCurve.Point

```

### Property **Ratio**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the distance ratio to the reference point.
This is a real parameter which corresponds to the ratio of the distance from the reference point with respect to the length of the supporting curve. The ratio can be null. In this case, the reference point is the curve end point defined using the Orientation parameter.

**Example:**      This example retrieves in `oRatio` the distance ratio from the reference point on the supporting curve for the `pointOnCurve` hybrid shape object.

```VBScript
     Dim oRatio As  CATIALength
     Set oRatio = PointOnCurve.Ratio

```

### Property **Type**( ) As long (Read Only)

   Returns the distance stored value type.

**Legal values** :

  * 1 when the type of measure is the length
  * -1 when the type of measure is the distance ratio

**Example:**      This example retrieves in `oType` the distance type computation for the `pointOnCurve` hybrid shape object.

```VBScript
     Dim oType As long
     Set oType = pointOnCurve.Type

```