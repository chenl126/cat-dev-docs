# HybridShapeCurvePar (Object)

**_Represents the hybrid shape curve parameter object._**

**Role** : To access the data of the hybrid shape curve parameter object. This data includes:

  * The face to process
  * The offset parameter.

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) to create a HybridShapeCurvePar object.

## Properties

### Property **CurveOffseted**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the offset curve of the curve parameter object.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example:**      This example retrieves the offset curve of the `hybShpCurvePar` in `offsetCrv`.

```VBScript
     Dim offsetCrv As CATIAReference
     offsetCrv = hybShpCurvePar.CurveOffseted

```

### Property **CurveParLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the offset law.

**Example** :      This example retrieves in `oLaw` the offset law for the `hybShpCurvePar` hybrid shape feature.

```VBScript
     Dim oLaw As Reference
     Set oLaw = hybShpCurvePar.CurveParLaw

```

### Property **CurveParType**( ) As long

   Returns or sets the corner type.

**Legal values** :

0
    CATGSMCurvePar_Sharp. corner with angle.
1
    CATGSMCurvePar_Round. round corner.

**Example** :      This example retrieves in `oCurveParType` the curve par type for the `hybShpCurvePar` hybrid shape feature.

```VBScript
     oCurveParType = hybShpCurvePar.CurveParType

```

### Property **Geodesic**( ) As boolean

   Returns or sets Geodesic mode.

**Legal values** : **True** Geodesic mode and **False** Euclidian mode .

**Example:**      This example sets that the geodesic mode of the `hybShpCurvePar` hybrid shape curve par feature to True.

```VBScript
     hybShpCurvePar.Geodesic = True

```

### Property **InvertDirection**( ) As boolean

   Returns or sets the orientation.

**Legal values** : **True** True to invert this orientation and **False** False means that there is no invertion of the curve orientation (orientation is the vector product of the tangent of the curve by the normal on the support).

**Example:**      This example sets that the orientation of the `hybShpCurvePar` hybrid shape curve par feature to True.

```VBScript
     hybShpCurvePar.InvertDirection = True

```

### Property **InvertMappingLaw**( ) As boolean

   Returns or sets the mapping orientation of the law (if offset is specified by a law).

**Legal values** : **True** Law is applied from the end to the beginning of the curve (mapping is inverted). **False** Law is applied from the beginning to the end of the curve (mapping is not inverted).

**Example:**      This example sets that the mapping orientation of the `hybShpCurvePar` hybrid shape curve par feature to True.

```VBScript
     hybShpCurvePar.InvertMappingLaw = True

```

### Property **KeepBothSides**( ) As boolean

   Returns or sets the both sides mode of the curve parameter object.

**Example:**      This example retrieves the both sides mode of the `hybShpCurvePar`

```VBScript
     Dim bothSides As Boolean
     bothSides = hybShpCurvePar.KeepBothSides

```

### Property **LawType**( ) As long

   Returns or sets the law type.

**Legal values** :

0
    CATGSMBasicLawType_None. Undefined law type.
1
    CATGSMBasicLawType_Constant. Constant law type.
2
    CATGSMBasicLawType_Linear. Linear law type.
3
    CATGSMBasicLawType_SType. S law type.
4
    CATGSMBasicLawType_Advanced. Law specified by a GSD law feature.

**Example** :      This example retrieves in `oLawType` the law type for the `hybShpCurvePar` hybrid shape feature.

```VBScript
     oLawType = hybShpCurvePar.LawType

```

### Property **MaximumDeviationValue**( ) As double

   Sets or Gets the maximum deviation allowed for smoothing operation.
Sets in distance unit, it corresponds to the radius of a pipe around the input curve in which the result is allowed to be. This value must be set in SI unit (m).

**Example** : This example retrieves in `DeviationValue` the maximum deviation value for the `CurvePar` hybrid shape feature.

```VBScript
     Dim DeviationValue As CATIALength
     Set DeviationValue = CurvePar.MaximumDeviationValue

```

### Property **Offset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the offset parameter of the curve parameter object.

**Example:**      This example retrieves the offset parameter of the `hybShpCurvePar` in `offsetParm`.

```VBScript
     Dim offsetParm As CATIALength
     offsetParm = hybShpCurvePar.Offset

```

### Property **Offset2**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the second offset parameter of the curve parameter object.

**Example:**      This example retrieves the second offset parameter of the `hybShpCurvePar` in `offsetParm`.

```VBScript
     Dim offsetParm As CATIALength
     offsetParm = hybShpCurvePar.Offset2

```

### Property **OtherSide**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

   Returns the other side of parallel curve if both sides mode is on.

**Example:**      This example retrieves the other side of the `hybShpCurvePar`

```VBScript
     Dim otherSide As CATIAReference
     Set otherSide = hybShpCurvePar.OtherSide

```

### Property **PassingPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the passing point of the curve parameter object.
Sub-element(s) supported (see [Point](../GSMInterfaces/interface_Point_5884.md) object):

**Example:**      This example retrieves the offset curve of the `hybShpCurvePar` in `offsetCrv`.

```VBScript
     Dim PassingPoint As CATIAReference
     offsetCrv = hybShpCurvePar.PassingPoint

```

### Property **SmoothingType**( ) As long

   Returns or sets the smoothing Type.
Smoothing type:

  * : 0 -> No Smoothing
  * : 2 -> G1 Smoothing : Enhance current continuity to tangent continuity
  * : 3 -> G2 Smoothing : Enhance current continuity to curvature continuity

**Example** : This example retrieves in `SType` the smoothing type for the `CurvePar` hybrid shape feature.

```VBScript
     Dim SType As long
     Set SType = CurvePar.SmoothingType

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support of the curve..

**Example** :      This example retrieves in `oElem` the support of the curve for the `hybShpCurvePar` hybrid shape feature.

```VBScript
     Dim oElem As Reference
     Set oElem = hybShpCurvePar.Support

```

### Property **p3DSmoothing**( ) As boolean

   Returns or sets the '3D Smoothing' option. **Role** : To activate or not the 3D smoothing option Available only for tangent or curvature smoothing type TRUE : Smoothing performed without specifying support FALSE : Smoothing performed with specific support

**Example** : This example retrieves in `3DSmoothingOption` the support for the `Project` hybrid shape feature.

```VBScript
     Dim 3DSmoothingOption As boolean
     Set 3DSmoothingOption = Project.p3DSmoothing

```

Methods

### Sub **GetPlaneNormal**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oNormal`)

   Returns the Normal of the plane created when the Support of the curve is not specified.

**Parameters:**

` oNormal`      Plane normal. It is returned as an array of three coordinates in SafeArrayVariant  **Example** :      This example retrieves in `oNormal` the normal of the `hybShpCurvePar` plane created.

```VBScript
     Dim oNormal(2)
     hybShpCurvePar.GetPlaneNormal(oNormal)

```

You can access each normal coordinate as follows:

  * `x` is in `oNormal(0)`
  * `y` is in `oNormal(1)`
  * `z` is in `oNormal(2)`

### Sub **PutPlaneNormal**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iNormal`)

   Sets the Normal of the plane created when the Support of the curve is not specified.

**Parameters:**

` iNormal`
` iNormal[0]`      The X Coordinate of the normal vector
` iNormal[1]`      The Y Coordinate of the normal vector
` iNormal[2]`      The Z Coordinate of the normal vector