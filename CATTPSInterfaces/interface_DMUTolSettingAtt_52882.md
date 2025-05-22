# DMUTolSettingAtt (Object)

**_Represents the DMU Tolerancing setting controller object._**
**Role** : The DMU Tolerancing setting controller object deals with the setting parameters displayed in:

  * The DMU Tolerancing property page for the Related Surface Color and the Design Mode setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Digital Mockup** to unfold the workbench list
    * Click **DMU Tolerancing Review**
  * The Cgr Management property page for the Save in CGR setting parameter.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Infrastructure** to unfold the workbench list
    * Click **Product Structure**
    * Click the **Cgr Management** property page

The Save in CGR setting parameter represents the state of the check button named: Save FTA 3D Annotation representation in CGR.

## Properties

### Property **DesignMode**( ) As boolean

Returns or sets the Design Mode setting parameter value.
**True** if the Design Mode setting parameter is checked and thus set to Automatic.
**Role** : When set to True, models are loaded in Design Mode to access technological data. Otherwise, when set to False, models are loaded in Visualization Mode, and only visualization data is loaded.  
### Property **PrevArea**( ) As boolean

Returns or sets the Preview Area setting parameter value.
**True** if the Preview Area setting parameter is checked.  
### Property **SaveCGR**( ) As boolean

Returns or sets the Save in CGR setting parameter value.
**True** if the Save in CGR setting parameter is checked.
**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **SectPattern**( ) As boolean

Returns or sets the Pattern of Visu setting parameter value.
**True** if the Pattern of Visu setting parameter is checked.
**Role** : When set to True, the FTA 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  Methods

### Func **GetDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the Design Mode setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetPrevAreaInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the Preview Area setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **GetRelatedColors**( long  `oRelatedR`,  long  `oRelatedG`,  long  `oRelatedB`)

Retrieves the Related Surface Color setting parameter value.
**Role** : The Related Surface Color setting parameter defines the color of the annotation related surfaces, that is, of all the surfaces referenced or toleranced using the CATIA V4 FD&T function.
**Legal values** :The three color indexes range from 0 to 255.

**Parameters:**

` oRelatedR`      [out] The Related Surface Color red index
` oRelatedG`      [out] The Related Surface Color green index
` oRelatedB`      [out] The Related Surface Color blue index

### Func **GetRelatedColorsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the Related Surface Color setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSaveCGRInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the Save in CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Func **GetSectPatternInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves informations about the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailled description.  
### Sub **SetDesignModeLock**( boolean  `iLocked`)

Locks or unlocks the Design Mode setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPrevAreaLock**( boolean  `iLocked`)

Locks or unlocks the Preview Area setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetRelatedColors**( long  `iRelatedR`,  long  `iRelatedG`,  long  `iRelatedB`)

Sets the Related Surface Color setting parameter value.
**Role** : The Related Surface Color setting parameter defines the color of the annotation related surfaces, that is, of all the surfaces referenced or toleranced using the CATIA V4 FD&T function.
**Legal values** :The three color indexes range from 0 to 255.

**Parameters:**

` iRelatedR`      [in] The Related Surface Color red index
` iRelatedG`      [in] The Related Surface Color green index
` iRelatedB`      [in] The Related Surface Color blue index

### Sub **SetRelatedColorsLock**( boolean  `iLocked`)

Locks or unlocks the Related Surface Color setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSaveCGRLock**( boolean  `iLocked`)

Locks or unlocks the Save in CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSectPatternLock**( boolean  `iLocked`)

Locks or unlocks the Pattern of Visu setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.