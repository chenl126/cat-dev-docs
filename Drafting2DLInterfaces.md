# Drafting2DLInterfaces Framework

## Object Index

  * [Layout2DFactory](Drafting2DLInterfaces/interface_Layout2DFactory_46634.md)
  * [Layout2DRoot](Drafting2DLInterfaces/interface_Layout2DRoot_29538.md)
  * [Layout2DSettingAtt](Drafting2DLInterfaces/interface_Layout2DSettingAtt_66620.md)
  * [Layout2DSheet](Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)
  * [Layout2DSheets](Drafting2DLInterfaces/interface_Layout2DSheets_40224.md)
  * [Layout2DView](Drafting2DLInterfaces/interface_Layout2DView_29234.md)
  * [Layout2DViews](Drafting2DLInterfaces/interface_Layout2DViews_34886.md)

## Enumerated Types Index

  * [CatClippingFrameReframeOnMode](Drafting2DLInterfaces/enum_CatClippingFrameReframeOnMode_170229.md)
  * [CatDedicatedFilterType](Drafting2DLInterfaces/enum_CatDedicatedFilterType_100522.md)
  * [CatView2DModeVisu](Drafting2DLInterfaces/enum_CatView2DModeVisu_57639.md)
  * [CatViewBackgroundMode](Drafting2DLInterfaces/enum_CatViewBackgroundMode_91360.md)
  * [CatViewFilterCreationMode](Drafting2DLInterfaces/enum_CatViewFilterCreationMode_129215.md)
  * [CatViewSide](Drafting2DLInterfaces/enum_CatViewSide_25154.md)
  * [CatViewType](Drafting2DLInterfaces/enum_CatViewType_26017.md)
  * [CatVisuBackgroundMode](Drafting2DLInterfaces/enum_CatVisuBackgroundMode_91752.md)
  * [CatVisuIn3DMode](Drafting2DLInterfaces/enum_CatVisuIn3DMode_43112.md)

---

# CatClippingFrameReframeOnMode (Enumeration)

**_At creation of a view the clipping frame is reframed on._**

**Values:**

` catViewContent`      Reframe on view content
` catViewBackground`      Reframe on view background

---

# CatDedicatedFilterType (Enumeration)

**_Specifies if the dedicated filter mask or not the background._**

**Values:**

` catDisplayInBackground`      View is diplayed in background
` catMaskInBackground`      View is masked in background

---

# CatView2DModeVisu (Enumeration)

**_Background 2D Mode values_**

**Values:**

` catView2DModeNotActivated`      2D Mode is not activated in background
` catView2DModeNoShow`      2D Mode is activated for background

---

# CatViewBackgroundMode (Enumeration)

**_The way the background of a view is displayed at creation._**

**Values:**

` catInvisible`      Background not display
` catStandard`      Background pickable and not in low intensity
` catUnpickable`      Background unpickable and not in low intensity
` catLowIntensity`      Background pickable and in low intensity
` catUnpickableLowIntensity`      Background unpickable and in low intensity

---

# CatViewFilterCreationMode (Enumeration)

**_At creation of a view, this enum defines how the filter of this view is configured._**

**Values:**

` catDefaultFilter`      A default filter is used (the first in the list)
` catDedicatedFilter`      A filter is created for the view
` catDisplayFilterDialogBox`      Filter dialog box is displayed after the creation of the view to assign a filter

---

# CatViewSide (Enumeration)

**_CatViewSide is used in conjonction with a reference View2DL and a ViewBox._**
It then determines precisely a View2DL type in the ViewBox. example: with the default ViewBox: \- Front + TopSide = Top. \- Right + LeftSide = Front. \- Front + TRCorner = isometric on the corner near Front, Right, Top.

---

# CatViewType (Enumeration)

**_Type of a view._**

**Values:**

