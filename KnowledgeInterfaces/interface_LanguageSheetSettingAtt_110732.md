# LanguageSheetSettingAtt (Object)

**_The interface to access a CATIALanguageSheetSettingAtt._**

## Properties

### Property **KnowledgeBuildPathDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the CATKnowledgeBuildPath setting parameter.
**Role** :Return or Set the CATKnowledgeBuildPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oKnowledgeBuildPathDirectory`      The knowledge build path directory: the path where all the resources are located.

### Property **ListOfPackagesToLoad**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the ListOfPackagesToLoad parameter.
**Role** :Return or Set the ListOfPackagesToLoad parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oListOfPackagesToLoad`      The list of packages to load.

### Property **LoadAllPackages**( ) As short

Returns or sets the LoadAllPackages parameter.
**Role** :Return or Set the LoadAllPackages parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLoadAllPackages`      **Legal values** :
`0 :` to not load all packages
`1 :` to load all packages.

### Property **LoadExtendedLanguageLib**( ) As short

Returns or sets the LoadExtendedLanguageLib parameter.
**Role** :Return or Set the LoadExtendedLanguageLib parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLoadExtendedLanguageLib`      **Legal values** :
`0 :` to not use extended libraries
`1 :` to use extended libraries.

### Property **ReferenceDirectoryForTypes**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the ReferenceDirectoryForTypes parameter.
**Role** :Return or Set the ReferenceDirectoryForTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReferenceDirectoryForTypes`      The reference directory for types.
Methods

### Func **GetKnowledgeBuildPathDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the CATKnowledgeBuildPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetListOfPackagesToLoadInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ListOfPackagesToLoad setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLoadAllPackagesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the LoadAllPackages setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLoadExtendedLanguageLibInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the LoadExtendedLanguageLib setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetReferenceDirectoryForTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ReferenceDirectoryForTypes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetKnowledgeBuildPathDirectoryLock**( boolean  `iLocked`)

Locks or unlocks the CATKnowledgeBuildPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetListOfPackagesToLoadLock**( boolean  `iLocked`)

Locks or unlocks the ListOfPackagesToLoad setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLoadAllPackagesLock**( boolean  `iLocked`)

Locks or unlocks the LoadAllPackages setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLoadExtendedLanguageLibLock**( boolean  `iLocked`)

Locks or unlocks the LoadExtendedLanguageLib setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetReferenceDirectoryForTypesLock**( boolean  `iLocked`)

Locks or unlocks the ReferenceDirectoryForTypes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.