# PrintersSettingAtt (Object)

**_Represents a setting controller for the printer settings._**

**Role** : This interface is implemented by a component which represents the controller of the printer settings.

## Methods

### Sub **AddPrinterDirectory**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iPrinterDir`,| | [CatPrinterDirState](../InfInterfaces/enum_CatPrinterDirState_67980.md) | `iPrinterDirState`)

   Add a printer file directory to printer directories list and define its state.

**Parameters:**

` iPrinterDir`      directory where some 3DPLM printers are defined.
The printers defined in this directory will be available for each user.
` iPrinterDirState`      printer directory state.
Each directory can be protected to prevent user access to the printers it contains.
The state could be protect or free.
If the state is CatPrinterDirProtect, the parameters of each printer included in the directory cannot be changed.
If the state is CatPrinterDirFree, the parameters of each printer included in the directory can be changed, and the printers can be removed.

**Legal values** :
`CatPrinterDirProtect :` the printers included in the directory are protected.
`CatPrinterDirFree :` the printers included in the directory are free.

### Sub **AddPrinterGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterGroupName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPrinterNames`)

   Add a printer group and define the printers included in this group.

**Parameters:**

` iPrinterGroupName`      printer group name
` iPrinterNames`      array of printers included in the group.

### Sub **GetDriverConfigurationPath**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oDriverCfgPath`)

   Returns the driver configuration file.

**Parameters:**

` oDriverCfgPath`      path of the driver configuration file

### Func **GetDriverConfigurationPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the driver configuration file.

**Role** : Retrieves the state of the driver configuration file in the current environment.

**Parameters:**

` oAdminLevel`      If the parameter is locked, oAdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, oAdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetNewPrinterDirectory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oNewPrinterDir`)

   Returns the directory where new printers will be added.

**Parameters:**

` oNewPrinterDir`      directory to add new printers

**Role** : Each new printer created by an user is added in this directory.

### Func **GetNewPrinterDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the directory where printers will be added.

**Role** : Retrieves the state of the directory where printers will be added in the current environment.

**Parameters:**

` oAdminLevel`      If the parameter is locked, oAdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, oAdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPrinterArrayForGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterGroupName`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns the definition of the printer group.

**Parameters:**

` iPrinterGroupName`      printer group name

**Returns:**      array of printers included in the group.  
### Func **GetPrinterDirectories**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns the directories of printer files.

**Returns:**      array of directories where 3DPLM printers are defined.  
### Func **GetPrinterDirectoriesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the directories of printer files and their states.

**Role** : Retrieves the state of the directories of printer files and their states in the current environment.

**Parameters:**

` oAdminLevel`      If the parameter is locked, oAdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, oAdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPrinterDirectoryState**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterDir`) As [CatPrinterDirState](../InfInterfaces/enum_CatPrinterDirState_67980.md)

   Returns the state of the directory of printer files.

**Parameters:**

` iPrinterDir`      directory where some 3DPLM printers are defined.

**Returns:**      printer directory state.
Each directory can be protected to prevent user access to the printers it contains.
The state could be protect or free.
If the state is CatPrinterDirProtect, the parameters of each printer included in the directory cannot be changed.
If the state is CatPrinterDirFree, the parameters of each printer included in the directory can be changed, and the printers can be removed.

**Legal values** :
`CatPrinterDirProtect :` the printers included in the directory are protected.
`CatPrinterDirFree :` the printers included in the directory are free.  
### Func **GetPrinterGroups**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns the printer groups.

**Returns:**      array of printer group names  
### Func **GetPrinterGroupsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the definition of each printer group.

**Role** : Retrieves the state of the definition of each printer group in the current environment.

**Parameters:**

` oAdminLevel`      If the parameter is locked, oAdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, oAdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **ModifyPrinterArrayForGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterGroupName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPrinterNames`)

   Modify a printer group: redefine the array of printers included in this group.

**Parameters:**

` iPrinterGroupName`      printer group name
` iPrinterNames`      array of printers included in the group.

### Sub **ModifyPrinterDirectoryState**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterDir`,  [CatPrinterDirState](../InfInterfaces/enum_CatPrinterDirState_67980.md)  `iPrinterDirState`)

   Modify a printer file directory state.

**Parameters:**

` iPrinterDir`      directory where some 3DPLM printers are defined.
` iPrinterDirState`      printer directory state.
Each directory can be protected to prevent user access to the printers it contains.
The state could be protect or free.
If the state is CatPrinterDirProtect, the parameters of each printer included in the directory cannot be changed.
If the state is CatPrinterDirFree, the parameters of each printer included in the directory can be changed, and the printers can be removed.

**Legal values** :
`CatPrinterDirProtect :` the printers included in the directory are protected.
`CatPrinterDirFree :` the printers included in the directory are free.

### Sub **RemoveAllPrinterDirectories**( )

   Remove all the directories including printer files.  
### Sub **RemoveAllPrinterGroups**( )

   Remove all the groups of printers.  
### Sub **RemovePrinterDirectory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterDir`)

   Remove a directory of printer files from the directories list.

**Parameters:**

` iPrinterDir`      directory where some 3DPLM printers are defined.

### Sub **RemovePrinterGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrinterGroupName`)

   Remove a group of printers.

**Parameters:**

` iPrinterGroupName`      name of the group to remove.

### Sub **SetDriverConfigurationPath**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDriverCfgPath`)

   Sets the driver configuration file.

**Parameters:**

` iDriverCfgPath`      path of the driver configuration file

### Sub **SetDriverConfigurationPathLock**( boolean  `iLock`)

   Locks or unlocks the driver configuration file.

**Role** : Locks or unlocks the driver configuration file if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed

**Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewPrinterDirectory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNewPrinterDir`)

   Sets the directory where new printers will be added.

**Parameters:**

` iNewPrinterDir`      directory to add new printers

**Role** : Each new printer created by an user is added in this directory.

### Sub **SetNewPrinterDirectoryLock**( boolean  `iLock`)

   Locks or unlocks the directory where printers will be added.

**Role** : Locks or unlocks the directory where printers will be added if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed

**Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPrinterDirectoriesLock**( boolean  `iLock`)

   Locks or unlocks the directories of printer files and their states.

**Role** : Locks or unlocks the directories of printer files and their states if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed

**Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPrinterGroupsLock**( boolean  `iLock`)

   Locks or unlocks the definition of each printer group.

**Role** : Locks or unlocks the definition of each printer group if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed

**Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.