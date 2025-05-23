# Groups (Collection)

**_A collection of all groups currently managed by the application._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("Groups")` on the root product retrieves this collection.

## Methods

### Func **Add**(| ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Creates an empty Group and adds it to the Groups Collection.

**Returns:**      The created group  **Example:**      This example creates a new group in the `TheGroups` collection.

```VBScript
        Dim NewGroup As Group
        Set NewGroup = TheGroups.Add

```

### Func **AddFromSel**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Creates a Group containing all products in the selection and adds it to the Groups Collection.

**Returns:**      The created group  **Example:**      This example creates a new group containing all products in the selection in the `TheGroups` collection.

```VBScript
        Dim NewGroup As Group
        Set NewGroup = TheGroups.AddFromSel

```

### Func **AllLeaves**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns a group which contains all the terminal nodes of the current root product.

**Example:**      This example retrieves the group in the `TheGroups` collection.

```VBScript
        Dim AllLeavesGroup As Group
        Set AllLeavesGroup = TheGroups.AllLeaves

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns a group using its index or its name from the Groups collection.

**Parameters:**

` iIndex`      The index or the name of the Group to retrieve from the collection of groups. As a numerics, this index is the rank of the Group in the collection. The index of the first Group in the collection is 1, and the index of the last Group is Count. As a string, it is the name you assigned to the Group.

**Returns:**      The retrieved Group  **Example:**      This example retrieves in `ThisGroup` the ninth Group, and in `ThatGroup` the Group named `Group3` from the `TheGroups` collection.

```VBScript
        Dim ThisGroup As Group
        Set ThisGroup = TheGroups.Item(9)
        Dim ThatGroup As Group
        Set ThatGroup = TheGroups.Item("Group3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a group from the Groups collection.

**Parameters:**

` iIndex`      The index or the name of the Group to retrieve from he collection of groups. As a numerics, this index is the rank of the Group in the collection. The index of the first Group in the collection is 1, and the index of the last Group is Count. As a string, it is the name you assigned to the Group.

**Example:**      The following example removes the tenth Group and the Group named `Group2` from the `TheGroups` collection.

```VBScript
        TheGroups.Remove(10)
        TheGroups.Remove("Group2")

```