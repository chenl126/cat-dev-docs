# DrawingView (Object)

**_Represents a drawing view in a drawing sheet._**

The drawing view is included in a drawing sheet and contains texts,leaders, dimensions, arrows, pictures, tables, 2D Geometry and 2D component.

**Warning** : This interface is not available with 2D Layout for 3D Design.

## Properties

### Property **Angle**(| ) As double

   Returns or sets the angle of the drawing view. The angle is measured between the axis system of the drawing view and the axis system of the drawing sheet where the drawing view lies. The angle is measured in radians and is counted counterclockwise.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the angle of the `MyView` drawing view to 90 degrees clockwise. You first need to compute the angle in radians and set the minus sign to indicate the rotation is clockwise.

```VBScript
     PI = 3.1415926535
     Angle90Clockwise = -PI/2
     MyView.Angle = Angle90Clockwise

```

### Property **Arrows**( ) As [CATIADrawingArrows](../DraftingInterfaces/interface_DrawingArrows_37200.md) (Read Only)

   Returns the drawing arrow collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `ArrowCollection` the collection of arrows of the `MyView` drawing view.

```VBScript
     Dim ArrowCollection As DrawingArrows
     Set ArrowCollection = MyView.Arrows

```

### Property **Components**( ) As [CATIADrawingComponents](../DraftingInterfaces/interface_DrawingComponents_63152.md) (Read Only)

   Returns the drawing component instances collection (i.e. ditto collection) of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `ComponentCollection` the collection of component instances of the `MyView` drawing view.

```VBScript
     Dim ComponentCollection As DrawingComponents
     Set ComponentCollection = MyView.Components

```

### Property **Dimensions**( ) As [CATIADrawingDimensions](../DraftingInterfaces/interface_DrawingDimensions_62653.md) (Read Only)

   Returns the drawing dimension collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `DimensionCollection` the collection of dimensions of the `MyView` drawing view.

```VBScript
     Dim DimensionCollection As DrawingDimensions
     Set DimensionCollection = MyView.Dimensions

```

### Property **Factory2D**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md) (Read Only)

   Returns the 2D factory of the drawing view. Take care that you must open edition on a sketch before adding or modifying elements in it. Take care that you must close edition on a sketch to keep all modifications before saving document.

**Warning** : This method is not available with 2D Layout for 3D Design. To get Sketch from factory2D:

```VBScript
      Set mySketch = my2DFactory.**GetParent**

```

**Example:**     The following example returns in `my2DFactory` the 2D factory
of the view `myView`:

```VBScript
     Set my2DFactory = myView.**Factory2D**

```

### Property **FrameVisualization**( ) As boolean

   Returns or sets the drawing view frame visualization state.

**True** if the drawing view frame is visible.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example shows the frame of the `MyView` drawing view.

```VBScript
     MyView.FrameVisualization = True

```

### Property **GenerativeBehavior**( ) As [CATIAGenerativeViewBehavior](../DraftingInterfaces/interface_DrawingViewGenerativeBehavior_176715.md) (Read Only)

   Returns the generative behavior of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `MyViewGenBehavior` the generative behavior of the `MyView` drawing view.

```VBScript
     Dim MyViewGenBehavior As DrawingViewGenerativeBehavior
     Set MyViewGenBehavior = MyView.GenerativeBehavior

```

### Property **GenerativeLinks**( ) As [CATIAGenerativeViewLinks](../DraftingInterfaces/interface_DrawingViewGenerativeLinks_142664.md) (Read Only)

   Returns the generative links of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `MyViewGenLinks` the generative links of the `MyView` drawing view.

```VBScript
     Dim MyViewGenLinks As DrawingViewGenerativeLinks
     Set MyViewGenLinks = MyView.GenerativeLinks

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

   Returns the collection of geometric elements included in the drawing view sketch.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**     The following example returns in `colGeometry` the list of geometric elements in the view `myView`:

```VBScript
     Dim colGeometry As GeometricElements
     Set colGeometry = myView.GeometricElements

```

### Property **LockStatus**( ) As boolean

   Returns or sets the lock status of a drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**precondition** : This property does not exist for the detail view. In this case, the method returns failed.

**Example:**      This example locks the `ViewToWorkOn` drawing view.

```VBScript
     ViewToWorkOn.LockStatus = True

