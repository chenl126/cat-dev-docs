# Clashes (Collection)

**_A collection of all Clash objects currently managed by the application._**

The method `GetTechnologicalObject("Clashes")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**( ) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

Creates a Clash object which takes all products into account and adds it to the Clashes collection.

**Returns:**      The created Clash  **Example:**      This example creates a new Clash in the `TheClashes` collection.

```VBScript
   Dim NewClash As Clash
   Set NewClash = TheClashes.Add

```

### Func **AddFromSel**( ) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

Creates a Clash object which takes all products in the selection into account and adds it to the Clashes collection.

**Returns:**      The created Clash  **Example:**      This example creates a new Clash in the `TheClashes` collection.

```VBScript
   Dim NewClash As Clash
   Set NewClash = TheClashes.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

Returns a Clash object using its index or its name from the Clashes collection.

**Parameters:**

` iIndex`      The index or the name of the Clash to retrieve from the collection of Clashes. As a numerics, this index is the rank of the Clash in the collection. The index of the first Clash in the collection is 1, and the index of the last Clash is Count. As a string, it is the name you assigned to the Clash.
**Example:**      This example retrieves in `ThisClash` the ninth Clash, and in `ThatClash` the Clash named `Clash Of MyProduct` from the `TheClashes` collection.

```VBScript
   Dim ThisClash As Clash
   Set ThisClash = TheClashes.Item(9)
   Dim ThatClash As Clash
   Set ThatClash = TheClashes.Item("Clash Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a Clash object from the Clashes collection.

**Parameters:**

` iIndex`      The index or the name of the Clash to remove from the collection of Clashes. As a numerics, this index is the rank of the Clash in the collection. The index of the first Clash in the collection is 1, and the index of the last Clash is Count. As a string, it is the name you assigned to the Clash.
**Example:**      The following example removes the tenth Clash and the Clash named `Clash Of MyProduct` from the `TheClashes` collection.

```VBScript
   TheClashes.Remove(10)
   TheClashes.Remove("Clash Of MyProduct")

```