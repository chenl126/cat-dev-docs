# Layout2DViews (Collection)

**__**

## Properties

### Property **ActiveView**(| ) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md) (Read Only)

   Returns the active Layout2D view of the active Layout2D sheet.

**Example:**      The following example retrieves in `ViewToWorkIn` the active Layout2D view in the Layout2DSheets collection of the layoutRoot

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")
     Dim ViewToWorkIn As Layout2DView
     Set ViewToWorkIn = MyRoot.Sheets.ActiveSheet.Layout2DViews.ActiveView

```

Methods

### Func **AddAuxiliary**( [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)  `iReferenceView`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iBCSegment`,  double  `iXorient`,  double  `iYorient`,  [CatViewType](../Drafting2DLInterfaces/enum_CatViewType_26017.md)  `iSectionType`,  double  `iX`,  double  `iY`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Creates a section or section-cut or auxiliary View2DL from a given Layout View2DL. The View2DL must be in this collection. Caracteristics of new view (view plane etc) are computed based on the given basic callout and reference view 2DL viewplane.

**Precondition** : 1/ The reference View2DL must be in this collection

**Precondition** : 2/ The reference View2DL must be a projection view.

**Precondition** : 3/ The callout segment's length must not be 0.

**Precondition** : 4/ iViewType must be either auxiliary or section or section cut.

**Parameters:**

` iReferenceView`      [in] The reference view. Must be a projection View.
` iBCSegment`      [in] The callout's segment gives the trace of the auxiliary View2DL's projection plane in the reference View2DL. It has the following contents:

`iBCSegment[0] = X1`     x coordinate of the first point `iBCSegment[1] = Y1`     y coordinate of the first point `iBCSegment[2] = X2`     x coordinate of the second point `iBCSegment[3] = Y2`     y coordinate of the second point
` iBCOrient`      [in] The callout's orientation gives the direction taken into account when Layout2D the auxilliary View2DL.
` iXorient`      [in]
` iYorient`      [in] This point determine the type taken into account when Layout2D the auxilliary View2DL.
` iSectionType`
` iX`      [in]
` iY`      [in] The coordinate in the Sheet2DL for the new View2DL.

**Returns:**      The created Layout2D view  **Example:**      The following example creates a Layout2D view named from the active view and retrieved in `MyView` in the Layout2D view collection of the `MySheet` Layout2D sheet. This sheet belongs to the Layout2D sheet collection of the layoutRoot

```VBScript
     Dim x As double
     Set x = 10.
     Dim y As double
     Set y = 10.
     Dim MySegment
     ReDim MySegment(3)
         MySegment(0) = 10.
         MySegment(1) = 200.
         MySegment(2) = 100.
         MySegment(3) = 200.
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")

     Dim MyFirstView As Layout2DView
     Set MyFirstView = MyRoot.Sheets.ActiveSheet.Views.ActiveView
     Dim MyView As Layout2DView
     Set MyView = MyRoot.Sheets.ActiveSheet.Views.

```

### Func **AddDetail**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDetailName`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Creates a detail view and adds it to the layout view collection. This layout view becomes the active one.

**Precondition** : The collection view must be a Detail Sheet

**Parameters:**

` iDetailName`      The name to assign to the created layout view

**Returns:**      The created layout view  **Example:**      The following example creates a detail view named `Ditto` and retrieved in `MyView` in the layout view collection of the `MyDetailSheet` layout sheet. Where `MyDetailSheet` is the active sheet of the layout sheet collection of the layout root

```VBScript
     Dim MyLayoutRoot As Layout2DRoot
     Set MyLayoutRoot = CATIA.Documents.Part.GetItem("CATLayoutRoot")
     Dim MyDetailSheet As Layout2DSheet
     Set MyDetailSheet = .Sheets.ActiveSheet
     Dim MyView As Layout2DView
     Set MyView = MyDetailSheet.Views.AddDetail("Ditto")

```

Dim MyView As Layout2DView Set MyView = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet. Views.AddDetail()  
### Func **AddFrom3DPlane**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPlane`,  [CatViewType](../Drafting2DLInterfaces/enum_CatViewType_26017.md)  `iViewType`,  double  `iX`,  double  `iY`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Creates a viewFrom3D View2DL with the given 3Dplane as its view plane at the given position in the given Sheet2DL.

**Parameters:**

` iPlane`      [in] Define the plane on wich the view as to be created It has the following contents:

