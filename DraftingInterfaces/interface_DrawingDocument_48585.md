# DrawingDocument (Object)

**_Represents the Document object for drawings._**

## Properties

### Property **DrawingRoot**( ) As [CATIADrawingDrawing](../DraftingInterfaces/interface_DrawingRoot_26516.md) (Read Only)

Retrieves the drawing root in the drawing document.

**Example:**      This example retrieves the drawing from the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.DrawingRoot

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection of parameters of the drawing document.

**Example:**      This example retrieves in `DrawingParameters` the collection of parameters currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim DrawingParameters As Parameters
Set DrawingParameters = CATIA.ActiveDocument.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

Returns the collection of relations of the drawing document.

**Example:**      This example retrieves in `DrawingRelations` the collection of relations currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim DrawingRelations As Relations
Set DrawingRelations = CATIA.ActiveDocument.Relations

```

### Property **Sheets**( ) As [CATIADrawingSheets](../DraftingInterfaces/interface_DrawingSheets_36522.md) (Read Only)

Returns the collection of drawing sheets of the drawing document.

**Example:**      This example retrieves in `SheetCollection` the collection of sheets currently managed by the active document, supposed to be a drawing document.

```VBScript
Dim SheetCollection As DrawingSheets
Set SheetCollection = CATIA.ActiveDocument.Sheets

```

### Property **Standard**( ) As [CatDrawingStandard](../DraftingInterfaces/enum_CatDrawingStandard_67878.md)

Returns or sets the drawing standard of the drawing document.

**Example:**      This example sets the drawing standard of the active document, supposed to be a drawing document, to ISO.

```VBScript
CATIA.ActiveDocument.Standard = catISO

```

Methods

### Sub **Isolate**( )

Isolates all the drawing views of all the drawing sheets of the drawing document.

**Example:**      This example isolates all the drawing views of all the drawing sheets of the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.Isolate

```

### Sub **Update**( )

Updates all the drawing sheets of the drawing document.

**Example:**      This example updates the active document, supposed to be a drawing document.

```VBScript
CATIA.ActiveDocument.Update

```