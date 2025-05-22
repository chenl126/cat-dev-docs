# HybridShapeSweepCircle (Object)

**_Represents the hybrid shape sweep circle feature object._**
**Role** : To access the data of the hybrid shape sweep circle feature object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **CanonicalDetection**( ) As long

Returns or sets whether canonical surfaces of the swept surface are detected.
**Legal values** :  | 0 | No detection of canonical surface is performed.
---|---
2 | Detection of canonical surfaces is performed.
### Property **ChoiceNo**( ) As long

Returns or sets the choice number, which corresponds to each solution of a given circular sweep case.
For example: a circular sweep with two guide curves and a radius leads to four possible solutions.  
### Property **Context**( ) As long

Returns or sets the context on Sweep feature.

  * **0** This option creates Swept surface.
  * **1** This option creates Swept volume.

Note: Setting volume result requires GSO License.

**Example** :      This example retrieves in `oContext` the context for the `Sweep` hybrid shape feature.

```VBScript
Dim oContext
Set oContext = Sweep.Context

```

### Property **FirstAngleLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first angle law useful in some circular sweep types.  
### Property **FirstAngleLawInversion**( ) As long

Returns or sets the first angle law inversion information.  
### Property **FirstGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation first guide curve.  
### Property **GuideDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the deviation value (length) from guide curves allowed during a sweeping operation in order to smooth it.  
### Property **GuideDeviationActivity**( ) As boolean

Returns or sets information whether a deviation from guide curves is allowed or not.
Gives the information on performing smoothing during sweeping operation.
TRUE if a deviation from guide curves is allowed, or FALSE otherwise (FALSE if not specified).  
### Property **Mode**( ) As long

Returns or sets the circular sweep mode.
Legal mode values are:  | 0 | Undefined circular profile swept surface (CATGSMCircularSweep_None)
---|---
2 | Circular profile swept surface defined by three guide curves (4 solutions) (CATGSMCircularSweep_ThreeGuides)
3 | Circular profile swept surface defined by a center curve and a reference curve (for angles and radius) (CATGSMCircularSweep_TwoGuidesAndRadius)
5 | Circular profile swept surface defined by a center curve and a reference curve (for angles and radius) (CATGSMCircularSweep_CenterAndAngleCurve)
6 | Circular profile swept surface defined by a center curve and a radius (CATGSMCircularSweep_CenterAndRadius)
7 | Circular profile swept surface defined by two guide curves with a tangency condition on the second one (with reference surface) (CATGSMCircularSweep_TwoGuidesAndTangency)
8 | Circular profile swept surface defined by a guide curve, a radius and a tangency surface (CATGSMCircularSweep_GuideAndTangencyAndRadius)
### Property **RadiusLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the radius law feature.  
### Property **RadiusLawInversion**( ) As long

Returns or sets the radius law inversion information.  
### Property **RadiusLawType**( ) As long

Returns or sets the radius law type.  
### Property **Reference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference (functional curve or guide surface).  
### Property **SecondAngleLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the second angle law useful in some circular sweep types.  
### Property **SecondAngleLawInversion**( ) As long

Returns or sets the second angle law inversion information.  
### Property **SecondGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation second guide curve.  
### Property **SmoothActivity**( ) As boolean

Returns or sets information whether a sweeping operation is smoothed or not.
TRUE if the sweeping operation is smoothed, or FALSE otherwise (FALSE if not specified).  
### Property **SmoothAngleThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the angular threshold.  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation spine (optional).  
### Property **ThirdGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation third guide curve.  
### Property **TrimOption**( ) As long

Returns or sets the trim option status.
The trim option status legal values are:  | 0 | No trim computed or undefined (CATGSMSweepTrimMode_None)
---|---
1 | Trim computed (CATGSMSweepTrimMode_On)
Methods
### Func **GetAngle**( long  `iI`) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Returns the angle values useful in some circular sweep types.

**Parameters:**

` iI`      The angle value index
**Returns:**      The angle value  
### Sub **GetAngleLawTypes**( long  `oFirstType`,  long  `oSecondType`)

Retrieves angle law types.

**Parameters:**

` oFirstType`      The first type of law (from CATGSMBasicLawType enumeration).  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
` oSecondType`      The second type of law (from CATGSMBasicLawType enumeration).
Same legal values as `oFirstType`
### Sub **GetFirstAngleLaw**( [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oElem1`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oElem2`,  long  `olLawType`)

Retrieves the first angle law useful in some circular sweep types.

**Parameters:**

` oElem1`      The angle law start value
` oElem2`      The angle law end value
` olLawType`      The angle law type

### Sub **GetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepCircle#GetRelimiters Retrieves the elements relimiting the spine (or the default spine).  **Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opIAElem2`      The second relimiting feature (plane or point)

### Sub **GetNbAngle**( long  `oAng`)

Retrieves the number of angles.

**Parameters:**

` oAng`      The number of angles

### Sub **GetNbGuide**( long  `oNum`)

