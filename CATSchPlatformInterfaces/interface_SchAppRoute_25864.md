# SchAppRoute (Object)

**_Manage a schematic route._**

## Methods

### Func **AppBreak**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Break the application route into 2 routes.

**Parameters:**

` oNewAppRoute`      New application route
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim objArg1 As AnyObject
 ...
Set objArg1 = objThisIntf.AppBreak

```

### Func **AppCreateLocalReference**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToPutCopyIn`) As [CATIASchAppRoute](../CATSchPlatformInterfaces/interface_SchAppRoute_25864.md)

Make a local route reference in another document by copying an existing one in the current document.

**Parameters:**

` iDocumentToPutCopyIn`      Pointer to the document to make the copy in
` oSchAppRoute`      Pointer to the copy.
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim objArg1 As Document
Dim objArg2 As SchAppRoute
 ...
Set objArg2 = objThisIntf.AppCreateLocalReference(objArg1)

```

### Sub **AppOKToBranch**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iBranchClassType`,  boolean  `oBYes`)

Query whether it is OK to create branch.

**Parameters:**

` iBranchClassType`      Class type of the branch to create.
` oBYes`      If TRUE, then it is OK to create a branch from an application route
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim strVar1 As String
Dim bVar2 As boolean
 ...
objThisIntf.AppOKToBranchstrVar1,bVar2

```

### Sub **AppOKToBreak**( boolean  `oBYes`)

Query whether it is OK to break.

**Parameters:**

` oBYes`      If TRUE, then it is OK to break the application route
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToBreakbVar1

```

### Sub **AppOKToConcatenate**( boolean  `oBYes`)

Query whether it is OK to concatenate.

**Parameters:**

` oBYes`      If TRUE, then it is OK to concatenate the application route with another
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToConcatenatebVar1

```

### Sub **AppOKToModifyPoints**( boolean  `oBYes`)

Query whether it is OK to modify (add or remove) the points.

**Parameters:**

` oBYes`      If TRUE, then it is OK to add or remove the points from the application route
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToModifyPointsbVar1

```

### Sub **AppPostBreakProcess**( [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iOldAppRoute`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iNewAppRoute`)

Post process after breaking an application route into 2 pieces.

**Parameters:**

` iOldAppRoute`      The old application route object
` iNewAppRoute`      The new Application route object
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim objArg1 As SchRoute
Dim objArg2 As SchRoute
 ...
objThisIntf.AppPostBreakProcessobjArg1,objArg2

```

### Sub **AppPostConcatenateProcess**( [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iSchRoute2`)

Post process after concatenate 2 application routes into one.

**Parameters:**

` iSchRoute2`      Second route to be concatenate to this. This route will be deleted.
**Example:**

```VBScript
Dim objThisIntf As SchAppRoute
Dim objArg1 As SchRoute
 ...
objThisIntf.AppPostConcatenateProcessobjArg1

```