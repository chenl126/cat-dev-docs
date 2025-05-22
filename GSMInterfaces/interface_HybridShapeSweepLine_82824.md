# HybridShapeSweepLine (Object)

**_Represents the sweep line object._**

## Properties

### Property **AngleLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the angular law.  
### Property **AngleLawInversion**( ) As long

Returns or sets whether the angular law has to be inverted.
Legal angular law inversion values are:  | 0 | The angular law has NOT to be inverted
---|---
1 | The angular law has to be inverted
### Property **AngleLawType**( ) As long

Returns or sets the angular law type.
Legal angular law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Property **CanonicalDetection**( ) As long

Returns or sets whether canonical surfaces of the swept surface are detected.
**Legal values** :  | 0 | No detection of canonical surface is performed.
---|---
2 | Detection of canonical surfaces is performed.
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

### Property **DraftComputationMode**( ) As long

Returns or sets the draft computation mode.  
### Property **DraftDirection**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the draft direction.

Example
:      This example retrieves in `oDirection` the direction of the `LinearSweep` feature.

```VBScript
Dim oDirection As CATIAHybridShapeDirection
Set oDirection = LinearSweep.DraftDirection

```

### Property **FirstGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation first guide curve.  
### Property **FirstGuideSurf**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation first guide surface.  
### Property **FirstLengthLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first length law useful in some linear sweep types.  
### Property **FirstLengthLawInversion**( ) As long

Returns or sets whether the first length law has to be inverted.
Legal length law inversion values are:  | 0 | The length law has NOT to be inverted
---|---
1 | The length law has to be inverted
### Property **GuideDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the deviation value (length) from guide curves allowed during a sweeping operation in order to smooth it.  
### Property **GuideDeviationActivity**( ) As boolean

Returns or sets whether a deviation from guide curves is allowed.
This property gives the information on performing smoothing during sweeping operation.
TRUE if a deviation from guide curves is allowed, or FALSE otherwise (FALSE if not specified).  
### Property **Mode**( ) As long

Returns or sets the linear sweep mode.
Legal mode values are:  | 0 | Undefined linear profile swept surface (CATGSMLinearSweep_None)
---|---
1 | Linear profile swept surface defined by two guide curves (CATGSMLinearSweep_TwoGuides)
2 | Linear profile swept surface defined by a guide curve and an angle (CATGSMLinearSweep_GuideAndAngleCurve)
3 | Linear profile swept surface defined by a guide curve and a middle curve (CATGSMLinearSweep_GuideAndMiddle)
4 | Linear profile swept surface defined by a guide curve and an angle from a reference surface (CATGSMLinearSweep_GuideAndRefSurfaceAngle)
5 | Linear profile swept surface defined by a guide curve and a tangency surface (CATGSMLinearSweep_GuideAndTangencySurface)
6 | Linear profile swept surface defined by a guide curve and a draft directio (CATGSMLinearSweep_GuideAndDraftDirection)
7 | Linear profile swept surface defined by two tangency surfaces (CATGSMLinearSweep_TwoTangencySurfaces)
### Property **SecondGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation second guide curve.  
### Property **SecondGuideSurf**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation second guide surface.  
### Property **SecondLengthLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets second length law useful in some linear sweep types.  
### Property **SecondLengthLawInversion**( ) As long

Returns or sets whether the second length law has to be inverted.
Legal length law inversion values are:  | 0 | The length law has NOT to be inverted
---|---
1 | The length law has to be inverted
### Property **SecondTrimOption**( ) As long

Returns or sets the trim option for the second tangency surface.

Legal trim option values are:  | 0 | No trim computed or trim undefined (CATGSMSweepTrimMode_None)
---|---
1 | Trim computed (CATGSMSweepTrimMode_On)
### Property **SmoothActivity**( ) As boolean

Returns whether the sweeping operation is smoothed.
TRUE if the sweeping operation is smoothed, or FALSE otherwise (FALSE if not specified).  
### Property **SmoothAngleThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the angular threshold.  
### Property **SolutionNo**( ) As long

