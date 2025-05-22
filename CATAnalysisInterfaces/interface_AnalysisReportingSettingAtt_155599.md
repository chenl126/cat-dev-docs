# AnalysisReportingSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "ReportingSetting"._**

## Properties

### Property **BackgroundImageMode**( ) As boolean

Returns or sets the BackgroundImageMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomBackgroundImage**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the CustomBackgroundImage parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the CustomImageFormat parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageHeight**( ) As long

Returns or sets the CustomImageHeight parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageWidth**( ) As long

Returns or sets the CustomImageWidth parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageQualityMode**( ) As boolean

Returns or sets the ImageQualityMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **TempOutputDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the TempOutputDirectory parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetBackgroundImageModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the BackgroundImageMode parameter.
**Role** :Retrieves the state of the BackgroundImageMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomBackgroundImageInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the CustomBackgroundImage parameter.
**Role** :Retrieves the state of the CustomBackgroundImage parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the CustomImageFormat parameter.
**Role** :Retrieves the state of the CustomImageFormat parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageHeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the CustomImageHeight parameter.
**Role** :Retrieves the state of the CustomImageHeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the CustomImageWidth parameter.
**Role** :Retrieves the state of the CustomImageWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageQualityModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ImageQualityMode parameter.
**Role** :Retrieves the state of the ImageQualityMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTempOutputDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the TempOutputDirectory parameter.
**Role** :Retrieves the state of the TempOutputDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetBackgroundImageModeLock**( boolean  `iLocked`)

Locks or unlocks the BackgroundImageMode parameter.
**Role** :Locks or unlocks the BackgroundImageMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomBackgroundImageLock**( boolean  `iLocked`)

Locks or unlocks the CustomBackgroundImage parameter.
**Role** :Locks or unlocks the CustomBackgroundImage parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageFormatLock**( boolean  `iLocked`)

Locks or unlocks the CustomImageFormat parameter.
**Role** :Locks or unlocks the CustomImageFormat parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageHeightLock**( boolean  `iLocked`)

Locks or unlocks the CustomImageHeight parameter.
**Role** :Locks or unlocks the ImageHeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageWidthLock**( boolean  `iLocked`)

Locks or unlocks the ImageWidth parameter.
**Role** :Locks or unlocks the ImageWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageQualityModeLock**( boolean  `iLocked`)

Locks or unlocks the ImageQualityMode parameter.
**Role** :Locks or unlocks the DefaultImageQuality parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTempOutputDirectoryLock**( boolean  `iLocked`)

Locks or unlocks the TempOutputDirectory parameter.
**Role** :Locks or unlocks the TempOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.