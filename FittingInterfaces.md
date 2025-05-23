# FittingInterfaces Framework

## Object Index

  * [FittingSettingAtt](FittingInterfaces/interface_FittingSettingAtt_61736.md)
  * [ManipSettingAtt](FittingInterfaces/interface_ManipSettingAtt_47906.md)
  * [Sampled](FittingInterfaces/interface_Sampled_10766.md)
  * [Shot](FittingInterfaces/interface_Shot_3832.md)
  * [Shots](FittingInterfaces/interface_Shots_5971.md)
  * [Shuttle](FittingInterfaces/interface_Shuttle_11297.md)
  * [Shuttles](FittingInterfaces/interface_Shuttles_14802.md)
  * [Track](FittingInterfaces/interface_Track_5573.md)
  * [Tracks](FittingInterfaces/interface_Tracks_8144.md)

## Enumerated Types Index

  * [CATFittingShuttleVector](FittingInterfaces/enum_CATFittingShuttleVector_111319.md)
  * [CATManipAutoInsertMode](FittingInterfaces/enum_CATManipAutoInsertMode_98682.md)
  * [CATManipClashMode](FittingInterfaces/enum_CATManipClashMode_57299.md)
  * [CatSampledAnalysisMode](FittingInterfaces/enum_CatSampledAnalysisMode_100650.md)
  * [CatSampledSplitType](FittingInterfaces/enum_CatSampledSplitType_76396.md)
  * [CatShuttleMoveMode](FittingInterfaces/enum_CatShuttleMoveMode_67700.md)
  * [CatShuttleVector](FittingInterfaces/enum_CatShuttleVector_55318.md)
  * [DMUTrackMoveMode](FittingInterfaces/enum_DMUTrackMoveMode_51428.md)

---

# CATFittingShuttleVector (Enumeration)

**_The Shuttle Vector setting attribute range of values._**

**Values:**

` CATFittingShuttleVectorX`      Use the X axis as the shuttle vector
` CATFittingShuttleVectorY`      Use the Y axis as the shuttle vector
` CATFittingShuttleVectorZ`      Use the Z axis as the shuttle vector

---

# CATManipAutoInsertMode (Enumeration)

**_The manipulation auto insert setting attribute possible values_**

**Values:**

` CATOnMouseRelease`      Automatic insert on each mouse release
` CATWhileMouseMoving`      Automatic insert based on specific parameters

---

# CATManipClashMode (Enumeration)

**_The manipulation clash mode attribute's possible values._**

**Values:**

` CATManipClashModeNo`      The clash detection mode will not be used (set to OFF)
` CATManipClashModeOn`      The clash detection mode will be used in ON mode (the parts that clash will be highlighted)
` CATManipClashModeStop`      The clash detection mode will be used in STOP mode (the parts that clash will be stop moving)

---

# CatSampledAnalysisMode (Enumeration)

**_Possible values of how analysis is to be used when it is added to a sampled based object._**

**Values:**

` CatSampledAnalysisOff`      Mode to set the analysis to Off
` CatSampledAnalysisOn`      Mode to set the analysis to On
` CatSampledAnalysisStop`      Mode to set the analysis to Stop
` CatSampledAnalysisVerbose`      Mode to set the analysis to Verbose

---

# CatSampledSplitType (Enumeration)

**__**

---

# CatShuttleMoveMode (Enumeration)

**__**

---

# CatShuttleVector (Enumeration)

---

# DMUTrackMoveMode (Enumeration)

**_The movement mode for tracks._**
To be used in automation scripts.

**Values:**

` DMUTrackSpeedMode`      The track is to be followed at the specified speed.
` DMUTrackTimeMode`      The track is to be traversed within the specified time.

---

# FittingSettingAtt (Object)

**_Interface to handle parameters of DMU Fitting Tools Options Tab page**Role** : This interface is implemented by a component which represents the controller of DMU Fitting Tools Options parameter settings._**

  * Methods to set value of each parameter
  * Methods to get value of each parameter
  * Methods to get information on each parameter
  * Methods to lock/unlock value of each parameter

## Properties

### Property **AngleLimit**( ) As boolean

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

---

# ManipSettingAtt (Object)

**_Interface to handle parameters of DMU Manip Tools Options Tab page**Role** : This interface is implemented by a component which represents the controller of DMU Manip Tools Options parameter settings._**

  * Methods to set value of each parameter
  * Methods to get value of each parameter
  * Methods to get information on each parameter
  * Methods to lock/unlock value of each parameter

## Properties

### Property **AngleStep**( ) As float

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

---

