# HybridShapeLineBiTangent (Object)

**_Line tangent to a curve._**

**Role** : To access data of the line feature created to be tangent to two entities

## Properties

### Property **Curve1**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the first tangency curve lying on the support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `oCurve` the first tangency curve for the `LineBiTangent` hybrid shape feature.

```VBScript
     Dim oCurve As Reference
     Set oCurve = LineBiTangent.Curve1

```

### Property **Element2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the second tangency element (point, curve) lying on the support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `oElement` the second tangency Element (point, curve) for the `LineBiTangent` hybrid shape feature.

```VBScript
     Dim oElement As Reference
     Set oElement = LineBiTangent.Element2

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the supporting surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `oSurface` the surface for the `LineBiTangent` hybrid shape feature.

```VBScript
     Dim oSurface As Reference
     Set oSurface = LineBiTangent.Surface

```

Methods

### Sub **GetChoiceNo**( long  `val1`,  long  `val2`,  long  `val3`,  long  `val4`,  long  `val5`)

   Returns a sequence which identifies a solution among all possibilities.

  * val1 = Solution number (from 1 to n).

* val2 = oOriTgt1

This orientation allows to compute just the results that are tangent to a specific region of the first curve.
It can take 3 values:

  * +1 : the result has the same orientation as the curve,
  * -1 : the result has the opposite orientation of the curve,
  * 0 : no orientation is specified.

* val3 = oOriCvt1

This orientation allows to compute just the results that are tangent to a specific side of the first curve.
It can take 3 values:

  * +1 : curvature direction of curve and cross product of support normal and result direction are in the same direction,
  * -1 : curvature direction of curve and cross product of support normal and result direction are in opposite directions,
  * 0 : no orientation is specified.

* val4 = oOriTgt2

In case of curve/curve bitangent line, this orientation allows to compute just the results that are tangent to a specific region of the second curve .
It can take 3 values:

  * +1 : the result has the same orientation as the curve,
  * -1 : the result has the opposite orientation of the curve,
  * 0 : no orientation is specified.

* val5 = oOriCvt2

In case of curve/curve bitangent line this orientation allows to compute just the results that are tangent to a specific side of the second curve.
It can take 3 values:

  * +1 : curvature direction of curve and cross product of support normal and result direction are in the same direction,
  * -1 : curvature direction of curve and cross product of support normal and result direction are in opposite directions,
  * 0 : no orientation is specified.

**Example** :      This example retrieves in `vakl1,val2,val3,val4,val5` parameters for solutions for the `LineBiTangent` hybrid shape feature.

```VBScript
     Dim oVal1 As long
     Dim oVal2 As long
     Dim oVal3 As long
     Dim oVal4 As long
     Dim oVal5 As long
     LineBiTangent.GetChoiceNo(ovla1, oVal2, oVal3, oVal4, oVal5)

```

### Func **GetLengthType**( ) As long

   Gets the length type Default is 0.

**Parameters:**

` oType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Sub **SetChoiceNo**( long  `val1`,  long  `val2`,  long  `val3`,  long  `val4`,  long  `val5`)

   Sets a sequence which identifies a solution among all possibilities.

  * val1 = Solution number (from 1 to n).

* val2 = oOriTgt1

This orientation allows to compute just the results that are tangent to a specific region of the first curve.
It can take 3 values:

  * +1 : the result has the same orientation as the curve,
  * -1 : the result has the opposite orientation of the curve,
  * 0 : no orientation is specified.

* val3 = oOriCvt1

This orientation allows to compute just the results that are tangent to a specific side of the first curve.
It can take 3 values:

  * +1 : curvature direction of curve and cross product of support normal and result direction are in the same direction,
  * -1 : curvature direction of curve and cross product of support normal and result direction are in opposite directions,
  * 0 : no orientation is specified.

* val4 = oOriTgt2

In case of curve/curve bitangent line, this orientation allows to compute just the results that are tangent to a specific region of the second curve .
It can take 3 values:

  * +1 : the result has the same orientation as the curve,
  * -1 : the result has the opposite orientation of the curve,
  * 0 : no orientation is specified.

* val5 = oOriCvt2

In case of curve/curve bitangent line this orientation allows to compute just the results that are tangent to a specific side of the second curve.
It can take 3 values:

  * +1 : curvature direction of curve and cross product of support normal and result direction are in the same direction,
  * -1 : curvature direction of curve and cross product of support normal and result direction are in opposite directions,
  * 0 : no orientation is specified.

**Example** :      This example retrieves in `vakl1,val2,val3,val4,val5` parameters for solutions for the `LineBiTangent` hybrid shape feature.

```VBScript
     Dim iVal1 As long
     Dim iVal2 As long
     Dim iVal3 As long
     Dim iVal4 As long
     Dim iVal5 As long
     ival1 = 1
     ival2 = 0
     ival3 = 0
     ival4 = 0
     ival5 = 0
     LineBiTangent.SetChoiceNo(ivla1, iVal2, iVal3, iVal4, iVal5)

```

### Sub **SetLengthType**( long  `iType`)

   Sets the length type Default is 0.

**Parameters:**

` iType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point