Returns or sets the choice number, which corresponds to each solution of a given linear sweep case.
For example: a linear sweep with reference surface leads to four possible solutions.  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the sweep operation spine (optional).  
### Property **TrimOption**( ) As long

Returns or sets the trim option.

Legal trim option values are:  | 0 | No trim computed or trim undefined (CATGSMSweepTrimMode_None)
---|---
1 | Trim computed (CATGSMSweepTrimMode_On)
Methods
### Sub **AddDraftAngleDefinitionLocation**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIALocElem`,  double  `iAng`)

Adds a draft angle location.

**Parameters:**

` ipIALocElem`      The geometric element where the draft angle applies
` iAng`      The draft angle

### Func **GetAngle**( long  `iI`) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Returns the angle values useful in some linear sweep types.

**Parameters:**

` iI`      The angle value index
**Returns:**      The angle value  
### Sub **GetAngularLaw**( [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `opStartAng`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `opEndAng`,  long  `oLawType`)

Retrieves the angular law useful in some linear sweep types.

**Parameters:**

` opStartAng`      The angular law start value
` opEndAng`      The angular law end value
` oLawType`      The angular law type
Legal angular law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Sub **GetChoiceNbSurfaces**( long  `oSurfOri1`,  long  `oSurfOri2`,  long  `oSurfCouplOri1`,  long  `oSurfCouplOri2`,  long  `oNo`)

Gets a sequence which identifies a solution amongst all possibilities of a line-profile swept surface, case CATGSMLinearSweep_TwoTangencySurfaces.

**Parameters:**

` oSurfOri1`      This orientation determines the location of the results with regard to the first surface. Possible values are:
* +1 : the result is in the semi-space defined by the normal to the surface,
* -1 : the result is in the semi-space defined by the opposite to the normal to the surface,
* 0 : no orientation is specified, all the results are output,
* 2 : the result changes of semi-space along the spine.

` oSurfOri2`      This orientation determines the location of the results with regard to the second surface. Possible values are as for oSurfOri1.
` oSurfCouplOri1`      This orientation determines the location of the results with regard to the trihedron defined by the the spine, the normal to the first surface and the tangent to the linear profile. Possible values are:
* +1 : the output results are such that the triedron is counter clockwise,
* -1 : the output results are such that the triedron is clockwise,
* 0 : no orientation is specified, all the results are output,
* 2 : the orientation of the trihedron changes along the spine.
` oSurfCouplOri2`      This orientation determines the location of the results with regard to the trihedron defined by the the spine, the normal to the second surface and the tangent to the linear profile. Possible values are as for oSurfCouplOri1.
` oNo`      Given the previous orientations, solution number in a distance ordered list.

### Sub **GetChoiceNo**( long  `oVal1`,  long  `oVal2`,  long  `oVal3`)

Retrieves the choice number associated with each solution of a given linear sweep case.
Example: a linear sweep with one guide curve and a tangency surface may lead to several possible solutions.

**Parameters:**

` oVal1`      The solution number (from 1 to n)
` oVal2`      In the example, the shell orientation : -1, +1 or 0 (both +1 and -1)
` val3`      In the example, the wire orientation : -1, +1 or 0 (both +1 and -1)

### Sub **GetDraftAngleDefinitionLocation**( long  `iLoc`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElement`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oAngle`)

Retrieves the draft angle location element.

**Parameters:**

` iLoc`      The draft angle location position in the list
` opIAElement`      The geometric element at that location and where the draft angle applies
` oAngle`      The draft angle

### Sub **GetDraftAngleDefinitionLocationsNb**( long  `oCount`)

Retrieves the draft angle location list size.

**Parameters:**

` oCount`      The draft angle location list size

### Sub **GetFirstLengthDefinitionType**( long  `oFirstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem`)

Retrieves the first length definition type.

**Parameters:**

