# PspStretchableData (Object)

**_Represents the PspStretchableData object._**

**Role** : To access the technological data on stretchable objects.

## Methods

### Func **ListBendData**(| ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the bend radii.

**Returns:**      List of bend radius.  **Example:**

```VBScript
     Dim objThisIntf As PspStretchableData
     Dim objArg1 As PspListOfDoubles
      ...
     Set objArg1 = objThisIntf.ListBendData

```

### Func **ListDefinitionPoints**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRelAxis`) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

   Returns the points defining the object.

**Parameters:**

` iRelAxis`      The relative axis object (Nothing means relative to parent).

**Returns:**      List of points defining object. A list of X-Y-Z coordinates of the points. 3 doubles per point.  **Example:**

```VBScript
     Dim objThisIntf As PspStretchableData
     Dim objArg1 As Product
     Dim objArg2 As PspListOfDoubles
      ...
     Set objArg2 = objThisIntf.ListDefinitionPoints (objArg1)

```