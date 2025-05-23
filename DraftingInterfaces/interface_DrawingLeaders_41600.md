# DrawingLeaders (Collection)

**_A collection of all the drawing leaders currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**(| double | `iHeadPointX`,| | double | `iHeadPointY`) As [CATIADrawingLeader](../DraftingInterfaces/interface_DrawingLeader_35465.md)

   Creates a drawing leader and adds it to the DrawingLeaders collection.

**Parameters:**

` iHeadPointX,iHeadPointY`      The x and y coordinates of head side of drawing leader

**Returns:**      The created drawing leader  **Example:**      The following example creates a drawing leader and retrieved in `MyLeader` in the drawing text collection of the `MyText` drawing text. This text belongs to the drawing text collection of the drawing view

```VBScript
     Dim MyTexts As DrawingTexts
     Set MyTexts = MySheet.Views.ActiveView
     Dim MyText As DrawingText
     Set MyText = MyTexts.Item(1)
     Dim MyLeader As DrawingLeader
     Set MyLeader = MyText.Leaders.Add(20., 50)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingLeader](../DraftingInterfaces/interface_DrawingLeader_35465.md)

   Returns a drawing leader using its index from the DrawingLeaders collection.

**Parameters:**

` iIndex`      The index of the drawing leader to retrieve from the collection of drawing arows. As a numerics, this index is the rank of the drawing leader in the collection. The index of the first drawing leader in the collection is 1, and the index of the last drawing leader is Count.

**Returns:**      The retrieved drawing view  **Example:**      This example retrieves in `ThisDrawingLeader` the second drawing leader, in the drawing view collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
     Dim MyView  As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     Dim ThisDrawingLeader As DrawingLeader
     Set ThisDrawingLeader = MyView.Leaders.Item(2)

```

### Sub **Remove**( long  `iIndex`)

   Removes a drawing leader from the DrawingLeaders collection.

**Parameters:**

` iIndex`      The index of the drawing leader to remove from the collection of drawing leaders. As a numerics, this index is the rank of the drawing leader in the collection. The index of the first drawing leader in the collection is 1, and the index of the last drawing leader is Count.  **Example:**      The following example removes the third drawing leader in the drawing leader collection of the active view of the active document, supposed to be a drawing document.

```VBScript
     Dim MyView As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     MyView.DrawingLeaders.Remove(3)

```