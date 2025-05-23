# DrawingViews (Collection)

**_A collection of all the drawing views currently managed by a drawing sheet in a drawing document._**

**Warning** : This interface is not available with 2D Layout for 3D Design.

## Properties

### Property **ActiveView**(| ) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md) (Read Only)

   Returns the active drawing view of the active drawing sheet.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      The following example retrieves in `ViewToWorkIn` the active drawing view in the DrawingSheets collection of the document named `CATDrawing1`

```VBScript
     Dim MyDrawingDoc As Document
     Set MyDrawingDoc = CATIA.Documents.Item("CATDrawing1")
     Dim ViewToWorkIn As DrawingView
     Set ViewToWorkIn = MyDrawingDoc.Sheets.ActiveSheet.DrawingViews.ActiveView

```

Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDrawingViewName`) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)

   Creates a drawing view and adds it to the drawing view collection. This drawing view becomes the active one.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iDrawingViewName`      The name to assign to the created drawing view

**Returns:**      The created drawing view  **Example:**      The following example creates a drawing view named `LeftView` and retrieved in `MyView` in the drawing view collection of the `MySheet` drawing sheet. This sheet belongs to the drawing sheet collection of the drawing document named `CATDrawing1`.

```VBScript
     Dim MyDrawingDoc As Document
     Set MyDrawingDoc = CATIA.Documents.Item("CATDrawing1")
     Dim MySheet As DrawingSheet
     Set MySheet = MyDrawingDoc.Sheets.Item("FirstSheet")
     Dim MyView As DrawingView
     Set MyView = MySheet.Views.Add("LeftView")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)

   Returns a drawing view using its index or its name from the DrawingViews collection.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iIndex`      The index or the name of the drawing view to retrieve from the collection of drawing views. As a numerics, this index is the rank of the drawing view in the collection. The index of the first drawing view in the collection is 1, and the index of the last drawing view is Count. As a string, it is the name you assigned to the drawing view using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved drawing view  **Example:**      This example retrieves in `ThisDrawingView` the second drawing view, and in `ThatDrawingView` the drawing view named `MyView` in the drawing view collection of the active sheet in the active document, supposed to be a drawing document.

```VBScript
     Dim MySheet As DrawingSheet
     Set MySheet = CATIA.ActiveDocument.Sheets.ActiveSheet
     Dim ThisDrawingView As DrawingView
     Set ThisDrawingView = MySheet.Views.ActiveView.Item(2)
     Dim ThatDrawingView As DrawingView
     Set ThatDrawingView = MySheet.Views.ActiveView.Item("MyView")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a drawing view from the DrawingViews collection.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iIndex`      The index or the name of the drawing view to remove from the collection of drawing views. As a numerics, this index is the rank of the drawing view in the collection. The index of the first drawing view in the collection is 1, and the index of the last drawing view is Count. As a string, it is the name you assigned to the drawing view using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Example:**      The following example removes the third drawing view and the drawing view named `TopView` in the drawing view collection of the active sheet of the active document, supposed to be a drawing document.

```VBScript
     Dim MySheet As DrawingSheet
     Set MySheet = CATIA.ActiveDocument.Sheets.ActiveSheet
     MySheet.ActiveViews.Remove(3)
     MySheet.ActiveViews.Remove("TopView")

```