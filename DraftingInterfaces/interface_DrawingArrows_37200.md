# DrawingArrows (Collection)

**_A collection of all the drawing arrows currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**( double  `iHeadPointX`,  double  `iHeadPointY`,  double  `iTailPointX`,  double  `iTailPointY`) As [CATIADrawingArrow](../DraftingInterfaces/interface_DrawingArrow_31476.md)

Creates a drawing arrow and adds it to the DrawingArrows collection.

**Parameters:**

` iHeadPointX,iHeadPointY`      The x and y coordinates of head side of drawing arrow
` iTailPointX,iTailPointY`      The x and y coordinates of tail side of drawing arrow
**Returns:**      The created drawing arrow  **Example:**      The following example creates a drawing arrow and retrieved in `MyArrow` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
Dim MyView As DrawingView
Set MyView = MySheet.Views.ActiveView
Dim MyArrow As DrawingArrow
Set MyArrow = MyView.Arrows.Add(0., 0., 20., 50)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingArrow](../DraftingInterfaces/interface_DrawingArrow_31476.md)

Returns a drawing arrow using its index from the DrawingArrows collection.

**Parameters:**

` iIndex`      The index of the drawing arrow to retrieve from the collection of drawing arows. As a numerics, this index is the rank of the drawing arrow in the collection. The index of the first drawing arrow in the collection is 1, and the index of the last drawing arrow is Count.
**Returns:**      The retrieved drawing view  **Example:**      This example retrieves in `ThisDrawingArrow` the second drawing arrow, in the drawing view collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
Dim MyView  As DrawingView
Set MyView  = MySheet.Views.ActiveView
Dim ThisDrawingArrow As DrawingArrow
Set ThisDrawingArrow = MyView.Arrows.Item(2)

```

### Sub **Remove**( long  `iIndex`)

Removes a drawing arrow from the DrawingArrows collection.

**Parameters:**

` iIndex`      The index of the drawing arrow to remove from the collection of drawing arrows. As a numerics, this index is the rank of the drawing arrow in the collection. The index of the first drawing arrow in the collection is 1, and the index of the last drawing arrow is Count.  **Example:**      The following example removes the third drawing arrow in the drawing arrow collection of the active view of the active document, supposed to be a drawing document.

```VBScript
Dim MyView As DrawingView
Set MyView  = MySheet.Views.ActiveView
MyView.DrawingArrows.Remove(3)

```