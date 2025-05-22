# PspLightPart (Object)

**_Represents the light part._**
**Role** : To access light object data.

## Methods

### Func **GetDefinition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

Retrieves the points defining the object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).
**Returns:**      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.  **Example:**

```VBScript
Dim objThisIntf As PspLightPart
Dim objArg1 As Product
Dim objArg2 As PspListOfDoubles
Set objArg1 = Nothing
 ...
Set objArg2 = objThisIntf.GetDefinition (objArg1)

```

### Sub **SetDefinition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListPoints`)

Set the points defining the light object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).
` oListPoints`      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.
**Example:**

```VBScript
Dim objThisIntf As PspLightPart
Dim objArg1 As CATSafeArrayVariant
Dim dbVar2(3) As CATSafeArrayVariant
 ...
objThisIntf.SetDefinition objArg1, dbVar2

```