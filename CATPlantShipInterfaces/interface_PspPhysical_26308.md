# PspPhysical (Object)

**_Represents the object to access Plant Ship physical object information._**

**Role** : To access access Plant Ship physical object information.

## Methods

### Func **GetFunctional**(| ) As [CATIAPspFunctional](../CATPlantShipInterfaces/interface_PspFunctional_36800.md)

   Returns the Function object.

**Returns:**      Functional object associated with the physical object  **Example:**

```VBScript
     Dim objThisIntf As PspPhysical
     Dim objArg1 As PspFunctional
      ...
     Set objArg1 = objThisIntf.GetFunctional

```

### Func **GetSpatial**( ) As [CATIAPspSpatial](../CATPlantShipInterfaces/interface_PspSpatial_21700.md)

   Returns the Spatial object.

**Returns:**      Spatial object associated with the physical object  **Example:**

```VBScript
     Dim objThisIntf As PspPhysical
     Dim objArg1 As PspSpatial
      ...
     Set objArg1 = objThisIntf.GetSpatial

```