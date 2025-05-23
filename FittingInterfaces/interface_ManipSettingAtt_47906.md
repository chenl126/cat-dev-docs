# ManipSettingAtt (Object)

**_Interface to handle parameters of DMU Manip Tools Options Tab page**Role** : This interface is implemented by a component which represents the controller of DMU Manip Tools Options parameter settings._**

  * Methods to set value of each parameter
  * Methods to get value of each parameter
  * Methods to get information on each parameter
  * Methods to lock/unlock value of each parameter

## Properties

### Property **AngleStep**(| ) As float

   Returns the Angle Step parameter

**Role** : Returns the Angle Step parameter

**Parameters:**

` oDefaultSpeed`
Will be set to the current value of the Angle Step

**Returns:**      S_OK : if the Angle Step value was correctly obtained E_FAIL : if the Angle Step value was not correctly obtained  
### Property **ClashMode**( ) As [CATManipClashMode](../FittingInterfaces/enum_CATManipClashMode_57299.md)

   Returns the ClashMode (manipulation mode) for simulation and tracks

**Role** : Returns the ClashMode (manipulation mode) for simulation and tracks

**Parameters:**

` oMode`      The ClashMode (manipulation mode) for simulation and tracks **Legal values** :
`CATManipClashModeNo` Clash Detection is set to OFF
`CATManipClashModeOn` Clash Detection is set to ON
`CATManipClashModeStop` Clash Detection is set to STOP

**Returns:**      S_OK : if the ClashMode value was correctly obtained E_FAIL : if the ClashMode value was not correctly obtained  
### Property **ClashSound**( ) As boolean

   Returns the Clash Sound parameter

**Role** : Returns the Clash Sound parameter

**Parameters:**

` oClashSound`      If Clash Beep feedback is to be used. **Legal values** :
`TRUE` Clash Beep feedback is enabled
`FALSE` Clash Beep feedback is disabled

**Returns:**      S_OK : if the Clash Sound value was correctly obtained E_FAIL : if the Clash Sound value was not correctly obtained  
### Property **DistanceStep**( ) As float

   Returns the Distance Step parameter

**Role** : Returns the Distance Step parameter

**Parameters:**

` oDefaultSpeed`
Will be set to the current value of the Distance Step

**Returns:**      S_OK : if the Distance Step value was correctly obtained E_FAIL : if the Distance Step value was not correctly obtained  
### Property **ManipAutoInsert**( ) As boolean

   Returns the ManipAutoInsert parameter

**Role** : Returns the ManipAutoInsert (Automatic insert for manipulation mode) parameter.

**Parameters:**

` oManipAutoInsert`      If Automatic insert for manipulation mode is to be used. **Legal values** :
`TRUE` Automatic insert for manipulation mode is enabled
`FALSE` Automatic insert for manipulation mode is disabled

**Returns:**      S_OK : if the ManipAutoInsert value was correctly obtained E_FAIL : if the ManipAutoInsert value was not correctly obtained  
### Property **RecordMode**( ) As [CATManipAutoInsertMode](../FittingInterfaces/enum_CATManipAutoInsertMode_98682.md)

   Returns the RecordMode for Auto Insert configuration

**Role** : Returns the RecordMode for Auto Insert configuration

**Parameters:**

` oMode`      The Record Mode that will be used for auto insert **Legal values** :
`CATOnMouseRelease` On each mouse release
`CATWhileMouseMoving` On specific parameters

**Returns:**      S_OK : if the RecordMode value was correctly obtained E_FAIL : if the RecordMode value was not correctly obtained  
### Property **SnapAngleDistance**( ) As float

   Returns the Snap Angle Distance parameter

**Role** : Returns the Angle Distance parameter of the Snap Sensitivity

**Parameters:**

` oSnapPosition`
Will be set to the current value of the Angle Distance parameter of the Snap Sensitivity

**Returns:**      S_OK : if the Snap Angle Distance value was correctly obtained E_FAIL : if the Snap Angle Distance value was not correctly obtained  
### Property **SnapPosition**( ) As float

   Returns the Snap Position parameter

**Role** : Returns the Position parameter of the Snap Sensitivity

**Parameters:**

` oSnapPosition`
Will be set to the current value of the Position parameter of the Snap Sensitivity

**Returns:**      S_OK : if the Snap Position value was correctly obtained E_FAIL : if the Snap Position value was not correctly obtained  Methods

### Func **GetAngleStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AngleStep parameter.

**Role** :Retrieves the state of the AngleStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetClashModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ClashMode parameter.

**Role** :Retrieves the state of the ClashMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetClashSoundInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ClashSound parameter.

**Role** :Retrieves the state of the ClashSound parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDistanceStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DistanceStep parameter.

**Role** :Retrieves the state of the DistanceStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetManipAutoInsertInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ManipAutoInsert parameter.

**Role** :Retrieves the state of the ManipAutoInsert parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRecordModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the RecordMode parameter.

**Role** :Retrieves the state of the RecordMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSnapAngleDistanceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SnapAngleDistance parameter.

**Role** :Retrieves the state of the SnapAngleDistance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSnapPositionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SnapPosition parameter.

**Role** :Retrieves the state of the SnapPosition parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAngleStepLock**( boolean  `iLocked`)

   Locks or unlocks the AngleStep parameter.

**Role** :Locks or unlocks the DistanceStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetClashModeLock**( boolean  `iLocked`)

   Locks or unlocks the ClashMode parameter.

**Role** :Locks or unlocks the ClashMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      S_OK : if the ManipAutoInsert value was correctly obtained E_FAIL : if the ManipAutoInsert value was not correctly obtained  
### Sub **SetClashSoundLock**( boolean  `iLocked`)

   Locks or unlocks the ClashSound parameter.

**Role** :Locks or unlocks the ClashSound parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      S_OK : if the RecordMode value was correctly obtained E_FAIL : if the RecordMode value was not correctly obtained  
### Sub **SetDistanceStepLock**( boolean  `iLocked`)

   Locks or unlocks the DistanceStep parameter.

**Role** :Locks or unlocks the DistanceStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetManipAutoInsertLock**( boolean  `iLocked`)

   Locks or unlocks the ManipAutoInsert parameter.

**Role** :Locks or unlocks the ManipAutoInsert parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetRecordModeLock**( boolean  `iLocked`)

   Locks or unlocks the RecordMode parameter.

**Role** :Locks or unlocks the RecordMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSnapAngleDistanceLock**( boolean  `iLocked`)

   Locks or unlocks the SnapAngleDistance parameter.

**Role** :Locks or unlocks the SnapAngleDistance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSnapPositionLock**( boolean  `iLocked`)

   Locks or unlocks the SnapPosition parameter.

**Role** :Locks or unlocks the SnapPosition parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure