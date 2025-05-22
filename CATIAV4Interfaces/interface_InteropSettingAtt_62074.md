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