# HybridShapeBump (Object)

**_The Bump feature : an Bump is made up of a body to process and some Bump parameters._**

## Properties

### Property **BodyToBump**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to Bump.  
### Property **CenterTension**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns or sets the tensuion center parameter.  
### Property **ContinuityType**( ) As long

   Returns or sets the continuity type ..

**Legal values** : the continuity type is either

```VBScript
     PointContinuity      =0
     TangentContinuity    =1
     CurvatureContinuity  =2

```

### Property **DeformationCenter**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Deformation Center.  
### Property **DeformationDir**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Deformation Direction.  
### Property **DeformationDist**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

   Returns the translate distance (CATIA Parameter).
Note: Distance value is seted or retrieve trough a Literaql parameter
Parameters are value are given in the Part Unit
Example : if Part Unit for dimensions is mm: for 1 mmm, oDefDist.Value will return 1.000  
### Property **DeformationDistValue**( ) As double

   Returns or sets the Deformation distance (double) .
Note: Distance value is expressed in MKS = Meters
Example to set up 1mm , use .001  
### Property **LimitCurve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the limit curve.  
### Property **ProjectionDir**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the limit curve.