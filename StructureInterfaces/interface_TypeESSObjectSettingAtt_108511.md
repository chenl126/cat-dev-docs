# TypeESSObjectSettingAtt (Object)

**_The interface to access a CATIATypeESSObjectSettingAtt._**

## Properties

### Property **MemberTypes**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the MemberTypes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlateTypes**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the PlateTypes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetMemberTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MemberTypes parameter.

**Role** :Retrieves the state of the MemberTypes parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlateTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlateTypes parameter.

**Role** :Retrieves the state of the PlateTypes parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberTypesLock**( boolean  `iLocked`)

   Locks or unlocks the MemberTypes parameter.

**Role** :Locks or unlocks the MemberTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateTypesLock**( boolean  `iLocked`)

   Locks or unlocks the PlateTypes parameter.

**Role** :Locks or unlocks the PlateTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.