```

### Property **Pictures**( ) As [CATIADrawingPictures](../DraftingInterfaces/interface_DrawingPictures_49135.md) (Read Only)

   Returns the drawing picture collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `PictureCollection` the collection of pictures of the `MyView` drawing view.

```VBScript
     Dim PictureCollection As DrawingPictures
     Set PictureCollection = MyView.Pictures

```

### Property **ReferenceView**( ) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)

   Returns or sets the reference view. The reference view is also the parent view to which the current drawing view is linked and which is used as reference for alignment. Generally, the reference view is the front view, and the other views, such as the top, bottom, left, and right views, are linked to it. This reference drawing view is used:

  * When moving the current drawing view. Its location remains constrained to the reference view, depending on its type. For example, a left view can move horizontally and a top view can move vertically.
  * To update the scale of the current drawing view according to the modification performed to the one of the reference drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `ReferenceView` the view used as reference by the `MyView` drawing view.

```VBScript
     Dim ReferenceView As DrawingView
     Set ReferenceView = MyView.RefView

```

### Property **Scale**( ) As double

   Returns or sets the scale of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the scale of the `MyView` drawing view to 0.5.

```VBScript
     MyView.Scale = 0.5

```

### Property **Scale2**( ) As double

   Returns or sets the scale of the drawing view (Workaround for VBA keyword).

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the scale of the `MyView` drawing view to 0.5.

```VBScript
     MyView.Scale2 = 0.5

```

### Property **Tables**( ) As [CATIADrawingTables](../DraftingInterfaces/interface_DrawingTables_35925.md) (Read Only)

   Returns the drawing table collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `TextCollection` the collection of texts of the `MyView` drawing view.

```VBScript
     Dim TableCollection As DrawingTables
     Set TableCollection = MyView.Tables

```

### Property **Texts**( ) As [CATIADrawingTexts](../DraftingInterfaces/interface_DrawingTexts_31836.md) (Read Only)

   Returns the drawing text collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `TextCollection` the collection of texts of the `MyView` drawing view.

```VBScript
     Dim TextCollection As DrawingTexts
     Set TextCollection = MyView.Texts

```

### Property **Threads**( ) As [CATIADrawingThreads](../DraftingInterfaces/interface_DrawingThreads_41838.md) (Read Only)

   Returns the drawing thread collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `ThreadCollection` the collection of threads of the `MyView` drawing view.

```VBScript
     Dim ThreadCollection As DrawingThreads
     Set ThreadCollection = MyView.Threads

```

### Property **ViewType**( ) As [CatDrawingViewType](../DraftingInterfaces/enum_CatDrawingViewType_68508.md) (Read Only)

   Returns the drawing view type.

**Warning** : This method is not available with 2D Layout for 3D Design.  
### Property **Weldings**( ) As [CATIADrawingWeldings](../DraftingInterfaces/interface_DrawingWeldings_48397.md) (Read Only)

   Returns the drawing welding collection of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves in `weldingCollection` the collection of weldings of the `MyView` drawing view.

```VBScript
     Dim weldingCollection As DrawingWeldings
     Set weldingCollection = MyView.Weldings

```

### Property **x**( ) As double

   For an interactive view, get_x and put_x methods are equivalents to get_xAxisData, put_xAxisData In a generative case, get_x. put_x returns or sets the x coordinate of the projection of the 3D centre of gravity. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves the x coordinate of the view relative position `MyView`.

```VBScript
     X = MyView.x

```

### Property **xAxisData**( ) As double

   Returns or sets the x coordinate of the drawing view coordinate system origin. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example retrieves the x coordinate of the coordinate system origin of the `MyView` drawing view.

```VBScript
     X = MyView.xAxisData

```

### Property **y**( ) As double

   For an interactive view, get_y and put_y methods are equivalents to get_yAxisData, put_yAxisData In a generative case, get_y. put_y returns or sets the y coordinate of the projection of the 3D centre of gravity. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the y coordinate of the view relative position `MyView` to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewYCoordinate = 5*25.4
     MyView.y = NewYCoordinate

```

### Property **yAxisData**( ) As double

   Returns or sets the y coordinate of the drawing view coordinate system origin. It is expressed with respect to the sheet coordinate system. This coordinate, like any length, is measured in millimeters.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the y coordinate of the coordinate system origin of the `MyView` drawing view to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewYCoordinate = 5*25.4
     MyView.yAxisData = NewYCoordinate

