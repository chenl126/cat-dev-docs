# SchCntrDocLink (Object)

**_Manage the on-off sheet connector._**

## Methods

### Sub **GetLink**(| [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md) | `oSchConnector`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oDocumentName`)

   Get the linked connector and its document name.

**Parameters:**

` oSchConnector`      The connector that is linked to this connector.
` oDocumentName`      Name of document containing the linked connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrDocLink
     Dim objArg1 As SchAppConnector
     Dim strVar2 As String
      ...
     objThisIntf.GetLinkobjArg1,strVar2

```

### Sub **Link**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchConnector`)

   Create an external link to another connector.

**Parameters:**

` iSchConnector`      The connector to link to.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrDocLink
     Dim objArg1 As SchAppConnector
      ...
     objThisIntf.LinkobjArg1

```

### Sub **UnLink**( )

   Remove external link to another connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrDocLink
      ...
     objThisIntf.UnLink

```