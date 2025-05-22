# DrawingThreads (Collection)

**_A collection of all the drawing threads currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iGeomElem`) As [CATIADrawingThread](../DraftingInterfaces/interface_DrawingThread_35692.md)

Creates a drawing thread and adds it to the DrawingThreads collection.

**Parameters:**

` iGeomElem`      Geometry to create the thread on. Be careful, this geometry must be a 2D geometry
**Returns:**      The created drawing thread  **Example:**      The following example creates a drawing thread and retrieved in `MyThread` in the drawing view collection of the `MyView` drawing view. This view belongs to the drawing view collection of the drawing sheet

```VBScript
Dim MyView As DrawingView
Set MyView = MySheet.Views.ActiveView
Dim MyThread As DrawingThread
Set MyThread = MyView.Threads.Add(iGeomElem)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingThread](../DraftingInterfaces/interface_DrawingThread_35692.md)

Returns a drawing thread using its index from the DrawingThreads collection.

**Parameters:**

` iIndex`      The index of the drawing thread to retrieve from the collection of drawing threads. As a numerics, this index is the rank of the drawing thread in the collection. The index of the first drawing thread in the collection is 1, and the index of the last drawing thread is Count.
**Returns:**      The retrieved drawing thread  **Example:**      This example retrieves in `ThisDrawingThread` the second drawing thread, in the drawing view collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
Dim MyView  As DrawingView
Set MyView  = MySheet.Views.ActiveView
Dim ThisDrawingThread As DrawingThread
Set ThisDrawingThread = MyView.Threads.Item(2)

```

### Sub **Remove**( long  `iIndex`)

Removes a drawing thread from the DrawingThreads collection.

**Parameters:**

` iIndex`      The index of the drawing thread to remove from the collection of drawing threads. As a numerics, this index is the rank of the drawing thread in the collection. The index of the first drawing thread in the collection is 1, and the index of the last drawing thread is Count.  **Example:**      The following example removes the third drawing thread in the drawing thread collection of the active view of the active document, supposed to be a drawing document.

```VBScript
Dim MyView As DrawingView
Set MyView  = MySheet.Views.ActiveView
MyView.DrawingThreads.Remove(3)

```