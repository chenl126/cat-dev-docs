# Layout2DSettingAtt (Object)

**_The interface to access a CATIA2DLSettingAtt._**

## Properties

### Property **Activate2DMode**(| ) As boolean

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