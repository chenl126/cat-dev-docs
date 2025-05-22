# HybridShapeCurveSmooth (Object)

**_Represents the hybrid shape curve smoothing operation feature._**
**Role** : To access the data of the curve smoothing operation.of the hybrid shape curve parameter object. This data includes:

  * The curve to smooth
  * The support (if exist )
  * The tangent tolerance value (threshold)
  * The curvature tolerance value (threshold)
  * The info if curvature threshold is activated
  * The maximum deviation accepted
  * The info if maxcimum deviation is activated
  * The fixed points
  * The fixed segments
  * The info if topology simplification is activated

Use the [HybridShapeFactory.AddNewCurveSmooth](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewCurveSmooth) to create a HybridShapeCurveSmooth object.

## Properties

### Property **CorrectionMode**( ) As long

Returns or sets the correction mode (threshold, point, tangency or curvature) applied to the smoothed curve.
**Legal values** :

0
    CATGSMCSCorrectionMode_Threshold. no continuity
1
    CATGSMCSCorrectionMode_Point. continuity in point (C0).
2
    CATGSMCSCorrectionMode_Tangency. continuity in tangency (C1).
3
    CATGSMCSCorrectionMode_Curvature. continuity in curvature (C2).
**Example** :      This example retrieves in `oMode` the correction mode for the `hybShpCurveSmooth` hybrid shape feature.

```VBScript
oMode = hybShpCurveSmooth.CorrectionMode

```

### Property **CurvatureThreshold**( ) As double

Returns or sets the CurvatureThreshold.

**Example** : This example retrieves the CurvatureThreshold of the `hybShpCurveSmooth` in `CurvatureThH`.

```VBScript
Dim CurvatureThH as double
CurvatureThH = hybShpCurvePar.CurvatureThreshold

```

### Property **CurvatureThresholdActivity**( ) As boolean

Returns or sets the CurvatureThresholdActivity.

**Example** : This example retrieves the CurvatureThresholdActivity of the `hybShpCurveSmooth` in `CurvatureActivity `.

```VBScript
Dim CurvatureActivity as boolean
CurvatureActivity = hybShpCurvePar.CurvatureThresholdActivity

```

### Property **CurveToSmooth**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the curve to smooth.

**Example** : This example retrieves the curve to smooth object of the `hybShpCurveSmooth` in `Curve`.

```VBScript
Dim Curve as CATIAReference
Curve  = hybShpCurvePar.CurveToSmooth

```

### Property **EndExtremityContinuity**( ) As long

Returns or sets the continuity condition (curvature, tangency or point) applied to the smoothed curve with regard to the input curve at the end extremity of the input curve.
**Legal values** :

0
    CATGSMContinuity_Point. continuity in point (C0).
1
    CATGSMContinuity_Tangency. continuity in tangency (C1).
2
    CATGSMContinuity_Curvature. continuity in curvature (C2).
**Example** :      This example retrieves in `oContinuity` the continuity at the end extremity for the `hybShpCurveSmooth` hybrid shape feature.

```VBScript
oContinuity = hybShpCurveSmooth.EndExtremityContinuity

```

### Property **MaximumDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the MaximumDeviation.

**Example** : This example retrieves the MaximumDeviation of the `hybShpCurveSmooth` in `MaximumDeviationVal`.

```VBScript
Dim MaximumDeviationVal as CATIALength
MaximumDeviationVal  = hybShpCurvePar.MaximumDeviation

```

### Property **MaximumDeviationActivity**( ) As boolean

Returns or sets the MaximumDeviationActivity.

**Example** : This example retrieves the MaximumDeviationActivity of the `hybShpCurveSmooth` in `MaxActivity `.

```VBScript
Dim MaxActivity as boolean
MaxActivity  = hybShpCurvePar.MaximumDeviationActivity

```

### Property **StartExtremityContinuity**( ) As long

Returns or sets the continuity condition (curvature, tangency or point) applied to the smoothed curve with regard to the input curve at the start extremity of the input curve.
**Legal values** :

0
    CATGSMContinuity_Point. continuity in point (C0).
1
    CATGSMContinuity_Tangency. continuity in tangency (C1).
2
    CATGSMContinuity_Curvature. continuity in curvature (C2).
**Example** :      This example retrieves in `oContinuity` the continuity at the start extremity for the `hybShpCurveSmooth` hybrid shape feature.

```VBScript
oContinuity = hybShpCurveSmooth.StartExtremityContinuity

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support of the curve.
if Suppport == nothing no support associated to the curve

**Example** : This example retrieves the support of curve to smooth object of the `hybShpCurveSmooth` in `Support`.

```VBScript
Dim Support  as CATIAReference
Support   = ybShpCurveSmooth.Support

