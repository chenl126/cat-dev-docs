# AnalysisPostProSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "PostProcessingSetting"._**

## Properties

### Property **AutoPreviewMode**(| ) As boolean

   Returns or sets the AutoPreviewMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageTextSize**( ) As float

   Returns or sets the ImageTextSize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageTextStacking**( ) As long

   Returns or sets the ImageTextStacking parameter.

**Parameters:**

` iImageTextStacking`      **Legal values** :
`0 :` Text stacking is Horizontal
`1 :` Text stacking is Vertical Ensure consistency with the C++ interface to which the work is delegated.

### Property **ModeImageTextSize**( ) As boolean

   Returns or sets the ModeImageTextSize parameter.

**Parameters:**

` iModeImageTextSize`      **Legal values** :
`TRUE :` Enables the setting of image text size
`FALSE:` Disables the setting of image text size Ensure consistency with the C++ interface to which the work is delegated.

### Property **SaveAsNewTemplateDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the SaveAsNewTemplateDirectory parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetAutoPreviewModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AutoPreviewMode parameter.

**Role** :Retrieves the state of the AutoPreviewMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageTextSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ImageTextSize parameter.

**Role** :Retrieves the state of the ImageTextSize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageTextStackingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ImageTextStacking parameter.

**Role** :Retrieves the state of the ImageTextStacking parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetModeImageTextSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ModeImageTextSize parameter.

**Role** :Retrieves the state of the ModeImageTextSize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSaveAsNewTemplateDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SaveAsNewTemplateDirectory parameter.

**Role** :Retrieves the state of the SaveAsNewTemplateDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAutoPreviewModeLock**( boolean  `iLocked`)

   Locks or unlocks the AutoPreviewMode parameter.

**Role** :Locks or unlocks the AutoPreviewMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageTextSizeLock**( boolean  `iLocked`)

   Locks or unlocks the ImageTextSize parameter.

**Role** :Locks or unlocks the ImageTextSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageTextStackingLock**( boolean  `iLocked`)

   Locks or unlocks the ImageTextStacking parameter.

**Role** :Locks or unlocks the ImageTextStacking parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetModeImageTextSizeLock**( boolean  `iLocked`)

   Locks or unlocks the ModeImageTextSize parameter.

**Role** :Locks or unlocks the ModeImageTextSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSaveAsNewTemplateDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the SaveAsNewTemplateDirectory parameter.

**Role** :Locks or unlocks the Xxx parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.