`iPlane[0] = X `     x coordinate of plane origin in 3D space `iPlane[1] = Y `     y coordinate of plane origin in 3D space `iPlane[2] = Z `     z coordinate of plane origin in 3D space `iPlane[3] = H1`     Define the direction which the view's viewplane H `iPlane[4] = H2`     axis has to be colinear with `iPlane[5] = H3`      `iPlane[6] = V1`     Define the direction which the view's viewplane V `iPlane[7] = V2`     axis has to be colinear with `iPlane[8] = V3`

**Precondition** : 1/iViewType must be either auxiliary or section or section cut.

**Precondition** : 2/ iFirstDirection and iSecondDirection must be orthogonal.
` iViewType`      The view type: `catAuxiliary` or `catSectionCut` or `catSectionView`
` iX`      [in]
` iY`      [in] The coordinate of the new View2DL in the Sheet2DL

**Returns:**      The created Layout2D view  
### Func **AddPrimary**( double  `iX`,  double  `iY`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Creates a Layout view and adds it to the Layout view collection. This Layout view becomes the active one.

**Parameters:**

` iX`      [in]
` iY`      [in] The coordinate in the Sheet2DL for the new View2DL.

**Returns:**      The created Layout2D view  **Example:**      The following example creates a Layout2D view and retrieved in `MyView` in the Layout2D view collection of the Layout2D sheet. This sheet belongs to the Layout2D sheet collection.

```VBScript
     Dim x as double
     Set x = 10.
     Dim y as double
     Set y = 10.
     Dim MyView As Layout2DView
     Set MyView = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet.
                  Views.AddPrimary(x, y).

```

### Func **AddRelated**( [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)  `iReferenceView`,  [CatViewSide](../Drafting2DLInterfaces/enum_CatViewSide_25154.md)  `iSide`,  double  `iX`,  double  `iY`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Creates a projection or isometric Layout View2DL from a given View2DL. The view will be created in the same collection as the given View2DL, at the given position. The caracteristics (ex: view plane etc) of this new View2DL are computed based on the caracteristics stored in the ViewBox its `iReferenceView` is associated with.

**Parameters:**

` iReferenceView`      [in] The reference View2DL from which the new View2DL is created.
` iSide`      [in] Used with the ViewBox and iReferenceView to give the related view to create (type etc).
` iX`      [in]
` iY`      [in] The coordinate in the Sheet2DL for the new View2DL.

**Returns:**      The created Layout2D view

**Precondition** : The reference View2DL must be in this collection  **Example:**      The following example creates a Layout2D view named from the active view and retrieved in `MyView` in the Layout2D view collection of the `MySheet` Layout2D sheet. This sheet belongs to the Layout2D sheet collection of the layoutRoot.

```VBScript
     Dim x as double
     Set x = 10.
     Dim y as double
     Set y = 10.
     Dim MyFirstView As Layout2DView
     Set MyFirstView = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet.Views.ActiveView
     Dim MyView As Layout2DView
     Set MyView = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet.Views.
                  AddRelated(MyFirstView,catLeftSide, x, y)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md)

   Returns a Layout2D view using its index or its name from the Layout2DViews collection.

**Parameters:**

` iIndex`      The index or the name of the Layout2D view to retrieve from the collection of Layout2D views. As a numerics, this index is the rank of the Layout2D view in the collection. The index of the first Layout2D view in the collection is 1, and the index of the last Layout2D view is Count. As a string, it is the name you assigned to the Layout2D view using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved Layout2D view  **Example:**      This example retrieves in `ThisLayout2DView` the second Layout2D view, and in `ThatLayout2DView` the Layout2D view named `MyView` in the Layout2D view collection of the active sheet of a layoutRoot of a part of the active document, supposed to be a part document.

```VBScript
     Dim MySheet As Layout2DSheet
     Set MySheet = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet
     Dim ThisLayout2DView As Layout2DView
     Set ThisLayout2DView = MySheet.Views.ActiveView.Item(2)
     Dim ThatLayout2DView As Layout2DView
     Set ThatLayout2DView = MySheet.Views.ActiveView.Item("MyView")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a layout2D view from the Layout2DViews collection.

**Parameters:**

` iIndex`      The index or the name of the Layout2D view to remove from the collection of Layout2D views. As a numerics, this index is the rank of the Layout2D view in the collection. The index of the first Layout2D view in the collection is 1, and the index of the last Layout2D view is Count. As a string, it is the name you assigned to the Layout2D view using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Example:**      The following example removes the third Layout2D view and the Layout2D view named `TopView` in the Layout2D view collection of the active sheet of a layoutRoot of a part of the active document, supposed to be a part document.

```VBScript
     Dim MySheet As Layout2DSheet
     Set MySheet = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot").Sheets.ActiveSheet
     MySheet.ActiveViews.Remove(3)
     MySheet.ActiveViews.Remove("TopView")

```