```

### Property **TangencyThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the TangencyThreshold.

**Example** : This example retrieves the curve to smooth object of the `hybShpCurveSmooth` in `AngleThH`.

```VBScript
Dim Curve as CATIAAngle
AngleThH  = ybShpCurveSmooth.TangencyThreshold

```

### Property **TopologySimplificationActivity**( ) As boolean

Returns or sets the TopologySimplificationActivity.

**Example** : This example retrieves the TopologySimplificationActivity of the `hybShpCurveSmooth` in `TopSimplifyAct`.

```VBScript
Dim TopSimplifyAct as boolean
TopSimplifyAct  = hybShpCurvePar.TogologySimplificationActivity

```

Methods

### Sub **AddFrozenCurveSegment**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`)

Adds a frozen curve to the hybrid shape curve smooth feature object.

**Parameters:**

` iCurve`      The curve to be added to the hybrid shape curve smooth feature object.  **Example** :      The following example adds the `iCurve` curve to the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.AddFrozenCurveSegment iCurve

```

### Sub **AddFrozenPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

Adds a frozen points to the hybrid shape curve smooth feature object.

**Parameters:**

` iPoint`      The frozen point to be added to the hybrid shape curve smooth feature object.  **Example** :      The following example adds the `iPoint` frozen point to the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.AddFrozenPoint iPoint

```

### Func **GetFrozenCurveSegment**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves the Frozen Curve Segment at specified position in the hybrid shape curve smooth object.

**Parameters:**

` iPos`      The position of the Frozen Curve Segment to retrieve.  **Example** :      The following example gets the `oCurve` Frozen Curve Segment of the `hybShpCurveSmooth` object at the position `iPos`.

```VBScript
Dim oCurve As Reference
Set oCurve = hybShpCurveSmooth.GetFrozenCurveSegment (iPos).

```

### Func **GetFrozenCurveSegmentsSize**( ) As long

Returns the number of frozen curve segments in the curve smooth object.

**Parameters:**

` oSize`      Number of frozen curve segments in the curve smooth.

**Example** :      This example retrieves the number of frozen curve segments. in the `hybShpCurveSmooth` hybrid shape curve smooth.

```VBScript
Dim oSize As  long
oSize = hybShpCurveSmooth.GetFrozenCurveSegmentsSize

```

### Func **GetFrozenPoint**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves the Frozen Point at specified position in the hybrid shape curve smooth object.

**Parameters:**

` iPos`      The position of the Frozen Point to retrieve.  **Example** :      The following example gets the `oPoint` Frozen Point of the `hybShpCurveSmooth` object at the position `iPos`.

```VBScript
Dim oPoint As Reference
Set oPoint = hybShpCurveSmooth.GetFrozenPoint (iPos).

```

### Func **GetFrozenPointsSize**( ) As long

Returns the number of Frozen Points in the curve smooth object.

**Parameters:**

` oSize`      Number of Frozen Points in the curve smooth.

**Example** :      This example retrieves the number of Frozen Points. in the `hybShpCurveSmooth` hybrid shape curve smooth.

```VBScript
Dim oSize As  long
oSize = hybShpCurveSmooth.GetFrozenPointsSize

```

### Sub **RemoveAllFrozenCurveSegments**( )

Removes all Frozen Curve Segment of the hybrid shape curve smooth object.  **Example** :      The following example removes all Frozen Curve Segments of the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.RemoveAllFrozenCurveSegments

```

### Sub **RemoveAllFrozenPoints**( )

Removes all Frozen Points of the hybrid shape curve smooth object.  **Example** :      The following example removes all Frozen Points of the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.RemoveAllFrozenPoints

```

### Sub **RemoveFrozenCurveSegment**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`)

Removes Frozen Curve Segment from the list of Forzen curves in hybrid shape curve smooth object.

**Parameters:**

` iCurve`      The Frozen Curve Segment to remove.  **Example** :      The following example removes the Frozen Curve Segment from the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.RemoveFrozenCurveSegment iCurve.

```

### Sub **RemoveFrozenPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

Removes Frozen Point from the list of frozen points in hybrid shape curve smooth object.

**Parameters:**

` iPoint`      The Frozen Point to remove.  **Example** :      The following example removes the Frozen Point from the `hybShpCurveSmooth` object.

```VBScript
hybShpCurveSmooth.RemoveFrozenPoint iPoint.

```

### Sub **SetMaximumDeviation**( double  `iMaxDeviation`)

Sets the maximum deviation.

**Parameters:**

` iMaxDeviation`      The maximium deviation

### Sub **SetTangencyThreshold**( double  `iTangencyThreshold`)

Sets the tangency threshold.

**Parameters:**

` iTangencyThreshold`      The tangency threshold