# SchAppCntrDocLink (Object)

**_Manage a schematic connector._**

## Methods

### Sub **AppGetLink**(| [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `oLCntrs`,| | [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md) | `oLDocumentNames`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oPublicationName`)

**Deprecated:**      V5R18 Use [SchAppCntrDocLink.AppGetLinkedDocs](../CATSchPlatformInterfaces/interface_SchAppCntrDocLink_58592.htm#AppGetLinkedDocs) instead. Get a list of linked connector(s) and its document names or publication name.  **Parameters:**

` oLCntrs`      A list of connectors that are linked to this connector.
` oLDocumentNames`      A list of document names containing the linked connector.
` oPublicationName`      The publication name of the connector(s) linked to this connector.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim objArg1 As SchListOfObjects
     Dim objArg2 As SchListOfBSTRs
     Dim strVar3 As String
      ...
     objThisIntf.AppGetLinkobjArg1,objArg2,strVar3

```

### Sub **AppGetLinkedDocs**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPublicationName`,  [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `oLDocumentName`,  [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `oLDocumentUuid`,  [CATIASchListOfLongs](../CATSchPlatformInterfaces/interface_SchListOfLongs_40964.md)  `oLOpenStatus`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntr`)

   Get a list of linked connectors, their documents' names, uuids, and 'open in session' statuses, and a publication name of the connectors.

**Parameters:**

` oPublicationName`      The publication name of the connector(s) linked to this connector.
` oLDocumentName`      A list of document names of the documents containing the linked connector(s).
` oLDocumentUuid`      A list of document UUIDs of the documents containing the linked connector(s).
` oLOpenStatus`      A list of integer flags specifying whether a linked document is open in the session or not (1 - yes; 0 - no).
` oLCntr`      A list of connectors that are linked to this connector.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim strVar1 As String
     Dim objArg2 As SchListOfBSTRs
     Dim objArg3 As SchListOfBSTRs
     Dim objArg4 As SchListOfLongs
     Dim objArg5 As SchListOfObjects
      ...
     objThisIntf.AppGetLinkedDocsstrVar1,objArg2,objArg3,objArg4,objArg5

```

### Sub **AppIsLinkable**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchConnector`,  boolean  `oBYes`)

   Query whether this connector and input connector can be linked.

**Parameters:**

` iSchConnector`      The connector to link to.
` oBYes`      If TRUE, connectors can be linked.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim objArg1 As SchAppConnector
     Dim bVar2 As boolean
      ...
     objThisIntf.AppIsLinkableobjArg1,bVar2

```

### Sub **AppLink**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchConnector`)

   Create an external link to another connector.

**Parameters:**

` iSchConnector`      The connector to link to.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim objArg1 As SchAppConnector
      ...
     objThisIntf.AppLinkobjArg1

```

### Sub **AppLinkInit**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPublicationName`)

   Publish this connector to make it available for linking.

**Parameters:**

` iPublicationName`      The publication name of connector.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim strVar1 As String
      ...
     objThisIntf.AppLinkInitstrVar1

```

### Sub **AppOpenLinkedDoc**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentUuid`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `oDocument`)

   Open a linked document.

**Parameters:**

` iDocumentName`      Name of the document (from oLDocumentName list in AppGetLinkedDocs).
` iDocumentUuid`      Uuid of the document (from oLDocumentUuid list in AppGetLinkedDocs).
` oDocument`      Pointer to the document.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim strVar1 As String
     Dim strVar2 As String
     Dim objArg3 As Document
      ...
     objThisIntf.AppOpenLinkedDocstrVar1,strVar2,objArg3

```

### Sub **AppUnLink**( long  `iUnpublish`)

   Remove external link to another connector.

**Parameters:**

` iUnpublish`      iUnpublish = 0, do not delete publication connector (default) iUnpublish > 0, delete publication connector

**Example:**

```VBScript
     Dim objThisIntf As SchAppCntrDocLink
     Dim intVar1 As Integer
      ...
     objThisIntf.AppUnLinkintVar1

```