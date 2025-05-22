# SpecV4SettingAtt (Object)

**_Represents the V4/V5 SPEC setting controller object._**
**Role** : The V4/V5 SPEC setting controller object deals with the setting parameters displayed in the V4/V5SPEC property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **General** to unfold the workbench list
  * Click **Compatibility**

**The different options for V4/V5SPEC tab** :  The Step By Step Update And Reroute | The Draft Feature Migration Mode

## Properties

### Property **DraftFeatureMigrationMode**( ) As [CATV4IV4V5SpecDraftMigrationEnum](../CATIAV4Interfaces/enum_CATV4IV4V5SpecDraftMigrationEnum_198820.md)

Returns or sets the activation state of the mode of migration for draft feature.
**Role** : This setting parameter manages the activation of the mode of migration for draft feature during a Copy/Paste As Spec.  
### Property **StepByStepUpdateAndReroute**( ) As boolean

Returns or sets the activation state of Step By Step Update And Reroute.
**Role** : The Step By Step Update And Reroute setting parameter manages the activation of the step by step update and reroute during a Copy/Paste As Spec when solids are involved.  Methods

### Func **GetDraftFeatureMigrationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the DraftFeatureMigrationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStepByStepUpdateAndRerouteInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the StepByStepUpdateAndReroute setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDraftFeatureMigrationModeLock**( boolean  `iLock`)

Locks or unlocks the DraftFeatureMigrationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStepByStepUpdateAndRerouteLock**( boolean  `iLock`)

Locks or unlocks the StepByStepUpdateAndReroute setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.