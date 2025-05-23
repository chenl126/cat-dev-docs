# Layout2DSheet (Object)

**_The interface to access a Layout2D Sheet._**

## Properties

### Property **Orientation**(| ) As [CatPaperOrientation](../InfInterfaces/enum_CatPaperOrientation_77334.md)

   Returns or sets the paper orientation.

**Example:**      This example sets the paper orientation for the `MySheet` Layout2D sheet to `catPaperLandscape`.

```VBScript
     MySheet.Orientation = catPaperLandscape

```

### Property **PageSetup**( ) As [CATIADrawingPageSetup](../DraftingInterfaces/interface_DrawingPageSetup_54222.md) (Read Only)

   Returns the page setup.

**Example:**      This example returns the page setup for the `MySheet` Layout2D sheet.

```VBScript
     Dim MySheetPageSetup As DrawingPageSetup
     Set MySheetPageSetup = MySheet.PageSetup

```

### Property **PaperHeight**( ) As double

   Gets or Sets the paper width of the layout sheet.

**Parameters:**

` oPaperHeight`

**Example:**      This example get the height of the `Layout2DSheet1`.

```VBScript
     Layout2DSheet1.GetPaperHeight oPaperHeight

```

### Property **PaperName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the paper format name.

**Example:**      This example sets the paper format name for the `MySheet` Layout2D sheet to `DSFormat1`.

```VBScript
     MySheet.PaperName = DSFormat1

```

### Property **PaperSize**( ) As [CatPaperSize](../InfInterfaces/enum_CatPaperSize_30452.md)

   Returns or sets the paper size.

**Example:**      This example sets the page size for the `MySheet` Layout2D sheet to `catPaperA4`.

```VBScript
     MySheet.PaperSize = catPaperA4

```

### Property **PaperWidth**( ) As double

   Gets or Sets the paper width of the layout sheet.

**Parameters:**

` oPaperWidth`

**Example:**      This example get the width of the `Sheet1`.

```VBScript
     Sheet1.GetPaperWidth oPaperWidth

```

### Property **PrintArea**( ) As [CATIA2DPrintArea](../DraftingInterfaces/interface_PrintArea_17142.md) (Read Only)

   Returns the print area definition object.

**Example:**      This example returns the print area for the `MySheet` Layout2D sheet 2DL.

```VBScript
     Dim MyPrintArea As PrintArea
     Set MyPrintArea = MySheet.PrintArea

```

### Property **ProjectionMethod**( ) As [CatSheetProjectionMethod](../DraftingInterfaces/enum_CatSheetProjectionMethod_121130.md)

   Returns or sets the sheet projection mode .

**Example:**      This example sets the projection mode of the `MySheet` Layout2D sheet to catFirstAngle.

```VBScript
     MySheet.ProjectionMethod = catFirstAngle

```

### Property **SheetScale**( ) As double

   Returns or sets the scale of the Layout2D sheet.

**Example:**      This example sets the scale of the `MySheet` Layout2D sheet to 0.5.

```VBScript
     MySheet.SheetScale = 0.5

```

### Property **Views**( ) As [CATIALayout2DViews](../Drafting2DLInterfaces/interface_Layout2DViews_34886.md) (Read Only)

   Returns the Layout2D view collection of the Layout2D sheet.

**Example:**      This example retrieves in `ViewCollection` the collection of views 2DL of the `MySheet` Layout2D sheet.

```VBScript
     Dim ViewCollection As Layout2DViews
     Set ViewCollection = MySheet.Views.

```

### Property **VisuIn3D**( ) As [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md)

   Set/Get the 3D visualization mode of the sheet in the 3D Viewer ie in the 3D windows and in the background of each view in every 2D context.

**See also:**      [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md) Methods

### Sub **Activate**( )

   Activates the Layout2D sheet. Activating a Layout2D sheet means that this Layout2D sheet is the one on which the end user is now working. The window in the application's window collection which contains this Layout2D sheet becomes the active one.

**Example:**      This example activates the `MySheet` layout2dsheet.

```VBScript
     MySheet.Activate

```

### Func **IsDetail**( ) As boolean

   Checks whether the sheet is a detail sheet.
TRUE if the sheet is a detail sheet.

**Example:**      This example checks whether `MySheet` is a detail sheet.

```VBScript
     IsDetail = MySheet.IsDetail

```

### Sub **PrintOut**( [CatRenderingMode](../InfInterfaces/enum_CatRenderingMode_53126.md)  `iRenderingMode`)

   Prints the Layout2D sheet according to its page setup on the default printer.

**Parameters:**

` iRenderingMode`      The rendering mode to use for the backgrounds of the views in the sheet.

**Example:**      This example prints the `Layout2DSheet1` on the default printer.

```VBScript
     Layout2DSheet1.PrintOut catRenderShadingWithEdges

```

### Sub **PrintOut2**( )

   Prints the Layout2D sheet according to its page setup on the default printer. If a rendering mode has been stored on the 2D Layout, it is used during print process for the backgrounds. Otherwise, "Shading with edges" rendering mode is used.

**Example:**      This example prints the `Layout2DSheet1` on the default printer.

```VBScript
     Layout2DSheet1.PrintOut2

```

### Sub **PrintToFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`,  [CatRenderingMode](../InfInterfaces/enum_CatRenderingMode_53126.md)  `iRenderingMode`)

   Prints the Layout2D sheet according its page setup in a file instead of being sent to a printer.

**Parameters:**

` fileName`      The full pathname of the file receiving the data.
` iRenderingMode`      The rendering mode to use for the backgrounds of the views in the sheet.  **Example:**      This example prints the `Layout2DSheet1` in a file.

```VBScript
     Layout2DSheet1.PrintToFile "e:\temp\sheet1.prn",catRenderShadingWithEdges

```

### Sub **PrintToFile2**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`)

   Prints the Layout2D sheet according its page setup in a file instead of being sent to a printer. If a rendering mode has been stored on the 2D Layout, it is used during print process for the backgrounds. Otherwise, "Shading with edges" rendering mode is used.

**Parameters:**

` fileName`      The full pathname of the file receiving the data.  **Example:**      This example prints the `Layout2DSheet1` in a file.

```VBScript
     Layout2DSheet1.PrintToFile2 "e:\temp\sheet1.prn"

```

### Sub **reorder_Views**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrderedViews`)

   Changes the positions of the views in this sheet according to the given ordered list. iOrderedViews is the result of a permutation applied to the list of **all** the views of this sheet with the following constraint: the two first elements of the list must be respectively the sheet's mainview and background view.

**Example:**      This example modifies the views order of a sheet made of a mainview, a backgroundview and two user-created views. (user-created views are inverted).

```VBScript
     Set drw =  CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot")
     Set drwviewsorder = drwsheetsorder.Sheets.ActiveSheet
     Set drwviews = drwviewsorder.Views
     Set mainview = drwviews.item(1)
     Set backview = drwviews.item(2)
     Set view1 = drwviews.item(3)
     Set view2 = drwviews.item(4)
     newvieworder = Array(mainview, backview, view2, view1)
     drwviewsorder.reorder_Views(newvieworder)

```