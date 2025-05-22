# Document (Object)

**_Represents the document._**
The document is the object handled by the operating system as a whole that stores your data in files and databases. It is assigned a type determined by its contents. It may contain other documents with a different type. For example, a PartDocument contains a part and can be contained in a ProductDocument. A workshop is associated with a document to gather all the commands that can be used to create, modify, and edit the objects making up the the document. These commands are arranged in menus and toolbars.

**See also:**      [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md), [ProductDocument](../ProductStructureInterfaces/interface_ProductDocument_49026.md), [DrawingDocument](../DraftingInterfaces/interface_DrawingDocument_48585.md)

## Properties

### Property **Cameras**( ) As [CATIACameras](../InfInterfaces/interface_Cameras_10798.md) (Read Only)

Returns the document's collection of cameras.

**Example:**      This example retrieves in `CameraCollection` the collection of cameras attached to the `Doc` document.

```VBScript
Dim CameraCollection As Cameras
Set CameraCollection = Doc.Cameras

```

### Property **CurrentFilter**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the current visualization filter. `CurrentFilter` uses the filter name and not its definition. The "All visible" filter means that all layers are visible. For all filters, remind that the current layer is always visible.

**Example:**      This example makes the filter named "Filter001" as the current visualization filter for the `Doc` document.

```VBScript
Doc.CurrentFilter = "Filter001"

```

### Property **CurrentLayer**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the current layer. `CurrentLayer` uses the layer name and not its number. The "None" layer means that there is no current layer.

**Example:**      This example makes the layer named "Layer 3" as the current layer for the `Doc` document.

```VBScript
Doc.CurrentLayer = "Layer 3"

```

### Property **FullName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the document's full file name, including its path.

**Example:**      This example retrieves in `DocFullName` the `Doc` document's full file name.

```VBScript
DocFullName = Doc.FullName

```

The returned value is like this:

```VBScript
e:\users\psr\Parts\MyNicePart.CATPart

```

### Property **Path**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the document's file path.

**Example:**      This example retrieves in `DocPath` the path where the `Doc` document is stored.

```VBScript
DocPath = Doc.Path

```

The returned value is like this:

```VBScript
e:\users\psr\Parts

```

### Property **ReadOnly**( ) As boolean (Read Only)

Returns whether the file containing the document can be read only, on can be read and written.
**True** if the file is read-only.

**Example:**      This example retrieves in `IsReadOnly` the ability to read, and possibly to write in, the file containing the `Doc` document.

```VBScript
IsReadOnly = Doc.ReadOnly

```

### Property **Saved**( ) As boolean (Read Only)

Returns whether the document has been modified, and thus needs to be saved.
This happens when the document has changed since either its creation or its last save.

  * **True** if the document has not been changed: the document doesn't need to be saved.
  * **False** if the document has been changed: the document needs to be saved.

**Example:**      This example retrieves in `HasChanged` whether the `Doc` document needs to be saved.

```VBScript
HasChanged = NOT Doc.Saved

```

### Property **SeeHiddenElements**( ) As boolean

Returns or sets the document's hidden elements visibility.
**True** if the document's hidden elements are visible to the user.

**Example:**      This example makes the `Doc` document's hidden elements visible.

```VBScript
Doc.SeeHiddenElements = True

```

### Property **Selection**( ) As [CATIASelection](../InfInterfaces/interface_Selection_18040.md) (Read Only)

Returns the current selection. The current selection is the object or the set of objects the end user has selected, usually with the mouse, in the active document displayed in the active window.

**Example:**      This example returns in `CurSel` the current selection in the `Doc` document

```VBScript
Dim CurSel As Selection
Set CurSel = Doc.Selection

```

Methods

### Sub **Activate**( )

Activates the document. Activating a document means that this document is the one on which the end user is now working on. This document possibly reconfigures the menu bar and toolbars with its own commands if its type is different from the type of the previous active document. The first window in the window collection which contains this document becomes the active one.

**Example:**      This example activates the `Doc` document.

```VBScript
Doc.Activate()

```

### Sub **Close**( )

Closes the document. This closes all the windows displaying the document. If the document needs to be saved, the end user is prompted whether to save the document, or to close it anyway.

**Example:**      This example closes the `Doc` document

```VBScript
Doc.Close()

```

### Sub **CreateFilter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilterName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilterDefinition`)

Creates a new visualization filter from a name and a definition. Fails if there is already a filter named iFilterName.

**Parameters:**

` iFilterName`      The filter name.
` iFilterDefinition`      The filter definition  **Example:**      This example creates the filter named "Filter001" and with "layer= 2 & layer= 1" definition for the `Doc` document.

