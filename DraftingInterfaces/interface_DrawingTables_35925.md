# DrawingTables (Collection)

**_A collection of all the drawing tables currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**( double  `iPositionX`,  double  `iPositionY`,  long  `iNumberOfRow`,  long  `iNumberOfColumn`,  double  `iRowHeight`,  double  `iColumnWidth`) As [CATIADrawingTable](../DraftingInterfaces/interface_DrawingTable_30236.md)

Creates a drawing table and adds it to the DrawingTables collection.

**Parameters:**

` iPositionX,iPositionY`      The drawing table x and y coordinates, expressed in millimeters, with respect to the drawing view coordinate system
` iNumberOfRow,iNumberOfColumn`      The drawing table number of rows and columns
` iRowHeight,iColumnWidth`      The row height and the column width
**Returns:**      The created drawing table  **Example:**      The following example creates an empty drawing table and retrieves it in `MyTable` in the drawing table collection of the active view `MyView` of the drawing sheet `MySheet`.

```VBScript
Dim MyView As DrawingView
Set MyView = MySheet.Views.ActiveView
Dim MyTable As DrawingTable
Set MyTable = MyView.Tables.Add(100., 100., 2, 2, 20., 50.)

```

### Func **Item**( long  `iIndex`) As [CATIADrawingTable](../DraftingInterfaces/interface_DrawingTable_30236.md)

Returns a drawing table using its index from the DrawingTables collection.

**Parameters:**

` iIndex`      The index of the drawing table to retrieve from the collection of drawing tables. As a numerics, this index is the rank of the drawing table in the collection. The index of the first drawing table in the collection is 1, and the index of the last drawing table is Count.
**Returns:**      The retrieved drawing table  **Example:**      This example retrieves in `ThisDrawingTable` the second drawing table, in the drawing view collection of the active view in the active sheet, in the active document supposed to be a drawing document.

```VBScript
Dim MyView  As DrawingView
Set MyView  = MySheet.Views.ActiveView
Dim ThisDrawingTable As DrawingTable
Set ThisDrawingTable = MyView.Tables.Item(2)

```

### Sub **Remove**( long  `iIndex`)

Removes a drawing table from the DrawingTables collection.

**Parameters:**

` iIndex`      The index of the drawing table to remove from the collection of drawing tables. As a numerics, this index is the rank of the drawing table in the collection. The index of the first drawing table in the collection is 1, and the index of the last drawing table is Count.  **Example:**      The following example removes the third drawing table in the drawing table collection of the active view of the active document, supposed to be a drawing document.

```VBScript
Dim MyView As DrawingView
Set MyView  = MySheet.Views.ActiveView
MyView.DrawingTables.Remove(3)

```