# Line (Object)

**_Represents the hybrid shape Line feature object._**
**Role** : Declare hybrid shape Line root feature object. All interfaces for different type of Line derivates HybridShapeLine.

Use the CATIAHybridShapeFactory to create a HybridShapeLine objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FirstUptoElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Gets the First upto element of the line.

**Parameters:**

` oFirstUpto`
**Returns:**      HRESULT S_OK if Ok E_FAIL else  
### Property **SecondUptoElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Gets the Second upto element of the line.

**Parameters:**

` oSecondUpto`
**Returns:**      HRESULT S_OK if Ok E_FAIL else  Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

**Role** : Returns the unit-vector pointing in the direction of the line.

**Parameters:**

` oDirection`
` oDirection[0]`      The X Coordinate of the unit vector pointing in the direction of the line
` oDirection[1]`      The Y Coordinate of the unit vector pointing in the direction of the line
` oDirection[2]`      The Z Coordinate of the unit vector pointing in the direction of the line
**Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

**Role** : Returns the origin of the line.

**Parameters:**

` oOrigin`
` oOrigin[0]`      The X Coordinate of a point lying on the line
` oOrigin[1]`      The Y Coordinate of a point lying on the line
` oOrigin[2]`      The Z Coordinate of a point lying on the line The Origin is evaluated from the geometry of the line.
**Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Sub **PutDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDirection`)

**Role** : Sets the unit-vector pointing in the direction of the line.

**Parameters:**

` iDirection`
` iDirection[0]`      The X Coordinate of the unit vector pointing in the direction of the line
` iDirection[1]`      The Y Coordinate of the unit vector pointing in the direction of the line
` iDirection[2]`      The Z Coordinate of the unit vector pointing in the direction of the line
**Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)