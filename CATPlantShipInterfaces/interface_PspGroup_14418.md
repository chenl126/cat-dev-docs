# PspGroup (Object)

**_Represent the Group._**

**Role** : It manages group members in making logical relationship.

## Properties

### Property **Members**(| ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Members of the Group.

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspListOfObjects

      ...
     Set ObjArg1 = objThisIntf.Members

```

Methods

### Sub **AddMember**( [CATIAPspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md)  `iGroupable`)

   Adds a member to the group.

**Parameters:**

` iGroupable`      Member to add

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspGroupable

      ...
      objThisIntf.AddMember objArg1

```

### Sub **RemoveMember**( [CATIAPspGroupable](../CATPlantShipInterfaces/interface_PspGroupable_31100.md)  `iGroupable`)

   Removes a member from the group.

**Parameters:**

` iGroupable`      a member to be removed

**Example:**

```VBScript
     Dim objThisIntf As PspGroup
     Dim objArg1 As PspGroupable

      ...
      objThisIntf.RemoveMember objArg1

```