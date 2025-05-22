# ToleranceSheetSettingAtt (Object)

**_The interface to access a CATIAToleranceSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Tolerance sheet.

## Properties

### Property **AngleMaxTolerance**( ) As double

Returns or sets the AngleMaxTolerance parameter.
**Role** :Return or Set the AngleMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAngleMaxTolerance`      The angle maximum tolerance value.

### Property **AngleMinTolerance**( ) As double

Returns or sets the AngleMinTolerance parameter.
**Role** :Return or Set the AngleMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAngleMinTolerance`      The angle minimum tolerance value.

### Property **DefaultTolerance**( ) As short

Returns or sets the DefaultTolerance parameter.
**Role** :Return or Set the DefaultTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDefaultTolerance`      **Legal values** :
`0 :` to not accept a default tolerance
`1 :` to accept a default tolerance.

### Property **LengthMaxTolerance**( ) As double

Returns or sets the LengthMaxTolerance parameter.
**Role** :Return or Set the LengthMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLengthMaxTolerance`      The length maximum tolerance value.

### Property **LengthMinTolerance**( ) As double

Returns or sets the LengthMinTolerance parameter.
**Role** :Return or Set the LengthMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLengthMinTolerance`      The length minimum tolerance value.
Methods

### Func **GetAngleMaxToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AngleMaxTolerance parameter.
**Role** :Retrieves the state of the AngleMaxTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAngleMinToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AngleMinTolerance parameter.
**Role** :Retrieves the state of the AngleMinTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDefaultToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the DefaultTolerance parameter.
**Role** :Retrieves the state of the DefaultTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLengthMaxToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the LengthMaxTolerance parameter.
**Role** :Retrieves the state of the LengthMaxTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLengthMinToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the LengthMinTolerance parameter.
**Role** :Retrieves the state of the LengthMinTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAngleMaxToleranceLock**( boolean  `iLocked`)

Locks or unlocks the AngleMaxTolerance parameter.
**Role** :Locks or unlocks the AngleMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAngleMinToleranceLock**( boolean  `iLocked`)

Locks or unlocks the AngleMinTolerance parameter.
**Role** :Locks or unlocks the AngleMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDefaultToleranceLock**( boolean  `iLocked`)

Locks or unlocks the DefaultTolerance parameter.
**Role** :Locks or unlocks the DefaultTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLengthMaxToleranceLock**( boolean  `iLocked`)

Locks or unlocks the LengthMaxTolerance parameter.
**Role** :Locks or unlocks the LengthMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLengthMinToleranceLock**( boolean  `iLocked`)

Locks or unlocks the LengthMinTolerance parameter.
**Role** :Locks or unlocks the LengthMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.