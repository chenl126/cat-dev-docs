# PspGroupable (Object)

**_Represent the Groupable object that can be grouped by Group object._**

**Role** : It is used to query the group object link to this object.

## Properties

### Property **Groups**(| ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

   Returns a list of Groups to which this object is a member.

**Example:**

```VBScript
     Dim objThisIntf As PspGroupable
     Dim objArg1 As PspListOfObjects

      ...
     Set ObjArg1 = objThisIntf.Groups

```