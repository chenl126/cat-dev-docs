# SchPostReplace (Object)

**_Manage post component replacement behaviors._**

## Methods

### Sub **PostReplaceText**( [CATIABase](../System/interface_AnyObject_17321.md)  `iNewSchObject`)

Handle associated annotations after replace.

**Parameters:**

` iNewSchObject`      Pointer to the object that is replacing 'this' object.
**Example:**

```VBScript
Dim objThisIntf As SchPostReplace
Dim objArg1 As AnyObject
 ...
objThisIntf.PostReplaceTextobjArg1

```