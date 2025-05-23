# HybridShapeExtremum (Object)

**_Represents the hybrid shape extremum feature object._**

**Role** : To access the data of the hybrid shape extremum feature object. This data includes:

  * The three directions into which the extremum is detected
  * The object onto which the extremum is detected
  * The extremum type of each direction

Use the CATIAHybridShapeFactory to create a HybridShapeExtremum object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Direction**(| ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the direction into which the extremum is detected.  
### Property **Direction2**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the second direction into which the extremum is detected.  
### Property **Direction3**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the third direction into which the extremum is detected.  
### Property **ExtremumType**( ) As long

   Returns or sets the extremum type.

**Legal values** : 1 to get a maximum element or 0 to get a minimum element.  
### Property **ExtremumType2**( ) As long

   Returns or sets the extremum type of the second direction.

**Legal values** : 1 to get a maximum element or 0 to get a minimum element.  
### Property **ExtremumType3**( ) As long

   Returns or sets the extremum type of the third direction.

**Legal values** : 1 to get a maximum element or 0 to get a minimum element.  
### Property **ReferenceElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the object on which the extremum is detected.