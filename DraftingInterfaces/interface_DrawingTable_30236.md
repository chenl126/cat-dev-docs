# DrawingTable (Object)

**_Represents a drawing table in a drawing view._**

## Properties

### Property **AnchorPoint**( ) As [CatTablePosition](../DraftingInterfaces/enum_CatTablePosition_54616.md)

Returns or sets the anchor point of a drawing table.

**Parameters:**

` iMode`      The invert mode to apply

**Example:**      This example sets the anchor point of the drawing table `MyTable` to bottom left.

```VBScript
MyTable.AnchorPoint = CatTableBottomLeft

```

### Property **Angle**( ) As double

Returns or sets the angle orientation of a drawing table.

**Example:**      This example sets the orientation of the table `MyTable` to vertical.

```VBScript
PI = 3.1415926535
X = MyTable.Angle = PI/2

```

### Property **ComputeMode**( ) As [CatTableComputeMode](../DraftingInterfaces/enum_CatTableComputeMode_74582.md)

Returns or sets the compute mode of a drawing table. If the compute mode is set to OFF, no display of the modifications applied to a table will be computed. This allows to save much time when executing a macro. To displayed the table, set the compute mode back to ON.

**Example:**      This example sets the compute mode of the drawing table `MyTable` to OFF.

```VBScript
MyTable.ComputeMode = CatTableOFF

```

### Property **Leaders**( ) As [CATIADrawingLeaders](../DraftingInterfaces/interface_DrawingLeaders_41600.md) (Read Only)

Returns the drawing leader collection of the drawing table.

**Example:**      This example retrieves in `LeaderCollection` the collection of leaders of the `MyTable` drawing table.

```VBScript
Dim LeaderCollection As DrawingLeaders
Set LeaderCollection = MyTable.Leaders

```

### Property **NumberOfColumns**( ) As long (Read Only)

Returns the number of columns of a drawing table.

**Example:**      This example returns the number of columns of the drawing table `MyTable`.

```VBScript
oNbCol = MyTable.NumberOfColumns

```

### Property **NumberOfRows**( ) As long (Read Only)

Returns the number of rows of a drawing table.

**Example:**      This example returns the number of rows of the drawing table `MyTable`.

```VBScript
oNbRow = MyTable.NumberOfRows

```

### Property **x**( ) As double

Returns or sets the x coordinate of the table. It is expressed with respect to the current view coordinate system. This coordinate, like any length, is measured in mm.

**Example:**      This example retrieves the x coordinate of the table `MyTable` drawing table.

```VBScript
X = MyTable.x

```

### Property **y**( ) As double

Returns or sets the y coordinate of the table. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in mm.

**Example:**      This example sets the y coordinate of the table `MyTable` drawing table to 5 inches. You need first to convert the 5 inches into mm.

```VBScript
NewYCoordinate = 100
MyTable.y =  NewYCoordinate

```

Methods

### Sub **AddColumn**( long  `iCol`)

Adds a column before the indicated column.

**Parameters:**

` iCol`      The column before which the new column will be inserted

**Example:**      This example adds a column after the last one of the drawing table `MyTable`.

```VBScript
iCol = 0
MyTable.AddColumn iCol

```

### Sub **AddRow**( long  `iRow`)

Adds a row before the indicated row.

**Parameters:**

` iRow`      The row before which the new row will be inserted

**Example:**      This example adds a row beetween the first row and the second row of the drawing table `MyTable`.

```VBScript
iRow = 2
MyTable.AddRow iRow

```

### Func **GetCellAlignment**( long  `iRow`,  long  `iCol`) As [CatTablePosition](../DraftingInterfaces/enum_CatTablePosition_54616.md)

Retrieves the alignment of the pointed cell of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` oAlign`      The alignment type of the cell

**Example:**      This example retrieves the alignment of the cell (1,3) of the table `MyTable`.

```VBScript
iRow = 1
iCol = 3
oAlign = MyTable.GetCellAlignment(iRow, iCol)

```

### Func **GetCellBorderType**( long  `iRow`,  long  `iCol`) As [CatTableBorderType](../DraftingInterfaces/enum_CatTableBorderType_67390.md)

Retrieves the drawing text contained in the cell of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` oType`      The type of the cell border

**Example:**      This example retrieves the border type of the cell (1, 3) of the drawing table `MyTable`.

```VBScript
iRow = 1
iCol = 3
oType = MyTable.GetCellBorderType(iRow, iCol)

```

