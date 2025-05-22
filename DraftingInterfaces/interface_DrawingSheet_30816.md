# DrawingSheet (Object)

**_Represents a drawing sheet of the drawing document._**

The drawing sheet is included in a drawing document and contains drawing views.
**Warning** : This interface is not available with 2D Layout for 3D Design.

## Properties

### Property **GenViewsPosMode**( ) As [CatSheetGenViewsPosMode](../DraftingInterfaces/enum_CatSheetGenViewsPosMode_108492.md)

Returns or sets the generative views position stability mode.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the stability mode of the `MySheet` drawing sheet so that after an update, existing and unmodified geometries don't move globally.

```VBScript
MySheet.GenViewsPosMode = catFixedAxis

```

### Property **Orientation**( ) As [CatPaperOrientation](../InfInterfaces/enum_CatPaperOrientation_77334.md)

Returns or sets the paper orientation.

**Example:**      This example sets the paper orientation for the `MySheet` drawing sheet to `catPaperLandscape`.

```VBScript
MySheet.Orientation = catPaperLandscape

```

### Property **PageSetup**( ) As [CATIADrawingPageSetup](../DraftingInterfaces/interface_DrawingPageSetup_54222.md) (Read Only)

Returns the page setup.

**Example:**      This example returns the page setup for the `MySheet` drawing sheet.

```VBScript
Dim MySheetPageSetup As DrawingPageSetup
Set MySheetPageSetup = MySheet.PageSetup

```

### Property **PaperSize**( ) As [CatPaperSize](../InfInterfaces/enum_CatPaperSize_30452.md)

Returns or sets the paper size.

**Example:**      This example sets the page size for the `MySheet` drawing sheet to `catPaperA4`.

```VBScript
MySheet.PaperSize = catPaperA4

```

### Property **PrintArea**( ) As [CATIA2DPrintArea](../DraftingInterfaces/interface_PrintArea_17142.md) (Read Only)

Returns the print area definition object.

**Example:**      This example returns the print area for the `MySheet` drawing sheet.

```VBScript
Dim MyPrintArea As PrintArea
Set MyPrintArea = MySheet.PrintArea

```

### Property **ProjectionMethod**( ) As [CatSheetProjectionMethod](../DraftingInterfaces/enum_CatSheetProjectionMethod_121130.md)

Returns or sets the sheet projection mode .

**Example:**      This example sets the projection mode of the `MySheet` drawing sheet to catFirstAngle.

```VBScript
MySheet.ProjectionMethod = catFirstAngle

```

### Property **Scale**( ) As double

Returns or sets the scale of the drawing sheet.

**Example:**      This example sets the scale of the `MySheet` drawing sheet to 0.5.

```VBScript
MySheet.Scale = 0.5

```

### Property **Scale2**( ) As double

Returns or sets the scale of the drawing sheet (Workaround for VBA keyword).

**Example:**      This example sets the scale of the `MySheet` drawing sheet to 0.5.

```VBScript
MySheet.Scale2 = 0.5

```

### Property **Views**( ) As [CATIADrawingViews](../DraftingInterfaces/interface_DrawingViews_31506.md) (Read Only)

Returns the drawing view collection of the drawing sheet.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `ViewCollection` the collection of views of the `MySheet` drawing sheet.

```VBScript
Dim ViewCollection As DrawingViews
Set ViewCollection = MySheet.Views

```

Methods

### Sub **Activate**( )

Activates the drawing sheet. Activating a drawing sheet means that this drawing sheet is the one on which the end user is now working. The window in the application's window collection which contains this drawing sheet becomes the active one.

**Example:**      This example activates the `MySheet` drawing sheet.

```VBScript
MySheet.Activate

```

### Sub **ForceUpdate**( )

Forces the update of all the drawing views of the drawing sheet. This update redraws all the views, whether their pointed objects have been modified since the drawing sheet creation or last update or not. These pointed objects can be CATIA Version 4 models, or CATIA Version 5 parts or assemblies.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example forces the update of all the dawing views in the `MySheet` drawing sheet.

```VBScript
MySheet.ForceUpdate

```

### Sub **GenerateDimensions**( )

