# SchGapDisplay (Object)

**_Manage the graphical representation of a schematic route._**

## Methods

### Sub **IsGapShown**(| boolean | `oBYes`)

   Query whether gaps are shown (gap attributes exist).

**Parameters:**

` oBYes`      If TRUE, then gaps are shown (gap attributes exist). If FALSE, then gaps are not shown (gap attributes do not exist).

**Example:**

```VBScript
     Dim objThisIntf As SchGapDisplay
     Dim bVar1 As boolean
      ...
     objThisIntf.IsGapShownbVar1

```

### Sub **SetGap**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLUKRoutes`)

   Add gap display attributes on the route.

**Parameters:**

` iLUKRoutes`      A list of routes to be processed, default is NULL (if NULL, then all routes in model are processed). Members are CATISchRoute interface pointers.

**Example:**

```VBScript
     Dim objThisIntf As SchGapDisplay
     Dim objArg1 As SchListOfObjects
      ...
     objThisIntf.SetGapobjArg1

```

### Sub **UnsetGap**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLUKRoutes`)

   Remove gap display attributes on the route. A list of routes to be processed, default is NULL (if NULL, then all routes in model are processed). Members are CATISchRoute interface pointers.

**Example:**

```VBScript
     Dim objThisIntf As SchGapDisplay
     Dim objArg1 As SchListOfObjects
      ...
     objThisIntf.UnsetGapobjArg1

```