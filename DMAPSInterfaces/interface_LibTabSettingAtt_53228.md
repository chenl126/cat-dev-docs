# LibTabSettingAtt (Object)

**__**

## Methods

### Sub **GetIDUniqueSetting**(| long | `oIsUnique`)

   Retrieves the option which enables to check ID uniqueness amongst sibling processes

**Role** : Retrieves the option which enables to check ID uniqueness amongst sibling processes

**Parameters:**

` oIsUnique`      Flag indicating whether the check should be enabled or not

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetIDUniqueSettingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Unique Check' parameter.

**Role** :Retrieves the state of the 'Unique Check' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetListOfLibraryFilePath**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the List of Libraries that are used in the Process document

**Role** : Retrieves the List of Libraries that are used in the Process document

**Parameters:**

` ioPath`      a CATSafeArrayVariant of CATBSTR that has the list of libraries

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetListOfLibraryFilePathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves the information about the list of libraries path that are used in the Process document

**Role** :Retrieves the information about the list of libraries path that are used in the Process document

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetProcessIDScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPath`)

   Retrieves the path of custom VB script to generate process ID

**Role** : Retrieves the path of custom VB script to generate process ID

**Parameters:**

` oPath`      The output path of the custom VB script

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetProcessIDScriptInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves the information about the custom VB script path that are used in the Process document

**Role** :Retrieves the information about the custom VB script path that are used in the Process document

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **PutListOfLibraryFilePath**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPath`)

   Sets a List of Libraries that are used in the Process document

**Role** : Sets the List of Libraries that are used in the Process document

**Parameters:**

` iPath`      a CATSafeArrayVariant of CATBSTR that has the list of libraries.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetIDUniqueSetting**( long  `isUnique`)

   Sets the option which enables to check ID uniqueness amongst sibling processes

**Role** : Sets the option which enables to check ID uniqueness amongst sibling processes

**Parameters:**

` isUnique`      Sets the option to enable uniqueness check or not

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetIDUniqueSettingLock**( boolean  `iLocked`)

   Locks or unlocks the "Unique Check" parameter.

**Role** : Locks or unlocks the 'Unique Check' parameter if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`1 :` to lock the parameter.
`0:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetListOfLibraryFilePathLock**( boolean  `iLocked`)

   Locks or unlocks the list of libraries to be used

**Role** :Locks or unlocks the "list of libraries" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetProcessIDScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

   Sets the path of custom VB script to generate process ID

**Role** : Sets the path of custom VB script to generate process ID

**Parameters:**

` iPath`      Path of the custom VB script to be set

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetProcessIDScriptLock**( boolean  `iLocked`)

   Locks or unlocks the "Custom VB Script" parameter.

**Role** : Locks or unlocks the 'Custom VB Script' parameter if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`1 :` to lock the parameter.
`0:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure