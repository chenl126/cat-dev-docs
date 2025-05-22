# DocumentationSettingAtt (Object)

**_Setting controller for the Help property tab page._**
**Role** : This interface is implemented by a component which represents the controller of the documentation settings.

## Properties

### Property **CompanionPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the User Companion location (path) parameter.  
### Property **DocLanguage**( ) As long

Returns the technical documentation language parameter.  
### Property **Priority**( ) As [CATDocContextualPriority](../InfInterfaces/enum_CATDocContextualPriority_122472.md)

Returns the contextual priority parameter.  
### Property **TechnicalDocumentationPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the technical documentation location (path) parameter.  Methods

### Func **GetCompanionPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the User Companion location parameter.
**Role** :Retrieves the state of the User Companion location parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDocLanguageInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the technical documentation language parameter.
**Role** :Retrieves the state of the technical documentation language parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPriorityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the contextual priority parameter.
**Role** :Retrieves the state of the contextual priority parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTechnicalDocumentationPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the technical documentation location parameter.
**Role** :Retrieves the state of the technical documentation location parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetCompanionPathLock**( boolean  `iLocked`)

Locks or unlocks the User Companion location parameter.
**Role** :Locks or unlocks the User Companion location parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDocLanguageLock**( boolean  `iLocked`)

Locks or unlocks the technical documentation language parameter.
**Role** :Locks or unlocks the technical documentation language parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPriorityLock**( boolean  `iLocked`)

Locks or unlocks the contextual priority parameter.
**Role** :Locks or unlocks the contextual priority parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTechnicalDocumentationPathLock**( boolean  `iLocked`)

Locks or unlocks the technical documentation location parameter.
**Role** :Locks or unlocks the technical documentation location parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.