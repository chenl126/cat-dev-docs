# CacheSettingAtt (Object)

**_Represents the base object to handle the parameters of the cache._**

## Properties

### Property **ActivationMode**(| ) As boolean

   Returns or sets the activation state of cache.

**Role** : Returns or sets the value of cache activation.  
### Property **CacheMaxSizeMo**( ) As long

   Returns or sets the value of the cache maximum size.

**Role** : Returns or sets the value of the maximum allowed cache size in Mo  
### Property **LODMode**( ) As boolean

   Returns or sets the LOD generation mode parameter.

**Role** : Returns or sets the value of the LOD generation mode.  
### Property **LocalPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the cache local path.

**Role** : Retrieves or sets the value of the cache local path. If the local path is defined with environment variables then this method return the unexpansed form.  
### Property **ReleasedVoxel**( ) As float

   Returns or sets the released voxel parameter.

**Role** : Returns or sets the value of the released voxel parameter.  
### Property **SizeControl**( ) As boolean

   Return or sets the cache size control.

**Role** : Returns or sets the cache size control. The cache use this parameter in conjunction with the maxixum allowed cache size. If it is turned off, the cache size has no limit.  
### Property **TimestampMode**( ) As boolean

   Retrieves or sets the timestamp control.

**Role** : If the timestamp control is turned on, the cache will verify if the cached object is uptodate with the master object. If not a new cached view will be generated.
If the timestamp control is turned off, the cache will consider that the cached views are always uptodate with their master object.  
### Property **UTCTimeFormat**( ) As boolean

   Retrieves or sets the the cache timestamp format.

**Role** : If the timestamp format is set to TRUE, then the time used used as timestamp by the cache is expressed in UTC format (GMT), in the other case the local time is used. The default format is local time.  Methods

### Func **GetActivationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the Cache activation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetCacheMaxSizeMoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache maximum size.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetLODModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the LOD generation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetLocalPathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache local path.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetReleasePath**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retieves the cache release paths.

**Role** : Sets the cache release paths in a symbolic format.

**Parameters:**

` ioRelPath`      a CATSafeArrayVariant of CATBSTR.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetReleasePathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `Locked`) As boolean

   Retrieves environment informations for the Cache release path.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetReleasedVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the Cache released voxel.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSizeControlInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the size control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetTimestampModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the timestamp control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetUTCTimeFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the timestamp control mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **PutReleasePath**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iRelPath`)

   Sets the cache release paths.

**Role** : Sets the cache release paths in a symbolic format.

**Parameters:**

` iRelPath`      a CATSafeArrayVariant of CATBSTR.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetActivationModeLock**( boolean  `iLocked`)

   Locks or unlocks the Cache Activation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetCacheMaxSizeMoLock**( boolean  `iLocked`)

   Locks the paramater Cache maximum size.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetLODModeLock**( boolean  `iLocked`)

   Locks or unlocks the LOD generation mode.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetLocalPathLock**( boolean  `iLocked`)

   Locks or unlocks the cache local path parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetReleasePathLock**( boolean  `iLocked`)

   Locks or unlocks the cache local path parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetReleasedVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the released voxel parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetSizeControlLock**( boolean  `iLocked`)

   Locks or unlocks the cache size control parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetTimestampModeLock**( boolean  `iLocked`)

   Locks or unlocks the timestamp control in cache.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetUTCTimeFormatLock**( boolean  `iLocked`)

   Locks or unlocks the timestamp format.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.