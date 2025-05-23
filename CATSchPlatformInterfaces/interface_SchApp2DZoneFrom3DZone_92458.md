# SchApp2DZoneFrom3DZone (Object)

**_Manage a 2D zone that is dropped off from 3D counterpart._**

## Methods

### Func **Create2DAppZone**(| ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Create an Application Zone.

**Parameters:**

` i3DZone`      The Bounded Zone (3D) object
` oAppZone`      The new Application zone object created (CATISchAppZone interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchApp2DZoneFrom3DZone
     Dim objArg1 As AnyObject
      ...
     Set objArg1 = objThisIntf.Create2DAppZone

```