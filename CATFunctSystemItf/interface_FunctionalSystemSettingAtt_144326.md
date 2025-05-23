# FunctionalSystemSettingAtt (Object)

**_Enables attribute access to PFD options._**

## Properties

### Property **DocumentContentAtCreation**(| ) As long

   Returns or sets the DocumentContentAtCreation parameter.

**Parameters:**

` iDocumentContentAtCreation`      oDocumentContentAtCreation Document Content At Creation Attribute **Legal values** :
`0 :` Sample elements
`1:` empty

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **FunctionalActionPresentation**( ) As long

   Returns or sets the FunctionalActionPresentation parameter.

**Parameters:**

` iDocumentContentAtCreation`      or oDocumentContentAtCreation Functional Action Presentation **Legal values** :
`0 :` A : Action
`1:` SAO : Subject Action Object
`2:` ASO : Action Subject Object

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **ShowParameters**( ) As long

   Returns or sets the ShowParameters parameter.

**Parameters:**

` iShowParameters`      or oShowParameters Show Parameters **Legal values** :
`False :`
`True:`

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **ShowRelations**( ) As long

   Returns or sets the ShowRelations parameter.

**Parameters:**

` iShowRelations`      or oShowRelations Show Relations **Legal values** :
`False :`
`True:`

### Property **ShowSynchroStatusOfLocalParamCache**( ) As long

   Returns or sets the ShowSynchroStatusOfLocalParamCache parameter.

**Parameters:**

` iShowSynchroStatusOfLocalParamCache`      or oShowSynchroStatusOfLocalParamCache Show Synchronisation Status OfLocal Parameter Cache **Legal values** :
`False :`
`True :`

### Property **SplitFunctionalObjectName**( ) As long

   Returns or sets the SplitFunctionalObjectName parameter.

**Parameters:**

` iSplitFunctionalObjectName`      or oSplitFunctionalObjectName **Legal values** :
`False :` don't split functional object name
`True :` split Functional object name

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **StringUsedAsCarriageReturn**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the StringUsedAsCarriageReturn parameter.

**Parameters:**

` iStringUsedAsCarriageReturn`      or oStringUsedAsCarriageReturn String Used As Carriage Return

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **TypeOfIconOnFunctionalElement**( ) As long

   Returns or sets the TypeOfIconOnFunctionalElement parameter.

**Parameters:**

` iTypeOfIconOnFunctionalElement`      or oTypeOfIconOnFunctionalElement Type Of Icon On Functional Elements **Legal values** :
`0 :` indicate a current association with PPR links.
`1:` indicate a current generative script.
Methods

### Func **GetDocumentContentAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DocumentContentAtCreation parameter.

**Role** :Retrieves the state of the DocumentContentAtCreation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetFunctionalActionPresentationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the FunctionalActionPresentation parameter.

**Role** :Retrieves the state of the FunctionalActionPresentation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowParametersInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowParameters parameter.

**Role** :Retrieves the state of the ShowParameters parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowRelationsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowRelations parameter.

**Role** :Retrieves the state of the ShowRelations parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowSynchroStatusOfLocalParamCacheInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowSynchroStatusOfLocalParamCache parameter.

**Role** :Retrieves the state of the ShowSynchroStatusOfLocalParamCache parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSplitFunctionalObjectNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SplitFunctionalObjectName parameter.

**Role** :Retrieves the state of the SplitFunctionalObjectName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetStringUsedAsCarriageReturnInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the StringUsedAsCarriageReturn parameter.

**Role** :Retrieves the state of the StringUsedAsCarriageReturn parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTypeOfIconOnFunctionalElementInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TypeOfIconOnFunctionalElement parameter.

**Role** :Retrieves the state of the TypeOfIconOnFunctionalElement parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetDocumentContentAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the DocumentContentAtCreation parameter.

**Role** :Locks or unlocks the DocumentContentAtCreation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetFunctionalActionPresentationLock**( boolean  `iLocked`)

   Locks or unlocks the FunctionalActionPresentation parameter.

**Role** :Locks or unlocks the FunctionalActionPresentation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowParametersLock**( boolean  `iLocked`)

   Locks or unlocks the ShowParameters parameter.

**Role** :Locks or unlocks the ShowParameters parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowRelationsLock**( boolean  `iLocked`)

   Locks or unlocks the ShowRelations parameter.

**Role** :Locks or unlocks the ShowRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowSynchroStatusOfLocalParamCacheLock**( boolean  `iLocked`)

   Locks or unlocks the ShowSynchroStatusOfLocalParamCache parameter.

**Role** :Locks or unlocks the ShowSynchroStatusOfLocalParamCache parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSplitFunctionalObjectNameLock**( boolean  `iLocked`)

   Locks or unlocks the SplitFunctionalObjectName parameter.

**Role** :Locks or unlocks the SplitFunctionalObjectName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetStringUsedAsCarriageReturnLock**( boolean  `iLocked`)

   Locks or unlocks the StringUsedAsCarriageReturn parameter.

**Role** :Locks or unlocks the StringUsedAsCarriageReturn parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTypeOfIconOnFunctionalElementLock**( boolean  `iLocked`)

   Locks or unlocks the TypeOfIconOnFunctionalElement parameter.

**Role** :Locks or unlocks the TypeOfIconOnFunctionalElement parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure