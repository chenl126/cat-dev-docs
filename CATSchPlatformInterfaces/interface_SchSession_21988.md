# SchSession (Object)

**_Represents a schematic session._**

## Methods

### Sub **CreateDocument**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocType`,  boolean  `iBInteractive`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `oNewDoc`)

Create a document with Schematic context.

**Parameters:**

` iDocType`      Document type, if NULL "Product" is assumed. These are the types shown in the File+New list
` iBInteractive`      If TRUE, document is created in interactive session with editor
` oNewDoc`      Document created.
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim strVar1 As String
Dim bVar2 As boolean
Dim objArg3 As Document
 ...
objThisIntf.CreateDocumentstrVar1,bVar2,objArg3

```

### Sub **GetCurrentApplicationID**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oApplicationID`)

Get the current application ID.

**Parameters:**

` oApplicationID`      Application ID
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim strVar1 As String
 ...
objThisIntf.GetCurrentApplicationIDstrVar1

```

### Func **GetCurrentDocument**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Get the current document.

**Parameters:**

` oCurDoc`      Pointer to current document. DO NOT NEED TO RELEASE OUTPUT POINTER.
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim objArg1 As Document
 ...
Set objArg1 = objThisIntf.GetCurrentDocument

```

### Func **GetSchExtContainer**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`) As [CATIABase](../System/interface_AnyObject_17321.md)

Get the schematic container (e.g. for CATISchBaseFactory implementation).

**Parameters:**

` iDoc`      Document in the session to retreive the container from
` oContainer`      Schematic container shown in the File+New list
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim objArg1 As Document
Dim objArg2 As AnyObject
 ...
Set objArg2 = objThisIntf.GetSchExtContainer(objArg1)

```

### Sub **SetCurrentApplicationID**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationID`)

Set the current application ID.

**Parameters:**

` iApplicationID`      Application ID
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim strVar1 As String
 ...
objThisIntf.SetCurrentApplicationIDstrVar1

```

### Sub **SetCurrentDocument**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iCurDoc`)

Set the current document.

**Parameters:**

` iCurDoc`      Pointer to current document.
**Example:**

```VBScript
Dim objThisIntf As SchSession
Dim objArg1 As Document
 ...
objThisIntf.SetCurrentDocumentobjArg1

```