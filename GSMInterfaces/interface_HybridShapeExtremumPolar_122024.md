# HybridShapeExtremumPolar (Object)

**_Represents the hybrid shape extremum polar feature._**

**Role** : To access the data of the extremum polar feature . This data includes:

  * The contour
  * The support (if exist )
  * The direction of evaluation
  * The extermum type

Use the [HybridShapeFactory.AddNewExtremumPolarto](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewExtremumPolarto) create a HybridShapeExtremumPolar object.

## Properties

### Property **Angle**(| ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   returns the resulting angle of extremum.  
### Property **Contour**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   returns or sets the input contour.  
### Property **Dir**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   returns or sets the direction of computation.  
### Property **ExtremumType**( ) As short

   returns or sets the type of extremum.  
### Property **Origin**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   returns or sets the origin of the polar axis.  
### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   returns the resulting radius of extremum.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   returns or sets the support (if exist).