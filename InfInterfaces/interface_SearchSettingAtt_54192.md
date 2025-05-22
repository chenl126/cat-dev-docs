# SearchSettingAtt (Object)

**_Represents the setting controller for the Search property tab page._**
**Role** : The setting controller is the object that enables to get and set setting parameters.

## Properties

### Property **DeepSearchActivation**( ) As boolean

Returns or sets the Deep Search Activation attribute.
**Role** : The Deep Search Activation attribute manages the Deep Search option available in the Search dialog box used to determine whether documents in visualization mode must be transiently loaded during a search query  
### Property **DefaultPowerInputContextPriority**( ) As boolean

Returns or sets the Default Power Input Context Priority attribute.
**Role** : The Default Power Input Context Priority attribute manages whether the default context scope must override the context scope stored in a favorite query  
### Property **DefaultPowerInputContextScope**( ) As [CATSearchContextScope](../InfInterfaces/enum_CATSearchContextScope_90973.md)

Returns or sets the Default Power Input Context Scope attribute.
**Role** : The Default Power Input Context Scope attribute manages the default context scope to be used when none is typed in the Power Input field  
### Property **DefaultPowerInputPrefix**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the Default Power Input Prefix attribute.
**Role** : The Default Power Input Prefix attribute manages the default prefix to be used when none is typed in the Power Input field  
### Property **MaxDisplayedResults**( ) As long

Returns or sets the Max Displayed Results attribute.
**Role** : The Max Displayed Results attribute indicates the maximum number of elements that can be displayed in the Search results page. Displaying too many lines can stick more or less the results list so it is recommended to limit this number.  
### Property **MaxPreHighlightedElements**( ) As long

Returns or sets the Max Pre-Highlighted Elements attribute.
**Role** : The Max Pre-Highlighted Elements attribute indicates the maximum number of elements that can be displayed in the Search results page. Displaying too many elements can stick the session so it is strongly recommended to limit this number.  Methods

### Func **GetDeepSearchActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Deep Search Activation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultPowerInputContextPriorityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Default Power Input Context Priority setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultPowerInputContextScopeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Default Power Input Context Scope setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultPowerInputPrefixInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Default Power Input Prefix setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMaxDisplayedResultsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Max Displayed Results setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMaxPreHighlightedElementsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Max Displayed Results setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDeepSearchActivationLock**( boolean  `iLocked`)

Locks or unlocks the Deep Search Activation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultPowerInputContextPriorityLock**( boolean  `iLocked`)

Locks or unlocks the Default Power Input Context Priority setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultPowerInputContextScopeLock**( boolean  `iLocked`)

Locks or unlocks the Default Power Input Context Scope setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultPowerInputPrefixLock**( boolean  `iLocked`)

Locks or unlocks the Default Power Input Prefix setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMaxDisplayedResultsLock**( boolean  `iLocked`)

Locks or unlocks the Max Displayed Results setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMaxPreHighlightedElementsLock**( boolean  `iLocked`)

Locks or unlocks the Max Displayed Results setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.