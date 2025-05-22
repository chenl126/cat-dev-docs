# SectioningSettingAtt (Object)

**_The interface to access a CATIASectioningSettingAtt._**

## Properties

### Property **ClippingMode**( ) As [CatSectionClippingMode](../SpaceAnalysisInterfaces/enum_CatSectionClippingMode_100444.md)

Returns or sets the ClippingMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DisplayCutInWireframe**( ) As boolean

Returns or sets the DisplayCutInWireframe parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridAutoFiltering**( ) As boolean

Returns or sets the GridAutoFiltering parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridAutoResize**( ) As boolean

Returns or sets the GridAutoResize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridHeightStep**( ) As float

Returns or sets the GridHeightStep parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridPositionMode**( ) As [CatGridPositionMode](../SpaceAnalysisInterfaces/enum_CatGridPositionMode_75400.md)

Returns or sets the GridPositionMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridStyle**( ) As [CatSectionGridStyle](../SpaceAnalysisInterfaces/enum_CatSectionGridStyle_76008.md)

Returns or sets the GridStyle parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridWidthStep**( ) As float

Returns or sets the GridWidthStep parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **HidePlane**( ) As boolean

Returns or sets the HidePlane parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **HideResult**( ) As boolean

Returns or sets the HideResult parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlaneNormal**( ) As [CatSectionPlaneNormal](../SpaceAnalysisInterfaces/enum_CatSectionPlaneNormal_91976.md)

Returns or sets the PlaneNormal parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlaneOrigin**( ) As [CatSectionPlaneOrigin](../SpaceAnalysisInterfaces/enum_CatSectionPlaneOrigin_91941.md)

Returns or sets the PlaneOrigin parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SectionFill**( ) As boolean

Returns or sets the SectionFill parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **UpdateResult**( ) As boolean

Returns or sets the UpdateResult parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerAutoOpen**( ) As boolean

Returns or sets the ViewerAutoOpen parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerAutoReframe**( ) As boolean

Returns or sets the ViewerAutoReframe parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerLock2D**( ) As boolean

Returns or sets the ViewerLock2D parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **WindowDefaultHeight**( ) As long

**Role** :Retrieve section window default height if the window open mode is catSecWindow_DefaultSize

**Parameters:**

` oWindowDefaultHeight`
**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  
### Property **WindowDefaultWidth**( ) As long

**Role** :Retrieve section window default width if the window open mode is catSecWindow_DefaultSize

**Parameters:**

` oWindowDefaultWidth`
**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  
### Property **WindowOpenMode**( ) As [CatSecWindowOpenMode](../SpaceAnalysisInterfaces/enum_CatSecWindowOpenMode_82170.md)

**Role** :Retrieve section window open mode

**Parameters:**

` oWindowOpenMode`      **Legal values** :
`catSecWindow_DefaultSize :`Opens the sectioning window(s) with the default size specified in the Tools->Options.
`catSecWindow_TileVertically :`Tiles the sectioning window(s) vertically in the viewer
**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  Methods

### Func **GetClippingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ClippingMode parameter.
**Role** :Retrieves the state of the ClippingMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayCutInWireframeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the DisplayCutInWireframe parameter.
**Role** :Retrieves the state of the DisplayCutInWireframe parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridAutoFilteringInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridAutoFiltering parameter.
**Role** :Retrieves the state of the GridAutoFiltering parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridAutoResizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridAutoResize parameter.
**Role** :Retrieves the state of the GridAutoResize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridHeightStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridHeightStep parameter.
**Role** :Retrieves the state of the GridHeightStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridPositionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridPositionMode parameter.
**Role** :Retrieves the state of the GridPositionMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridStyle parameter.
**Role** :Retrieves the state of the GridStyle parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridWidthStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the GridWidthStep parameter.
**Role** :Retrieves the state of the GridWidthStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHidePlaneInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the HidePlane parameter.
**Role** :Retrieves the state of the HidePlane parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHideResultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the HideResult parameter.
**Role** :Retrieves the state of the HideResult parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPlaneColor**( long  `oR`,  long  `oG`,  long  `oB`)

