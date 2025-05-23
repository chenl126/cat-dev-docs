# DrawingPictures (Collection)

**_A collection of all the drawing pictures currently managed by a drawing view of drawing sheet in a drawing document._**

## Methods

### Func **Add**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iDrawingPicturePath`,| | double | `iPositionX`,| | double | `iPositionY`) As [CATIADrawingPicture](../DraftingInterfaces/interface_DrawingPicture_42512.md)

   Inserts a drawing picture in the drawing view and adds it to the DrawingPictures collection.

**Parameters:**

` iDrawingPicturePath`      The path of the picture file (ex : "C:\tmp\ball.bmp") .
` iPositionX,iPositionY`      The drawing picture x and y coordinates, expressed in millimeters, with respect to the drawing view coordinate system

**Returns:**      The inserted drawing picture  **Example:**      The following example inserts a drawing picture from a given picture file path The `MyView` is the active view in the active drawing sheet

```VBScript
     Dim MySheet As DrawingSheet
     Set MySheet = CATIA.ActiveDocument.Sheets.ActiveSheet
     Dim MyView As DrawingView
     Set MyView = MySheet.Views.ActiveView
     Dim MyDrawingPicture1 As DrawingPicture
     Set MyDrawingPicture1 = MyView.Pictures.Add("C:\tmp\ball.bmp", 100., 50.)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADrawingPicture](../DraftingInterfaces/interface_DrawingPicture_42512.md)

   Returns a drawing picture using its index or its name from the DrawingPictures collection.

**Parameters:**

` iIndex`      The index or the name of the drawing picture to retrieve from the collection of drawing pictures. As a numerics, this index is the rank of the drawing picture in the collection. The index of the first drawing picture in the collection is 1, and the index of the last drawing picture is Count. As a string, it is the name you assigned to the drawing picture using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved drawing picture  **Example:**      This example retrieves in `ThisDrawingPicture` the second drawing picture, `MyView` in the drawing view collection of the active sheet in the active document, supposed to be a drawing document.

```VBScript
     Dim MySheet As DrawingSheet
     Set MySheet = CATIA.ActiveDocument.Sheets.ActiveSheet
     Dim MyView  As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     Dim ThisDrawingPicture As DrawingPicture
     Set ThisDrawingPicture = MyView.Pictures.Item(2)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a drawing picture from the DrawingPictures collection.

**Parameters:**

` iIndex`      The index of the drawing picture to remove from the collection of drawing pictures. As a numerics, this index is the rank of the drawing picture in the collection. The index of the first drawing picture in the collection is 1, and the index of the last drawing picture is Count. As a string, it is the name you assigned to the drawing picture using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the third drawing picture in the drawing pictures collection of the active view of the active document, supposed to be a drawing document.

```VBScript
     Dim MyView As DrawingView
     Set MyView  = MySheet.Views.ActiveView
     MyView.Pictures.Remove(3)

```