Generates dimensions in all the drawing views of the drawing sheet. These dimensions are generated from the constraints of the pointed 3D part(s). One dimension only is generated for a given constraint. Only dimensions for the following constraints are generated: distance, length, angle, radius, and diameter.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example generates the dimensions for all the views in the `MySheet` drawing sheet.

```VBScript
MySheet.GenerateDimensions

```

### Func **GetPaperHeight**( ) As double

Gets the paper width of the drawing sheet.

**Parameters:**

` oPaperHeight`

**Example:**      This example get the height of the `DrawingSheet1`.

```VBScript
DrawingSheet1.GetPaperHeight oPaperHeight

```

### Func **GetPaperWidth**( ) As double

Gets the paper width of the drawing sheet.

**Parameters:**

` oPaperWidth`

**Example:**      This example get the width of the `DrawingSheet1`.

```VBScript
DrawingSheet1.GetPaperWidth oPaperWidth

```

### Func **IsDetail**( ) As boolean

Checks whether the sheet is a detail sheet.
**Warning** : This method is not available with 2D Layout for 3D Design.
TRUE if the sheet is a detail sheet.

**Example:**      This example checks whether `MySheet` is a detail sheet.

```VBScript
IsDetail = MySheet.IsDetail

```

### Sub **Isolate**( )

Isolates the drawing sheet.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example isolates the `MySheet` drawing sheet.

```VBScript
MySheet.Isolate

```

### Sub **PrintOut**( )

Prints the drawing sheet according to its page setup on the default printer.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example prints the `DrawingSheet1` on the default printer.

```VBScript
DrawingSheet1.PrintOut

```

### Sub **PrintToFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`)

Prints the drawing sheet according its page setup in a file instead of being sent to a printer.

**Parameters:**

` fileName`      The full pathname of the file receiving the data.
**Warning** : This method is not available with 2D Layout for 3D Design.  **Example:**      This example prints the `DrawingSheet1` in a file.

```VBScript
DrawingSheet1.PrintToFile "e:\temp\sheet1.prn"

```

### Sub **SetAsDetail**( )

Sets the sheet as a detail sheet. You can now create views into this sheet that will be taken as details. A detail is made to be reuse as dittos in views.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example changes the `MySheet` into a detail sheet.

```VBScript
MySheet.SetAsDetail

```

### Sub **SetPaperHeight**( double  `oPaperHeight`)

Sets the paper width of the drawing sheet, avalaible on user format.

**Parameters:**

` iPaperHeight`

**Example:**      This example set the height of the `DrawingSheet1`.

```VBScript
DrawingSheet1.PaperSize = catPaperUser
DrawingSheet1.SetPaperHeight iPaperHeight

```

### Sub **SetPaperWidth**( double  `oPaperWidth`)

Sets the paper width of the drawing sheet, avalaible on user format.

**Parameters:**

` iPaperWidth`

**Example:**      This example set the width of the `DrawingSheet1`.

```VBScript
DrawingSheet1.PaperSize = catPaperUser
DrawingSheet1.SetPaperWidth iPaperWidth

```

### Sub **Update**( )

Updates the drawing views of the drawing sheet. This update redraws all the views whose pointed objects have been modified since the drawing sheet creation or last update, but do not redraw the views whose pointed have not been modifed. These pointed objects can be CATIA Version 4 models, or CATIA Version 5 parts or assemblies.
**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example updates the drawing views in the `MySheet` drawing sheet.

```VBScript
MySheet.Update

```

### Sub **reorder_Views**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrderedViews`)

Changes the positions of the views in this sheet according to the given ordered list. iOrderedViews is the result of a permutation applied to the list of **all** the views of this sheet with the following constraint: the two first elements of the list must be respectively the sheet's mainview and background view.

**Example:**      This example modifies the views order of a sheet made of a mainview, a backgroundview and two user-created views. (user-created views are inverted).

```VBScript
Set drwviewsorder = CATIA.ActiveDocument.Sheets.ActiveSheet
Set drwviews = drwviewsorder.Views
Set mainview = drwviews.item(1)
Set backview = drwviews.item(2)
Set view1 = drwviews.item(3)
Set view2 = drwviews.item(4)
newvieworder = Array(mainview, backview, view2, view1)
drwviewsorder.reorder_Views(newvieworder)

```