### Func **GetCellName**( long  `iRow`,  long  `iCol`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of a table cell.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` oName`      The cell name

**Example:**      This example returns the name of the cell (1,2) of the table `MyTable`.

```VBScript
iRow = 1
iCol = 2
oName = MyTable.GetCellName(iRow, iCol)

```

### Func **GetCellObject**( long  `iRow`,  long  `iCol`) As [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)

Retrieves the object contained in the cell of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` oText`      The object contained in the cell : this object only supports font properties, color, line spacing, Super/Sub script. Do not use position and/or orientation properties on this object, it is useless.

**Example:**      This example retrieves the drawing text `MyText` of the cell (1,3) of the table `MyTable`.

```VBScript
iRow = 1
iCol = 3
Set MyText = MyTable.GetCellObject(iRow, iCol)

```

### Func **GetCellString**( long  `iRow`,  long  `iCol`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the string contained in the cell of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` oString`      The string contained in the cell

**Example:**      This example returns the string contained in the cell (1,4) of the table `MyTable`.

```VBScript
iRow = 1
iCol = 4
oString = MyTable.GetCellString(iRow, iCol)

```

### Sub **GetCellsMerge**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfMergeCells`)

Returns the merge cells.

**Parameters:**

` oListOfMergeCells`      @param oListOfMergeCells List of merge cells.

**Example:**      This example returns the merge cells of the drawing table `MyTable`.

```VBScript
nbrow = MyTable.NumberOfRows
nbcol = MyTable.NumberOfColumns
sizetab = nbrow*nbcol
ReDim infoMerge (sizetab-1)
MyTable.GetCellsMerge(oListOfmergeCells)

```

### Func **GetColumnSize**( long  `iCol`) As double

Returns the width of a column of a drawing table.

**Parameters:**

` iCol`      The cell column
` oColSize`      The cell width in mm. If 0, it means that the width is automatic (corresponds to the size of the widest cell of the column).

**Example:**      This example returns the width of the column (1) of the drawing table `MyTable`.

```VBScript
iCol = 1
oColSize = MyTable.GetColumnSize(iCol)

```

### Sub **GetMergeInfos**( long  `iRow`,  long  `iCol`,  long  `oFirstRow`,  long  `oFirstCol`,  long  `oNbRow`,  long  `oNbCol`)

Returns informations about a group of merge cells from a cell.

**Parameters:**

` iRow`      @param iCol cell of merge
` iFirstRow`      Row of the first cell of the group Column of the first cell of the group
` iNbRowMerge`      Number of rows of the group
` iNbColMerge`      Number of columns of the group

**Example:**      This example returns informations of a group of merge cells from cell (2, 3) of the drawing table `MyTable`.

```VBScript
MyTable.GetMergeInfos 2, 3, oFirstRow, oFirstCol, oNbRow, oNbCol

```

### Func **GetRowSize**( long  `iRow`) As double

Returns the height of a row of a drawing table.

**Parameters:**

` iRow`      The cell row
` oRowSize`      The cell height in mm. If 0, it means that the height is automatic (corresponds to the size of the highest cell of the row).

**Example:**      This example returns the height of the row (1) of the drawing table `MyTable`.

```VBScript
iRow = 1
oRowSize = MyTable.GetRowSize(iRow)

```

### Sub **InvertMode**( [CatTableInvertMode](../DraftingInterfaces/enum_CatTableInvertMode_67010.md)  `iMode`)

Sets a mode of table inversion.

**Example:**      This example swaps the columns of the drawing table `MyTable`.

```VBScript
MyTable.InvertMode CatInvertColumn

```

### Sub **MergeCells**( long  `iFirstRow`,  long  `iFirstCol`,  long  `iNbRowMerge`,  long  `iNbColMerge`)

Merges a group of cells.

**Parameters:**

` iFirstRow`      @param iFirstCol First cell of merge
` iNbRowMerge`      Number of rows to merge
` iNbColMerge`      Number of columns to merge

**Example:**      This example merges cells from cell (2, 3) to cell (4, 5) of the drawing table `MyTable`.

```VBScript
MyTable.MergeCells 2, 3, 3, 3

```

### Sub **Move**( double  `iDeltaX`,  double  `iDeltaY`)

Moves the table relatively to its original position.

**Parameters:**

` iDeltaX`      The X deviation
` ideltaY`      The Y deviation

**Example:**      This example moves the table `MyTable` to 20mm in X.

