# SchAppClass (Object)

**_Manage the class hierarchy of an application model._**

## Methods

### Func **AppGetComponentBaseClass**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

Provide the application class names for the base component classes.

**Parameters:**

` oLBaseCompClasses`      Class names of application base component classes.
**Example:**

```VBScript
Dim objThisIntf As SchAppClass
Dim objArg1 As SchListOfBSTRs
 ...
Set objArg1 = objThisIntf.AppGetComponentBaseClass

```

### Sub **AppGetGroupBaseClass**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oGroupClassName`)

Provide the application class name for Schematic Group class.

**Parameters:**

` oGroupClassName`      Class name of application class.
**Example:**

```VBScript
Dim objThisIntf As SchAppClass
Dim strVar1 As String
 ...
objThisIntf.AppGetGroupBaseClassstrVar1

```

### Sub **AppGetRouteBaseClass**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRouteClassName`)

Provide the application class name for Schematic Route class.

**Parameters:**

` oRouteClassName`      Class name of application class.
**Example:**

```VBScript
Dim objThisIntf As SchAppClass
Dim strVar1 As String
 ...
objThisIntf.AppGetRouteBaseClassstrVar1

```

### Sub **AppGetZoneBaseClass**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oZoneClassName`)

Provide the application class name for Schematic Zone class.

**Parameters:**

` oZoneClassName`      Class name of application class.
**Example:**

```VBScript
Dim objThisIntf As SchAppClass
Dim strVar1 As String
 ...
objThisIntf.AppGetZoneBaseClassstrVar1

```

### Func **AppListValidRouteTypes**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

List the valid application route types allowed to be created.

**Parameters:**

` oLValidRouteTypes`      A list of route class types allowed.
**Example:**

```VBScript
Dim objThisIntf As SchAppClass
Dim objArg1 As SchListOfBSTRs
 ...
Set objArg1 = objThisIntf.AppListValidRouteTypes

```