# RenderingSettingAtt (Object)

**_The interface to access a CATIARenderingSettingAtt._**

## Properties

### Property **EngineInterface**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the EngineInterface parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **OutputHeight**( ) As short

Returns or sets the OutputHeight parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **OutputPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the OutputPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **OutputSizeFrom**( ) As short

Returns or sets the OutputSizeFrom parameter.  Ensure consistency with the C++ interface to which the work is delegated.

**Parameters:**

` OutputSizeFrom`      where to get the image size for a QuickRender. **Legal values** :
`1 :` same size as viewpoint.
`2 :` fixed size. Ensure consistency with the C++ interface to which the work is delegated.

### Property **OutputType**( ) As short

Returns or sets the OutputType parameter.  Ensure consistency with the C++ interface to which the work is delegated.

**Parameters:**

` OutputType`      where to save the image after a QuickRender. **Legal values** :
`1 :` image saved to default file.
`2 :` save image to specific file.

### Property **OutputWidth**( ) As short

Returns or sets the OutputWidth parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SaveAutoIncrement**( ) As boolean

Returns or sets the SaveAutoIncrement parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetEngineInterfaceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the EngineInterface parameter.
**Role** :Retrieves the state of the EngineInterface parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputHeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the OutputHeight parameter.
**Role** :Retrieves the state of the OutputHeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the OutputPath parameter.
**Role** :Retrieves the state of the OutputPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputSizeFromInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the OutputSizeFrom parameter.
**Role** :Retrieves the state of the OutputSizeFrom parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputTypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the OutputType parameter.
**Role** :Retrieves the state of the OutputType parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the OutputWidth parameter.
**Role** :Retrieves the state of the OutputWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSaveAutoIncrementInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the SaveAutoIncrement parameter.
**Role** :Retrieves the state of the SaveAutoIncrement parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetEngineInterfaceLock**( boolean  `iLocked`)

Locks or unlocks the EngineInterface parameter.
**Role** :Locks or unlocks the EngineInterface parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputHeightLock**( boolean  `iLocked`)

Locks or unlocks the OutputHeight parameter.
**Role** :Locks or unlocks the OutputHeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputPathLock**( boolean  `iLocked`)

Locks or unlocks the OutputPath parameter.
**Role** :Locks or unlocks the OutputPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputSizeFromLock**( boolean  `iLocked`)

Locks or unlocks the OutputSizeFrom parameter.
**Role** :Locks or unlocks the OutputSizeFrom parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputTypeLock**( boolean  `iLocked`)

Locks or unlocks the OutputType parameter.
**Role** :Locks or unlocks the OutputType parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputWidthLock**( boolean  `iLocked`)

Locks or unlocks the OutputWidth parameter.
**Role** :Locks or unlocks the OutputWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSaveAutoIncrementLock**( boolean  `iLocked`)

Locks or unlocks the SaveAutoIncrement parameter.
**Role** :Locks or unlocks the SaveAutoIncrement parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.