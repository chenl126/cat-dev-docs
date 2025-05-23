# ProductScenes (Collection)

**_A collection of ProductScenes contained in a given ProductDocument._**

## Methods

### Func **AddProductSceneFull**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iReferenceProducts`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Creates a new FULL scene from a set of products and adds it to the ProductScenes collection.

**Parameters:**

` iName`      The name of the new scene
` iReferenceProducts`      Products used as root nodes of the new scene

**Returns:**      The created new full scene  **Example:**      This example creates the `SpareWheel` new scene from the reference product `FrontRightWheel` and adds the scene to the `ToolKits` collection.

```VBScript
        Dim SpareWheel As ProductScene
        Set SpareWheel = ToolKits.AddProductSceneFull("SpareWheel", FrontRightWheel)

```

### Func **AddProductScenePartial**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferenceProducts`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Creates a new DELTA scene from a set of products and adds it to the ProductScenes collection.

**Parameters:**

` iName`      The name of the new scene
` iReferenceProducts`      Products used as root nodes of the new scene

**Returns:**      The created new delta scene  **Example:**      This example creates the `SpareWheel` new scene from the reference product `FrontRightWheel` and adds the scene to the `ToolKits` collection.

```VBScript
        Dim SpareWheel As ProductScene
        Set SpareWheel = ToolKits.AddProductScenePartial("SpareWheel", FrontRightWheel)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Returns a scene using its index or its name from the ProductScenes collection.

**Parameters:**

` iIndex`      The index or the name of the ProductScene to retrieve from the collection of ProductScenes. As a numerics, this index is the rank of the ProductScene in the collection. The index of the first ProductScene in the collection is 1, and the index of the last ProductScene is Count. As a string, it is the name you assigned to the ProductScene.

**Returns:**      The retrieved ProductScene.  **Example:**      This example retrieves in `ThisProductScene` the ninth ProductScene, and in `ThatProductScene` the ProductScene named `ProductScene3` from the `TheProductScenes` collection.

```VBScript
        Dim ThisProductScene As ProductScene
        Set ThisProductScene = TheProductScenes.Item(9)
        Dim ThatProductScene As ProductScene
        Set ThatProductScene = TheProductScenes.Item("ProductScene3")

```

### Sub **Remove**( [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)  `iProductScene`)

   Removes a product-scene from the ProductScenes collection.

**Parameters:**

` iScene`      The scene to remove.

**Example:**      This example removes the `Engine` product-scene from the `ToolKits` collection.

```VBScript
        ToolKits.Remove Engine

```