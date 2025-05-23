# PathESSRessourcesSettingAtt (Object)

**_The interface to access a CATIAPathESSRessourcesSettingAtt._**

## Properties

### Property **ResolvedSectionsPath**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ResolvedSectionsPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SectionsCatalogPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the SectionsCatalogPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ThicknessListPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ThicknessListPath parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetResolvedSectionsPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ResolvedSectionsPath parameter.

**Role** :Retrieves the state of the ResolvedSectionsPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSectionsCatalogPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SectionsCatalogPath parameter.

**Role** :Retrieves the state of the SectionsCatalogPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetThicknessListPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ThicknessListPath parameter.

**Role** :Retrieves the state of the ThicknessListPath parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetResolvedSectionsPathLock**( boolean  `iLocked`)

   Locks or unlocks the ResolvedSectionsPath parameter.

**Role** :Locks or unlocks the ResolvedSectionsPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSectionsCatalogPathLock**( boolean  `iLocked`)

   Locks or unlocks the SectionsCatalogPath parameter.

**Role** :Locks or unlocks the SectionsCatalogPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetThicknessListPathLock**( boolean  `iLocked`)

   Locks or unlocks the ThicknessListPath parameter.

**Role** :Locks or unlocks the ThicknessListPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.