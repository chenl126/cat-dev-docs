# AnnotatedViews (Collection)

**_A collection of AnnotatedView objects._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("AnnotatedViews")` on the root product retrieves this collection.

## Methods

### Func **Add**(| ) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Creates an annotated view using the current viewpoint and adds it to the AnnotatedView collection.

**Returns:**      The created AnnotatedView  **Example:**      This example creates a new AnnotatedView in the `TheAnnotatedViews` collection.

```VBScript
        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add

```

### Func **AddFromViewpoint**( [CATIAViewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md)  `iViewpoint`) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Creates an annotated view using a given viewpoint and adds it to the AnnotatedView collection.

**Parameters:**

` iViewpoint`      The viewpoint.

**Returns:**      The created AnnotatedView  **Example:**      This example creates a new AnnotatedView in the `TheAnnotatedViews` collection using a `AViewpoint` viewpoint object.

```VBScript
        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.AddFromViewpoint(AViewpoint)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Returns an annotated view using its index or its name from the AnnotatedViews collection.

**Parameters:**

` iIndex`      The index or the name of the AnnotatedView to retrieve from the collection of AnnotatedViews. As a numerics, this index is the rank of the AnnotatedView in the collection. The index of the first AnnotatedView in the collection is 1, and the index of the last AnnotatedView is Count. As a string, it is the name you assigned to the AnnotatedView.

**Returns:**      The retrieved AnnotatedView  **Example:**      This example retrieves in `ThisAnnotatedView` the ninth AnnotatedView, and in `ThatAnnotatedView` the AnnotatedView named `AnnotatedView3` from the `TheAnnotatedViews` collection.

```VBScript
        Dim ThisAnnotatedView As AnnotatedView
        Set ThisAnnotatedView = TheAnnotatedViews.Item(9)
        Dim ThatAnnotatedView As AnnotatedView
        Set ThatAnnotatedView = TheAnnotatedViews.Item("AnnotatedView3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an annotated view from the AnnotatedViews collection.

**Parameters:**

` iIndex`      The index or the name of the AnnotatedView to retrieve from he collection of AnnotatedViews. As a numerics, this index is the rank of the AnnotatedView in the collection. The index of the first AnnotatedView in the collection is 1, and the index of the last AnnotatedView is Count. As a string, it is the name you assigned to the AnnotatedView.

**Example:**      The following example removes the tenth AnnotatedView and the AnnotatedView named `AnnotatedView2` from the `TheAnnotatedViews` collection.

```VBScript
        TheAnnotatedViews.Remove(10)
        TheAnnotatedViews.Remove("AnnotatedView2")

```