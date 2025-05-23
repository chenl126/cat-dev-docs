# SchAppDeleteCheck (Object)

**_Manage the deletion of a schematic object._**

## Methods

### Sub **AppGetDeleteWarning**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oCaption`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oMessage`)

   Returns the caption and message text to be used as a warning for the delete operation.

**Parameters:**

` oCaption`      Pointer to a CATUnicode string used for the caption of the message box.
` oMessage`      Pointer to a CATUnicode string used as the warning message.

**Example:**

```VBScript
     Dim objThisIntf As SchAppDeleteCheck
     Dim strVar1 As String
     Dim strVar2 As String
      ...
     objThisIntf.AppGetDeleteWarningstrVar1,strVar2

```

### Sub **AppOkToDeleteWithoutWarning**( boolean  `oOk`)

   Reports if a warning message should be issued before deleting the object.

**Example:** A Logical Line with members cannot be deleted without complications. Its members must also be deleted for model integrity. A Logical Line with members would return FALSE in this case.

**Parameters:**

` oOK`      Pointer to the CATBoolean to receive the ok.

**Example:**

```VBScript
     Dim objThisIntf As SchAppDeleteCheck
     Dim bVar1 As boolean
      ...
     objThisIntf.AppOkToDeleteWithoutWarningbVar1

```