```VBScript
DeltaX = 20.0
DeltaY =  0.0
MyTable.Move DeltaX, DeltaY

```

### Sub **RemoveColumn**( long  `iCol`)

Removes the indicated column.

**Parameters:**

` iCol`      The column to remove

**Example:**      This example removes the first column of the drawing table `MyTable`.

```VBScript
iCol = 1
MyTable.RemoveColumn iCol

```

### Sub **RemoveRow**( long  `iRow`)

Removes the indicated row.

**Parameters:**

` iRow`      The row to remove

**Example:**      This example removes the third row of the drawing table `MyTable`.

```VBScript
iRow = 3
MyTable.RemoveRow iRow

```

### Sub **Rotate**( double  `iDeltaAngle`)

Rotates the table relatively to its original position.

**Parameters:**

` iDeltaAngle`      The angle of rotation from the current position

**Example:**      This example rotates the table `MyTable` to 45 degrees.

```VBScript
PI = 3.1415926535
MyTable.Rotate PI/4

```

### Sub **SetCellAlignment**( long  `iRow`,  long  `iCol`,  [CatTablePosition](../DraftingInterfaces/enum_CatTablePosition_54616.md)  `iAlign`)

Sets the pointed cell alignment of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` iAlign`      The type of alignment to be applied

**Example:**      This example sets the cell (3,2) alignment of the table `MyTable` to bottom left.

```VBScript
iRow = 3
iCol = 2
MyTable.SetCellAlignment iRow, iCol, CatTableBottomLeft

```

### Sub **SetCellBorderType**( long  `iRow`,  long  `iCol`,  long  `iType`)

Sets the pointed cell border type of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` iType`      The type of border to be applied

**Example:**      This example sets the cell (3,2) border type of the table `MyTable` to right.

```VBScript
iRow = 3
iCol = 2
MyTable.SetCellBorderType iRow, iCol, CatTableRight

```

### Sub **SetCellName**( long  `iRow`,  long  `iCol`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

Sets the name of a table cell.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` iName`      The cell name

**Example:**      This example sets the name of the cell (1,2) of the table `MyTable` to "Cell 2".

```VBScript
iRow = 1
iCol = 2
iName = "Cell 2"
MyTable.SetCellName iRow, iCol, iName

```

### Sub **SetCellObject**( long  `iRow`,  long  `iCol`,  [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)  `iText`)

Sets an object in a cell of a drawing table.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` iText`      The Drawing Text to set in the cell

**Example:**      This example puts the drawing text `iText` in the cell (1,3) of the table `MyTable`.

```VBScript
iRow = 1
iCol = 3
MyTable.SetCellObject iRow, iCol, iText

```

### Sub **SetCellString**( long  `iRow`,  long  `iCol`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iString`)

Fills in a table cell with a string.

**Parameters:**

` iRow`      The cell row
` iCol`      The cell column
` iString`      The Text to be set

**Example:**      This example fills in the cell (3,2) of the table `MyTable` with "Title".

```VBScript
iRow = 3
iCol = 2
iString = "Title"
MyTable.SetCellString iRow, iCol, iString

```

### Sub **SetColumnSize**( long  `iCol`,  double  `iColSize`)

Sets the width of a column of a drawing table.

**Parameters:**

` iCol`      The cell column
` iColSize`      The cell width in mm. If 0, the width is automatic (corresponds to the size of the widest cell of the column).

**Example:**      This example sets the width of the column (1) of the drawing table `MyTable` to 20.

```VBScript
iCol = 1
iColSize = 20
MyTable.SetColumnSize iCol, iColSize

```

### Sub **SetRowSize**( long  `iRow`,  double  `iRowSize`)

Sets the height of a row of a drawing table.

**Parameters:**

` iRow`      The cell row
` iRowSize`      The cell height in mm. If 0, the height is automatic (corresponds to the size of the highest cell of the row).

**Example:**      This example sets the height of the row (1) of the drawing table `MyTable` to 20.

```VBScript
iRow = 1
iRowSize = 20
MyTable.SetRowSize iRow, iRowSize

```

### Sub **UnMergeCells**( long  `iRow`,  long  `iCol`)

Unmerges a group of cells.

**Parameters:**

` iRow`      @param iCol A cell of a merge

**Example:**      This example unmerges a group of cells of the drawing table `MyTable` from the cell (3, 5).

```VBScript
MyTable.UnMergeCells 3, 5

```