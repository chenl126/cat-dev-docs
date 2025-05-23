# GlobalStatisticsSettingAtt (Object)

**_Interface for Global statistic Controler

**Role** : the global statistics controler manages the values of all or only a part of the attributes available for all the statistics thematics._**

## Properties

### Property **BufferSize**(| ) As long

   Returns or sets the size of buffer.

**Role** : Returns or sets the size of the buffer.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **CopyDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the copy directory.

**Role** : Returns or sets the path of the directory where the copy files are located.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **MaxCopyFile**( ) As long

   Returns or sets the maximum number of copy files.

**Role** : Returns or sets the value of the maximum number of statistics files copies.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  
### Property **MaxSizePerFile**( ) As long

   Returns or sets the maximum size per file.

**Role** : Returns or sets the value of the maximum size of statistics files.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure  Methods

### Func **GetThematicsParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the global statistics parameters.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetThematicsParameterLock**( boolean  `iLocked`)

   Locks or unlocks the global statistics parameters.

**Role** :Locks or unlocks the global statistics parameters.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on Failure