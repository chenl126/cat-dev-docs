# HybridShapeSweepExplicit (Object)

**_Represents the hybrid shape Sweep explicit feature object._**
**Role** : To access the data of the hybrid shape sweep explicit feature object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AngleLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the angle law feature associated to the reference surface.

**Parameters:**

` oElem`      Angle law element. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **AngleLawInversion**( ) As long

Returns or sets the angle law inversion information.

**Parameters:**

` oElem`      Angle law inversion information.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **AngleLawType**( ) As long

Returns or sets the angle law type associated to the reference surface.

**Parameters:**

` oElem`      Angle law type.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
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

### Property **FirstGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the first guide curve.

**Parameters:**

` oElem`      Guide curve. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **GuideDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.  
### Property **GuideDeviationActivity**( ) As boolean

Returns or sets information whether a deviation from guide curves is allowed or not.
Gives the information on performing smoothing during sweeping operation.
TRUE or FALSE (FALSE if not specified).  
### Property **GuideProjection**( ) As boolean

Returns or sets the projection of the guide curve onto the reference plane in order to use it as spine, in pulling direction case only. Removes Spine if GuideProjection is set to TRUE.
**Legal values** : **True** projection is required and **False** if not

**Example:**      This example sets that the GuideProjection mode of the `Sweep` hybrid shape sweep explicit feature to True.

```VBScript
Sweep.GuideProjection = True

```

### Property **Mode**( ) As long

Returns or sets positioning mode used for the profile.

**Parameters:**

` oElem`
**Values :**
= 1 - CATGSMPositionMode_NoneOrPositioned : no positioning,

= 2 - CATGSMPositionMode_ExplicitSweep : the explicit profile is to be moved from its initial plane to the first sweep plane,

= 3 - CATGSMPositionMode_Develop : === DO NOT USE IN THIS CASE ===
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **PositionMode**( ) As long

Returns or sets positioning mode.
**Legal values** :

0
    CATGSMPositionMode_NoneOrPositioned.
1
    CATGSMPositionMode_ExplicitSweep. if a positioning operation is done.
**Example** :      This example retrieves in `oPosMode` the position mode for the `Sweep` hybrid shape feature.

```VBScript
oPosMode = Sweep.PositionMode

```

### Property **PositionedProfile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the positioning transformation associated to the explicit swept surface and which result corresponds to the positioned profile.

**Parameters:**

` oElem`      Positioning transformation / positioned profile. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Profile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the profile to be swept out.

**Parameters:**

` oElem`      Profile element. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **ProfileXAxisComputationMode**( ) As long

Returns or sets the computation mode of the X axis (or direction) of the initial axis system (on the profile). Default value is CATGSMPositionDirCompMode_None when PosDirection(OutputDirection) is not specified and CATGSMPositionDirCompMode_User if OutputDirection is specified.
**Legal values** :

0
    CATGSMPositionDirCompMode_None. No X axis specified.
1
    CATGSMPositionDirCompMode_Tangent: the X axis is implicitly the tangent of the profile at the origin (the origin then HAS to be on the profile)
2
    CATGSMPositionDirCompMode_User: the X axis is specified by a direction via SetPosDirection(UserInputDirection, 1)
**Example** :      This example retrieves in `oDirCompMode` the Profile X Axis ComputationMode for the `Sweep` hybrid shape feature.

```VBScript
oDirCompMode = Sweep.ProfileXAxisComputationMode

```

### Property **PullingDirection**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Gets or sets the pulling direction
If the direction is specified, the plane normal to this direction is taken as reference surface.

**Example** :      This example retrieves in `ohDir` the pulling direction feature for the `Sweep` hybrid shape feature.

```VBScript
Dim ohDir As CATIAHybridShapeDirection
Set ohDir = Sweep.PullingDirection

```

### Property **Reference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference surface (optional).

**Parameters:**

` oElem`      Reference surface. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) 
### Property **SecondGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the second guide curve (optional).

**Parameters:**

` oElem`      Guide curve. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **SmoothActivity**( ) As boolean