# Sampled (Object)

**_The interface to access a CATIASampled based object._**
The Sampled class defines characteristics for simulatable tasks within DMU Fitting. CATIASampled is the parent class for tracks. Key samples are recorded (as shots or CATIAShots) for an object and then during simulation the object is interpolated with these shots over time.

## Properties

### Property **Interpolater**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves/sets the sampled's interpolater. **Role:** Retrieves/sets the interpolator used by the sampled during simulation. Note that the name of the interpolater is used (which is a string).  
### Property **Object**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns or sets the Sampled object. **Role:/b> Retrieves/stores the object that will be used in the sampled based simulation. Please note that the object will move to the shots defined in the sampled. 
### Property **Scaling**( ) As double

   Returns or sets the Sampled object.  
### Property **Shots**( ) As [CATIAShots](../FittingInterfaces/interface_Shots_5971.md) (Read Only)

   Returns or sets the Sampled object.  
### Property **Time**( ) As double

   Retrieves/sets the sampled's time. **Role:** Retrieves/sets the internal time associated to the current sampled object. Note that the time is handled as a double.  Methods

### Func **Append**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTracks`) As [CATIASampled](../FittingInterfaces/interface_Sampled_10766.md)

   Returns or sets the Sampled object.  
### Sub **BindAnalysis**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`,  [CatSampledAnalysisMode](../FittingInterfaces/enum_CatSampledAnalysisMode_100650.md)  `iAnalysisMode`,  boolean  `iMonitorMode`)

   Add (bind) an analysis object to a Track.

**Parameters:**

` iObject`      The analysis to add (bind) to the Track
` iAnalysisMode`      Indicates the analysis status for iAnalysis CatSampledAnalysisOff CatSampledAnalysisOn, CatSampledAnalysisStop CatSampledAnalysisVerbose
` iMonitorMode`      Indicates the monitor status for iAnalysis - Off (0) or On (1)

### Sub **BreakInheritance**( )

   Returns or sets the Sampled object.  
### Sub **GetKnownInterpolaters**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInterpolaters`)

   Returns or sets the Sampled object.  
### Func **GetTotalDuration**( ) As double

   Returns the total duration  
### Sub **RemoveAnalyses**( )

   Returns or sets the Sampled object.  
### Sub **ReverseTime**( )

   Returns or sets the Sampled object.  
### Sub **SetObjectKeepingPosition**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`)

   Sets the object in the sampled. **Role:** Stores the object that will be used in the sampled based simulation. The object will not move and the sample's shots will be repositioned relative to the object position.  
### Sub **Split**( [CatSampledSplitType](../FittingInterfaces/enum_CatSampledSplitType_76396.md)  `iType`,  short  `iIndice`)

   Returns or sets the Sampled object.

---

# Shot (Object)

**_The interface to access a CATIAShot._**

**Role:** A CATIAShot (or shot) is the base element that [Sampled](../FittingInterfaces/interface_Sampled_10766.md) objects are composed of. For example, when considering a [Track](../FittingInterfaces/interface_Track_5573.md), each recorded position is a shot.

## Methods

### Sub **AppendAbsDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Appends to the data related to the shot. **Role:** In certain cases, a shot contains more than one data item. The SetDatas method is used to store the first data item. This method is then used to specify any additional data items

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

### Sub **AppendDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Appends to the data related to the shot. **Role:** In certain cases, a shot contains more than one data item. The SetDatas method is used to store the first data item. This method is then used to specify any additional data items.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are relative to the position of object, specifically to where the object started from.

### Sub **GetAbsDatas**( short  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPosition`)

   Retrieves the data related to the shot. **Role:** To get the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

**Parameters:**

` iIndex`      A shot can have more than one piece of data associated to it. The value of iIndex refers to which specific data item to retrieve. The legal values of iIndex correspond to the rank of the data item (that is the 0 for the first item, 1 for the second item).

**Returns:**      An array of associated values to the shot.  
### Sub **GetDatas**( short  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPosition`)

   Retrieves the data related to the shot. **Role:** To get the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory. Please note that these values are relative to the position of object, specifically to where the object started from.

**Parameters:**

` iIndex`      A shot can have more than one piece of data associated to it. The value value of iIndex refers to which specific data item to retrieve. The legal values of iIndex correspond to the rank of the data item (that is the 0 for the first item, 1 for the second item).

**Returns:**      An array of associated values to the shot.  
### Func **GetDuration**( ) As double

   Retrieves the duration (time) associated to a shot. The duration of a shot is the amount of time needed to travel from the previous shot to the current shot. Some key things to note are:

  * The first shot should have a duration of zero.
  * The value of the duration is a positive real number. Hence, 0.454 & 1345 are legal while -18 is not.