` oFirstType`      The first length definition type
Legal length definition types are:  | 0 | Undefined length type (CATGSMLinearSweepLengthType_None)
---|---
1 | Length of the swept line in the sweeping plane from the guide curve (CATGSMLinearSweepLengthType_Standard)
2 | No numerical value is required, equivalent to standard length at zero (CATGSMLinearSweepLengthType_FromCurve)
3 | Up to or from a geometrical reference (a surface) (CATGSMLinearSweepLengthType_Reference)
4 | Only for draft surfaces, the length is computed in the draft direction from an extremum point on the guide curve (CATGSMLinearSweepLengthType_FromExtremum)
5 | Only for draft surfaces, the length will be used in a way similar to euclidean parallel curve distance on the swept surface (CATGSMLinearSweepLengthType_AlongSurface)
` opIAElem`      The geometric element where the first length definition type applies
### Sub **GetFirstLengthLaw**( [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `oLength1`,  [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `oLength2`,  long  `oLawType`)

Retrieves the first length law useful in some linear sweep types.

**Parameters:**

` oLength1`      The length law start value
` oLength2`      The length law end value
` oLawType`      The length law type
Legal length law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Func **GetLength**( long  `iI`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns the length values useful in some linear sweep types.

**Parameters:**

` iI`      The length value index
**Returns:**      The length value  
### Sub **GetLengthLawTypes**( long  `oFirstType`,  long  `oSecondType`)

Gets length law types.

**Parameters:**

` oFirstType`      First type of law.
` oSecondType`      Second type of law. oFirstType and oSecondType = 0 : Undefined law type = 1 : Constant law type = 2 : Linear law type = 3 : S law type = 4 : Law specified by a GSD law feature = 5 : Law specified by a set of points and parameters

### Sub **GetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepLine#GetRelimiters Retrieves the elements relimiting the spine (or the default spine).  **Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opIAElem2`      The second relimiting feature (plane or point)

### Sub **GetNbAngle**( long  `oAng`)

Retrieves the number of angles.

**Parameters:**

` oAng`      The number of angles

### Sub **GetNbGuideCrv**( long  `oNum`)

Retrieves the number of guides curves.

**Parameters:**

` oNum`      The number of guide curves

### Sub **GetNbGuideSur**( long  `oNum`)

Retrieves the number of guide surfaces.

**Parameters:**

` oNum`      The number of guides surfaces

### Sub **GetNbLength**( long  `oLen`)

Retrieves the number of lengths.

**Parameters:**

` oLen`      The number of lengths

### Sub **GetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  long  `opOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`,  long  `opOrient2`)

Retrieves the elements relimiting the spine (or the default spine).

**Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` opIAElem2`      The second relimiting feature (plane or point)
` opOrient2`      Split direction for the second relimitation

### Sub **GetSecondLengthDefinitionType**( long  `oSecondType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem`)

Retrieves the second length definition type.

**Parameters:**

` oSecondType`      The second length definition type
Legal length definition types are:  | 0 | Undefined length type (CATGSMLinearSweepLengthType_None)
---|---
1 | Length of the swept line in the sweeping plane from the guide curve (CATGSMLinearSweepLengthType_Standard)
2 | No numerical value is required, equivalent to standard length at zero (CATGSMLinearSweepLengthType_FromCurve)
3 | Up to or from a geometrical reference (a surface) (CATGSMLinearSweepLengthType_Reference)
4 | Only for draft surfaces, the length is computed in the draft direction from an extremum point on the guide curve (CATGSMLinearSweepLengthType_FromExtremum)
5 | Only for draft surfaces, the length will be used in a way similar to euclidean parallel curve distance on the swept surface (CATGSMLinearSweepLengthType_AlongSurface)
` opIAElem`      The geometric element where the second length definition type applies
### Sub **GetSecondLengthLaw**( [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `oLength1`,  [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `oLength2`,  long  `oLawType`)

Retrieves the second length law useful in some linear sweep types.

**Parameters:**

` oLength1`      The length law start value
` oLength2`      The length law end value
` oLawType`      The length law type
Legal length law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Sub **InsertDraftAngleDefinitionLocation**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `iAngle`,  long  `iPos`)

