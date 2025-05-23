# SchAppCntrData (Object)

**_Manage a schematic connector data._**

## Methods

### Sub **AppGetApplicationData**(| [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md) | `iLAppData`,| | [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md) | `iLAppNlsData`)

   Get application data.

**Parameters:**

` iLAppData`      A list of character string data.
` iLAppNlsData`      A list of character string data.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrData
     Dim objArg1 As SchListOfBSTRs
     Dim objArg2 As SchListOfBSTRs
      ...
     objThisIntf.AppGetApplicationDataobjArg1,objArg2

```

### Sub **AppListPotentialData**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLAppData`,  [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLAppNlsData`)

   Get a list valid potential application data that can be set.

**Parameters:**

` iLAppData`      A list of character string data.
` iLAppNlsData`      A list of character string data.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrData
     Dim objArg1 As SchListOfBSTRs
     Dim objArg2 As SchListOfBSTRs
      ...
     objThisIntf.AppListPotentialDataobjArg1,objArg2

```

### Sub **AppSetApplicationData**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLAppData`)

   Set application data.

**Parameters:**

` iLAppData`      A list of character string data.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrData
     Dim objArg1 As SchListOfBSTRs
      ...
     objThisIntf.AppSetApplicationDataobjArg1

```