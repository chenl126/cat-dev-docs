# Plane (Object)

**_Represents the hybrid shape Plane feature object._**
**Role** : Declare hybrid shape Plane root feature object. All interfaces for different type of Plane derivates HybridShapePlane.

Use the CATIAHybridShapeFactory to create a HybridShapePlane objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Sub **GetFirstAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFirstAxis`)

Returns the coordinates of the first plane axis.

**Parameters:**

` oFirstAxis[0]`      The X Coordinate of the first plane axis
` oFirstAxis[1]`      The Y Coordinate of the first plane axis
` oFirstAxis[2]`      The Z Coordinate of the first plane axis
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

Returns the origin of the plane.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the plane origin
` oOrigin[1]`      The Y Coordinate of the plane origin
` oOrigin[2]`      The Z Coordinate of the plane origin
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **GetPosition**( double  `oX`,  double  `oY`,  double  `oZ`)

Gets the position where the plane is displayed.

**Parameters:**

` oX`      X coordinates
` oY`      Y coordinates
` oZ`      Z coordinates
**Returns:**      S_OK if the position has been set before, E_FAIL else.  
### Sub **GetSecondAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSecondAxis`)

Returns the coordinates of the second plane axis.

**Parameters:**

` oSecondAxis[0]`      The X Coordinate of the second plane axis
` oSecondAxis[1]`      The Y Coordinate of the second plane axis
` oSecondAxis[2]`      The Z Coordinate of the second plane axis
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Func **IsARefPlane**( ) As long

Queries whether the plane is a reference plane (fixed axis plane).

**Returns:**      0 when the plane is a reference plane, 1 else.  
### Sub **PutFirstAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iFirstAxis`)

Sets the first axis. The first plane axis must be a point-direction line.
Note: This method can only be used on CATIAHybridShapePlane2Lines feature

**Parameters:**

` iFirstAxis[0]`      The X Coordinate of the first plane axis
` iFirstAxis[1]`      The Y Coordinate of the first plane axis
` iFirstAxis[2]`      The Z Coordinate of the first plane axis
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`)

Sets the origin of the plane.
Note: This method can only be used on CATIAHybridShapePlane2Lines feature

**Parameters:**

` iOrigin[0]`      The X Coordinate of the plane origin
` iOrigin[1]`      The Y Coordinate of the plane origin
` iOrigin[2]`      The Z Coordinate of the plane origin
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **PutSecondAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSecondAxis`)

Sets the coordinates of the second plane axis. The second plane axis must be a point-direction line
Note: This method can only be used on CATIAHybridShapePlane2Lines feature

**Parameters:**

` iSecondAxis[0]`      The X Coordinate of the second plane axis
` iSecondAxis[1]`      The Y Coordinate of the second plane axis
` iSecondAxis[2]`      The Z Coordinate of the second plane axis
**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **RemovePosition**( )

Removes reference position of a plane.
Note: When removed, the plane is displayed at its default position.  
### Sub **SetPosition**( double  `iX`,  double  `iY`,  double  `iZ`)

Sets the position where the plane is displayed.

**Parameters:**

` iX`      X coordinates
` iY`      Y coordinates
` iZ`      Z coordinates