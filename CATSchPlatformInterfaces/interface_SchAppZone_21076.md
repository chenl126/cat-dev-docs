# SchAppZone (Object)

**_Manage a schematic zone._**

## Methods

### Sub **AppAddZoneMember**(| [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md) | `iAppCntblToAdd`)

   Add an application connectable object to the zone as member.

**Parameters:**

` iAppCntblToAdd`      The application connectable object to be added to the zone.

**Example:**

```VBScript
     Dim objThisIntf As SchAppZone
     Dim objArg1 As SchAppConnectable
      ...
     objThisIntf.AppAddZoneMemberobjArg1

```

### Func **AppListZoneMembers**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all members of an application zone.

**Parameters:**

` oLAppCntbl`      A list of zone members (application connectables).

**Example:**

```VBScript
     Dim objThisIntf As SchAppZone
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.AppListZoneMembers

```

### Sub **AppRemoveZoneMember**( [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iAppCntblToRemove`)

   Remove an application connectable object to the zone as member.

**Parameters:**

` iAppCntblToRemove`      The application connectable object to be removed to the zone.

**Example:**

```VBScript
     Dim objThisIntf As SchAppZone
     Dim objArg1 As SchAppConnectable
      ...
     objThisIntf.AppRemoveZoneMemberobjArg1

```