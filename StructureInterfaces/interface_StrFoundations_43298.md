# StrFoundations (Collection)

**_A collection of the Foundation objects contained in a given Product object of a ProductDocument object._**
A Product object aggregates zero or one Foundations collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the Foundation collection from the `oProduct` Product.

```VBScript
Dim oFoundations as AnyObject
Set oFoundations = oProduct.GetTechnologicalObject("StructureFoundations")

```

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrFoundation](../StructureInterfaces/interface_StrFoundation_37108.md)

Returns a Foundation from its index in the Foundations collection.

**Parameters:**

` iIndex`      The index of the Foundation to retrieve in the collection of Foundations. This index can either be the rank of the Foundation in the collection or the name you assign to the Foundation. As a numerics, this index is the rank of the Foundation in the collection. The index of the first Foundation in the collection is 1, and the index of the last Foundation is Count. As a string, it is the name you assigned to the Foundation using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved Foundation  **Example:**      The following example returns in `ThisFoundation` the third Foundation, and in `ThatFoundation` the Foundation named `Column_1` in the `Assembly_1` Foundation collection.

```VBScript
Dim ThisFoundation As Foundation
Set ThisFoundation = Assembly_1.Item(3)
Dim ThatFoundation As Foundation
Set ThatFoundation = Assembly.Item("Column_1")

```