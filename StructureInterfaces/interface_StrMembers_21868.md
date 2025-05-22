# StrMembers (Collection)

**_A collection of the Member objects contained in a given Product object of a ProductDocument object._**
A Product object aggregates zero or one Members collection. This collection is retrieved using the [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) method of the product.

**Example:**      The following example retrieves the member collection from the `oProduct` Product.

```VBScript
Dim oMembers as AnyObject
Set oMembers = oProduct.GetTechnologicalObject("StructureMembers")

```

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAStrMember](../StructureInterfaces/interface_StrMember_17505.md)

Returns a member from its index in the Members collection.

**Parameters:**

` iIndex`      The index of the member to retrieve in the collection of members. This index can either be the rank of the member in the collection or the name you assign to the member. As a numerics, this index is the rank of the member in the collection. The index of the first member in the collection is 1, and the index of the last member is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved member  **Example:**      The following example returns in `ThisMember` the third member, and in `ThatMember` the member named `Column_1` in the `Assembly_1` member collection.

```VBScript
Dim ThisMember As Member
Set ThisMember = Assembly_1.Item(3)
Dim ThatMember As Member
Set ThatMember = Assembly.Item("Column_1")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a member from the Members collection.

**Parameters:**

` iIndex`      The index of the member to remove. This index can either be the rank of the member in the collection or the name you assigned to the member. As a numerics, this index is the rank of the member in the collection. The index of the first member in the collection is 1, and the index of the last member is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the sixth member and the member named `Column_1` from the `Assembly_1` member collection.

```VBScript
Assembly_1.Remove(6)
Assembly_1.Remove("Column_1")

```