Returns or sets information whether sweeping operation is smoothed or not.
TRUE or FALSE (FALSE if not specified).  
### Property **SmoothAngleThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns angular threshold.  
### Property **SolutionNo**( ) As long

Returns or sets the choice number, which corresponds to each solution of a given explicit sweep case.
For example: a explicit sweep with reference surface leads to four possible solutions.  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the spine (optional) for sweep operation.

**Parameters:**

` oElem`      Spine curve. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **SubType**( ) As long

Returns or sets the explicit sweep subtype.
Legal subtype values are:  | 1 | Explicit profile swept surface defined with reference surface
---|---
2 | Explicit profile swept surface defined with two guide curves
3 | Explicit profile swept surface defined with pulling direction
Methods
### Func **GetAngleRef**( long  `ii`) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Gets the angle value associated to the reference surface.

**Parameters:**

` iI`      Angle value index (1: start value, 2: end value).
` oElem`      Angle value. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **GetFittingPoints**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElemA`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElemB`)

Gets the fitting points : located in the profile plane, these points are used for two-guide swept surfaces to determine guide intersection locations.
param opIAElem1 Fitting point associated to the first guide
param opIAElem2 Fitting point associated to the second guide  
### Sub **GetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElemA`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElemB`)

**Deprecated:**      V5R16 CATHybridShapeSweepExplicit#GetRelimiters Returns the elements relimiting the spine (or the default spine).
param : opIAElem1 First relimiting feature (plane or point)
param : opIAElem2 Second relimiting feature (plane or point)  
### Sub **GetNbAngle**( long  `oAng`)

Returns the number of Angles.
param : oAng Number of Angle.  
### Sub **GetNbGuide**( long  `oNum`)

Gets the number of guides curves.
param : oNum Number of guide curves.  
### Sub **GetNbPosAngle**( long  `oPosAng`)

Gets the number of numerical positioning parameters corresponding to angles from the default positions of the X axes.
param : oPosAng Number of parameters  
### Sub **GetNbPosCoord**( long  `oPosCoord`)

Gets the number of numerical positioning parameters corresponding to coordinates of the new axes systems origins.
param oPosCoord Number of parameters  
### Func **GetPosAngle**( long  `ii`) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Gets angles if both profile and first sweep plane axis systems from default positions.

**Parameters:**

