# MaterialFamilies (Collection)

**_A collection of all the MaterialFamily objects._**
This collection is currently managed by a CATIAMaterialDocument object.

## Methods

### Func **Add**( ) As [CATIAMaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md)

Adds a new material family to the MaterialFamilies collection.  **Example:**      The following adds a material family to the collection attached to a document. This document must be a [MaterialDocument](../CATMatInterfaces/interface_MaterialDocument_54972.md) object.

```VBScript
FileToOpen = "e:\users\ast\materials\Catalog.CATMaterial"
Dim MyDocument As MaterialDocument
Set MyDocument = Documents.Open(FileToOpen)
Dim MyMaterialFamily As MaterialFamily
Set MyMaterialFamily = MyDocument.MaterialFamilies.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md)

Returns a material family from its index in the MaterialFamilies collection.

**Parameters:**

` iIndex`      The index of the material family to retrieve in the collection of material families. Compared with other collections, you cannot use the name of the material family as argument.
**Returns:**      The retrieved material family  **Example:**      The following example returns in `MyMaterialFamily` the sixth material family in the collection.

```VBScript
Dim MyMaterialFamily As MaterialFamily
Set MyMaterialFamily = MaterialFamilies.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a material family from the MaterialFamilies collection.

**Parameters:**

` iIndex`      The index of the material family to remove. Compared with other collections, you cannot use the name of the material family as argument.  **Example:**      The following example removes the second material family in the collection attached to the active document. This document must be a
[MaterialDocument](../CATMatInterfaces/interface_MaterialDocument_54972.md) object.

```VBScript
FileToOpen = "e:\users\ast\materials\Catalog.CATMaterial"
Dim MyDocument As MaterialDocument
Set MyDocument = Documents.Open(FileToOpen)
MyDocument.MaterialFamilies.Remove(2)

```