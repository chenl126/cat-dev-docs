# Layout2DRoot (Object)

**_Interface to manage the 2D Layout root._**

## Properties

### Property **ActiveSheet**(| ) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)

   Retrieves or sets the active sheet of the layout.

**Example:**      This example retrieves the active sheet currently managed by the layout root of a part of the active document, supposed to be a part document.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     Dim MySheet = MyRoot.GetActiveSheet

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection of parameters of the layout.

**Example:**      This example retrieves in `layoutParameters` the collection of parameters currently managed by the layout root of a part of the active document, supposed to be a part document.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     Dim layoutParameters As Parameters
     Set layoutParameters = MyRoot.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

   Returns the collection of relations of the part document.

**Example:**      This example retrieves in `layoutRelations` the collection of relations currently managed by the layout root of a part of the active document, supposed to be a part document.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     Dim layoutRelations As Relations
     Set layoutRelations = MyRoot.Relations

```

### Property **RenderingMode**( ) As [CatRenderingMode](../InfInterfaces/enum_CatRenderingMode_53126.md)

   Set/Get the rendering mode of Layout2D. get_RenderingMode method can fail if rendering value stored on Layout is not a value defined in CatRenderingMode enum.

**Example:**      This example sets the rendering mode to `catRenderShadingWithEdges` for the layout root of a part of the active document.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     MyRoot. RenderingMode  = catRenderShadingWithEdges

```

### Property **Sheets**( ) As [CATIALayout2DSheets](../Drafting2DLInterfaces/interface_Layout2DSheets_40224.md) (Read Only)

   Returns the collection of Layout2D sheets of the part document.

**Example:**      This example retrieves in `SheetCollection` the collection of sheets currently managed by the layout root of a part of the active document, supposed to be a part document.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     Dim SheetCollection As Layout2DSheets
     Set SheetCollection = MyRoot.Sheets.

```

### Property **Standard**( ) As [CatDrawingStandard](../DraftingInterfaces/enum_CatDrawingStandard_67878.md)

   Returns or sets the DrawingStandard of the part document.

**Example:**      This example sets the drawing standard currently managed by the layout root of a part of the active document, supposed to be a part document, to ISO.

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayout2DRoot)"
     MyRoot.Standard = catISO

```

### Property **VisuIn3D**( ) As [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md)

   Set/Get the 3D visualization mode of the layout in the 3D Viewer ie in the 3D windows and in the background of each view in every 2D context.

**See also:**      [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md) Methods

### Sub **reorder_Sheets**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrderedSheets`)

   Changes the positions of the sheets in this drawing according to the given ordered list. iOrderedSheets is the result of a permutation applied to the list of **all** the sheets of this drawing, with the following constraint: For every non-detail sheet, there is not any detail sheet appearing before in iOrderedSheets.

**Example:**      This example inverts the sheet order of a drawing made of exactly two regular sheets.

```VBScript
     Set drwsheetsorder =  CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot")
     Set drwsheets = drwsheetsorder.Sheets
     Set sheet1 = drwsheets.item(1)
     Set sheet2 = drwsheets.item(2)
     newsheetorder = Array(sheet2, sheet1)
     drwsheetsorder.reorder_Sheets(newsheetorder)

```