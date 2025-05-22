# ManufacturingFeatures (Collection)

**_Collection of Manufacturing Features._**

**See also:**      [ManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

Create and Add a Manufacturing Feature of a specified type to the Collection.

**Example:**     The following example creates and adds in `Features` the manufacturing feature `Feature` of type : `type`

```VBScript
Set Feature = Features.Add(Type)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingFeature](../ManufacturingInterfaces/interface_ManufacturingFeature_85800.md)

Retrieve the Manufacturing Feature of a the specified index from the Collection.

**Example:**     The following example retrieves from `Feature` the manufacturing feature `Feature` from index : `Index`

```VBScript
Set Feature = Features.Item(Index)

```