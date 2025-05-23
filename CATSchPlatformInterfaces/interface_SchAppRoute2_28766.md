# SchAppRoute2 (Object)

**_Manage a schematic route._**

## Methods

### Sub **AppPostRouteProcess**(| [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md) | `iCntblConnectedTo`)

   Post process after creating a route instance.

**Parameters:**

` iCntbleConnectedTo`      The connectable that the route is connected to this route It is optional

**Example:**

```VBScript
     Dim objThisIntf As SchAppRoute2
     Dim objArg1 As SchAppConnectable
      ...
     objThisIntf.AppPostRouteProcessobjArg1

```