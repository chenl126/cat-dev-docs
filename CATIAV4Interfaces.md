# CATIAV4Interfaces Framework

## Object Index

  * [InteropSettingAtt](CATIAV4Interfaces/interface_InteropSettingAtt_62074.md)
  * [MigrBatchSettingAtt](CATIAV4Interfaces/interface_MigrBatchSettingAtt_75348.md)
  * [SpecV4SettingAtt](CATIAV4Interfaces/interface_SpecV4SettingAtt_52346.md)
  * [V4MasterModel](CATIAV4Interfaces/interface_V4MasterModel_34751.md)
  * [V4V5SpaceSettingAtt](CATIAV4Interfaces/interface_V4V5SpaceSettingAtt_72466.md)
  * [V4WritingSettingAtt](CATIAV4Interfaces/interface_V4WritingSettingAtt_75623.md)

## Enumerated Types Index

  * [CATV4IV4V5SpecDraftMigrationEnum](CATIAV4Interfaces/enum_CATV4IV4V5SpecDraftMigrationEnum_198820.md)
  * [CATV4IV5V4AssociativityModeEnum](CATIAV4Interfaces/enum_CATV4IV5V4AssociativityModeEnum_188892.md)
  * [CATV4IV5V4ErrorFeatureCreationEnum](CATIAV4Interfaces/enum_CATV4IV5V4ErrorFeatureCreationEnum_226848.md)
  * [CATV4IV5V4InternalCurveCreationEnum](CATIAV4Interfaces/enum_CATV4IV5V4InternalCurveCreationEnum_241084.md)

---

# CATV4IV4V5SpecDraftMigrationEnum (Enumeration)

**_The mode of migration of draft during Copy/Paste As Spec._**

**Values:**

` squareMode`      Drafts are migrated using the square mode for ribbon progation. This mode is the mode used by default by V4 and Copy/Paste As Spec.
` coneMode`      Drafts are migrated using the cone mode for ribbon progation. This mode is the mode used by default by V5.

---

# CATV4IV5V4AssociativityModeEnum (Enumeration)

**_The associativity mode of migration during Save As Model._**

**Values:**

` AssociativeMode`      The migration is made using the associative mode.
` NonAssociativeMode`      The migration is made using the non associative mode.
` NonAssociativityModeAndNoSolidCreation`      The migration is made using the non associative mode and no solid will be created.

**See also:**      [V4WritingSettingAtt](../CATIAV4Interfaces/interface_V4WritingSettingAtt_75623.md)

---

# CATV4IV5V4ErrorFeatureCreationEnum (Enumeration)

**_The error feature's creation mode during Save As Model._**

**Values:**

` NeverCreateErrorFeatures`      The error feature is never created.
` CreateAnErrorFeatureAfterUserAgreement`      The error feature is created when the save is partial and after user agreement.
` AlwaysCreateErrorFeatures`      The error feature is always created when the save is partial.

**See also:**      [V4WritingSettingAtt](../CATIAV4Interfaces/interface_V4WritingSettingAtt_75623.md)

---

# CATV4IV5V4InternalCurveCreationEnum (Enumeration)

**_The internal curves' creation mode during Save As Model._**

**Values:**

` AllCurvesAreCreated`      All V4 curves are created in the model.
` OnlyConicsAreCreated`      Only internal conics are created.
` NoInternalCurveIsCreated`      None of the curves associated to internal face boundaries is created.

**See also:**      [V4WritingSettingAtt](../CATIAV4Interfaces/interface_V4WritingSettingAtt_75623.md)

---

# InteropSettingAtt (Object)

**_Represents the object to handle the setting parameters of the "V4 Data Reading" tab page._**

**Role** : This interface is implemented by a component named CATV4IInteropSettingCtrl which represents the controller of the Setting. The setting parameters of the tab are the following:

  * "Display only elements with Sensitive Attribute"
  * "Display 3D elements labels"
  * "Open in Light Mode: 2D Data are not taken into account"
  * "Reading Code page"
  * "PROJECT File Path"
  * "DLNAME"
  * "Prj Warn"
  * "Characters Equivalence Table Path"

To access this property page:
  * Click the **Options** command in the **Tools** menu
  * Click + left of **General** to unfold the workbench list
  * Click **Compatibility**

This interface defines:

  * A method to get each parameter
  * A method to set the value of each parameter
  * A method to lock/unlock each parameter
  * A method to retrieve the informations concerning each parameter

