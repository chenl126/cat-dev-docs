# Layout2DView (Object)

**_The interface to access a Layout2D View._**

## Properties

### Property **Angle**(| ) As double

   Returns or sets the angle of the Layout2D view. The angle is measured between the axis system of the Layout2D view and the axis system of the Layout2D sheet where the Layout2D view lies. The angle is measured in radians and is counted counterclockwise.

**Example:**      This example sets the angle of the `MyView` Layout2D view to 90 degrees clockwise. You first need to compute the angle in radians and set the minus sign to indicate the rotation is clockwise.

```VBScript
     PI = 3.1415926535
     Angle90Clockwise = -PI/2
     MyView.Angle = Angle90Clockwise

```

### Property **Arrows**( ) As [CATIADrawingArrows](../DraftingInterfaces/interface_DrawingArrows_37200.md) (Read Only)

   Returns the drawing arrow collection of the Layout2D view.

**Example:**      This example retrieves in `ArrowCollection` the collection of arrows of the `MyView` Layout2D view.

```VBScript
     Dim ArrowCollection As DrawingArrows
     Set ArrowCollection = MyView.Arrows

```

### Property **Components**( ) As [CATIADrawingComponents](../DraftingInterfaces/interface_DrawingComponents_63152.md) (Read Only)

   Returns the Layout2D component instances collection (i.e. ditto collection) of the Layout2D view.

**Example:**      This example retrieves in `ComponentCollection` the collection of component instances of the `MyView` Layout2D view.

```VBScript
     Dim ComponentCollection As DrawingComponents
     Set ComponentCollection = MyView.Components

```

### Property **Dimensions**( ) As [CATIADrawingDimensions](../DraftingInterfaces/interface_DrawingDimensions_62653.md) (Read Only)

   Returns the drawing dimension collection of the Layout2D view.

**Example:**      This example retrieves in `DimensionCollection` the collection of dimensions of the `MyView` Layout2D view.

```VBScript
     Dim DimensionCollection As DrawingDimensions
     Set DimensionCollection = MyView.Dimensions

```

### Property **Factory2D**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md) (Read Only)

   Returns the 2D factory of the Layout2D view. Take care that you must open edition on a sketch before adding or modifying elements in it. Take care that you must close edition on a sketch to keep all modifications before saving document. To get Sketch from factory2D:

```VBScript
      Set mySketch = my2DFactory.**GetParent**

```

**Example:**     The following example returns in `my2DFactory` the 2D factory
of the view `myView`:

```VBScript
     Set my2DFactory = myView.**Factory2D**

```

### Property **FrameVisualization**( ) As boolean

   Returns or sets the Layout2D view frame visualization state.

**True** if the Layout2D view frame is visible.

**Example:**      This example shows the frame of the `MyView` Layout2D view.

```VBScript
     MyView.FrameVisualization = True

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

   Returns the collection of geometric elements included in the Layout2D view sketch.

**Example:**     The following example returns in `colGeometry` the list of geometric elements in the view `myView`:

```VBScript
     Dim colGeometry As GeometricElements
     Set colGeometry = MyView.GeometricElements

```

### Property **LockStatus**( ) As boolean

   Returns or sets the lock status of a Layout2D view.

**precondition** : This property does not exist for the detail view. In this case, the method returns failed.

**Example:**      This example locks the `ViewToWorkOn` Layout2D view.

```VBScript
     ViewToWorkOn.LockStatus = True

```

### Property **Pictures**( ) As [CATIADrawingPictures](../DraftingInterfaces/interface_DrawingPictures_49135.md) (Read Only)

   Returns the drawing picture collection of the Layout2D view.

**Example:**      This example retrieves in `PictureCollection` the collection of pictures of the `MyView` Layout2D view.

```VBScript
     Dim PictureCollection As DrawingPictures
     Set PictureCollection = MyView.Pictures

```

### Property **ReferenceView**( ) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Returns or sets the reference view. The reference view is also the parent view to which the current Layout2D view is linked and which is used as reference for alignment. Generally, the reference view is the front view, and the other views, such as the top, bottom, left, and right views, are linked to it. This reference Layout2D view is used:

  * When moving the current Layout2D view. Its location remains constrained to the reference view, depending on its type. For example, a left view can move horizontally and a top view can move vertically.
  * To update the scale of the current Layout2D view according to the modification performed to the one of the reference Layout2D view.

**Example:**      This example retrieves in `ReferenceView` the view used as reference by the `MyView` Layout2D view.

```VBScript
     Dim ReferenceView As Layout2DView
     Set ReferenceView = MyView.RefView

```

### Property **Tables**( ) As [CATIADrawingTables](../DraftingInterfaces/interface_DrawingTables_35925.md) (Read Only)

   Returns the drawing table collection of the drawing view.

**Example:**      This example retrieves in `TextCollection` the collection of texts of the `MyView` Layout2D view.

```VBScript
     Dim TableCollection As DrawingTables
     Set TableCollection = MyView.Tables

```

### Property **Texts**( ) As [CATIADrawingTexts](../DraftingInterfaces/interface_DrawingTexts_31836.md) (Read Only)

   Returns the drawing text collection of the Layout2D view.

**Example:**      This example retrieves in `TextCollection` the collection of texts of the `MyView` Layout2D view.

```VBScript
     Dim TextCollection As DrawingTexts
     Set TextCollection = MyView.Texts

```

### Property **Threads**( ) As [CATIADrawingThreads](../DraftingInterfaces/interface_DrawingThreads_41838.md) (Read Only)

   Returns the drawing thread collection of the Layout2D view.

**Example:**      This example retrieves in `ThreadCollection` the collection of threads of the `MyView` Layout2D view.

```VBScript
     Dim ThreadCollection As DrawingThreads
     Set ThreadCollection = MyView.Threads

