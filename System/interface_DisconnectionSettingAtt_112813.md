# DisconnectionSettingAtt (Object)

**_Represents the base object to handle the parameters of automatic disconnection._**
If the automatic disconnection is enable, the V5 session will be kill after a user-defined duration of inactivity.

## Properties

### Property **ActivationState**(| ) As boolean

   Returns or sets the activation state of automatic disconnection.

**Role** :Returns or sets the activation mode of automatic disconnection.  
### Property **InactivityDuration**( ) As long

   Returns or sets the inactivity duration.

**Role** : Returns or sets the timeout in seconds before the automatic disconnection when no activity has been detected, if the mechanism is enabled.  Methods

### Func **GetActivationStateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the activation mode of automatic disconnection.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetInactivityDurationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for inactivity duration.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetActivationStateLock**( boolean  `iLocked`)

   Locks or unlocks the activation mode of automatic disconnection.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetInactivityDurationLock**( boolean  `iLocked`)

   Locks or unlocks the inactivity duration.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.