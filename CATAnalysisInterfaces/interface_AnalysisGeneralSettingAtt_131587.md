# AnalysisGeneralSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "GeneralSetting"._**

## Properties

### Property **AnalysisCacheMode**(| ) As long

   Tells if Product Structure Cache Mode will be handled.  
### Property **AnalysisLoadMode**( ) As long

   Retrieves if pointed document will be loaded.  
### Property **AnalysisNamingAuto**( ) As long

   Tells if Automatic naming will be activated.  
### Property **DefaultAnalysisFlag**( ) As long

   Retrieves if a default analysis Case will be created.  
### Property **DefaultAnalysisTemplate**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the name of the default analysis Case that will be created.  
### Property **ViewAnalysisParameter**( ) As long

   Retrieves if the Parameter set is visible in the feature tree of the analysis document.  
### Property **ViewAnalysisRelation**( ) As long

   Retrieves if the Relation set is visible in the feature tree of the analysis document.  Methods

### Func **GetAnalysisCacheModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnalysisLoadModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnalysisNamingAutoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDefaultAnalysisFlagInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the default flag.

**Role** :Retrieves the state of the default flag in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDefaultAnalysisTemplateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the default template.

**Role** :Retrieves the state of the default template in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetViewAnalysisParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetViewAnalysisRelationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisCacheModeLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisLoadModeLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisNamingAutoLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultAnalysisFlagLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultAnalysisTemplateLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetViewAnalysisParameterLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetViewAnalysisRelationLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure