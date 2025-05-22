# AsmGeneralSettingAtt (Object)

**_Represents the Assembly General setting controller object._**
**Role** : the Assembly General setting controller object deals with the setting parameters displayed in the Assembly General property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **Mechanical Design** to unfold the workbench list
  * Click **Assembly Design: General tab**

## Properties

### Property **AutoSwitchToDesignMode**( ) As [CatAsmAutoSwitchToDesignMode](../CATAssemblyInterfaces/enum_CatAsmAutoSwitchToDesignMode_159986.md)

Returns or sets the implicit switch from visualization mode to design mode setting parameter .
**Role** : The implicit switch from visualization mode to design mode setting parameter manages the loading of necessayr data whenever they are needed. Note that this option is useful only when the Cache option is activated
**Legal values** :  | catAutoSwitchUnavailable | Automatic switch to design mode unavailable
---|---
catAutoSwitchAvailable | Automatic switch to design mode available

**Example:**      The following example retrieves the implicit switch setting parameter of `AsmGeneralSettingAtt1` in `SwitchMode` and enables the switch

```VBScript
Set SwitchMode = AsmGeneralSettingAtt1.AutoSwitchToDesignMode
AsmGeneralSettingAtt1.AutoSwitchToDesignMode = catAutoSwitchAvailable

```

### Property **AutoUpdateMode**( ) As [CatAsmUpdateMode](../CATAssemblyInterfaces/enum_CatAsmUpdateMode_52340.md)

Returns or sets the automatic update setting parameter.
**Role** : The automatic update setting parameter manages the automatic launching of the Update command.
**Legal values** :  | catManualUpdate | Manual update mode
---|---
catAutomaticUpdate | Automatic update mode

**Example:**      The following example retrieves the automatic update setting parameter of `AsmGeneralSettingAtt1` in `UpdateMode` and sets the mode to manual update.

```VBScript
Set UpdateMode = AsmGeneralSettingAtt1.AutoUpdateMode
AsmGeneralSettingAtt1.AutoUpdateMode = catManualUpdate

```

### Property **MoveWithFixTExtendMode**( ) As [CatAsmExtendMoveToFixT](../CATAssemblyInterfaces/enum_CatAsmExtendMoveToFixT_97992.md)

Returns or sets the setting parameter managing the extension of a move to the components involved in a FixTogether.
**Role** : This setting parameter manages whether the components involved in a FixTogether will be moved or not.
**Legal values** :  | catNeverExtendMoveToFixT | Never extend move to all component involved in a FixTogether
---|---
catAskIfExtendMoveToFixT | Ask question to extend move to all component involved in a FixTogether
catAlwaysExtendMoveToFixT | Always extend move to all component involved in a FixTogether

**Example:**      The following example retrieves the move setting parameter of `AsmGeneralSettingAtt1` in `MoveMode` and sets it to Always

```VBScript
Set MoveMode = AsmGeneralSettingAtt1.MoveWithFixTExtendMode
AsmGeneralSettingAtt1.MoveWithFixTExtendMode = catAlwaysExtendMoveToFixT

```

### Property **UpdateStatusMode**( ) As [CatAsmUpdateStatusComputeMode](../CATAssemblyInterfaces/enum_CatAsmUpdateStatusComputeMode_175422.md)

Returns or sets the update status computation setting parameter.
**Role** : The update status computation setting parameter manages the loading at open of the data necessary to the exact update status computation. Note that this option is useful only when the Cache option is activated
**Legal values** :  | catManualCompute | At open the update status is unknown
---|---
catAutomaticCompute | Additional data are being loaded at open to compute an exact Update status

**Example:**      The following example retrieves the update status computation setting parameter of `AsmGeneralSettingAtt1` in `StatusMode` and sets the mode to automatic computation.

```VBScript
Set StatusMode = AsmGeneralSettingAtt1.UpdateStatusMode
AsmGeneralSettingAtt1.UpdateStatusMode = catAutomaticCompute

```

Methods
### Func **GetAutoSwitchToDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves the state of the implicit switch from visualization mode to design mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAutoUpdateModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves informations about the automatic update setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMoveWithFixTExtendModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves the state of the setting parameter managing the extension of a move to the components involved in a FixTogether.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUpdateStatusModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the update status computation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAutoSwitchToDesignModeLock**( boolean  `iLocked`)

Locks or unlocks the implicit switch from visualization mode to design mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAutoUpdateModeLock**( boolean  `iLocked`)

Locks or unlocks the automatic update setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMoveWithFixTExtendModeLock**( boolean  `iLocked`)

Locks or unlocks the setting parameter managing the extension of a move to the components involved in a FixTogether.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUpdateStatusModeLock**( boolean  `iLocked`)

Locks or unlocks the update status computation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.