Inserts a geometrical element and a value necessary for draft angle definition after a given position in the lists.

**Parameters:**

` iElem`      Geometrical element
` iAngle`      Angular parameter
` iPos`      Position in lists. To insert in the beginning of the list put iPos = 0.

### Sub **RemoveAllDraftAngleDefinitionLocations**( )

Removes all geometrical elements and values necessary for draft angle definition.  
### Sub **RemoveAngle**( )

Removes an angle.  
### Sub **RemoveDraftAngleDefinitionLocationPosition**( long  `iPos`)

Removes a draft angle location.

**Parameters:**

` iPos`      The position in the list of the draft angle location to remove

### Sub **RemoveGuideCrv**( )

Removes a guide curve.  
### Sub **RemoveGuideSur**( )

Removes a guide surface.  
### Sub **RemoveLength**( )

Removes a length.  
### Sub **SetAngle**( long  `iI`,  double  `iElem`)

Sets the angle values useful in some linear sweep types.

**Parameters:**

` iI`      The angle value index
` iElem`      The angle value

### Sub **SetAngularLaw**( double  `iStartAng`,  double  `iEndAng`,  long  `iLawType`)

Sets the angular law useful in some linear sweep types.

**Parameters:**

` iStartAng`      The angular law start value
` iEndAng`      The angular law end value
` iLawType`      The angular law type
Legal angular law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Sub **SetChoiceNbSurfaces**( long  `iSurfOri1`,  long  `iSurfOri2`,  long  `iSurfCouplOri1`,  long  `iSurfCouplOri2`,  long  `iNo`)

Sets a sequence which identifies a solution amongst all possibilities of a line-profile swept surface, case CATGSMLinearSweep_TwoTangencySurfaces.

**Parameters:**

` iSurfOri1`      This orientation determines the location of the results with regard to the first surface. Possible values are:
* +1 : the result is in the semi-space defined by the normal to the surface,
* -1 : the result is in the semi-space defined by the opposite to the normal to the ,
* 0 : no orientation is specified, all the results are output,
* 2 : the result changes of semi-space along the spine.

` iSurfOri2`      This orientation determines the location of the results with regard to the second surface. Possible values are as for iSurfOri1.
` iSurfCouplOri1`      This orientation determines the location of the results with regard to the trihedron defined by the the spine, the normal to the first surface and the tangent to the linear profile. Possible values are:
* +1 : the output results are such that the triedron is counter clockwise,
* -1 : the output results are such that the triedron is clockwise,
* 0 : no orientation is specified, all the results are output,
* 2 : the orientation of the trihedron changes along the spine.
` iSurfCouplOri2`      This orientation determines the location of the results with regard to the trihedron defined by the the spine, the normal to the second surface and the tangent to the linear profile. Possible values are as for iSurfCouplOri2.
` iNo`      Given the previous orientations, solution number in a distance ordered list.

### Sub **SetChoiceNo**( long  `iVal1`,  long  `iVal2`,  long  `iVal3`)

Sets the choice number associated with each solution of a given linear sweep case.
Example: a linear sweep with one guide curve and a tangency surface may lead to several possible solutions.

**Parameters:**

` iVal1`      The solution number (from 1 to n)
` iVal2`      In the example, the shell orientation : -1, +1 or 0 (both +1 and -1)
` iVal3`      In the example, the wire orientation : -1, +1 or 0 (both +1 and -1)

### Sub **SetFirstLengthDefinitionType**( long  `iFirstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem`)

Sets the first length definition type.

**Parameters:**

