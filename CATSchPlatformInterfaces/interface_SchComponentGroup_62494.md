# SchComponentGroup (Object)

**_Represents a temporary group of schematic objects for component placement._**

## Methods

### Sub **AddMember**( [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iCntblToAdd`)

Add a member to the component group.

**Parameters:**

` iCntblToAdd`      The application connectable to be added to the group
**Example:**

```VBScript
Dim objThisIntf As SchComponentGroup
Dim objArg1 As SchAppConnectable
 ...
objThisIntf.AddMemberobjArg1

```

### Func **ListMembers**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

List all connectable members in the group.

**Parameters:**

` oLGRR`      A list of connectables.
**Example:**

```VBScript
Dim objThisIntf As SchComponentGroup
Dim objArg1 As SchListOfObjects
 ...
Set objArg1 = objThisIntf.ListMembers

```

### Sub **RemoveMember**( [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iCntblToRemove`)

Remove a member to the component group.

**Parameters:**

` iCntbleToRemove`      The application connectable to be removed from the group
**Example:**

```VBScript
Dim objThisIntf As SchComponentGroup
Dim objArg1 As SchAppConnectable
 ...
objThisIntf.RemoveMemberobjArg1

```