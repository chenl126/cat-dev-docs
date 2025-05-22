# SchAppReplace (Object)

**_Manage a schematic component._**

## Methods

### Sub **AppOKToReplace**( [CATIABase](../System/interface_AnyObject_17321.md)  `iSchObjectToBeReplacedByThis`,  boolean  `oBYes`)

Query whether it is OK to replace an existing object (component, route...) with this object.

**Parameters:**

` iSchObjectToBeReplacedByThis`      Pointer to the existing object to be replaced by this object.
` oBYes`      If TRUE, then it is OK to replace the object.
**Example:**

```VBScript
Dim objThisIntf As SchAppReplace
Dim objArg1 As AnyObject
Dim bVar2 As boolean
 ...
objThisIntf.AppOKToReplaceobjArg1,bVar2

```

### Sub **AppPostReplaceProcess**( [CATIABase](../System/interface_AnyObject_17321.md)  `iSchObjectToBeReplacedByThis`)

Post process after replacing an object.

**Parameters:**

` iNewObject`      The new Application object
**Example:**

```VBScript
Dim objThisIntf As SchAppReplace
Dim objArg1 As AnyObject
 ...
objThisIntf.AppPostReplaceProcessobjArg1

```