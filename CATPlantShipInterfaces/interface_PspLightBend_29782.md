# PspLightBend (Object)

**_Represents the Light bendable object._**
**Role** : It is used access light bendable data.

## Methods

### Func **GetBendData**( ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

Returns the list of bend radii.

**Returns:**      List of bend radius (PspListOfDoubles).  **Example:**

```VBScript
Dim objThisIntf As PspLightBend

Dim objArg1 As PspListOfDoubles
 ...
Set objArg1 = objThisIntf.GetBendData

```

### Sub **SetBendData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListOfBendRadius`)

Sets a list of bend radii.

**Parameters:**

` iListOfBendRadius`      List of bend radius.
**Example:**

```VBScript
Dim objThisIntf As PspLightBend

Dim objArg1 As CATSafeArrayVariant
 ...
objThisIntf.SetBendData objArg1

```