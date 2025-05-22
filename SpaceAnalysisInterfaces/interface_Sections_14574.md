# Sections (Collection)

**_A collection of all Section objects currently managed by the application._**

The method `GetTechnologicalObject("Sections")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**( ) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

Creates a Section object which takes all products of the documents into account and adds it to the Sections collection.

**Returns:**      The created Section  **Example:**      This example creates a new Section in the `TheSections` collection.

```VBScript
   Dim NewSection As Section
   Set NewSection = TheSections.Add

```

### Func **AddFromSel**( ) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

Creates a Section object which takes all products in the selection into account and adds it to the Sections collection.

**Returns:**      The created Section  **Example:**      This example creates a new Section in the `TheSections` collection.

```VBScript
   Dim NewSection As Section
   Set NewSection = TheSections.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

Returns a Section object using its index or its name from the Sections collection.

**Parameters:**

` iIndex`      The index or the name of the Section to retrieve from the collection of Sections. As a numerics, this index is the rank of the Section in the collection. The index of the first Section in the collection is 1, and the index of the last Section is Count. As a string, it is the name you assigned to the Section.
**Example:**      This example retrieves in `ThisSection` the ninth Section, and in `ThatSection` the Section named `Section Of MyProduct` from the `TheSections` collection.

```VBScript
   Dim ThisSection As Section
   Set ThisSection = TheSections.Item(9)
   Dim ThatSection As Section
   Set ThatSection = TheSections.Item("Section Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a Section object from the Sections collection.

**Parameters:**

` iIndex`      The index or the name of the Section to remove from the collection of Sections. As a numerics, this index is the rank of the Section in the collection. The index of the first Section in the collection is 1, and the index of the last Section is Count. As a string, it is the name you assigned to the Section.
**Example:**      The following example removes the tenth Section and the Section named `Section Of MyProduct` from the `TheSections` collection.

```VBScript
   TheSections.Remove(10)
   TheSections.Remove("Section Of MyProduct")

```