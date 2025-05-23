# Distances (Collection)

**_A collection of all Distance objects currently managed by the application._**

The method `GetTechnologicalObject("Distances")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**(| ) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Creates a Distance object which takes all products of the document into account and adds it to the Distances collection.

**Returns:**      The created Distance  **Example:**      This example creates a new Distance in the `TheDistances` collection.

```VBScript
        Dim NewDistance As Distance
        Set NewDistance = TheDistances.Add

```

### Func **AddFromSel**( ) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Creates a Distance object which takes all products in the selection into account and adds it to the Distances collection.

**Returns:**      The created Distance  **Example:**      This example creates a new Distance in the `TheDistances` collection.

```VBScript
        Dim NewDistance As Distance
        Set NewDistance = TheDistances.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Returns a Distance object using its index or its name from the Distances collection.

**Parameters:**

` iIndex`      The index or the name of the Distance to retrieve from the collection of Distances. As a numerics, this index is the rank of the Distance in the collection. The index of the first Distance in the collection is 1, and the index of the last Distance is Count. As a string, it is the name you assigned to the Distance.

**Example:**      This example retrieves in `ThisDistance` the ninth Distance, and in `ThatDistance` the Distance named `Distance Of MyProduct` from the `TheDistances` collection.

```VBScript
        Dim ThisDistance As Distance
        Set ThisDistance = TheDistances.Item(9)
        Dim ThatDistance As Distance
        Set ThatDistance = TheDistances.Item("Distance Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Distance object from the Distances collection.

**Parameters:**

` iIndex`      The index or the name of the Distance to remove from the collection of Distances. As a numerics, this index is the rank of the Distance in the collection. The index of the first Distance in the collection is 1, and the index of the last Distance is Count. As a string, it is the name you assigned to the Distance.

**Example:**      The following example removes the tenth Distance and the Distance named `Distance Of MyProduct` from the `TheDistances` collection.

```VBScript
        TheDistances.Remove(10)
        TheDistances.Remove("Distance Of MyProduct")

```