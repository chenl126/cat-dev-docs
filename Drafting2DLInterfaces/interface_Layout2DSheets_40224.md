# Layout2DSheets (Collection)

**_A collection of all the Layout sheets 2DL currently managed by the LayoutRoot._**

## Properties

### Property **ActiveSheet**( ) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md) (Read Only)

Returns the active Layout sheet of the Layout document.

**Example:**      The following example shows how to get the active sheet and retrieved in `MySheet` in the Layout sheet collection of the layout root of `Part` supposed to be in the active document

```VBScript
Dim MyLayoutRoot As Layout2DRoot
Set MyLayoutRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")
Dim MySheet As Layout2DSheet
Set MySheet =  MyLayoutRoot.Sheets.ActiveSheet

```

Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLayoutSheetName`) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)

Creates a Layout sheet and adds it to the Layout2DSheets collection. This Layout sheet becomes the active one.

**Parameters:**

` iLayoutSheetName`      The name to assign to the created Layout2DSheet object
**Returns:**      The created Layout sheet  **Example:**      The following example creates a Layout sheet named `FirstSheet` and retrieved in `MySheet` in the Layout sheet collection of the layout root of `Part` supposed to be in the active document

```VBScript
Dim MyLayoutRoot As Layout2DRoot
Set MyLayoutRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")
Dim MySheet As Layout2DSheet
Set MySheet = MyLayoutRoot.Sheets.Add("FirstSheet").

```

### Func **AddDetail**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLayoutSheetName`) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)

Creates a detail Layout sheet 2DL and adds it to the LayoutSheets2DL collection. This detail Layout sheet becomes the active one.

**Parameters:**

` iLayoutSheetName`      The name to assign to the created detail LayoutSheet object
**Returns:**      The created layout sheet  **Example:**      The following example creates a detail Layout sheet named `FirstSheet` and retrieved in `MySheet` in the Layout sheet collection of the layout root of `Part` supposed to be in the active document

```VBScript
Dim MyLayoutRoot As Layout2DRoot
Set MyLayoutRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")
Dim MySheet As Layout2DSheet
Set MySheet = MyLayoutRoot.Sheets.Add("FirstSheet")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)

Returns a Layout sheet using its index or its name from the Layout2DSheets collection.

**Parameters:**

` iIndex`      The index or the name of the Layout sheet to retrieve from the collection of Layout sheets. As a numerics, this index is the rank of the Layout sheet in the collection. The index of the first Layout sheet in the collection is 1, and the index of the last Layout sheet is Count. As a string, it is the name you assigned to the Layout sheet using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved Layout sheet  **Example:**      This example retrieves in `ThisLayoutSheet` the third Layout sheet, and in `ThatLayoutSheet` the Layout sheet named `MySheet` in the Layout sheet collection of the layout root of `Part` supposed to be in the active document.

```VBScript
Dim ThisLayoutRoot As Layout2DRoot
Set ThisLayoutRoot = CATIA.ActiveDocument.Part.GetItem("CATlayoutRoot")
Dim ThisLayoutSheet As Layout2DSheet
Set ThisLayoutSheet = ThisLayoutRoot.Sheets.Item(3)
Dim ThatLayoutSheet As Layout2DSheet
Set ThatLayoutSheet = ThisLayoutRoot.Sheets.Item("MySheet")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a Layout2Dsheet from the Layout2DSheets collection.

**Parameters:**

` iIndex`      The index or the name of the Layout sheet to remove from the collection of Layout sheets. As a numerics, this index is the rank of the Layout sheet in the collection. The index of the first Layout sheet in the collection is 1, and the index of the last Layout sheet is Count. As a string, it is the name you assigned to the Layout sheet using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Example:**      The following example removes the second Layout sheet and the Layout sheet named `SheetToBeRemoved` in the Layout sheet collection of the layout root of `Part` supposed to be in the active document.

```VBScript
Dim ThisLayoutRoot As Layout2DRoot
Set ThisLayoutRoot = CATIA.ActiveDocument.Part.GetItem("CATlayoutRoot")
ThisLayoutRoot.Layout2DSheets.Remove("SheetToBeRemoved")

```