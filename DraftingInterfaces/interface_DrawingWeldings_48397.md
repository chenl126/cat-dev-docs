# DrawingWeldings (Collection)

**_A collection of all the drawing weldings currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**(| [CatWeldingSymbol](../DraftingInterfaces/enum_CatWeldingSymbol_54418.md) | `iSymbol`,| | double | `iPositionX`,| | double | `iPositionY`) As [CATIADrawingWelding](../DraftingInterfaces/interface_DrawingWelding_41792.md)

   Creates a drawing welding and adds it to the drawing weldings collection. This drawing welding becomes the active one.

**Parameters:**

` iSymbol`      The drawing welding symbol to assign to the drawing welding
` iPositionX,iPositionY`      The drawing welding x and y coordinates, expressed in millimeters, and expressed with respect to the view coordinate system

**Returns:**      The created drawing welding  **Example:**      The following example creates a drawing welding, retrieved in `MyWelding`, in the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet.

```VBScript
     Dim MyView As DrawingView
     Set MyView = MySheet.Views.ActiveView
     Dim MyWelding As DrawingWelding
     Set MyWelding =
        MyView.Weldings.Add(catSquareWelding, 0., 0.)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingWelding](../DraftingInterfaces/interface_DrawingWelding_41792.md)

   Returns a drawing welding using its index from the drawing weldings collection.

**Parameters:**

` iIndex`      The index of the drawing welding to retrieve from the collection of drawing weldings. As a numerics, this index is the rank of the drawing welding in the collection. The index of the first drawing welding in the collection is 1, and the index of the last drawing welding is Count.

**Returns:**      The retrieved drawing welding  **Example:**      This example retrieves in `ThisDrawingWelding` the second drawing welding, in the drawing welding collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
     Dim MyView  As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     Dim ThisDrawingWelding As DrawingWelding
     Set ThisDrawingWelding = MyView.Weldings.Item(2)

```

### Sub **Remove**( long  `iIndex`)

   Removes a drawing welding from the drawing weldings collection.

**Parameters:**

` iIndex`      The index of the drawing welding to remove from the collection of drawing weldings. As a numerics, this index is the rank of the drawing text in the collection. The index of the first drawing welding in the collection is 1, and the index of the last drawing welding is Count.  **Example:**      The following example removes the third drawing welding from the drawing welding collection of the active view of the active document, supposed to be a drawing document.

```VBScript
     Dim MyView As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     MyView.Drawing.Remove(3)

```