```

Methods

### Sub **Activate**( )

   Activates the drawing view. Activating a drawing view means that this drawing view is the one on which the end-user is now working.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example activates the `ViewToWorkOn` drawing view.

```VBScript
     ViewToWorkOn.Activate()

```

### Sub **AlignedWithReferenceView**( )

   Activates the alignment with the reference view. Activating the alignment with the reference view restores the constraints that the reference view imposes to the current drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example activates the alignment from the `MyView` drawing view to its reference view.

```VBScript
     MyView.AlignedWithReferenceView()

```

### Sub **GetViewName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNamePrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameIdent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameSuffix`)

   Returns the prefix, the ident and the suffix of the name of the drawing view. The method returns an error in case of 2D component reference.

**Note** : Prefix of drawing view can be also retrieved across name property defined in CATIABase

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example gets the prefix, the ident, and the suffix of the name of the `MyView` drawing view

```VBScript
     Dim MyPrefix, MyIdent, MySuffix As CATBSTR
     MyView.GetViewName (MyPrefix, MyIdent, MySuffix)

```

### Sub **InsertViewAngle**( long  `iFirst`,  [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)  `ioText`)

   Insert the Angle parameter in the text of the drawing text.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iFirst`      The first character from which the parameter is inserted
` ioText`      The text on wich the scale parameter will be inserted  **Example:**      This example insert the Angle parameter of `MyView` drawing view at the end of `MyText` drawing text.

```VBScript

     index = Len(MyText.Text)+1
     MyView.InsertViewScale index, MyText

```

### Sub **InsertViewScale**( long  `iFirst`,  [CATIADrawingText](../DraftingInterfaces/interface_DrawingText_26559.md)  `ioText`)

   Insert the scale parameter in the text of the drawing text.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` iFirst`      The first character from which the parameter is inserted
` ioText`      The text on wich the scale parameter will be inserted  **Example:**      This example insert the Scale parameter of `MyView` drawing view at the first character of `MyText` drawing text.

```VBScript

     MyView.InsertViewScale 1, MyText

```

### Func **IsGenerative**( ) As boolean

   Returns whether the drawing view has a generative behavior.

**Warning** : This method is not available with 2D Layout for 3D Design.

**True** if the drawing view has a generative behavior.

**Example:**      This example retrieves in `GenView` if the `MyView` drawing view has a generative behavior property set.

```VBScript
     GenView = MyView.IsGenerative()

```

### Sub **Isolate**( )

   Isolates the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example isolates the `MyView` drawing view.

```VBScript
     MyView.Isolate

```

### Sub **SaveEdition**( )

   Saves the Sketch Edition. Once you have finished working with the drawing view, you must save its edition in order to register modification for UNDO/REDO. Indeed when activating a view, this view is open in edition while the previous active view is closed in edition. So calling SaveEdition() before exiting a macro without changing active view will allow a correct UNDO/REDO behavior.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**     The following example saves the edition of the drawing view `MyView`:

```VBScript
     MyView.**SaveEdition**

```

### Sub **SetViewName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNamePrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameIdent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iViewNameSuffix`)

   Sets the prefix, the ident and the suffix of the name of the drawing view. The method returns an error in case of 2D component reference.

**Note** : Prefix of drawing view can be also modified across name property defined in CATIABase

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example sets the prefix, the ident, and the suffix of the name of the `MyView` drawing view respectively to "MyPrefix", "MyIdent", and "MySuffix".

```VBScript
     MyView.SetViewName ("MyPrefix", "MyIdent", "MySuffix")

```

### Sub **Size**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oValues`)

   Returns the bounding box of the drawing view.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Parameters:**

` oValues`      The values of the view bounding box: Xmin, Xmax, Ymin, Ymax

**Example:**           This example gets the bounding box of the `ViewToWorkOn` drawing view.

```VBScript
     Dim oXY(4) As Double
     ViewToWorkOn.Size oXY
     Xmin = oXY(0)
     Xmax = oXY(1)
     Ymin = oXY(2)
     Ymax = oXY(3)

```

### Sub **UnAlignedWithReferenceView**( )

   Deactivates the alignment with the reference view. Deactivating the alignment to the reference view removes the constraints that the reference view imposes to the current drawing view. You can then, for example, move and position it freely.

**Warning** : This method is not available with 2D Layout for 3D Design.

**Example:**      This example deactivates the alignment from the `MyView` drawing view to its reference view.

```VBScript
     MyView.UnAlignedWithReferenceView()

```