Retrieves the number of guide curves.

**Parameters:**

` oNum`      The number of guide curves

### Sub **GetNbRadius**( long  `oRad`)

Retrieves the number of radii.

**Parameters:**

` oRad`      The number of radii

### Func **GetRadius**( long  `iI`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns the radius value useful in some circular sweep types.

**Parameters:**

` iI`      The radius value index (1: start value, 2: end value)
**Returns:**      The radius value  
### Sub **GetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  long  `opOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`,  long  `opOrient2`)

Retrieves the elements relimiting the spine (or the default spine).

**Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` opIAElem2`      The second relimiting feature (plane or point)
` opOrient2`      Split direction for the second relimitation

### Sub **GetSecondAngleLaw**( [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oElem1`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oElem2`,  long  `olLawType`)

Retrieves the second angle law useful in some circular sweep types.

**Parameters:**

` oElem1`      The angle law start value
` oElem2`      The angle law end value
` olLawType`      The angle law type

### Sub **GetTangencyChoiceNo**( long  `oNo`,  long  `oShellOri`,  long  `oGuideOri`)

Retrieves a sequence which identifies a solution among all possibilities of a circular profile sweep tangent to a surface. (case CATGSMCircularSweep_GuideAndTangencyAndRadius).

**Parameters:**

` oNo`      Given the orientations, solution number in a distance ordered list.
` oShellOri`      This orientation allows to compute just the results that are tangent to a specific side of the shell. It can take three values:  | +1 | The result is on the normal side of the shell
---|---
-1 | The result is on the side of the shell opposite to the normal
0 | No orientation is specified
` oGuideOri`      This orientation allows to compute just the results that are on the "left" or the "right" side of the shell, when looking in the guide direction. It can take three values:  +1 | The result is on the "left" side
---|---
-1 | The result is on the "right" side
0 | No orientation is specified
### Sub **RemoveAngle**( )

Removes an angle.  
### Sub **RemoveGuide**( )

Removes a guide curve.  
### Sub **RemoveRadius**( )

Removes a radius.  
### Sub **SetAngle**( long  `iI`,  double  `iElem`)

Sets the angle values useful in some circular sweep types.

**Parameters:**

` iI`      The angle value index
` iElem`      The angle value

### Sub **SetAngleLawTypes**( long  `iFirstType`,  long  `iSecondType`)

Sets angle law types.

**Parameters:**

` iFirstType`      The first type of law (from CATGSMBasicLawType enumeration).
**Legal values** :  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
` iSecondType`      The second type of law (from CATGSMBasicLawType enumeration).
Same legal values as `iFirstType`
### Sub **SetFirstAngleLaw**( double  `iElem1`,  double  `iElem2`,  long  `ilLawType`)

Sets the first angle law useful in some circular sweep types.

**Parameters:**

` iElem1`      The angle law start value
` iElem2`      The angle law end value
` ilLawType`      The angle law type

### Sub **SetGuideDeviation**( double  `iLength`)

Sets the deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.

**Parameters:**

` iLength`      The deviation value

### Sub **SetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepCircle#SetRelimiters Sets the elements relimiting the spine (or the default spine).  **Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipIAElem2`      The second relimiting feature (plane or point)

### Sub **SetRadius**( long  `iI`,  double  `iRadius`)

Sets the radius value useful in some circular sweep types.

**Parameters:**

` iI`      The radius value index (1: start value, 2: end value)
` iRadius`      The radius value

### Sub **SetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  long  `ipOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`,  long  `ipOrient2`)

Sets the elements relimiting the spine (or the default spine).

**Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` ipIAElem2`      The second relimiting feature (plane or point)
` ipOrient2`      Split direction for the second relimitation

### Sub **SetSecondAngleLaw**( double  `iElem1`,  double  `iElem2`,  long  `ilLawType`)

Sets the second angle law useful in some circular sweep types.

**Parameters:**

` iElem1`      The angle law start value
` iElem2`      The angle law end value
` ilLawType`      Tha angle law type

### Sub **SetSmoothAngleThreshold**( double  `iAngle`)

Sets the angular threshold.

**Parameters:**

` iAngle`      The angular threshold

### Sub **SetTangencyChoiceNo**( long  `iShellOri`,  long  `iGuideOri`,  long  `iNo`)

Sets a sequence which identifies a solutionamong all possibilities of a circular profile sweep tangent to a surface.

**Parameters:**

` iNo`      Given the orientations, solution number in a distance ordered list.
` iShellOri`      This orientation allows to compute just the results that are tangent to a specific side of the shell. It can take three values:  | +1 | The result is on the normal side of the shell
---|---
-1 | The result is on the side of the shell opposite to the normal
0 | No orientation is specified
` iGuideOri`      This orientation allows to compute just the results that are on the "left" or the "right" side of the shell, when looking in the guide direction. It can take three values:  +1 | The result is on the "left" side
---|---
-1 | The result is on the "right" side
0 | No orientation is specified