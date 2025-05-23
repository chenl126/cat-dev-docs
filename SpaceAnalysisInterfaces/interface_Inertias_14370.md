# Inertias (Collection)

**_A collection of all inertia objects currently managed by the application._**

WARNING: this collection will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Inertia")` on the product to analyze, to retrieve an `Inertia` object.

## Methods

### Func **Add**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iObject`) As [CATIAInertia](../SpaceAnalysisInterfaces/interface_Inertia_10894.md)

   Creates an Inertia object from an object and adds it to the Inertias collection.

**Parameters:**

` iObject`      The Object

**Returns:**      The created Inertia  **Example:**      This example creates a new Inertia from a product `TheProduct` in the `TheInertias` collection.

```VBScript
        Dim NewInertia As Inertia
        Set NewInertia = TheInertias.Add(TheProduct)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAInertia](../SpaceAnalysisInterfaces/interface_Inertia_10894.md)

   Returns an Inertia object using its index or its name from the Inertias collection.

**Parameters:**

` iIndex`      The index or the name of the Inertia to retrieve from the collection of inertias. As a numerics, this index is the rank of the Inertia in the collection. The index of the first Inertia in the collection is 1, and the index of the last Inertia is Count. As a string, it is the name you assigned to the Inertia.

**Example:**      This example retrieves in `ThisInertia` the ninth Inertia, and in `ThatInertia` the Inertia named `Inertia Of MyProduct` from the `TheInertias` collection.

```VBScript
        Dim ThisInertia As Inertia
        Set ThisInertia = TheInertias.Item(9)
        Dim ThatInertia As Inertia
        Set ThatInertia = TheInertias.Item("Inertia Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an Inertia object from the Inertias collection.

**Parameters:**

` iIndex`      The index or the name of the Inertia to remove from the collection of inertias. As a numerics, this index is the rank of the Inertia in the collection. The index of the first Inertia in the collection is 1, and the index of the last Inertia is Count. As a string, it is the name you assigned to the Inertia.

**Example:**      The following example removes the tenth Inertia and the Inertia named `Inertia Of MyProduct` from the `TheInertias` collection.

```VBScript
        TheInertias.Remove(10)
        TheInertias.Remove("Inertia Of MyProduct")

```