` iFirstType`      The first length definition type
Legal length definition types are:  | 0 | Undefined length type (CATGSMLinearSweepLengthType_None)
---|---
1 | Length of the swept line in the sweeping plane from the guide curve (CATGSMLinearSweepLengthType_Standard)
2 | No numerical value is required, equivalent to standard length at zero (CATGSMLinearSweepLengthType_FromCurve)
3 | Up to or from a geometrical reference (a surface) (CATGSMLinearSweepLengthType_Reference)
4 | Only for draft surfaces, the length is computed in the draft direction from an extremum point on the guide curve (CATGSMLinearSweepLengthType_FromExtremum)
5 | Only for draft surfaces, the length will be used in a way similar to euclidean parallel curve distance on the swept surface (CATGSMLinearSweepLengthType_AlongSurface)
` ipIAElem`      The geometric element where the first length definition type applies
### Sub **SetFirstLengthLaw**( double  `iLength1`,  double  `iLength2`,  long  `iLawType`)

Sets the first length law useful in some linear sweep types.

**Parameters:**

` iLength1`      The length law start value
` iLength2`      The length law end value
` iLawType`      The length law type
Legal length law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Sub **SetGuideDeviation**( double  `iLength`)

Sets the deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.

**Parameters:**

` iLength`      The deviation value

### Sub **SetLength**( long  `iI`,  double  `iElem`)

Sets the linear values useful in some linear sweep types.

**Parameters:**

` iI`      The linear value index
` iElem`      The linear value

### Sub **SetLengthLawTypes**( long  `iFirstType`,  long  `iSecondType`)

Sets length law types.

**Parameters:**

` iFirstType`      First type of law.
` iSecondType`      Second type of law. iFirstType and iSecondType = 0 : Undefined law type = 1 : Constant law type = 2 : Linear law type = 3 : S law type = 4 : Law specified by a GSD law feature = 5 : Law specified by a set of points and parameters

### Sub **SetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepLine#SetRelimiters Sets the elements relimiting the spine (or the default spine).  **Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipIAElem2`      The second relimiting feature (plane or point)

### Sub **SetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  long  `ipOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`,  long  `ipOrient2`)

Sets the elements relimiting the spine (or the default spine).

**Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` ipIAElem2`      The second relimiting feature (plane or point)
` ipOrient2`      Split direction for the second relimitation

### Sub **SetSecondLengthDefinitionType**( long  `iSecondType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem`)

Sets the second length definition type.

**Parameters:**

` iSecondType`      The second length definition type
Legal length definition types are:  | 0 | Undefined length type (CATGSMLinearSweepLengthType_None)
---|---
1 | Length of the swept line in the sweeping plane from the guide curve (CATGSMLinearSweepLengthType_Standard)
2 | No numerical value is required, equivalent to standard length at zero (CATGSMLinearSweepLengthType_FromCurve)
3 | Up to or from a geometrical reference (a surface) (CATGSMLinearSweepLengthType_Reference)
4 | Only for draft surfaces, the length is computed in the draft direction from an extremum point on the guide curve (CATGSMLinearSweepLengthType_FromExtremum)
5 | Only for draft surfaces, the length will be used in a way similar to euclidean parallel curve distance on the swept surface (CATGSMLinearSweepLengthType_AlongSurface)
` ipIAElem`      The geometric element where the second length definition type applies
### Sub **SetSecondLengthLaw**( double  `iLength1`,  double  `iLength2`,  long  `iLawType`)

Sets the second length law useful in some linear sweep types.

**Parameters:**

` iLength1`      The length law start value
` iLength2`      The length law end value
` iLawType`      The length law type
Legal length law type values are:  | 0 | Undefined law type (CATGSMBasicLawType_None)
---|---
1 | Constant law type (CATGSMBasicLawType_Constant)
2 | Linear law type (CATGSMBasicLawType_Linear)
3 | S law type (CATGSMBasicLawType_SType)
4 | Law specified by a GSD law feature (CATGSMBasicLawType_Advanced)
### Sub **SetSmoothAngleThreshold**( double  `iAngle`)

Sets the angular threshold.

**Parameters:**

` iAngle`      The angle numerical value