**Returns:**      the duration of a shot.  
### Sub **GetTechnologicalDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDatas`)

   Retrieves all the data associated to the part.  
### Sub **SetAbsDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Set the data related to the shot. **Role:** To set the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are absolute (relative to the world coordinate system), specifically to where the object started from.

### Sub **SetDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`)

   Set the data related to the shot. **Role:** To set the numerical information related to the shot. For example, for a [Track](../FittingInterfaces/interface_Track_5573.md), each shot corresponds to a position that is used when evaluating a defined trajectory.

**Parameters:**

` iPosition`      An array of associated values to the shot. Please note that these values are relative to the position of object, specifically to where the object started from.

### Sub **SetDuration**( double  `iDuration`)

   Sets the duration (time) associated to a shot. The duration of a shot is the amount of time needed to travel from the previous shot to the current shot. Some key things to note are:

  * The first shot should have a duration of zero.
  * The value of the duration is a positive real number. Hence, 0.454 & 1345 are legal while -18 is not.

### Sub **SetTechnologicalDatas**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDatas`)

   Sets all the data associated to the part.

---

# Shots (Collection)

**_The collection of all shot objects contained in the current sampled._**

## Methods

### Sub **Append**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iShot`)

   Adds a shot to the end of the shots collection.

**Parameters:**

