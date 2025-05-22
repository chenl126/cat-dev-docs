# ManufacturingMachinableFeature (Object)

**_Machinable Feature in Manufacturing._**
It is the base object for machinable geometry and machinable area

**See also:**      [ManufacturingMachinableArea](../ManufacturingInterfaces/interface_ManufacturingMachinableArea_149911.md), [ManufacturingMachinableGeometry](../ManufacturingInterfaces/interface_ManufacturingMachinableGeometry_202868.md)

## Properties

### Property **FeatRemark**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the manufacturing machinable feature remark.

**Returns:**      oFeatRemark The manufacturing machinable feature remark  **Example:**     The following example returns in `tFeatRemark` the remark of manufacturing machinable feature `firstMachFeat`:

```VBScript
Dim firstMachFeat As ManufacturingMachinableFeature
Set firstMachFeat = ...
Dim tFeatRemark As CATBSTR
Set tFeatRemark = firstMachFeat.FeatRemark

```

### Property **FeatType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the manufacturing machinable feature type.

**Returns:**      oFeatType The manufacturing machinable feature type  **Example:**     The following example returns in `tFeatType` the type of manufacturing machinable feature `firstMachFeat`:

```VBScript
Dim firstMachFeat As ManufacturingMachinableFeature
Set firstMachFeat = ...
Dim tFeatType As CATBSTR
Set tFeatType = firstMachFeat.FeatType

```