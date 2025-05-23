# SchAppGroup (Object)

**_Manage application group._**

## Methods

### Sub **ListZones**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iClassType`,| | [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `oLZones`)

   List application zone objects.

**Parameters:**

` iClassType`      Class type filter. If null, no filtering will be applied.
` oLZones`      (members are CATISchAppZone interfaces pointers) A list of zones

**Example:**

```VBScript
     Dim objThisIntf As SchAppGroup
     Dim strVar1 As String
     Dim objArg2 As SchListOfObjects
      ...
     objThisIntf.ListZonesstrVar1,objArg2

```