# MaterialESSObjectSettingAtt (Object)

**_The interface to access a CATIAMaterialESSObjectSettingAtt._**

## Properties

### Property **MemberMaterial**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the MemberMaterial parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlateMaterial**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the PlateMaterial parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetMemberMaterialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MemberMaterial parameter.
**Role** :Retrieves the state of the MemberMaterial parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlateMaterialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PlateMaterial parameter.
**Role** :Retrieves the state of the PlateMaterial parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberMaterialLock**( boolean  `iLocked`)

Locks or unlocks the MemberMaterial parameter.
**Role** :Locks or unlocks the MemberMaterial parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateMaterialLock**( boolean  `iLocked`)

Locks or unlocks the PlateMaterial parameter.
**Role** :Locks or unlocks the PlateMaterial parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.