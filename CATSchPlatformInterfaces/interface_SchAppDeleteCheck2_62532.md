# SchAppDeleteCheck2 (Object)

**_Manage the deletion of a schematic object._**

## Methods

### Sub **AppOkToDelete**(| boolean | `oOk`)

   Reports if an application object can be deleted.

**Parameters:**

` oOK`      Pointer to the CATBoolean to receive the ok.

**Example:**

```VBScript
     Dim objThisIntf As SchAppDeleteCheck2
     Dim bVar1 As boolean
      ...
     objThisIntf.AppOkToDeletebVar1

```