Returns the PlaneColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Func **GetPlaneColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PlaneColor parameter.
**Role** :Retrieves the state of the PlaneColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlaneNormalInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PlaneNormal parameter.
**Role** :Retrieves the state of the PlaneNormal parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlaneOriginInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PlaneOrigin parameter.
**Role** :Retrieves the state of the PlaneOrigin parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSectionFillInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the SectionFill parameter.
**Role** :Retrieves the state of the SectionFill parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateResultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the UpdateResult parameter.
**Role** :Retrieves the state of the UpdateResult parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerAutoOpenInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ViewerAutoOpen parameter.
**Role** :Retrieves the state of the ViewerAutoOpen parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerAutoReframeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ViewerAutoReframe parameter.
**Role** :Retrieves the state of the ViewerAutoReframe parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerLock2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ViewerLock2D parameter.
**Role** :Retrieves the state of the ViewerLock2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowDefaultHeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the WindowDefaultHeight parameter.
**Role** :Retrieves the state of the WindowDefaultHeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowDefaultWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the WindowDefaultWidth parameter.
**Role** :Retrieves the state of the WindowDefaultWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowOpenModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the WindowOpenMode parameter.
**Role** :Retrieves the state of the WindowOpenMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetClippingModeLock**( boolean  `iLocked`)

Locks or unlocks the ClippingMode parameter.
**Role** :Locks or unlocks the PlaneOrigin parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayCutInWireframeLock**( boolean  `iLocked`)

Locks or unlocks the DisplayCutInWireframe parameter.
**Role** :Locks or unlocks the DisplayCutInWireframe parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridAutoFilteringLock**( boolean  `iLocked`)

Locks or unlocks the GridAutoFiltering parameter.
**Role** :Locks or unlocks the GridAutoFiltering parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridAutoResizeLock**( boolean  `iLocked`)

Locks or unlocks the GridAutoResize parameter.
**Role** :Locks or unlocks the GridAutoResize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridHeightStepLock**( boolean  `iLocked`)

Locks or unlocks the GridHeightStep parameter.
**Role** :Locks or unlocks the GridHeightStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridPositionModeLock**( boolean  `iLocked`)

Locks or unlocks the GridPositionMode parameter.
**Role** :Locks or unlocks the GridPositionMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridStyleLock**( boolean  `iLocked`)

Locks or unlocks the GridStyle parameter.
**Role** :Locks or unlocks the GridStyle parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridWidthStepLock**( boolean  `iLocked`)

Locks or unlocks the GridWidthStep parameter.
**Role** :Locks or unlocks the GridWidthStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHidePlaneLock**( boolean  `iLocked`)

Locks or unlocks the HidePlane parameter.
**Role** :Locks or unlocks the HidePlane parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHideResultLock**( boolean  `iLocked`)

Locks or unlocks the HideResult parameter.
**Role** :Locks or unlocks the HideResult parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneColor**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the PlaneColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Sub **SetPlaneColorLock**( boolean  `iLocked`)

Locks or unlocks the PlaneColor parameter.
**Role** :Locks or unlocks the PlaneColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneNormalLock**( boolean  `iLocked`)

Locks or unlocks the PlaneNormal parameter.
**Role** :Locks or unlocks the PlaneNormal parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneOriginLock**( boolean  `iLocked`)

Locks or unlocks the PlaneOrigin parameter.
**Role** :Locks or unlocks the PlaneOrigin parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSectionFillLock**( boolean  `iLocked`)

Locks or unlocks the SectionFill parameter.
**Role** :Locks or unlocks the SectionFill parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateResultLock**( boolean  `iLocked`)

Locks or unlocks the UpdateResult parameter.
**Role** :Locks or unlocks the UpdateResult parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerAutoOpenLock**( boolean  `iLocked`)

Locks or unlocks the ViewerAutoOpen parameter.
**Role** :Locks or unlocks the ViewerAutoOpen parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerAutoReframeLock**( boolean  `iLocked`)

Locks or unlocks the ViewerAutoReframe parameter.
**Role** :Locks or unlocks the ViewerAutoReframe parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerLock2DLock**( boolean  `iLocked`)

Locks or unlocks the ViewerLock2D parameter.
**Role** :Locks or unlocks the ViewerLock2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowDefaultHeightLock**( boolean  `iLocked`)

Locks or unlocks the WindowDefaultHeight parameter.
**Role** :Locks or unlocks the WindowDefaultHeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowDefaultWidthLock**( boolean  `iLocked`)

Locks or unlocks the WindowDefaultWidth parameter.
**Role** :Locks or unlocks the WindowDefaultWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowOpenModeLock**( boolean  `iLocked`)

Locks or unlocks the WindowOpenMode parameter.
**Role** :Locks or unlocks the WindowOpenMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.