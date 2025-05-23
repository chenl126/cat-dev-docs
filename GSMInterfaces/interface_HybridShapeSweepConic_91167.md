# HybridShapeSweepConic (Object)

**_Represents the hybrid shape conic sweep feature._**

**Role** : To access the data of the conic sweep feature .

Use the [HybridShapeFactory.AddNewSweepConic](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewSweepConic) to create a HybridShapeConicSweep object.

## Properties

### Property **CanonicalDetection**(| ) As long

   Returns or sets whether canonical surfaces of the swept surface are detected.

**Legal values** :  | 0 | No detection of canonical surface is performed.
---|---
2 | Detection of canonical surfaces is performed.
### Property **FifthGuideCrv**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the fifth guide curve.  
### Property **FirstGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first guide curve.  
### Property **FourthGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the fourth guide curve.  
### Property **GuideDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.  
### Property **GuideDeviationActivity**( ) As boolean

   Returns or sets information whether a deviation from guide curves is allowed or not.
Gives the information on performing smoothinh during sweeping operation.
TRUE or FALSE (FALSE if not specified).  
### Property **Parameter**( ) As double

   Returns or sets the parameter for conic sweep operation.
if the parameter is a law, the method returns FALSE see [HybridShapeLawDistProj](../GSMInterfaces/interface_HybridShapeLawDistProj_100210.md) 
### Property **ParameterLaw**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the parameter law useful in conic sweep operation.  
### Property **ParameterLawInversion**( ) As boolean

   Returns or sets the parameter law inversion flag of conic sweep operation.
TRUE if parameter law is inverted. Else it is FALSE. see [HybridShapeLawDistProj](../GSMInterfaces/interface_HybridShapeLawDistProj_100210.md) 
### Property **ParameterLawType**( ) As long

   Returns or sets the parameter law type in conic sweep operation.  
### Property **SecondGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second guide curve.  
### Property **SmoothActivity**( ) As boolean

   Returns or sets information whether sweeping operation is smoothed or not.
TRUE or FALSE (FALSE if not specified).  
### Property **SmoothAngleThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns angular threshold under which discontinuities .
moving frame,tangency net on reference surface will be smoothed when sweeping.  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the spine (optional) for sweep operation.
param : oElem Spine curve.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) 
### Property **ThirdGuideCrv**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the third guide curve.  Methods

### Sub **GetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepConic#GetRelimiters Gets the elements relimiting the spine (or the default spine).
param : opIAElem1 First relimiting feature (plane or point)
param : opIAElem2 Second relimiting feature (plane or point)  
### Sub **GetNbGuides**( long  `oNum`)

   Gets the number of guides.
param : oNum Number of guides curve.  
### Sub **GetParameterLaw**( double  `oParamStart`,  double  `oParamEnd`,  long  `oLawType`)

   Gets the parameter law used in conic sweep operation.
param : oParamStart Parameter law start value.
param : oParamEnd Parameter law end value.
param : oLawType Parameter law type.  
### Sub **GetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem1`,  long  `opOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem2`,  long  `opOrient2`)

   Retrieves the elements relimiting the spine (or the default spine).

**Parameters:**

` opIAElem1`      The first relimiting feature (plane or point)
` opOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` opIAElem2`      The second relimiting feature (plane or point)
` opOrient2`      Split direction for the second relimitation

### Sub **GetTangency**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `opIAAngleStart`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `opIAAngleEnd`,  long  `oLawType`,  long  `iIndex`)

   Gets tangency surface or curve and its angle given the guide curve index.
param : opIAElem
param : opIAAngleStart Start tangency angle from surface or curve reference.
param : opIAAngleEnd End tangency angle from surface or curve reference.
param : oLawType Type of law used for tangency angle from surface or curve reference.
param : iIndex Guide curve index : 1 to 5.  
### Sub **GetTangencyAngleLawInversion**( long  `iIndex`,  long  `oInversion`)

   Gets information whether tangency angle law has to be inverted or not for a specified guide curve.
param : iIndex Guide curve index : 1 to 5
param : oInversion Non-Zero for TRUE and 0 for FALSE.  
### Sub **GetTangencyLaw**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIALaw`,  long  `iIndex`)

   Gets tangency surface or curve and its angle given the guide curve index.
param : opIAElem Tangency surface or curve feature.
param : opIALaw Start tangency angle from surface or curve reference.
param : iIndex Guide curve index : 1 to 5.  
### Sub **RemoveGuide**( long  `iIndex`)

   Removes a guide curve given its index.
it removes also tangency element if specified.
param : iIndex Guide curve index : 1 to 5. If 0, all guides are removed.  
### Sub **RemoveParameter**( )

   Removes conical sweep parameter, whether it is a single value or a law.  
### Sub **RemoveTangency**( long  `iIndex`)

   removes tangency surface or curve and its angle given the guide curve index.
param : iIndex Guide curve index : 1 to 5.  
### Sub **SetGuideDeviation**( double  `iLength`)

   Sets deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.
param : iLength Numerical value.  
### Sub **SetLongitudinalRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`)

**Deprecated:**      V5R16 CATHybridShapeSweepConic#SetRelimiters Sets the elements relimiting the spine (or the default spine).
param : ipIAElem1 First relimiting feature (plane or point)
param : ipIAElem2 Second relimiting feature (plane or point)  
### Sub **SetParameterLaw**( double  `iParamStart`,  double  `iParamEnd`,  long  `iLawType`)

   Sets the parameter law that will be used in conic sweep operation.
param : iParamStart Parameter law start value.
param : iParamEnd Parameter law end value.
param : iLawType Parameter law type.  
### Sub **SetRelimiters**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem1`,  long  `ipOrient1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem2`,  long  `ipOrient2`)

   Sets the elements relimiting the spine (or the default spine).

**Parameters:**

` ipIAElem1`      The first relimiting feature (plane or point)
` ipOrient1`      Split direction for the first relimitation
0 means that the beginning of the spine (considering its orientation) is removed, 1 means that the end of the spine is removed
` ipIAElem2`      The second relimiting feature (plane or point)
` ipOrient2`      Split direction for the second relimitation

### Sub **SetSmoothAngleThreshold**( double  `iAngle`)

   Sets angular threshold under which discontinuities.
note: moving frame,tangency net on reference surface will be smoothed when sweeping.
param : iAngle Numerical value.  
### Sub **SetTangency**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem`,  double  `iAngleStart`,  double  `iAngleEnd`,  long  `ilawType`,  long  `iIndex`)

   Sets tangency surface or curve and its angle given the guide curve index.
param : ipIAElem Tangency surface or curve feature.
param : iAngleStart Start tangency angle from surface or curve reference.
param : iAngleEnd End tangency angle from surface or curve reference.
param : iAngleLawType Type of law used for tangency angle from surface or curve reference.
param : iIndex Guide curve index : 1 to 5.  
### Sub **SetTangencyAngleLawInversion**( long  `iIndex`,  long  `iInversion`)

   Sets information whether tangency angle law has to be inverted or not for a specified guide curve.
param : iIndex Guide curve index : 1 to 5
param : iInversion 1 for TRUE and 0 for FALSE.  
### Sub **SetTangencyLaw**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIALaw`,  long  `iIndex`)

   Sets tangency surface or curve and its angle given the guide curve index.
param : ipIAElem Tangency surface or curve feature.
param : ipIALaw Start tangency angle from surface or curve reference.
param : iIndex Guide curve index : 1 to 5.