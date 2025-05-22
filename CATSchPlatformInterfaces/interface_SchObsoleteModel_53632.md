# SchObsoleteModel (Object)

**_Manage obsolete model elements._**

## Methods

### Func **FindObsoleteClasses**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

Find obsolete base classes. This method will internally call CATISchAppObsoleteClass to ask the application for the names of the obsolete classes.

**Parameters:**

` oListObsoleteObj`      A list of objects with obsoleted base class types.
**Example:**

```VBScript
Dim objThisIntf As SchObsoleteModel
Dim objArg1 As SchListOfObjects
 ...
Set objArg1 = objThisIntf.FindObsoleteClasses

```

### Sub **HasObsoleteClass**( boolean  `oBYes`)

Is there any obsolete class in the application model.

**Parameters:**

` oBYes`      If yes, then there is.
**Example:**

```VBScript
Dim objThisIntf As SchObsoleteModel
Dim bVar1 As boolean
 ...
objThisIntf.HasObsoleteClassbVar1

```