# SchAppCntrName (Object)

**_Manage a schematic connector._**

## Methods

### Func **AppListNames**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

List connector names allowed.

**Parameters:**

` oLConnectorNamesAllowed`      A list of connector names allowed. The caller must allocate memory for the first level pointer (i.e. oLConnectorNamesAllowed) and release the second level pointer (i.e. *oLConnectorNamesAllowed) after usage.
**Example:**

```VBScript
Dim objThisIntf As SchAppCntrName
Dim objArg1 As SchListOfBSTRs
 ...
Set objArg1 = objThisIntf.AppListNames

```

### Sub **GetName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oName`)

Get the application connector name.

**Parameters:**

` oName`      The connector name. The caller must allocate memory for the first level pointer (i.e. oName) and release the second level pointer (i.e. *oName) after usage.
**Example:**

```VBScript
Dim objThisIntf As SchAppCntrName
Dim strVar1 As String
 ...
objThisIntf.GetNamestrVar1

```

### Sub **SetName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

Set the application connector name.

**Parameters:**

` oName`      The connector name.
**Example:**

```VBScript
Dim objThisIntf As SchAppCntrName
Dim strVar1 As String
 ...
objThisIntf.SetNamestrVar1

```