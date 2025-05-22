# DraftingSettingAtt (Object)

**_Manages drafting settings._**

## Properties

### Property **CreateNewSheetFrom**( ) As [CatDrwNewSheetFrom](../DraftingInterfaces/enum_CatDrwNewSheetFrom_67056.md)

Returns the CreateNewSheetFrom parameter.  
### Property **DisplayResetButton**( ) As boolean

Returns the DisplayResetButton parameter.  
### Property **LockUserDefault**( ) As boolean

Returns the LockUserDefault parameter.  
### Property **PreventBackgroundAccess**( ) As boolean

Returns the PreventBackgroundAccess parameter.  
### Property **PreventDimDriving3DCstr**( ) As boolean

Returns the PreventDimDriving3DCstr parameter.  
### Property **PreventFileNew**( ) As boolean

Returns the PreventFileNew parameter.  
### Property **PreventGenViewStyle**( ) As boolean

Returns the PreventGenViewStyle parameter.  
### Property **PreventSetAsDefault**( ) As boolean

Returns the PreventSetAsDefault parameter.  
### Property **PreventSwitchStandard**( ) As boolean

Returns the PreventSwitchStandard parameter.  
### Property **PreventTrueDimensionCreation**( ) As boolean

Returns the PreventTrueDimensionCreation parameter.  
### Property **PreventUpdateStandard**( ) As boolean

Returns the PreventUpdateStandard parameter.  
### Property **UseStyleCreateObjects**( ) As boolean

Returns the UseStyleCreateObjects parameter.  Methods

### Func **GetCreateNewSheetFromInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the CreateNewSheetFrom parameter.
**Role** :Retrieves the state of the CreateNewSheetFrom parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayResetButtonInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the DisplayResetButton parameter.
**Role** :Retrieves the state of the DisplayResetButton parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLockUserDefaultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the LockUserDefault parameter.
**Role** :Retrieves the state of the LockUserDefault parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventBackgroundAccessInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventBackgroundAccess parameter.
**Role** :Retrieves the state of the PreventBackgroundAccess parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventDimDriving3DCstrInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventDimDriving3DCstr parameter.
**Role** :Retrieves the state of the PreventDimDriving3DCstr parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPreventFileNewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`,  boolean  `oModified`)

Retrieves environment informations for the PreventFileNew parameter.
**Role** :Retrieves the state of the PreventFileNew parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventGenViewStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventGenViewStyle parameter.
**Role** :Retrieves the state of the PreventGenViewStyle parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventSetAsDefaultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventSetAsDefault parameter.
**Role** :Retrieves the state of the PreventSetAsDefault parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventSwitchStandardInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventSwitchStandard parameter.
**Role** :Retrieves the state of the PreventSwitchStandard parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventTrueDimensionCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventTrueDimensionCreation parameter.
**Role** :Retrieves the state of the PreventTrueDimensionCreation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPreventUpdateStandardInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PreventUpdateStandard parameter.
**Role** :Retrieves the state of the PreventUpdateStandard parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUseStyleCreateObjectsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the UseStyleCreateObjects parameter.
**Role** :Retrieves the state of the UseStyleCreateObjects parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetCreateNewSheetFromLock**( boolean  `iLocked`)

Locks or unlocks the CreateNewSheetFrom parameter.
**Role** :Locks or unlocks the CreateNewSheetFrom parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayResetButtonLock**( boolean  `iLocked`)

Locks or unlocks the DisplayResetButton parameter.
**Role** :Locks or unlocks the DisplayResetButton parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLockUserDefaultLock**( boolean  `iLocked`)

Locks or unlocks the LockUserDefault parameter.
**Role** :Locks or unlocks the LockUserDefault parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventBackgroundAccessLock**( boolean  `iLocked`)

Locks or unlocks the PreventBackgroundAccess parameter.
**Role** :Locks or unlocks the PreventBackgroundAccess parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventDimDriving3DCstrLock**( boolean  `iLocked`)

Locks or unlocks the PreventDimDriving3DCstr parameter.
**Role** :Locks or unlocks the PreventDimDriving3DCstr parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventFileNewLock**( boolean  `iLocked`)

Locks or unlocks the PreventFileNew parameter.
**Role** :Locks or unlocks the PreventFileNew parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventGenViewStyleLock**( boolean  `iLocked`)

Locks or unlocks the PreventGenViewStyle parameter.
**Role** :Locks or unlocks the PreventGenViewStyle parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventSetAsDefaultLock**( boolean  `iLocked`)

Locks or unlocks the PreventSetAsDefault parameter.
**Role** :Locks or unlocks the PreventSetAsDefault parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventSwitchStandardLock**( boolean  `iLocked`)

Locks or unlocks the PreventSwitchStandard parameter.
**Role** :Locks or unlocks the PreventSwitchStandard parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventTrueDimensionCreationLock**( boolean  `iLocked`)

Locks or unlocks the PreventTrueDimensionCreation parameter.
**Role** :Locks or unlocks the PreventTrueDimensionCreation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPreventUpdateStandardLock**( boolean  `iLocked`)

Locks or unlocks the PreventUpdateStandard parameter.
**Role** :Locks or unlocks the PreventUpdateStandard parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUseStyleCreateObjectsLock**( boolean  `iLocked`)

Locks or unlocks the UseStyleCreateObjects parameter.
**Role** :Locks or unlocks the UseStyleCreateObjects parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.