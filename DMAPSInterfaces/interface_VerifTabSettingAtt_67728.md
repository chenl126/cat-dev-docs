# VerifTabSettingAtt (Object)

**__**

## Properties

### Property **AllResourceFilter**(| ) As long

   Returns or sets the value to signify Whether all the resources will appear during Process Navigation

**Role** : Returns or sets the value to signify Whether all the resources will appear during Process Navigation  
### Property **AutoReframeFilter**( ) As long

   Returns or sets the value to signify Whether the 'Auto Reframe' will happen during Process navigation

**Role** : Returns or sets the value to signify Whether all the items/resources will be reframed during Process Navigation  
### Property **ImpliedResourceFilter**( ) As long

   Returns or sets the value to signify Whether the Assigned resource will appear during Process Navigation

**Role** : Returns or sets the value to signify Whether all the Assigned resource will appear during Process Navigation  Methods

### Func **GetAllResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "View All Resources" parameter.

**Role** :Retrieves the state of the "View All Resources" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAutoReframeFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Auto Reframe" parameter.

**Role** :Retrieves the state of the "Auto Reframe" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImpliedResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "View Implied Resource" parameter.

**Role** :Retrieves the state of the "View Implied Resource" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAllResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "View All Resources" parameter.

**Role** :Locks or unlocks the "View All Resources" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAutoReframeFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Auto Reframe" parameter.

**Role** :Locks or unlocks the "Auto Reframe" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImpliedResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the Xxx parameter.

**Role** :Locks or unlocks the "View Implied Resource" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.