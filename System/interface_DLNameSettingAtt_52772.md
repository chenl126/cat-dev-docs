# DLNameSettingAtt (Object)

**_Interface to handle the DLNames._**
**Role** : This interface is implemented by a component which represents the controller of the DLNames.
This interface defines:

  * A method to set each DLName
  * A method to get the value of each DLName
  * A method to lock/unlock each parameter
  * A method to retrieve the informations concerning each parameter

## Properties

### Property **DLNameCreationRight**( ) As boolean

Returns or set the right to create new DLNames.
**Role** : Retrieves or set the right to create new DLNames.  
### Property **RootDLNameCreationRight**( ) As boolean

Returns or set the right to create new Root DLNames.
**Role** : Retrieves or set the right to create new Root DLNames.  Methods

### Sub **GetDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oFather`)

Retrieves the mapping between a logical name and the physical path.
**Role** : Retrieves the mapping between a logical name and the physical path.

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameCreationRightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves the state of the parameter DLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **GetDLNameExp**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oFather`)

Retrieves the mapping between a logical name and the physical path.
**Role** : Retrieves the mapping between a logical name and the physical path in a litteral form.

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves the state of the for a given DLName.
**Role** : This information defines the state of the setting parameter and is made up of:

  * The administration level that sets the current value or the value used to reset it
  * The administration level that has locked the setting parameter.
  * A flag to indicate whether the setting parameter was modified.

**Parameters:**

` iDLName`      a DLname.
` ioAdminLevel`      [inout] The administration leve that defines the value used when resetting the setting parameter. **Legal values** :

  * **Default value** if the DLName has never been defined in the administration concatenation.
  * **Admin Level n** if the setting parameter has been administered,
where n is an integer starting from 0 representing the rank of the administration level.

` ioLocked`      [inout] A character string to indicate whether the parameter is locked and the level of administration where the locking has been proceeded.
**Legal values** :

  * **Locked at Admin Level n** if the setting parameter is locked by then administration level n,
where n is an integer starting from 0.
  * **Upper Locked** if the setting parameter is locked by the current administration level
  * **Unlocked** if the setting parameter is not locked

**Returns:**          **True** to indicate that the DLName value has been defined at the current administrator or user level. This is only possible with unlocked DLNames. **False** means that the DLName is inherited from the administration.

### Func **GetDLNameList**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Retrieves the list of the DLNames.
**Role** : Retrieves the list of the defined DLNames.

**Parameters:**

` oTabDLName`      a CATSafeArrayVariant of CATBSTR of nb elements.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDLNameSubList**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Retrieves the list of the Sub-DLNames.
**Role** : Retrieves the list of the DLNames created in a given DLName.

**Parameters:**

` iDLName`      The Father DLName. if iDLName=NULL all DLNames created at the root level are return.
` oNbDLname`      The number of defined DLNames.
` oTabDLName`      The array of DLNames
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_OUTOFMEMORY:` on allocation failure
`E_FAIL:` on other failures  
### Func **GetRootDLNameCreationRightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves the state of the parameter RootDLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **RemoveDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`)

Remove a logical name.
**Role** : Remove a DLName in the current set if it is possible.

**Parameters:**

` iDLName`      the logical name.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **RenameDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNewName`)

Rename an existing DLName.
**Role** : Rename a DLName in the current set if it is possible.

**Parameters:**

` iDLName`      the logical name to rename.
` iNewName`      the new logical name.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDLName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRealNameUnix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRealNameNT`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFather`,  boolean  `iVerifDirectory`)

Sets the mapping between a logical name and the physical path.
**Role** : Sets the value of the cache maximum size in Mo

**Parameters:**

` iDLName`      the logical name.
` oRealNameUnix`      the real physical path corresponding to the logical name on Unix.
` oRealNameNT`      the real physical path corresponding to the logical name on Windows.
` iFather`      if applicable the Name of the parent DLName
` iVerifDirectory`      if VerifDirectory is set the existence of the directory on the current platform will be check.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDLNameCreationRightLock**( boolean  `iLocked`)

Locks or unlocks the parameter DLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetDLNameLock**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDLName`,  boolean  `iLocked`)

Locks or unlocks the DLName.
**Role** : Locks or unlocks the given DLName if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iDLname`      the DLname to be locked.
` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetRootDLNameCreationRightLock**( boolean  `iLocked`)

Locks or unlocks the parameter RootDLNameCreationRight.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.