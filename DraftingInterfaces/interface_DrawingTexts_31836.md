# DrawingTexts (Collection)

**_A collection of all the drawing texts currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iDrawingText`,| | double | `iPositionX`,| | double | `iPositionY`) As [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)

   Creates a drawing text and adds it to the DrawingTexts collection.

**Parameters:**

` iDrawingText`      The character string that makes up the drawing text to create
` iPositionX,iPositionY`      The drawing text x and y coordinates, expressed in millimeters, with respect to the drawing view coordinate system

**Returns:**      The created drawing text  **Example:**      The following example creates a drawing text with the string `ComplexText` and retrieved in `MyText` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
     Dim MyView As DrawingView
     Set MyView = MySheet.Views.ActiveView
     Dim MyText As DrawingText
     Set MyText = MyView.Texts.Add("ComplexText", 0., 0.)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)

   Returns a drawing text using its index from the DrawingTexts collection.

**Parameters:**

` iIndex`      The index of the drawing text to retrieve from the collection of drawing texts. As a numerics, this index is the rank of the drawing text in the collection. The index of the first drawing text in the collection is 1, and the index of the last drawing text is Count.

**Returns:**      The retrieved drawing view  **Example:**      This example retrieves in `ThisDrawingText` the second drawing text, in the drawing view collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
     Dim MyView  As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     Dim ThisDrawingText As DrawingText
     Set ThisDrawingText = MyView.Texts.Item(2)

```

### Sub **Remove**( long  `iIndex`)

   Removes a drawing text from the DrawingTexts collection.

**Parameters:**

` iIndex`      The index of the drawing text to remove from the collection of drawing texts. As a numerics, this index is the rank of the drawing text in the collection. The index of the first drawing text in the collection is 1, and the index of the last drawing text is Count.  **Example:**      The following example removes the third drawing text in the drawing text collection of the active view of the active document, supposed to be a drawing document.

```VBScript
     Dim MyView As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     MyView.DrawingTexts.Remove(3)

```