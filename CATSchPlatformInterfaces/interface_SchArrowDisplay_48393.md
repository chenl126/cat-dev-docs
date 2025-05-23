# SchArrowDisplay (Object)

**_Manage the graphical representation of a schematic route._**

## Methods

### Sub **IsArrowShown**(| boolean | `oBYes`)

   Query whether flow arrows are shown (arrow attributes exist).

**Parameters:**

` oBYes`      If TRUE, then Flow arrows are shown (arrow attributes exist). If FALSE, then Flow arrows are not shown (arrow attributes do not exist).

**Example:**

```VBScript
     Dim objThisIntf As SchArrowDisplay
     Dim bVar1 As boolean
      ...
     objThisIntf.IsArrowShownbVar1

```

### Sub **SetArrow**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  long  `iSegNum`)

   Add arrow display attributes on the route.

**Parameters:**

` iGRR`      iGRR means apply only to segments of iGRR. (if iGRR = NULL, apply to segments of all GRR's of the route, and ignore iSegNum)
` iSegNum`      iSegNum = 0 means apply to all segments of iGRR. iSegnum > 0 means apply to only to segment number iSegNum iGRR.

**Example:**

```VBScript
     Dim objThisIntf As SchArrowDisplay
     Dim objArg1 As SchGRRRoute
     Dim intVar2 As Integer
      ...
     objThisIntf.SetArrowobjArg1,intVar2

```

### Sub **UnsetArrow**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  long  `iSegNum`)

   Remove arrow display attributes on the route.

**Parameters:**

` iGRR`      iGRR means apply only to segments of iGRR. (if iGRR = NULL, apply to segments of all GRR's of the route, and ignore iSegNum)
` iSegNum`      iSegNum = 0 means apply to all segments of iGRR. iSegnum > 0 means apply to only to segment number iSegNum iGRR.

**Example:**

```VBScript
     Dim objThisIntf As SchArrowDisplay
     Dim objArg1 As SchGRRRoute
     Dim intVar2 As Integer
      ...
     objThisIntf.UnsetArrowobjArg1,intVar2

```