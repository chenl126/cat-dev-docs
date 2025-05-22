# Materials (Collection)

**_A collection of all the Material objects._**
This collection is currently managed by a [MaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md) object.

## Methods

### Func **Add**( ) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

Adds a new material to the material collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

Returns a material from its index in the Material collection.

**Parameters:**

` iIndex`      The index of the material to retrieve in the collection of materials. Compared with other collections, you cannot use the name of the material as argument.
**Returns:**      The retrieved material  **Example:**      The following example returns in `MyMaterial` the sixth material in a material collection.

```VBScript
Dim MyMaterial As Material
Set MyMaterial = Materials.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a material from the materials collection.  
### Func **SortedItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  short  `iMode`) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

Returns a material from its index in the sorted Material collection.

**Parameters:**

` iIndex`      The index of the material to retrieve in the sorted collection of materials. Compared with other collections, you cannot use the name of the material as argument.
` iMode`      The sorted mode of material collection

Possible mode values are:
  * 0: Alphabetical order
  * 1: Inverse alphabetical order

**Returns:**      The retrieved material