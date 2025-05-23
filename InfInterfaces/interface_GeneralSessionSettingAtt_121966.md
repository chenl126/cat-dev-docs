# GeneralSessionSettingAtt (Object)

**_Setting controller for the General property tab page._**

**Role** : This interface is implemented by a component which represents the controller of the general settings.

## Properties

### Property **AutoSave**(| ) As [CATGenDataSave](../InfInterfaces/enum_CATGenDataSave_38228.md)

   Returns the data save parameter.  
### Property **Conferencing**( ) As [CATGenConferencing](../InfInterfaces/enum_CATGenConferencing_66130.md)

   Returns the conference driver parameter.  
### Property **DragDrop**( ) As boolean

   Returns the drag & drop parameter.  
### Property **RefDoc**( ) As boolean

   Returns the referenced documents parameter.  
### Property **TimeRoll**( ) As long

   Returns the data save parameter (in milliseconds).  
### Property **UIStyle**( ) As [CATGenUIStyle](../InfInterfaces/enum_CATGenUIStyle_33253.md)

   Returns the user interface style parameter.  Methods

### Func **GetAutoSaveInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the data save parameter.

**Role** :Retrieves the state of the data save parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetConferencingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the conference driver parameter.

**Role** :Retrieves the state of the conference driver parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDragDropInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the drag & drop parameter.

**Role** :Retrieves the state of the drag & drop parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRefDocInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the referenced documents parameter.

**Role** :Retrieves the state of the referenced documents parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUIStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the user interface style parameter.

**Role** :Retrieves the state of the user interface style parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAutoSaveLock**( boolean  `iLocked`)

   Locks or unlocks the data save parameter.

**Role** :Locks or unlocks the data save parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetConferencingLock**( boolean  `iLocked`)

   Locks or unlocks the conference driver parameter.

**Role** :Locks or unlocks the conference driver parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDragDropLock**( boolean  `iLocked`)

   Locks or unlocks the drag & drop parameter.

**Role** :Locks or unlocks the drag & drop parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRefDocLock**( boolean  `iLocked`)

   Locks or unlocks the referenced documents parameter.

**Role** :Locks or unlocks the referenced documents parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUIStyleLock**( boolean  `iLocked`)

   Locks or unlocks the user interface style parameter.

**Role** :Locks or unlocks the user interface style parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.