` iI`      Index of numerical positioning coordinates in profile (value 1) or first sweep plane (value 2) axis system.
` oElem`      Angle value. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **GetPosCoord**( long  `ii`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Gets translations coordinates if both profile axis system and first sweep plane axis system from default positions.

**Parameters:**

` iI`      Index of numerical positioning coordinates in profile (value 1 or 2) or first sweep plane (value 3 or 4) axis system.
` oElem`      Coordinate value. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **GetPosDirection**( long  `ii`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the positioning directions : profile plane or first sweep plane X-axis direction.

**Parameters:**

` iI`      Plane index : 1 for profile plane, 2 for first sweep plane.
` oElem`      Direction element. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **GetPosPoint**( long  `ii`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the points designated as the origins of the profile plane and first sweep plane.

**Parameters:**

` iI`      Plane index : 1 for profile plane, 2 for first sweep plane.
` oElem`      Origin point. return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **GetPosSwapAxes**( long  `ii`) As long

Gets axes inversion from previous definition for both profile plane and first sweep plane.

**Parameters:**

` iI`      Axis system index (1 for profile plane, 2 for first sweep plane).
` oElem`      Inversion value:
**Inversion values :**
= 1 - CATGSMAxisInversionMode_None : no axis inverted.
= 2 - CATGSMAxisInversionMode_X : only X axis inverted.
= 3 - CATGSMAxisInversionMode_Y : only Y axis inverted.
= 4 - CATGSMAxisInversionMode_Both : both axes inverted.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **GetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  long  `opOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`,  long  `opOrient2`)

Retrieves the elements relimiting the spine (or the default spine).

**Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` opIAElem2`      The second relimiting feature (plane or point)
` opOrient2`      Split direction for the second relimitation

### Sub **IsSketchAxisUsedAsDefault**( boolean  `oBoolean`)

Queries status wherere Sketch axis used as default or not.
In case of a sketch profile, specify if the 2D sketch axis must be used as default planar profile axis (for positioning purpose) or not.
param oBoolean TRUE if the 2D sketch axis must be used, FALSE if not.  
### Sub **RemoveAngle**( )

Removes an Angle.  
### Sub **RemoveFittingPoints**( )

Removes the fitting points.  
### Sub **RemoveGuide**( )

Removes a guide curve.  
### Sub **SetAngleRef**( long  `ii`,  double  `Elem`)

Sets the angle value associated to the reference surface.

**Parameters:**

` iI`      Angle value index (1: start value, 2: end value).
` iElem`      Angle value.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetFittingPoints**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElemA`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElemB`)

Sets the fitting points.
Does not work with NULL_var values, Use RemoveFittingPoints() method instead.
param ipIAElem1 Fitting point associated to the first guide (must not be equal to NULL_var)
param ipIAElem2 Fitting point associated to the second guide (can be equal to NULL_var)  
### Sub **SetGuideDeviation**( double  `iLength`)

Sets deviation value (length) from guide curves allowed during sweeping. operation in order to smooth it.
param : iLength Numerical value.  
### Sub **SetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElemA`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElemB`)

**Deprecated:**      V5R16 CATHybridShapeSweepExplicit#SetRelimiters Sets the elements relimiting the spine (or the default spine).
param : ipIAElem1 First relimiting feature (plane or point)
param : ipIAElem2 Second relimiting feature (plane or point)  
### Sub **SetPosAngle**( long  `ii`,  double  `Elem`)

Sets angles if both profile and first sweep plane axis systems from default positions.

**Parameters:**

` iI`      Index of numerical positioning coordinates in profile (value 1) or first sweep plane (value 2) axis system.
` iElem`      Angle value.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetPosCoord**( long  `ii`,  double  `Elem`)

Sets translations coordinates if both profile axis system and first sweep plane axis system from default positions.

**Parameters:**

` iI`      Index of numerical positioning coordinates in profile (value 1 or 2) or first sweep plane (value 3 or 4) axis system.
` iElem`      Coordinate value.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetPosDirection**( long  `ii`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Elem`)

Sets the positioning directions : profile plane or first sweep plane X-axis direction.

**Parameters:**

` iI`      Plane index : 1 for profile plane, 2 for first sweep plane.
` iElem`      Direction element.
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetPosPoint**( long  `ii`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Elem`)

Sets the points designated as the origins of the profile plane and first sweep plane.

**Parameters:**

` iI`      Plane index : 1 for profile plane, 2 for first sweep plane.
` iElem`      Origin point.
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetPosSwapAxes**( long  `ii`,  long  `Elem`)

Sets axes inversion from previous definition for both profile plane and first sweep plane.

**Parameters:**

` iI`      Axis system index (1 for profile plane, 2 for first sweep plane).
` iElem`      Inversion value:

**Inversion values :**
= 1 - CATGSMAxisInversionMode_None : no axis inverted.
= 2 - CATGSMAxisInversionMode_X : only X axis inverted.
= 3 - CATGSMAxisInversionMode_Y : only Y axis inverted.
= 4 - CATGSMAxisInversionMode_Both : both axes inverted.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  long  `ipOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`,  long  `ipOrient2`)

Sets the elements relimiting the spine (or the default spine).

**Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` ipIAElem2`      The second relimiting feature (plane or point)
` ipOrient2`      Split direction for the second relimitation

### Sub **SetSmoothAngleThreshold**( double  `iAngle`)

Sets angular threshold.
param : iAngle Numerical value.  
### Sub **UseSketchAxisAsDefault**( boolean  `iBoolean`)

Uses Sketch Axis As Default.
In case of a sketch profile, specify if the 2D sketch axis must be used as default planar profile axis (for positioning purpose) or not.
param iBoolean TRUE if the 2D sketch axis must be used, FALSE if not.