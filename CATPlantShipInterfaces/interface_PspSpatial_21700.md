# PspSpatial (Object)

**_Represents the Psp Spatial object._**
**Role** : To access Plant Ship spatial object information.

## Properties

### Property **Physicals**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

Returns all physical objects associated to this spatial object.

**Example:**

```VBScript
Dim objThisIntf As PspSpatial
Dim objArg1 As CATIAPspListOfObjects
 ...
Set objArg1 = objThisIntf.Physicals

```