` catAuxiliaryView`      The auxiliary view is a representation of a part regarding to an user defined projection plane
` catSectionView`      The section view is a view of a part which is first sectionned regarding to a user defined profile. The part geometry beside the section plane is visible.
` catSectionCutView`      The section cut view is a view of a part which is first sectionned regarding to a user defined profile. Only the geometry in the section plane is visible.

---

# CatVisuBackgroundMode (Enumeration)

**_Background Visu Mode._**

**Values:**

` catNoBackground`      Hide visu background.
` catPick`      Background is shown and pickable
` catNoPick`      Background is shown and not pickable
` catLowIntPick`      Background is shown in low intensity and pickable
` catLowIntNoPick`      Background is shown in low intensity and not pickable

---

# CatVisuIn3DMode (Enumeration)

**_3D Visu Mode._**

**Values:**

` catShowAll`      Show all geometry and annotation in the 3D Viewer.
` catHideAll`      Hide all geometry and annotation in the 3D Viewer.

---

# Layout2DFactory (Object)

**__**

## Methods

### Func **Create2DLayout**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iStandardName`) As [CATIALayout2DLayout](../Drafting2DLInterfaces/interface_Layout2DRoot_29538.md)

   Create the `2DLayout` associated to the 3D mechanical feature tha implement this interface. E.g. a Mechanical Part.

**Parameters:**

