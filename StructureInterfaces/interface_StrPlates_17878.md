# StrPlates (Collection)

**_A collection of the Plate objects contained in a given Product object of a ProductDocument object._**
A Product object can aggregate one or zero Plates collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the plate collection from the `oProduct` Product.

```VBScript
     Dim oPlates as AnyObject
     Set oPlates = oProduct.GetTechnologicalObject("StructurePlates")

```

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIAStrPlate](../StructureInterfaces/interface_StrPlate_13958.md)

   Returns a plate from its index in the Plates collection.

**Parameters:**

` iIndex`      The index of the plate to retrieve in the collection of plates. This index can either be the rank of the plate in the collection or the name you assign to the plate. As a numerics, this index is the rank of the plate in the collection. The index of the first plate in the collection is 1, and the index of the last plate is Count. As a string, it is the name you assigned to the plate using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved plate

**Example:**      The following example returns in `ThisPlate` the third plate, and in `ThatPlate` the plate named `EndPlate_1` in the `Assembly_1` plate collection.

```VBScript
     Dim ThisPlate As Plate
     Set ThisPlate = Assembly_1.Item(3)
     Dim ThatPlate As Plate
     Set ThatPlate = Assembly.Item("EndPlate_1")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a plate from the Plates collection.

**Parameters:**

` iIndex`      The index of the plate to remove. This index can either be the rank of the plate in the collection or the name you assigned to the plate. As a numerics, this index is the rank of the plate in the collection. The index of the first plate in the collection is 1, and the index of the last plate is Count. As a string, it is the name you assigned to the plate using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property

**Example:**      The following example removes the sixth plate and the plate named `EndPlate_1` from the `Assembly_1` plate collection.

```VBScript
     Assembly_1.Remove(6)
     Assembly_1.Remove("EndPlate_1")

```