## Properties

### Property **Code_page**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the value of the "Reading Code page" setting parameter.

**Role** : The "Reading Code page" declares the language to identify the data read if this data is not labeled. It is stored in the CATIA data to be written when saving Version 5 CATPart documents as CATIA Version 4 models.  
### Property **Conversion_Table**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the location of the "Characters Equivalence Table Path" setting parameter.

**Role** : The "Characters Equivalence Table" allows to convert characters contained in CATIA V4 documents. It is mainly used to generate V5 compliant names from V4 names by replacing special characters (", *, /, etc...) by standard characters.  
### Property **DisplayMode**( ) As boolean

   Retrieves or sets the state of the "Display only elements with Sensitive Attribute" setting parameter.

**Role** : The "Display only elements with Sensitive Attribute" mode enables you to decide whether to display or not the elements which were sensitive to the shading mode in CATIA Version 4.  
### Property **DisplayV4Text3D**( ) As boolean

   Retrieves or sets the state of the "Display 3D elements labels" setting parameter.

**Role** : The "Display 3D elements labels" mode is activated in order to enable the reading of the 3D text associated to the V4 elements.  
### Property **Dlname**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the "DLNAME" setting parameter.

**Role** : Retrieves the DLNAME referenced by the Model.  
### Property **Draw**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Open in Light Mode: 2D Data are not taken into account" setting parameter.

**Role** : This mode is activated in order to disable the reading of DRAW data in a V4 Model.  
### Property **PROJECT_File_Path**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the value of the "PROJECT File Path" setting parameter.

**Role** : The "PROJECT File Path" field contains the location of the external project file referenced by the V4 model.  Methods

### Func **GetCode_pageInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Reading Code page" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetConversion_TableInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Characters Equivalence Table Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Display only elements with Sensitive Attribute" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayV4Text3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Display 3D elements labels" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDlnameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "DlNAME" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDrawInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Open in Light Mode: 2D Data are not taken into account" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetPROJECT_File_PathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "PROJECT File Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetCode_pageLock**( boolean  `iLock`)

   Locks or unlocks the "Reading Code page" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetConversion_TableLock**( boolean  `iLock`)

   Locks or unlocks the "Characters Equivalence Table Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayModeLock**( boolean  `iLock`)

   Retrieves information about the "Display only elements with Sensitive Attribute" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayV4Text3DLock**( boolean  `iLock`)

   Locks or unlocks the "Display 3D elements labels" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDlnameLock**( boolean  `iLock`)

   Locks or unlocks the "DLNAME" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDrawLock**( boolean  `iLock`)

   Locks or unlocks the "Open in Light Mode: 2D Data are not taken into account" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPROJECT_File_PathLock**( boolean  `iLock`)

   Locks or unlocks the "PROJECT File Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

# MigrBatchSettingAtt (Object)

**_Represents the object to handle the setting parameters of the "Migration Batch" tab page._**

**Role** : This interface is implemented by a component named CATV4IMigrBatchSettingCtrl which represents the controller of the Setting. The setting parameters of the tab are the following:

  * "Format"
  * "V4 Part Definition"
  * "Conversion Mode"
  * "Display Report Attribute"
  * "Initial Drawing Path "
  * "Projection of Space for transparent views"
  * "Mapping Files Location for Saving "
  * "Specified Directory "
  * "Mapping Files Location for Retrieving "
  * "Interface Name"

To access this property page:
  * Click the **Options** command in the **Tools** menu
  * Click + left of **General** to unfold the workbench list
  * Click **Compatibility**
  * Click on the **Migration Batch**
tabpage

This interface defines:

  * A method to get each parameter
  * A method to set the value of each parameter
  * A method to lock/unlock each parameter
  * A method to retrieve the informations concerning each parameter

## Properties

### Property **Affiche_Attribut**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Display Report Attribute" setting parameter.

**Role** : This functionality allows the visualization of 3D elements attributes in the Migration Report. For each element, the list of its attributes is displayed with their names and values.  
### Property **Mapping_File_Save_Mode**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Mapping Files Location for Saving" setting parameter.

**Role** : The "Mapping Files Location for Saving " mode enables you to store a file which indicates the pointed entities in V4 MML Solids and which allows to retrieve associativity in CATIA V5. You can specify the directory path of your choice: Batch Target Directory, Model Directory or Specified Directory.  
### Property **Mapping_Saving_File**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Specified Directory" setting parameter.

**Role** : The "Specified Directory" mode enables you to find pointed entities in V4 MML Solids and to retrieve associativity in CATIA V5. You can specify the directory path of your choice.  
### Property **Migration_Format**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Format" setting parameter.

**Role** : The "Format" mode enables you to select the format of the Migration in Batch Mode: AS SPEC or AS RESULT.  
### Property **Migration_Interface**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the "Migration Interace" setting parameter.

**Role** : This option allows you to customize migrations from CATIA V4 to CATIA V5. You can choose how your applicative data will be migrated by writing source code  
### Property **Migration_Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Conversion Mode" setting parameter.

**Role** : The "Conversion Mode" mode enables you to separate the treatment of SPACE data and DRAW data when a model is migrated.  
### Property **Search_List_Size**( ) As long

   Retrieves or sets the size of the "Mapping Files Location for Retrieving" list.

**Role** : This setting enables to retrieve the size of the "Mapping Files Location for Retrieving" list.  
### Property **StartUp_Model_For_Drawing**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Initial Drawing Path" setting parameter.

**Role** : The "Initial Drawing Path" mode enables you to specify a .CATDrawing document which will serve as a template. The standard used by this document will be used during the migration.  
### Property **V4_Part_Definition**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "V4 Part Definition" setting parameter.

**Role** : The "V4 Part Definition" mode enables you to define the CATParts obtained after the migration: A CATPart by Geometric Set or A CATPart by Solid. .  
### Property **Visu_Mode_2D**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves or sets the state of the "Projection of Space for transparent views" setting parameter.

**Role** : The "Projection of Space for transparent views" mode enables you to specify what kind of projection mode you want to use for transparent views during the migration: NHR, HLR or the same projection mode as the V4 model.  Methods

### Func **GetAffiche_AttributInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Display Report Attribute" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMapping_File_Save_ModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Mapping Files Location for Saving" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMapping_Saving_FileInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Specified Directory" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMigration_FormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Format" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMigration_InterfaceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Migration Interface" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMigration_TypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Conversion" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSearch_Mapping_List**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the state of the "Mapping Files Location for Retrieving" setting parameter.

**Role** : The "Mapping Files Location for Retrieving " mode enables you to store a list of mapping tables.  
### Func **GetStartUp_Model_For_DrawingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Initial Drawing Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetV4_Part_DefinitionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "V4 Part Definition" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetVisu_Mode_2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the "Projection of Space for transparent views" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **PutSearch_Mapping_List**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iRelPath`)

   Sets the state of the "Mapping Files Location for Retrieving" setting parameter.

**Role** : The "Mapping Files Location for Retrieving " mode enables you to store a list of mapping tables.  
### Sub **SetAffiche_AttributLock**( boolean  `iLock`)

   Locks or unlocks the "Display Report Attribute" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMapping_File_Save_ModeLock**( boolean  `iLock`)

   Locks or unlocks the "Mapping Files Location for Saving" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMapping_Saving_FileLock**( boolean  `iLock`)

   Locks or unlocks the "Specified Directory" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMigration_FormatLock**( boolean  `iLock`)

   Locks or unlocks the "Format" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMigration_InterfaceLock**( boolean  `iLock`)

   Locks or unlocks the "Migration Interface" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMigration_TypeLock**( boolean  `iLock`)

   Locks or unlocks the "Conversion" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStartUp_Model_For_DrawingLock**( boolean  `iLock`)

   Locks or unlocks the "Initial Drawing Path" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetV4_Part_DefinitionLock**( boolean  `iLock`)

   Locks or unlocks the "V4 Part Definition" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetVisu_Mode_2DLock**( boolean  `iLock`)

   Locks or unlocks the "Projection of Space for transparent views" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

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

---

# V4MasterModel (Object)

**_Represents the V4 Master Model._**
The Master is the root cotainer of a V4 Model.

## Properties

### Property **V4DocumentModel**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md) (Read Only)

   Returns the V4 Document that contains the Master's Model.

**Example:**      This example retrieves in `V4Document` the document that contains the `V4Master`.

```VBScript
     Dim V4Document As Document
     Set V4Document = V4Master.V4DocumentModel

```

---

# V4V5SpaceSettingAtt (Object)

**_Represents the object to handle the setting parameters of the "V4V5 Space" tab page._**

**Role** : This interface is implemented by a component named CATV4IV4V5SpaceSettingCtrl which represents the controller of the Setting. parameters displayed in the V4V5 Space Data property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **General** to unfold the workbench list
  * Click **Compatibility**

**The different options for V4/V5 SPACE tab** are the following :  Gap Healing | Curvature Improvement  | Surface and Curve sub-elements  | Migration of DETAILS spaces udes by dittos | Isolated Solid Mock-up migration  | 3D Text Migration
This interface defines:

  * A method to get each parameter
  * A method to set the value of each parameter
  * A method to lock/unlock each parameter
  * A method to retrieve the informations concerning each parameter

## Properties

### Property **DetailsModeExplode**( ) As long

   Returns or sets the activation state of mode for details migration (Explode Mode)

**Role** : Returns or sets the state of mode for details migration.  
### Property **DetailsModeUsual**( ) As long

   Returns or sets the activation state of mode for details migration (Usual Mode)

**Role** : Returns or sets the state of mode for details migration.  
### Property **DetailsModeWireframe**( ) As long

   Returns or sets the activation state of mode for details migration (WireFrame Mode)

**Role** : Returns or sets the state of mode for details migration.  
### Property **ExternalMaxDeformation**( ) As double

   Returns or sets the activation state of mode with external deformation (Gap Healing).

**Role** : Returns or sets the activation state of mode with external deformation (Gap Healing). during a Copy/Paste As Spec.  
### Property **ExternalTypeDeformation**( ) As long

   Returns or sets the activation state of type for external deformation (Gap Healing).

**Role** : Returns or sets the activation state of type for external deformation (Model relative or User defined value) during a Copy/Paste As Spec.  
### Property **InternalMaxDeformation**( ) As double

   Returns or sets the activation state of mode with internal deformation (Curve Improvement).

**Role** : Returns or sets the activation state of mode with internal deformation during a Copy/Paste As Spec.  
### Property **InternalTypeDeformation**( ) As long

   Returns or sets the activation state of type for internal deformation (Curve Improvement).

**Role** : Returns or sets the activation state of type for internal deformation (Model relative or User defined value) during a Copy/Paste As Spec.  
### Property **KeepSegmentation**( ) As long

   Returns or sets the activation state of mode with segmentation (Keep V4 Segmentation ).

**Role** : Returns or sets the activation state of mode with segmentation during a Copy/Paste As Spec.  
### Property **SolidMU**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the activation state of mode for isolated Solids Mock-Up migration

**Role** : Returns or sets the state of mode for isolated Solids Mock-Up migration.  
### Property **TextMigration**( ) As long

   Returns or sets the activation state of mode for 3D Text migration

**Role** : Returns or sets the state of mode for 3D Text migration.  Methods

### Func **GetDetailsModeExplodeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDetailsModeUsualInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDetailsModeWireframeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExternalMaxDeformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the ExternalMaxDeformation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExternalTypeDeformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for activation mode with external deformation (Gap Healing).
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetInternalMaxDeformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the InternalMaxDeformation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetInternalTypeDeformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves environment informations for activation mode with internal deformation (Curve Improvement).
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetKeepSegmentationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the KeepSegmentation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSolidMUInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the Solid Mock-Up Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetTextMigrationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves information about the 3D Text Migration setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDetailsModeExplodeLock**( boolean  `iLock`)

   Locks or unlocks the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDetailsModeUsualLock**( boolean  `iLock`)

   Locks or unlocks the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDetailsModeWireframeLock**( boolean  `iLock`)

   Locks or unlocks the Details Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExternalMaxDeformationLock**( boolean  `iLock`)

   Locks or unlocks the "External Control Point Maximum Deformation" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExternalTypeDeformationLock**( boolean  `iLock`)

   Locks or unlocks the activation mode with external deformation (Gap Healing).

**Role** :Locks or unlocks the activation mode with external deformation if it is possible
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetInternalMaxDeformationLock**( boolean  `iLock`)

   Locks or unlocks the "Internal Control Point Maximum Deformation" setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetInternalTypeDeformationLock**( boolean  `iLock`)

   Locks or unlocks the activation mode with internal deformation (Curve Improvement).

**Role** :Locks or unlocks the activation mode with external deformation if it is possible
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetKeepSegmentationLock**( boolean  `iLock`)

   Locks or unlocks the KeepSegmentation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSolidMULock**( boolean  `iLock`)

   Locks or unlocks the Solid Mock-Up Migration Mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetTextMigrationLock**( boolean  `iLock`)

   Locks or unlocks the 3D Text Migration setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

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