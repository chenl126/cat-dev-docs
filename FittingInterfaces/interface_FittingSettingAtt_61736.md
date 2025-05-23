# FittingSettingAtt (Object)

**_Interface to handle parameters of DMU Fitting Tools Options Tab page**Role** : This interface is implemented by a component which represents the controller of DMU Fitting Tools Options parameter settings._**

  * Methods to set value of each parameter
  * Methods to get value of each parameter
  * Methods to get information on each parameter
  * Methods to lock/unlock value of each parameter

## Properties

### Property **AngleLimit**(| ) As boolean

   Returns the value of the Shuttle Angle Limit parameter

**Role** : Returns the Shuttle Angle Limit parameter

**Parameters:**

` oAngleLimit`      If shuttle angle limitation is to be used. **Legal values** :
`TRUE` Angle Limitation is enabled
`FALSE` Angle Limitation is disabled

**Returns:**      S_OK : if the AngleLimit value was correctly obtained E_FAIL : if the AngleLimit value was not correctly obtained  
### Property **ClashWhileMoving**( ) As boolean

   Returns the Clash While Moving parameter

**Role** : Returns the Clash Detection While Moving parameter

**Parameters:**

` oClashWhileMoving`      If Clash Detection While Moving is to be used. **Legal values** :
`TRUE` Clash Detection While Moving is enabled
`FALSE` Clash Detection While Moving is disabled used

**Returns:**      S_OK : if the Clash While Moving value was correctly obtained E_FAIL : if the Clash While Moving value was not correctly obtained  
### Property **DefaultSpeed**( ) As double

   Returns the Default Speed parameter

**Role** : Returns the Default Speed parameter for a track

**Parameters:**

` oDefaultSpeed`
Will be set to the current value of the Default Speed for a track

**Returns:**      S_OK : if the Default Speed value was correctly obtained E_FAIL : if the Default Speed value was not correctly obtained  
### Property **DefaultTime**( ) As double

   Returns the Default Time parameter

**Role** : Returns the Default Time parameter for a track

**Parameters:**

` oDefaultTime`
Will be set to the current value of the Default Time for a track

**Returns:**      S_OK : if the Default Time value was correctly obtained E_FAIL : if the Default Time value was not correctly obtained  
### Property **MaxAngle**( ) As float

   Returns the Maximum Angle if angle limitation is being used

**Role** : Returns the Maximum Angle if angle limitation is being used

**Parameters:**

` oMaxAngle`
Will be set to the current value of the Maximum Angle for shuttle angle limitation validation.

**Returns:**      S_OK : if the Max Validation value was correctly obtained E_FAIL : if the Max Validation value was not correctly obtained  
### Property **PathFinderSmooth**( ) As boolean

   Returns the Path Finder Automatic Smooth parameter

**Role** : Returns the Path Finder Automatic Smooth parameter

**Parameters:**

` oPathFinderSmooth`      If Path Finder Automatic Smooth is to be used. **Legal values** :
`TRUE` Path Finder Automatic Smooth is enabled
`FALSE` Path Finder Automatic Smooth is disabled used

**Returns:**      S_OK : if the Path Finder Automatic Smooth value was correctly obtained E_FAIL : if the Path Finder Automatic Smooth value was not correctly obtained  
### Property **TrackAutoUpdate**( ) As boolean

   Returns the Automatic Track Update parameter

**Role** : Returns the Automatic Track Update parameter

**Parameters:**

` oTrackAutoUpdate`      If Automatic Track Update is to be used. **Legal values** :
`TRUE` Automatic Track Update is enabled
`FALSE` Automatic Track Update is disabled used

**Returns:**      S_OK : if the Automatic Track Update value was correctly obtained E_FAIL : if the Automatic Track Update value was not correctly obtained  
### Property **Vector**( ) As [CATFittingShuttleVector](../FittingInterfaces/enum_CATFittingShuttleVector_111319.md)

   Returns the Vector if angle limitation is being used

**Role** : Returns the Vector if angle limitation is being used

**Parameters:**

` oVector`      The axis that will be used for shuttle angle validation **Legal values** :
`CATFittingShuttleVectorX` Along the vector X axis
`CATFittingShuttleVectorY` Along the vector Y axis
`CATFittingShuttleVectorZ` Along the vector Z axis

**Returns:**      S_OK : if the Vector value was correctly obtained E_FAIL : if the Vector value was not correctly obtained  Methods

### Func **GetAngleLimitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the AngleLimit parameter.

**Role** :Retrieves the state of the AngleLimit parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetClashWhileMovingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the AskAnlMode parameter.

**Role** :Retrieves the state of the AskAnlMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDefaultSpeedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the DefaultSpeed parameter.

**Role** :Retrieves the state of the DefaultSpeed parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDefaultTimeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the DefaultTime parameter.

**Role** :Retrieves the state of the DefaultTime parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMaxAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the MaxAngle parameter.

**Role** :Retrieves the state of the MaxAngle parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPathFinderSmoothInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the PathFinderSmooth parameter.

**Role** :Retrieves the state of the PathFinderSmooth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTrackAutoUpdateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the TrackAutoUpdate parameter.

**Role** :Retrieves the state of the TrackAutoUpdate parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetVectorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment information for the VisualizationMode parameter.

**Role** :Retrieves the state of the VisualizationMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAngleLimitLock**( boolean  `iLocked`)

   Locks or unlocks the AngleLimit parameter.

**Role** :Locks or unlocks the AngleLimit parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetClashWhileMovingLock**( boolean  `iLocked`)

   Locks or unlocks the ClashWhileMoving parameter.

**Role** :Locks or unlocks the ClashWhileMoving parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultSpeedLock**( boolean  `iLocked`)

   Locks or unlocks the DefaultSpeed parameter.

**Role** :Locks or unlocks the DefaultSpeed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultTimeLock**( boolean  `iLocked`)

   Locks or unlocks the DefaultTime parameter.

**Role** :Locks or unlocks the DefaultTime parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetMaxAngleLock**( boolean  `iLocked`)

   Locks or unlocks the MaxAngle parameter.

**Role** :Locks or unlocks the MaxAngle parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetPathFinderSmoothLock**( boolean  `iLocked`)

   Locks or unlocks the PathFinderSmooth parameter.

**Role** :Locks or unlocks the PathFinderSmooth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetTrackAutoUpdateLock**( boolean  `iLocked`)

   Locks or unlocks the TrackAutoUpdate parameter.

**Role** :Locks or unlocks the TrackAutoUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetVectorLock**( boolean  `iLocked`)

   Locks or unlocks the VisualizationMode parameter.

**Role** :Locks or unlocks the VisualizationMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure