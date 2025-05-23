# DrawingSheets (Collection)

**_A collection of all the drawing sheets currently managed by the drawing document._**

**Warning** : This interface is not available with 2D Layout for 3D Design.

## Properties

### Property **ActiveSheet**(| ) As [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md) (Read Only)

   Returns the active drawing sheet of the drawing document.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      The following example retrieves in `SheetToWorkIn` the active drawing sheet of the drawing document named `CATDrawing1`.

```VBScript
     Dim MyDrawingDoc As Document
     Set MyDrawingDoc = CATIA.Documents.Item("CATDrawing1")
     Dim SheetToWorkIn As DrawingSheet
     Set SheetToWorkIn =  MyDrawingDoc.Sheets.ActiveSheet

```

Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDrawingSheetName`) As [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md)

   Creates a drawing sheet and adds it to the DrawingSheets collection. This drawing sheet becomes the active one.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iDrawingSheetName`      The name to assign to the created DrawingSheet object

**Returns:**      The created drawing sheet  **Example:**      The following example creates a drawing sheet named `FirstSheet` and retrieved in `MySheet` in the drawing sheet collection of the document named `CATDrawing1`.

```VBScript
     Dim MyDrawingDoc As Document
     Set MyDrawingDoc = CATIA.Documents.Item("CATDrawing1")
     Dim MySheet As DrawingSheet
     Set MySheet = MyDrawingDoc.Sheets.Add("FirstSheet")

```

### Func **AddDetail**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDrawingSheetName`) As [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md)

   Creates a detail drawing sheet and adds it to the DrawingSheets collection. This detail drawing sheet becomes the active one.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iDrawingSheetName`      The name to assign to the created detail DrawingSheet object

**Returns:**      The created drawing sheet  **Example:**      The following example creates a detail drawing sheet named `FirstSheet` and retrieved in `MySheet` in the drawing sheet collection of the document named `CATDrawing1`.

```VBScript
     Dim MyDrawingDoc As Document
     Set MyDrawingDoc = CATIA.Documents.Item("CATDrawing1")
     Dim MySheet As DrawingSheet
     Set MySheet = MyDrawingDoc.Sheets.Add("FirstSheet")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md)

   Returns a drawing sheet using its index or its name from the DrawingSheets collection.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iIndex`      The index or the name of the drawing sheet to retrieve from the collection of drawing sheets. As a numerics, this index is the rank of the drawing sheet in the collection. The index of the first drawing sheet in the collection is 1, and the index of the last drawing sheet is Count. As a string, it is the name you assigned to the drawing sheet using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved drawing sheet  **Example:**      This example retrieves in `ThisDrawingSheet` the third drawing sheet, and in `ThatDrawingSheet` the drawing sheet named `MySheet` in the drawing sheet collection of the active document, supposed to be a drawing document.

```VBScript
     Dim ThisDrawingSheet As DrawingSheet
     Set ThisDrawingSheet = CATIA.ActiveDocument.Sheets.Item(3)
     Dim ThatDrawingSheet As DrawingSheet
     Set ThatDrawingSheet = CATIA.ActiveDocument.Sheets.Item("MySheet")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a drawing sheet from the DrawingSheets collection.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iIndex`      The index or the name of the drawing sheet to remove from the collection of drawing sheets. As a numerics, this index is the rank of the drawing sheet in the collection. The index of the first drawing sheet in the collection is 1, and the index of the last drawing sheet is Count. As a string, it is the name you assigned to the drawing sheet using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Example:**      The following example removes the second drawing sheet and the drawing sheet named `SheetToBeRemoved` in the drawing sheet collection of the active document, supposed to be a drawing document.

```VBScript
     CATIA.ActiveDocument.DrawingSheets.Remove(2)
     CATIA.ActiveDocument.DrawingSheets.Remove("SheetToBeRemoved")

```