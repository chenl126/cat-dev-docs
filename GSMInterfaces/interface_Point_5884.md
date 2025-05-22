# Point (Object)

**_Represents the hybrid shape Point feature object._**
**Role** : Declare hybrid shape Point root feature object. All interfaces for different type of Point derivates HybridShapePoint.

Use the CATIAHybridShapeFactory to create a HybridShapePoint objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

Gets cartesian coordinates of the point.

**Parameters:**

` oCoordinates`      coordinates of the point.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **SetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

Sets cartesian coordinates of the point.
Note: SetCoordinates can only be used on CATIAHybridShapePointCoord feature

**Parameters:**

` iCoordinates`      coordinates of the point.
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)