```

### Property **ViewScale**( ) As double

   Returns or sets the scale of the Layout2D view.

**Example:**      This example sets the scale of the `MyView` Layout2D view to 0.5.

```VBScript
     MyView.Scale = 0.5

```

### Property **Visu2DMode**( ) As [CatView2DModeVisu](../Drafting2DLInterfaces/enum_CatView2DModeVisu_57639.md)

   Sets/Gets the 2D mode for background visualization of the view.

**See also:**      [CatView2DModeVisu](../Drafting2DLInterfaces/enum_CatView2DModeVisu_57639.md) **Example:**           This example shows how to switch on the background 2D mode

```VBScript
     View1.Visu2DMode = catView2DModeNoShow

```

### Property **VisuBackground**( ) As [CatVisuBackgroundMode](../Drafting2DLInterfaces/enum_CatVisuBackgroundMode_91752.md)

   Sets/Gets the 2D-3D background visu mode of the view ie in the 3D windows and in the background of each view in every 2D context.

**See also:**      [CatVisuBackgroundMode](../Drafting2DLInterfaces/enum_CatVisuBackgroundMode_91752.md) **Example:**           This example shows how to set the background to LowInt

```VBScript
     View1.VisuBackground = catLowIntPick

```

### Property **VisuIn3D**( ) As [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md)

   Sets/Gets the 3D visualization mode of the view in the 3D Viewer ie in the 3D windows and in the background of each view in every 2D context.

**See also:**      [CatVisuIn3DMode](../Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md) **Example:**           This example shows how to make the `View1` Layout2D view visible in 3D

```VBScript
     View1.HideIn3DSize = catShowAll

```

### Property **Weldings**( ) As [CATIADrawingWeldings](../DraftingInterfaces/interface_DrawingWeldings_48397.md) (Read Only)

   Returns the drawing welding collection of the Layout2D view.

**Example:**      This example retrieves in `weldingCollection` the collection of weldings of the `MyView` Layout2D view.

```VBScript
     Dim weldingCollection As DrawingWeldings
     Set weldingCollection = MyView.Weldings

```

### Property **x**( ) As double

   Returns or sets the x coordinate of the Layout2D view coordinate system origin. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example retrieves the x coordinate of the coordinate system origin of the `MyView`.

```VBScript
     X = MyView.x

```

### Property **y**( ) As double

   Returns or sets the y coordinate of the Layout2D view coordinate system origin. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the y coordinate of the coordinate system origin of the `MyView` to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewYCoordinate = 5*25.4
     MyView.y = NewYCoordinate

```

Methods

### Sub **Activate**( )

   Activates the Layout2D view. Activating a Layout2D view means that this Layout2D view is the one on which the end-user is now working.

**Example:**      This example activates the `ViewToWorkOn` Layout2D view.

```VBScript
     ViewToWorkOn.Activate()

```

### Sub **AlignedWithReferenceView**( )

   Activates the alignment with the reference view. Activating the alignment with the reference view restores the constraints that the reference view imposes to the current Layout2D view.

**Example:**      This example activates the alignment from the `MyView` Layout2D view to its reference view.

```VBScript
     MyView.AlignedWithReferenceView()

```

### Sub **GetViewName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNamePrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameIdent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameSuffix`)

   Returns the prefix, the ident and the suffix of the name of the Layout2D view. The method returns an error in case of 2D component reference. Do not confuse with the method Name which can be different.

**Example:**      This example gets the prefix, the ident, and the suffix of the name of the `MyView` Layout2D view

```VBScript
     Dim MyPrefix, MyIdent, MySuffix As CATBSTR
     MyView.GetViewName (MyPrefix, MyIdent, MySuffix)

```

### Sub **SaveEdition**( )

   Saves the Sketch Edition. Once you have finished working with the Layout2D view, you must save its edition in order to register modification for UNDO/REDO. Indeed when activating a view, this view is open in edition while the previous active view is closed in edition. So calling SaveEdition() before exiting a macro without changing active view will allow a correct UNDO/REDO behavior.

**Example:**     The following example saves the edition of the Layout2D view `MyView`:

```VBScript
     MyView.**SaveEdition**

```

### Sub **SetViewName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNamePrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameIdent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameSuffix`)

   Sets the prefix, the ident and the suffix of the name of the Layout2D view. The method returns an error in case of 2D component reference. Do not confuse with the method Name which can be different.

**Example:**      This example sets the prefix, the ident, and the suffix of the name of the `MyView` Layout2D view respectively to "MyPrefix", "MyIdent", and "MySuffix".

```VBScript
     MyView.SetViewName ("MyPrefix", "MyIdent", "MySuffix")

```

### Sub **Size**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oValues`)

   Returns the bounding box of the Layout2D view.

**Warning** : This method is not implemented.

**Parameters:**

` oValues`      The values of the view bounding box: Xmin, Xmax, Ymin, Ymax

**Example:**           This example gets the bounding box of the `ViewToWorkOn` Layout2D view.

```VBScript
     Dim oXY(4) As Double
     ViewToWorkOn.Size oXY
     Xmin = oXY(0)
     Xmax = oXY(1)
     Ymin = oXY(2)
     Ymax = oXY(3)

```

### Sub **UnAlignedWithReferenceView**( )

   Deactivates the alignment with the reference view. Deactivating the alignment to the reference view removes the constraints that the reference view imposes to the current Layout2D view. You can then, for example, move and position it freely.

**Example:**      This example deactivates the alignment from the `MyView` Layout2D view to its reference view.

```VBScript
     MyView.UnAlignedWithReferenceView()

```