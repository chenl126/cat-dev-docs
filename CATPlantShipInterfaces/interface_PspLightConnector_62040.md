# PspLightConnector (Object)

**_Represents the light connector._**

**Role** : To access light connector data.

## Methods

### Func **GetAlignmentVector**(| [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetAlignmentVector (objArg1)

```

### Func **GetOrientationVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the Orientation Direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oAlignmentDirection`      Three double values stand for X,Y,Z components of the alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetOrientationVector (objArg1)

```

### Func **GetOrigin**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` oOrigin`      Origin point position-three double values stand for x,y,z

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.GetOrigin (objArg1)

```

### Sub **SetAlignmentVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAlignmentDirection`)

   Sets the alignment direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iAlignmentDirection`      Three double values stand for X,Y,Z component of the Alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetAlignmentVector objArg1, dbVar2

```

### Sub **SetOrientationVector**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrientationDirection`)

   Sets the Orientation Direction of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iAlignmentDirection`      Three double values stand for X,Y,Z component of the Alignment vector

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetAlignmentVector objArg1, dbVar2

```

### Sub **SetOrigin**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb3Position`)

   Sets the position of the connector.

**Parameters:**

` iRelAxis`      the relative axis object (Nothing means relative to parent)
` iDb3Position`      absolute X-Y-Z coordinates of the current position of the connector to be set

**Example:**

```VBScript
     Dim objThisIntf As PspLightConnector
     Dim objArg1 As  Product
     Dim dbVar2(3) As CATSafeArrayVariant
      ...
     objThisIntf.SetOrigin objArg1, dbVar2

```