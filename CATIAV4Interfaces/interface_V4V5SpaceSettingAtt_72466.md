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