```VBScript
Doc.CreateFilter ("Filter001", "layer= 2 & layer= 1")

```

### Func **CreateReferenceFromName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from a GenericNaming label. Each kind of document provides a specific implementation.

**Parameters:**

` iLabel`      The GenericNaming identification for an object.
**Returns:**      The reference to the object.  
### Sub **ExportData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `format`)

Exports the data contained in the document to another format.

**Parameters:**

` fileName`      The name of the exported file
` format`      The name of the format  **Example:**      This example writes the `Doc` document in the IGES format under the `IGESDoc` name.

```VBScript
Doc.ExportData("IGESDoc", "igs")

```

### Func **GetWorkbench**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `workbenchName`) As [CATIAWorkbench](../InfInterfaces/interface_Workbench_17725.md)

Returns one of the workbenches of the document.

**Parameters:**

` workbenchName`      The name of the workbench

**Example:**      This example retrieves the Structural workbench on the `Doc` document

```VBScript
Doc.GetWorkbench("Structural")

```

### Func **Indicate2D**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMessage`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDocumentWindowLocation`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Runs an 2D interactive indication command.
**Role** : `Indicate2D` asks to the user to select a location in the document window. It can be used:

* When this document is a [DrawingDocument](../DraftingInterfaces/interface_DrawingDocument_48585.md)

