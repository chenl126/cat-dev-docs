# MemoryWarningSettingAtt (Object)

**_Represents the base object to handle the parameters of memory warning mechanism._**
This mechanism informs the user when the process memory use exceeds a given percentage of the address space usage. This mechanism warns you that because the amout of remaining memory is becoming low, you should save your data and leave the session.

## Properties

### Property **ActivationState**(| ) As boolean

   Returns or sets the activation state of the memory warning mechanism.

**Role** : Returns or sets the value of of the memory warning.  
### Property **MemoryStopperState**( ) As boolean

   Returns or sets the activation state of the memory stopper mechanism.

**Role** : Returns or sets the value of of the memory stopper.  
### Property **UsageLimit**( ) As long

   Returns or sets the alert percentage.

**Role** : Returns or sets the percentage of the address space usage that can be used by the process before sending the warning.  Methods

### Func **GetActivationStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the memory warning mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetMemoryStopperStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the memory stopper mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetUsageLimitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for the alert percentage.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetActivationStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of the memory warning mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetMemoryStopperStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of the memory stopper mechanism.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetUsageLimitLock**( boolean  `iLocked`)

   Locks or unlocks the the alert percentage.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.