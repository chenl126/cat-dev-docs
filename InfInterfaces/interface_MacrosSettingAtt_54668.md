# MacrosSettingAtt (Object)

**_Setting controller for the Macros tab page._**

## Methods

### Func **GetDefaultMacroLibraries**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Returns the list of default macro libraries.  
### Func **GetDefaultMacroLibrariesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves environment informations for the default macro libraries setting.
**Role** :Retrieves the state of the parameter default macro libraries setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

### Func **GetExternalReferences**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Returns the list of external references.  
### Func **GetExternalReferencesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves environment informations for the external references setting.
**Role** :Retrieves the state of the parameter external references setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

### Func **GetLanguageEditor**( [CATScriptLanguage](../System/enum_CATScriptLanguage_59191.md)  `iLanguage`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the editor path for the specified language.  
### Func **GetLanguageEditorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves environment informations for the language editors setting.
**Role** :Retrieves the state of the parameter language editors setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

### Sub **SetDefaultMacroLibraries**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLibraries`)

Sets the list of default macro libraries.  
### Sub **SetDefaultMacroLibrariesLock**( boolean  `iLocked`)

Locks or unlocks the default macro libraries setting.
**Role** :Locks or unlocks the default macro libraries setting if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`True :` to lock the parameter.
`False:` to unlock the parameter.

### Sub **SetExternalReferences**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferences`)

Sets the list of external references.  
### Sub **SetExternalReferencesLock**( boolean  `iLocked`)

Locks or unlocks the external references setting.
**Role** :Locks or unlocks the external references setting if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`True :` to lock the parameter.
`False:` to unlock the parameter.

### Sub **SetLanguageEditor**( [CATScriptLanguage](../System/enum_CATScriptLanguage_59191.md)  `iLanguage`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iEditorPath`)

Sets the editor path for the specified language.  
### Sub **SetLanguageEditorLock**( boolean  `iLocked`)

Locks or unlocks the language editors setting.
**Role** :Locks or unlocks the language editors setting if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`True :` to lock the parameter.
`False:` to unlock the parameter.