` iShot`      The shot to be added  **Example:**      The following example adds a shot (called `myShot` to the shots collection.

```VBScript
     Shots.Append (myShot)

```

### Func **CreateShot**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Creates a new shot and adds it to the Shots collection.

**Returns:**      The created shot  **Example:**      The following example creates a shot `newShot` in the Shots collection.

```VBScript
     Dim newShot
     Set newShot = Shots.CreateShot

```

### Func **CreateSpecificShot**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Creates a new shot of a specific type and adds it to the Shots collection.

**Parameters:**

` iType`      Specifies the type of the shot to be created. The legal values are FITShotPoints, FITShotDouble, FITShotSimple and FITShotGeneric. These different types correspond to the need of creating different shots for different types of objects.

**Returns:**      The created Shot  **Example:**      The following example creates a shot `shot` in the Shots collection.

```VBScript
     Set newShots = Shots.CreateShot (FITSHOTDouble)

```

### Sub **InsertAfter**( short  `iIndex`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iShot`)

   Adds a shot to a specific location to the shots collection.

**Parameters:**

` iIndex`      The value of the location of an already existing shot. Then when inserting a new shot, it will be placed after it. It is a positive integer, with the range of 1 to the value of the last shot.
` iShot`      The shot to be added  **Example:**      The following example inserts a shot after the second shot.

```VBScript
     Shots.InsertAfter (2, myShot)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns a shot using its index from the colection.

**Parameters:**

` iIndex`      The index of the item to retrieve from the collection of shots. Numerically, the index value corresponds to the rank of the shot in the collection (ie. the first is 1, second is 2, ...).

**Returns:**      The retrieved Shot  **Example:**      The following example retrieves the second shot from the Shots collection.

```VBScript
     Dim myShot
     Set myShot = myShots.Item (2)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a shot from the collection.

**Parameters:**

` iIndex`      The index of the shot to remove from the collection of the shots. Numerically, the index value corresponds to the rank of the shot in the collection (ie. the first is 1, second is 2, ...).  **Example:**      The following example removes the third shot from the Shots collection of the active document.

```VBScript
     Shots.Remove (3)

```

---

# Shuttle (Object)

**_The interface to access a CATIAShuttle._**

**Role:** The shuttle object is used to define a grouping of products. Once products have been placed in the shuttle then they can be moved all at once. Also the shuttle has a base location defined by the shuttle axis.

## Properties

### Property **AngleLimit**( ) As double

   Returns/Stores the angle limit attribute. **Role:/b> Retrieves/stores the shuttle's angle limit attribute. 
### Property **AngleValidation**( ) As boolean

   Returns/Stores the angle validation attribute. **Role:/b> Retrieves/stores the shuttle's angle validation attribute. 
### Property **Group**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the associated group object. **Role:/b> Retrieves/stores the objects within the shuttle as a group, that is a CATIAGroup. 
### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the shuttle's move object. The move object is aggregated by the shuttle object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your shuttle according to this isometry.

**Example:**      This example retrieves the move object for the `Engine` shuttle.

```VBScript
     Dim EngineMoveObject As Move
     Set EngineMoveObject = Engine.Move

```

### Property **MoveMode**( ) As [CatShuttleMoveMode](../FittingInterfaces/enum_CatShuttleMoveMode_67700.md)

   Returns/Stores the shuttle move mode. **Role:/b> Retrieves/stores the shuttle move mode. This can be either shuttle mode (to move the shuttle) or axis mode (to simply move the shuttle axis). 
### Property **Position**( ) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md) (Read Only)

   Returns the shuttle's position object. The position object is the object aggregated by the ahuttle object that holds the position of the shuttle in the space.

**Example:**      This example retrieves the position object for the `Engine` shuttle.

```VBScript
     Dim EnginePositionObject As Position
     Set EnginePositionObject = Engine.Position

```

### Property **Reference**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns or sets the associated reference object. **Role:/b> Retrieves/stores the shuttle's reference object. 
### Property **SubShuttles**( ) As [CATIAShuttles](../FittingInterfaces/interface_Shuttles_14802.md) (Read Only)

   Returns any shuttles that are contained within the current shuttle. **Role:/b> Returns any shuttles that are contained within the current shuttle. 
### Property **Vector**( ) As [CatShuttleVector](../FittingInterfaces/enum_CatShuttleVector_55318.md)

   Returns/Stores the validation vector attribute. **Role:/b> Retrieves/stores the validation vector attribute.

---

# Shuttles (Collection)

**_The interface to access a CATIAShuttles

Using this prefered syntax will enable mkdoc to document your class._**

## Methods

### Func **Add**( ) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

   Creates a new Shuttle and adds it to the Shuttles collection.

**Returns:**      The created Shuttle  **Example:**      The following example creates a Shuttle `newShuttle` in the Shuttles collection.

```VBScript
     Set newShuttles = Shuttles.Add

```

### Func **AddFromSel**( ) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

   Creates a new Shuttle from the selection and adds it to the Shuttles collection.

**Returns:**      The created Shuttle  **Example:**      The following example creates a Shuttle `newShuttle` in the Shuttles collection.

```VBScript
     Set newShuttles = Shuttles.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)

### Sub **Remove**( [CATIAShuttle](../FittingInterfaces/interface_Shuttle_11297.md)  `iShuttle`)

---

# Track (Object)

**_The interface to access a CATIATrack._**

**Role:** A CATIATrack (or track) object is an object to define motion to various items (such as a product or a shuttle). These tracks can be simulated which results in them to move along the defined trajectory (with a set speed).

## Properties

### Property **MoveMode**( ) As [DMUTrackMoveMode](../FittingInterfaces/enum_DMUTrackMoveMode_51428.md)

   Returns or sets the track's movement mode. Can be speed or time based. In Speed mode, the total time is calculated based on the time need to travel the distance of the track at the given speed. In Time mode, the movement speed to calculated so that the end of the track is reached by the end of the total time. Uses enum DMUTrackMoveMode, which defined is in this interface.  
### Property **Speed**( ) As double

   Returns or sets the track speed. Please note that the value of the speed should be greater than zero.

**Example**      This example sets the track speed to `17.54`.

```VBScript
     myTrack.Speed =  17.54

```

Methods

### Sub **GetMatrixAll**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMatrixAll`)

   GetMatrixAll Gets the base location of the track. The sum of several internal transforms.

**Parameters:**

` oMatrixAll`      An array of 12 doubles. A 3 by 3 rotation matrix followed by a position (x/y/z) vector, in millimeters.

**Returns:**      S_OK if everything was succcessfull  
### Sub **Mirror**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPoint`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iNormal`)

   Produces a "mirror image" of the track. **Role:** Determines the "mirror image" of a track. The "mirror" is a 3d plane specified by a point on the plane and the normal to the surface of the plane. The mirror calculation involves going through each shot and projecting it in the space on the other side of the mirror plane. The projection "reflects" the point perpendicularly to the plane.

**Parameters:**

` iPoint`      A point on the plane that will be used to define the mirror.
` iNormal`      A normal to the plane that will be used to define the mirror.

### Sub **Move**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTransfo`)

   Moves the track a certain position.

**Parameters:**

` iTransfo`      Specifies a relative amount to move the track.

---

# Tracks (Collection)

**_A collection of all the track objects contained in the current document._**

## Methods

### Sub **AddFromFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`)

   Creates a track in the collection, from information from an external file.

**Parameters:**

` iFileName`      The path to a valid xml file.  **Example:**      The following example reads a file called `exmple.xml` and creates a track in the tracks collection.

```VBScript
     myTracks.AddFromFile ("example.xml")

```