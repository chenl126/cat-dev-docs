# DrawingRoot (Object)

**_Represents the drawing object in drawing documents._**

**Warning** : This interface is not available with 2D Layout for 3D Design.

## Properties

### Property **ActiveSheet**( ) As [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md)

Retrieves or sets the active sheet of the drawing.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves the active sheet in the drawing of the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.DrawingRoot.GetActiveSheet

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection of parameters of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `DrawingParameters` the collection of parameters currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim DrawingParameters As Parameters
Set DrawingParameters = CATIA.ActiveDocument.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

Returns the collection of relations of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `DrawingRelations` the collection of relations currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim DrawingRelations As Relations
Set DrawingRelations = CATIA.ActiveDocument.Relations

```

### Property **Sheets**( ) As [CATIADrawingSheets](../DraftingInterfaces/interface_DrawingSheets_36522.md) (Read Only)

Returns the collection of drawing sheets of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `SheetCollection` the collection of sheets currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim SheetCollection As DrawingSheets
Set SheetCollection = CATIA.ActiveDocument.Sheets

```

### Property **Standard**( ) As [CatDrawingStandard](../DraftingInterfaces/enum_CatDrawingStandard_67878.md)

Returns or sets the drawing standard of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the drawing standard of the active document, supposed to be a drawing document, to ISO.

```VBScript
CATIA.ActiveDocument.Standard = catISO

```

Methods

### Sub **Isolate**( )

Isolates all the drawing views of all the drawing sheets of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example isolates all the drawing views of all the drawing sheets of the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.Isolate

```

### Sub **Update**( )

Updates all the drawing sheets of the drawing document.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example updates the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.Update

```

### Sub **reorder_Sheets**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrderedSheets`)

Changes the positions of the sheets in this drawing according to the given ordered list. iOrderedSheets is the result of a permutation applied to the list of **all** the sheets of this drawing, with the following constraint: For every non-detail sheet, there is not any detail sheet appearing before in iOrderedSheets.

**Example:**      This example inverts the sheet order of a drawing made of exactly two regular sheets.

```VBScript
Set drwsheets = CATIA.ActiveDocument.Sheets
Set drwsheetsorder =  CATIA.ActiveDocument.DrawingRoot
Set sheet1 = drwsheets.item(1)
Set sheet2 = drwsheets.item(2)
newsheetorder = Array(sheet2, sheet1)
drwsheetsorder.reorder_Sheets(newsheetorder)

```