* When this document is a [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md), and a sketch is being edited ( [Sketch.OpenEdition](../SketcherInterfaces/interface_Sketch_8026.htm#OpenEdition) has been called and [Sketch.CloseEdition](../SketcherInterfaces/interface_Sketch_8026.htm#CloseEdition) has not been called yet)

**See also:** [Selection.IndicateOrSelectElement2D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement2D) which can, in particular, enable indication and not selection (positionning the iFilterType parameter to an empty string), whichs enables to subscribe to mouse move events, positionning the iTriggeringOnPreSelection to true.
**Note:** If the scripting language is Visual Basic for Applications or Visual Basic 6 Development Studio, then, you have to know that during the execution of an interactive selection method such as this one, no form (dialog box) must be displayed, otherwise it would lead to unpredictible results. In a form method, before calling an interactive selection method such as Document.Indicate2D, you must hide all forms, and, after the call to the method, you must show the forms.

**Parameters:**

` iMessage`      A string which instructs the user that he must select a location in the document window. This string is displayed in the message area located at the left of the power input area.
` oDocumentWindowLocation`      An array made of 2 doubles: X, Y - coordinates array of the location the user specified in the document window.
` oOutputState`      The state of the indication command once `Indicate2D` returns. It can be either "Normal" (the indication has succeeded), "Cancel" (the user wants to cancel the VB command, which must exit immediately, see the oOutputState parameter of the
[Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method), "Undo" or "Redo". About the use of "Undo" and "Redo", see the example of the [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method.  **Example:**      The following example suppose a drawing document is currently edited. It asks the end user to select a location in the current drawing window, and creates a text (see [DrawingText](../DraftingInterfaces/interface_DrawingText_26559.md) ) at the specified location:

```VBScript
Set Document = CATIA.ActiveDocument : Set Selection = Document.Selection : Set DrawingSheets  = Document.Sheets
Set DrawingSheet = DrawingSheets.ActiveSheet : Set DrawingViews = DrawingSheet.Views
Set DrawingView = DrawingViews.ActiveView : Set DrawingTexts = DrawingView.Texts
'We propose to the user that he specify a location in the drawing window
Dim DrawingWindowLocation(1)
Status=Document.Indicate2D("select a location into the drawing window",DrawingWindowLocation)
if (Status = "Cancel") then Exit Sub
Set DrawingText=DrawingTexts.Add("Hello world",DrawingWindowLocation(0),DrawingWindowLocation(1))

```

### Func **Indicate3D**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPlanarGeometricObject`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMessage`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioWindowLocation2D`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioWindowLocation3D`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Runs an 3D interactive indication command.
**Role** : `Indicate3D` asks to the user to select a location in the document window. It cannot be used:

* When this document is a [DrawingDocument](../DraftingInterfaces/interface_DrawingDocument_48585.md)

* When this document is a [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md), and a sketch is being edited ( [Sketch.OpenEdition](../SketcherInterfaces/interface_Sketch_8026.htm#OpenEdition) has been called and [Sketch.CloseEdition](../SketcherInterfaces/interface_Sketch_8026.htm#CloseEdition) has not been called yet)

In these cases, `Indicate2D` must be used.
**See also:** [Selection.IndicateOrSelectElement3D](../InfInterfaces/interface_Selection_18040.htm#IndicateOrSelectElement3D) which can, in particular, enable indication and not selection (positionning the iFilterType parameter to an empty string), whichs enables to subscribe to mouse move events, positionning the iTriggeringOnPreSelection to true.
**Note:** If the scripting language is Visual Basic for Applications or Visual Basic 6 Development Studio, then, you have to know that during the execution of an interactive selection method such as this one, no form (dialog box) must be displayed, otherwise it would lead to unpredictible results. In a form method, before calling an interactive selection method such as Document.Indicate2D, you must hide all forms, and, after the call to the method, you must show the forms.

**Parameters:**

` iPlanarGeometricObject`      A planar geometric object.
The following objects are supported:
[HybridShapeCircle](../GSMInterfaces/interface_HybridShapeCircle_59719.md), [HybridShapeCircleExplicit](../GSMInterfaces/interface_HybridShapeCircleExplicit_130251.md), [HybridShapeConic](../GSMInterfaces/interface_HybridShapeConic_52888.md), [Sketch](../SketcherInterfaces/interface_Sketch_8026.md), [Circle2D](../SketcherInterfaces/interface_Circle2D_11806.md), [Ellipse2D](../SketcherInterfaces/interface_Ellipse2D_15520.md), [Hyperbola2D](../SketcherInterfaces/interface_Hyperbola2D_23520.md), [Parabola2D](../SketcherInterfaces/interface_Parabola2D_18844.md) and [Spline2D](../SketcherInterfaces/interface_Spline2D_12098.md). ` iMessage`      A string which instructs the user that he must select a location in the document window. This string is displayed in the message area located at the left of the power input area.
` oWindowLocation2D`      An array made of 2 doubles: X, Y - coordinates array of the location the user specified in the document window, in the input planar object coordinates system
` oWindowLocation3D`      An array made of 3 doubles: X, Y, Z - coordinates array of the location the user specified in the document window
` oOutputState`      The state of the indication command once `Indicate3D` returns. It can be either "Normal" (the indication has succeeded), "Cancel" (the user wants to cancel the VB command, which must exit immediately, see the oOutputState parameter of the
[Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method), "Undo" or "Redo". About the use of "Undo" and "Redo", see the example of the [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method.  **Example:**      The following example asks the end user to select a location in the document window, on the Plane.1 plane, and creates a [HybridShapePointOnPlane](../GSMInterfaces/interface_HybridShapePointOnPlane_108958.md) at the specified location:

```VBScript
Set Document = CATIA.ActiveDocument : Set Part  = Document.Part : Set Selection = Document.Selection
Set HybridShapeFactory = Part.HybridShapeFactory
Set HybridShapePlane = Part.Bodies.Item("PartBody").HybridShapes.Item("Plane.1")
Set PlaneReference = Part.CreateReferenceFromObject(HybridShapePlane)
'We propose to the user that he select a location in the window
ReDim WindowLocation2D(1),WindowLocation3D(2)
Status=Document.Indicate3D(HybridShapePlane,"select a location in the document window", _
                            WindowLocation2D,WindowLocation3D)
if (Status = "Cancel") then Exit Sub
Set HybridShapePointOnPlane = HybridShapeFactory.AddNewPointOnPlane( _
                                PlaneReference,WindowLocation2D(0),WindowLocation2D(1))
Part.Bodies.Item("PartBody").InsertHybridShape HybridShapePointOnPlane
Part.InWorkObject = HybridShapePointOnPlane
Part.Update

```

### Func **NewWindow**( ) As [CATIAWindow](../InfInterfaces/interface_Window_8384.md)

Creates a new window for the document. This implies creating a window, displaying the document in this window, making this document the active one if it was not, making this window the active one, and adding the window to the collection of windows.

**Example:**      This example creates the `MyWindow` new window for the `Doc` document.

```VBScript
Dim MyWindow As Window
Set MyWindow = Doc.NewWindow()

```

### Sub **RemoveFilter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilterName`)

Removes an existing visualization filter. Fails if the filter to be removed is the current filter.

**Parameters:**

` iFilterName`      The filter name.  **Example:**      This example removes the filter named "Filter001" for the `Doc` document.

```VBScript
Doc.RemoveFilter ("Filter001")

```

### Sub **Save**( )

Saves the document.

**Example:**      This example saves the `Doc` document.

```VBScript
Doc.Save()

```

### Sub **SaveAs**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`)

Saves the document with another name.

**Parameters:**

` fileName`      The name to assign to the document  **Example:**      This example saves the `Doc` document with the `NewName` name.

```VBScript
Doc.SaveAs("NewName")

```