` CATBSTR`      iStandardName The standard name to apply to the new layout.
` oLayout`      The created `2DLayout`. This feature is unique for a given 3D context feature. Consequently requesting this interface on a 3D feature that is already associated to a `2DLayout` feature will fail. You must first request for any existing `2DLayout` via
[AnyObject.GetItem](../System/interface_AnyObject_17321.htm#GetItem) method using `CATLayoutRoot` key parameter to check for `2DLayout` pre-existing feature as follow :

```VBScript
     Dim MyRoot As Layout2DRoot
     Set MyRoot = CATIA.ActiveDocument.Part.GetItem("CATLayoutRoot")
     if MyRoot Is Nothing then
       Dim MyRootFact As Layout2DFactory
       Set MyRootFact = CATIA.ActiveDocument.Part.GetItem("CATLayoutRootFactory")
       Set MyRoot = MyRootFact.Create2DLayout("ISO_3D")
     end if

```

---

# Layout2DRoot (Object)

**_Interface to manage the 2D Layout root._**

## Properties

### Property **ActiveSheet**( ) As [CATIALayout2DSheet](../Drafting2DLInterfaces/interface_Layout2DSheet_34133.md)

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

---

# Layout2DSettingAtt (Object)

**_The interface to access a CATIA2DLSettingAtt._**

## Properties

### Property **Activate2DMode**( ) As boolean

   Returns the Activate2DMode parameter.  
### Property **BackClippingPlane**( ) As boolean

   Returns the BackClippingPlane parameter.  
### Property **ClippingFrame**( ) As boolean

   Returns the ClippingFrame parameter.  
### Property **ClippingFrameReframeOnMode**( ) As [CatClippingFrameReframeOnMode](../Drafting2DLInterfaces/enum_CatClippingFrameReframeOnMode_170229.md)

   Returns the ClippingFrameReframeOnMode parameter.

**Deprecated:**      V5R18  
### Property **ClippingViewOutlineLinetype**( ) As long

   Returns the ClippingViewOutlineLinetype parameter.  
### Property **ClippingViewOutlineThickness**( ) As long

   Returns the ClippingViewOutlineThickness parameter.  
### Property **CreateAssociativeUseEdges**( ) As boolean

   Returns the CreateAssociativeUseEdges parameter.  
### Property **DedicatedFilterType**( ) As [CatDedicatedFilterType](../Drafting2DLInterfaces/enum_CatDedicatedFilterType_100522.md)

   Returns the DedicatedFilterType parameter.  
### Property **DisplayBackAndCuttingPlane**( ) As boolean

   Returns the DisplayBackAndCuttingPlane parameter.  
### Property **DisplayClippingOutline**( ) As boolean

   Returns the DisplayClippingOutline parameter.  
### Property **EditDedicatedFilterDialogBox**( ) As boolean

   Returns the EditDedicatedFilterDialogBox parameter.  
### Property **HideIn3D**( ) As boolean

   Returns the HideIn3D parameter.  
### Property **PropagateHighlight**( ) As boolean

   Returns the PropagateHighlight parameter.  
### Property **ViewBackgroundMode**( ) As [CatViewBackgroundMode](../Drafting2DLInterfaces/enum_CatViewBackgroundMode_91360.md)

   Returns the ViewBackgroundMode parameter.  
### Property **ViewFilterCreationMode**( ) As [CatViewFilterCreationMode](../Drafting2DLInterfaces/enum_CatViewFilterCreationMode_129215.md)

   Returns the ViewFilterCreationMode parameter.  Methods

### Sub **GetActivate2DModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the Activate2DMode parameter.

**Role** :Retrieves the state of the Activate2DMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetBackClippingPlaneInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the BackClippingPlane parameter.

**Role** :Retrieves the state of the BackClippingPlane parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetClippingFrameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the ClippingFrame parameter.

**Role** :Retrieves the state of the ClippingFrame parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetClippingFrameReframeOnModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      V5R18 Retrieves environment informations for the ClippingFrameReframeOnMode parameter.

**Role** :Retrieves the state of the ClippingFrameReframeOnMode parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetClippingViewOutlineColor**( long  `oValueR`,  long  `oValueG`,  long  `oValueB`)

   Returns the ClippingViewOutlineColor parameter.  
### Sub **GetClippingViewOutlineColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the ClippingViewOutlineColor parameter.

**Role** :Retrieves the state of the ClippingViewOutlineColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetClippingViewOutlineLinetypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the ClippingViewOutlineLinetype parameter.

**Role** :Retrieves the state of the ClippingViewOutlineLinetype parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetClippingViewOutlineThicknessInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the ClippingViewOutlineThickness parameter.

**Role** :Retrieves the state of the ClippingViewOutlineThickness parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetCreateAssociativeUseEdgesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the CreateAssociativeUseEdges parameter.

**Role** :Retrieves the state of the CreateAssociativeUseEdges parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDedicatedFilterTypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DedicatedFilterType parameter.

**Role** :Retrieves the state of the DedicatedFilterType parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetDisplayBackAndCuttingPlaneInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the DisplayBackAndCuttingPlane parameter.

**Role** :Retrieves the state of the DisplayBackAndCuttingPlane parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetDisplayClippingOutlineInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the DisplayClippingOutline parameter.

**Role** :Retrieves the state of the DisplayClippingOutline parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetEditDedicatedFilterDialogBoxInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the EditDedicatedFilterDialogBox parameter.

**Role** :Retrieves the state of the EditDedicatedFilterDialogBox parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetHideIn3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the HideIn3D parameter.

**Role** :Retrieves the state of the HideIn3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPropagateHighlightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the PropagateHighlight parameter.

**Role** :Retrieves the state of the PropagateHighlight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetProtectedElementsColor**( long  `oValueR`,  long  `oValueG`,  long  `oValueB`)

   Returns the ProtectedElementsColor parameter.  
### Sub **GetProtectedElementsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

   Retrieves environment informations for the ProtectedElementsColor parameter.

**Role** :Retrieves the state of the ProtectedElementsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewBackgroundModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ViewBackgroundMode parameter.

**Role** :Retrieves the state of the ViewBackgroundMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewFilterCreationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ViewFilterCreationMode parameter.

**Role** :Retrieves the state of the ViewFilterCreationMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetActivate2DModeLock**( boolean  `iLocked`)

   Locks or unlocks the Activate2DMode parameter.

**Role** :Locks or unlocks the Activate2DMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetBackClippingPlaneLock**( boolean  `iLocked`)

   Locks or unlocks the BackClippingPlane parameter.

**Role** :Locks or unlocks the BackClippingPlane parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetClippingFrameLock**( boolean  `iLocked`)

   Locks or unlocks the ClippingFrame parameter.

**Role** :Locks or unlocks the ClippingFrame parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetClippingFrameReframeOnModeLock**( boolean  `iLocked`)

**Deprecated:**      V5R18 Locks or unlocks the ClippingFrameReframeOnMode parameter.

**Role** :Locks or unlocks the ClippingFrameReframeOnMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetClippingViewOutlineColor**( long  `iValueR`,  long  `iValueG`,  long  `iValueB`)

   Sets the ClippingViewOutlineColor parameter.  
### Sub **SetClippingViewOutlineColorLock**( boolean  `iLocked`)

   Locks or unlocks the ClippingViewOutlineColor parameter.

**Role** :Locks or unlocks the ClippingViewOutlineColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetClippingViewOutlineLinetypeLock**( boolean  `iLocked`)

   Locks or unlocks the ClippingViewOutlineLinetype parameter.

**Role** :Locks or unlocks the ClippingViewOutlineLinetype parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetClippingViewOutlineThicknessLock**( boolean  `iLocked`)

   Locks or unlocks the ClippingViewOutlineThickness parameter.

**Role** :Locks or unlocks the ClippingViewOutlineThickness parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCreateAssociativeUseEdgesLock**( boolean  `iLocked`)

   Locks or unlocks the CreateAssociativeUseEdges parameter.

**Role** :Locks or unlocks the CreateAssociativeUseEdges parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDedicatedFilterTypeLock**( boolean  `iLocked`)

   Locks or unlocks the DedicatedFilterType parameter.

**Role** :Locks or unlocks the DedicatedFilterType parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayBackAndCuttingPlaneLock**( boolean  `iLocked`)

   Locks or unlocks the DisplayBackAndCuttingPlane parameter.

**Role** :Locks or unlocks the DisplayBackAndCuttingPlane parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayClippingOutlineLock**( boolean  `iLocked`)

   Locks or unlocks the DisplayClippingOutline parameter.

**Role** :Locks or unlocks the DisplayClippingOutline parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetEditDedicatedFilterDialogBoxLock**( boolean  `iLocked`)

   Locks or unlocks the EditDedicatedFilterDialogBox parameter.

**Role** :Locks or unlocks the EditDedicatedFilterDialogBox parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHideIn3DLock**( boolean  `iLocked`)

   Locks or unlocks the HideIn3D parameter.

**Role** :Locks or unlocks the HideIn3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPropagateHighlightLock**( boolean  `iLocked`)

   Locks or unlocks the PropagateHighlight parameter.

**Role** :Locks or unlocks the PropagateHighlight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetProtectedElementsColor**( long  `iValueR`,  long  `iValueG`,  long  `iValueB`)

   Sets the ProtectedElementsColor parameter.  
### Sub **SetProtectedElementsColorLock**( boolean  `iLocked`)

   Locks or unlocks the ProtectedElementsColor parameter.

**Role** :Locks or unlocks the ProtectedElementsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewBackgroundModeLock**( boolean  `iLocked`)

   Locks or unlocks the ViewBackgroundMode parameter.

**Role** :Locks or unlocks the ViewBackgroundMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewFilterCreationModeLock**( boolean  `iLocked`)

   Locks or unlocks the ViewFilterCreationMode parameter.

**Role** :Locks or unlocks the ViewFilterCreationMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# Layout2DSheet (Object)

**_The interface to access a Layout2D Sheet._**

## Properties

### Property **Orientation**( ) As [CatPaperOrientation](../InfInterfaces/enum_CatPaperOrientation_77334.md)

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

---

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

---

# Layout2DView (Object)

**_The interface to access a Layout2D View._**

## Properties

### Property **Angle**( ) As double

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

---

# Layout2DViews (Collection)

**__**

## Properties

### Property **ActiveView**( ) As [CATIALayout2DView](../Drafting2DLInterfaces/interface_Layout2DView_29234.md) (Read Only)

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