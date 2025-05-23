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

### Property **Affiche_Attribut**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

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