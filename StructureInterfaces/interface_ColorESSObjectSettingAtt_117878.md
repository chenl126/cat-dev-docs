# ColorESSObjectSettingAtt (Object)

**_The interface to access a CATIAColorESSObjectSettingAtt._**

## Methods

### Sub **GetMemberColor**( long  `oMemberColorR`,  long  `oMemberColorG`,  long  `oMemberColorB`)

Returns or sets the MemberColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetMemberColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MemberColor parameter.
**Role** :Retrieves the state of the MemberColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPlateColor**( long  `oPlateColorR`,  long  `oPlateColorG`,  long  `oPlateColorB`)

Returns or sets the PlateColor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetPlateColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PlateColor parameter.
**Role** :Retrieves the state of the PlateColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMemberColor**( long  `iMemberColorR`,  long  `iMemberColorG`,  long  `iMemberColorB`)

### Sub **SetMemberColorLock**( boolean  `iLocked`)

Locks or unlocks the MemberColor parameter.
**Role** :Locks or unlocks the MemberColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlateColor**( long  `iPlateColorR`,  long  `iPlateColorG`,  long  `iPlateColorB`)

### Sub **SetPlateColorLock**( boolean  `iLocked`)

Locks or unlocks the PlateColor parameter.
**Role** :Locks or unlocks the PlateColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.