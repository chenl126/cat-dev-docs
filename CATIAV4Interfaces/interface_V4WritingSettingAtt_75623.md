# V4WritingSettingAtt (Object)

**_Represents the Saving As V4 Data setting controller object._**
**Role** : The Saving As V4 Data setting controller object deals with the setting parameters displayed in the Saving As V4 Data property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **General** to unfold the workbench list
  * Click **Compatibility**

**The different options for V4/V5SPEC tab** :  The Writing Code Page | The Model Dimension  | The Model Unit  | The Initial Model File Path  | The Associativity Mode  | The Layer For Non Associative Data  | The Error Feature Creation if the Save is not complete  | The Curves Associated To Face Boundaries Creation  | The V4 Model File Name In Capitals Letters  | The Small Edges And Faces Cleaning Tolerance

## Properties

### Property **Asso_mode**( ) As [CATV4IV5V4AssociativityModeEnum](../CATIAV4Interfaces/enum_CATV4IV5V4AssociativityModeEnum_188892.md)

Returns or sets the associativity mode of migration.
**Role** : Returns or sets the associativity mode of migration.If non associative mode is chosen, it is possible to create or not the solid.  
### Property **CleanTolCheck**( ) As boolean

Returns or sets the small edges and faces cleaning tolerance activation.
**Role** : Returns or sets the small edges and faces cleaning tolerance activation.  
### Property **CleanTolValue**( ) As double

Returns or sets the small edges and faces cleaning tolerance value if activated.
**Role** : Returns or sets the small edges and faces cleaning tolerance value if activated.  
### Property **Code_page_Dest**( ) As long

Returns or sets the activation state of the writing code page.
**Role** : Returns or sets the value of the writing code page.  
### Property **Initial_Model_File_Path**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the initial model file path.
**Role** : Returns or sets the initial model file path.  
### Property **Layer_for_No_Asso**( ) As long

Returns or sets the layer for not associative data.
**Role** : Returns or sets the layer for not associative data.  
### Property **ModeCreateDisplay**( ) As [CATV4IV5V4InternalCurveCreationEnum](../CATIAV4Interfaces/enum_CATV4IV5V4InternalCurveCreationEnum_241084.md)

Returns or sets the curves associated to faces'boundaries creation option.
**Role** : Returns or sets the curves associated to faces'boundaries creation option.  
### Property **ModeErrorDisplay**( ) As [CATV4IV5V4ErrorFeatureCreationEnum](../CATIAV4Interfaces/enum_CATV4IV5V4ErrorFeatureCreationEnum_226848.md)

Returns or sets the error feature creation option.
**Role** : Returns or sets the error feature creation option.  
### Property **Model_Dimension**( ) As double

Returns or sets the model dimension.
**Role** : Returns or sets the model dimension.  
### Property **Model_Factor**( ) As double

Returns or sets the model factor.
**Role** : Returns or sets the model factor that manages the conversion of model dimension in millimeters.  
### Property **Model_File_Name**( ) As boolean

Returns or sets the model file name in capital letters option.
**Role** : Returns or sets the model file name in capital letters option.  
### Property **Model_Unit**( ) As long

Returns or sets the model unit.
**Role** : Returns or sets the model unit.  Methods

### Func **GetAsso_modeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Asso_mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetCleanTolCheckInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the CleanTolCheck setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetCleanTolValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the CleanTolValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetCode_page_DestInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Code_page_Dest setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetInitial_Model_File_PathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Initial_Model_File_Path setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLayer_for_No_AssoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Layer_for_No_Asso setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModeCreateDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the ModeCreateDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModeErrorDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the ModeErrorDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModel_DimensionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Model_Dimension setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModel_FactorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Model_Factor setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModel_File_NameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Model_File_Name setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetModel_UnitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Model_Unit setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAsso_modeLock**( boolean  `iLock`)

Locks or unlocks the Asso_mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetCleanTolCheckLock**( boolean  `iLock`)

Locks or unlocks the CleanTolCheck setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetCleanTolValueLock**( boolean  `iLock`)

Locks or unlocks the CleanTolValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetCode_page_DestLock**( boolean  `iLock`)

Locks or unlocks the Code_page_Dest setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetInitial_Model_File_PathLock**( boolean  `iLock`)

Locks or unlocks the Initial_Model_File_Path setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLayer_for_No_AssoLock**( boolean  `iLock`)

Locks or unlocks the Layer_for_No_Asso setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModeCreateDisplayLock**( boolean  `iLock`)

Locks or unlocks the ModeCreateDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModeErrorDisplayLock**( boolean  `iLock`)

Locks or unlocks the ModeErrorDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModel_DimensionLock**( boolean  `iLock`)

Locks or unlocks the Model_Dimension setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModel_FactorLock**( boolean  `iLock`)

Locks or unlocks the Model_Factor setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModel_File_NameLock**( boolean  `iLock`)

Locks or unlocks the Model_File_Name setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetModel_UnitLock**( boolean  `iLock`)

Locks or unlocks the Model_Unit setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.