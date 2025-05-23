# SchAppGapPriority (Object)

**_Manage the graphical representation of a route._**

## Methods

### Sub **AppChooseGapPriority**(| [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md) | `iTheOtherRoute`,| | [CatSchIDLGapPriority](../CATSchPlatformInterfaces/enum_CatSchIDLGapPriority_81298.md) | `oPriority`)

   Identify which of 2 intersecting routes should be gapped.

**Parameters:**

` iTheOtherRoute`      The route intersecting This route.
` oPriority`      Gap Priority.

**Example:**

```VBScript
     Dim objThisIntf As SchAppGapPriority
     Dim objArg1 As SchRoute

      ...
     objThisIntf.AppChooseGapPriorityobjArg1,CatSchIDLGapPriority_Enum

```