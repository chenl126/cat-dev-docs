# ViewCharacteristicCurvesSettingAtt (Object)

**_Represents the CATIA Sheet Metal Aerospace Display setting controller object._**

**Role** : The CATIA Sheet Metal Aerospace setting Display controller object deals with the setting attributes displayed in the Aerospace Sheet Metal Design Display property page. The Sheet Metal Aerospace Display property page manage the visibility of **Characteristic Curves** in Folded and Unfolded view. THE METHODS DEDICATED FOR SURFACIC FLANGE ARE USEFUL FOR BOTH SURFACIC FLANGE AND SWEPT FLANGE.

**Characteristic Curves** summary :  BTLSupp | Bend Tangent Line bounding the Support (Flange)
---|---
BTLFeat | Bend Tangent Line bounding the Base Feature (Web or Flange)
OML | Outer Mold Line
OML2 | Second Outer Mold Line (Unfolded view)
IML | Inner Mold Line
CLB | Center Line of Bend
To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **Mechanical Design** to unfold the workbench list
  * Click **Display**

The Sheet Metal Aerospace Display setting controller object can be retrieved as an item of the setting controller collection using its name "CATIStmViewCharacteristicCurvesSettingCtrl" as follows:

```VBScript
     Dim settingControllers1 As SettingControllers
     Set settingControllers1 = CATIA.SettingControllers
     Dim CATIAStmViewCharacteristicCurvesSettingAtt1 As SettingController
     Set CATIAStmViewCharacteristicCurvesSettingAtt1 = settingControllers1.Item("CATIStmViewCharacteristicCurvesSettingCtrl")

```

Note that there is NO default value : if a setting attribute is not set, the corresponding check button will be unchecked and the setting attribute will take the value "hidden" if the User clicks "OK" in the Display property page.

## Properties

### Property **SHMViewFDBeadBTLFeat**(| ) As long

   Returns or sets SHMViewFDBeadBTLFeat setting parameter value.

**Role** : The XXX SHMViewFDBeadBTLFeat parameter manage the visibility of the BTL Base Feature on a Bead in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDCircStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDCircStampBTLFeat setting parameter value.

**Role** : The SHMViewFDCircStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Circular Stamp in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDCurveStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDCurveStampBTLFeat setting parameter value.

**Role** : The SHMViewFDCurveStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Curve Stamp in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgCutBTLFeat**(| ) As long

   Returns or sets SHMViewFDFlgCutBTLFeat setting parameter value.

**Role** : The SHMViewFDFlgCutBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Flanged Cutout in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgCutIML**(| ) As long

   Returns or sets SHMViewFDFlgCutIML setting parameter value.

**Role** : The SHMViewFDFlgCutIML setting parameter manage the visibility of the IML on a Flanged Cutout in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgCutOML**(| ) As long

   Returns or sets SHMViewFDFlgCutOML setting parameter value.

**Role** : The SHMViewFDFlgCutOML setting parameter manage the visibility of the OML on a Flanged Cutout in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgHoleBTLFeat**(| ) As long

   Returns or sets SHMViewFDFlgHoleBTLFeat setting parameter value.

**Role** : The SHMViewFDFlgHoleBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Flanged Hole in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgHoleIML**(| ) As long

   Returns or sets SHMViewFDFlgHoleIML setting parameter value.

**Role** : The SHMViewFDFlgHoleIML setting parameter manage the visibility of the IML on a Flanged Hole in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDFlgHoleOML**(| ) As long

   Returns or sets SHMViewFDFlgHoleOML setting parameter value.

**Role** : The SHMViewFDFlgHoleOML setting parameter manage the visibility of the OML on a Flanged Hole in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDOtherStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDOtherStampBTLFeat setting parameter value.

**Role** : The SHMViewFDOtherStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on an other Stamp ( F&A; -> Bridge, Louver ... ) in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDStiffStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDStiffStampBTLFeat setting parameter value.

**Role** : The SHMViewFDStiffStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Stiffrning Rib in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgBTLFeatBF**(| ) As long

   Returns or sets SHMViewFDSurfFlgBTLFeatBF setting parameter value.

**Role** : The SHMViewFDSurfFlgBTLFeatBF setting parameter manage the visibility of the BTL Base Feature on a Surfacic Flange Brake formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgBTLFeatHF**(| ) As long

   Returns or sets SHMViewFDSurfFlgBTLFeatHF setting parameter value.

**Role** : The SHMViewFDSurfFlgBTLFeatHF setting parameter manage the visibility of the BTL Base Feature on a Surfacic Flange Hydro-Press formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgBTLSuppBF**(| ) As long

   Returns or sets SHMViewFDSurfFlgBTLSuppBF setting parameter value.

**Role** : The SHMViewFDSurfFlgBTLSuppBF setting parameter manage the visibility of the BTL Base Feature on a Surfacic Flange Brake formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgBTLSuppHF**(| ) As long

   Returns or sets SHMViewFDSurfFlgBTLSuppHF setting parameter value.

**Role** : The SHMViewFDSurfFlgBTLSuppHF setting parameter manage the visibility of the BTL Support on a Surfacic Flange Hydro-Press formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgIMLBF**(| ) As long

   Returns or sets SHMViewFDSurfFlgIMLBF setting parameter value.

**Role** : The SHMViewFDSurfFlgIMLBF setting parameter manage the visibility of the IML on a Surfacic Flange Brake formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgIMLHF**(| ) As long

   Returns or sets SHMViewFDSurfFlgIMLHF setting parameter value.

**Role** : The SHMViewFDSurfFlgIMLHF setting parameter manage the visibility of the IML on a Surfacic Flange Hydro-Press formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgOMLBF**(| ) As long

   Returns or sets SHMViewFDSurfFlgOMLBF setting parameter value.

**Role** : The SHMViewFDSurfFlgOMLBF setting parameter manage the visibility of the OML on a Surfacic Flange Brake formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfFlgOMLHF**(| ) As long

   Returns or sets SHMViewFDSurfFlgOMLHF setting parameter value.

**Role** : The SHMViewFDSurfFlgOMLHF setting parameter manage the visibility of the OML on a Surfacic Flange Hydro-Press formed in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDSurfStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDSurfStampBTLFeat setting parameter value.

**Role** : The SHMViewFDSurfStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Surface Stamp in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFDUserStampBTLFeat**(| ) As long

   Returns or sets SHMViewFDUserStampBTLFeat setting parameter value.

**Role** : The SHMViewFDUserStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a User Stamp in Folded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPBeadBTLFeat**(| ) As long

   Returns or sets SHMViewFPBeadBTLFeat setting parameter value.

**Role** : The SHMViewFPBeadBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Bead in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPCircStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPCircStampBTLFeat setting parameter value.

**Role** : The SHMViewFPCircStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Circular Stamp in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPCurveStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPCurveStampBTLFeat setting parameter value.

**Role** : The SHMViewFPCurveStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Curve Stamp in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgCutBTLFeat**(| ) As long

   Returns or sets SHMViewFPFlgCutBTLFeat setting parameter value.

**Role** : The SHMViewFPFlgCutBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Flanged Cutout in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgCutIML**(| ) As long

   Returns or sets SHMViewFPFlgCutIML setting parameter value.

**Role** : The SHMViewFPFlgCutIML setting parameter manage the visibility of the IML on a Flanged Cutout in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgCutOML**(| ) As long

   Returns or sets SHMViewFPFlgCutOML setting parameter value.

**Role** : The SHMViewFPFlgCutOML setting parameter manage the visibility of the OML on a Flanged Cutout in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgHoleBTLFeat**(| ) As long

   Returns or sets SHMViewFPFlgHoleBTLFeat setting parameter value.

**Role** : The SHMViewFPFlgHoleBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Flanged Hole in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgHoleIML**(| ) As long

   Returns or sets SHMViewFPFlgHoleIML setting parameter value.

**Role** : The SHMViewFPFlgHoleIML setting parameter manage the visibility of the IML on a Flanged Hole in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPFlgHoleOML**(| ) As long

   Returns or sets SHMViewFPFlgHoleOML setting parameter value.

**Role** : The SHMViewFPFlgHoleOML setting parameter manage the visibility of the OML on a Flanged Hole in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPOtherStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPOtherStampBTLFeat setting parameter value.

**Role** : The SHMViewFPOtherStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on an other Stamp ( F&A; -> Bridge, Louver ... ) in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPStiffStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPStiffStampBTLFeat setting parameter value.

**Role** : The SHMViewFPStiffStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Stiffening Rib in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgBTLFeatBF**(| ) As long

   Returns or sets SHMViewFPSurfFlgBTLFeatBF setting parameter value.

**Role** : The SHMViewFPSurfFlgBTLFeatBF setting parameter manage the visibility of the BTL Base Feature on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgBTLFeatHF**(| ) As long

   Returns or sets SHMViewFPSurfFlgBTLFeatHF setting parameter value.

**Role** : The SHMViewFPSurfFlgBTLFeatHF setting parameter manage the visibility of the BTL Base Feature on a Surfacic Flange Hydro-Press formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgBTLSuppBF**(| ) As long

   Returns or sets SHMViewFPSurfFlgBTLSuppBF setting parameter value.

**Role** : The SHMViewFPSurfFlgBTLSuppBF setting parameter manage the visibility of the BTL Support on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgBTLSuppHF**(| ) As long

   Returns or sets SHMViewFPSurfFlgBTLSuppHF setting parameter value.

**Role** : The SHMViewFPSurfFlgBTLSuppHF setting parameter manage the visibility of the BTL Support on a Surfacic Flange Hydro-Press formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgCLBBF**(| ) As long

   Returns or sets SHMViewFPSurfFlgCLBBF setting parameter value.

**Role** : The SHMViewFPSurfFlgCLBBF setting parameter manage the visibility of CLB on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgCLBHF**(| ) As long

   Returns or sets SHMViewFPSurfFlgCLBHF setting parameter value.

**Role** : The SHMViewFPSurfFlgCLBHF setting parameter manage the visibility of CLB on a Surfacic Flange Hydro-Pressed formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgIMLBF**(| ) As long

   Returns or sets SHMViewFPSurfFlgIMLBF setting parameter value.

**Role** : The SHMViewFPSurfFlgIMLBF setting parameter manage the visibility of the IML on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgIMLHF**(| ) As long

   Returns or sets SHMViewFPSurfFlgIMLHF setting parameter value.

**Role** : The SHMViewFPSurfFlgIMLHF setting parameter manage the visibility of the IML on a Surfacic Flange Hydro-Press formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgOML2BF**(| ) As long

   Returns or sets SHMViewFPSurfFlgOML2BF setting parameter value.

**Role** : The SHMViewFPSurfFlgOML2BF setting parameter manage the visibility of he Second OML on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgOML2HF**(| ) As long

   Returns or sets SHMViewFPSurfFlgOML2HF setting parameter value.

**Role** : The SHMViewFPSurfFlgOML2HF setting parameter manage the visibility of the Second OML on a Surfacic Flange Hydro-Press formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgOMLBF**(| ) As long

   Returns or sets SHMViewFPSurfFlgOMLBF setting parameter value.

**Role** : The SHMViewFPSurfFlgOMLBF setting parameter manage the visibility of the OML on a Surfacic Flange Brake formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfFlgOMLHF**(| ) As long

   Returns or sets SHMViewFPSurfFlgOMLHF setting parameter value.

**Role** : The SHMViewFPSurfFlgOMLHF setting parameter manage the visibility of the OML on a Surfacic Flange Hydro-Press formed in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPSurfStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPSurfStampBTLFeat setting parameter value.

**Role** : The SHMViewFPSurfStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a Surface Stamp in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
### Property **SHMViewFPUserStampBTLFeat**(| ) As long

   Returns or sets SHMViewFPUserStampBTLFeat setting parameter value.

**Role** : The SHMViewFPUserStampBTLFeat setting parameter manage the visibility of the BTL Base Feature on a User Stamp in UnFolded View.

**Legal values** :  | 1 | The characteristic curve is shown
---|---
0 | The characteristic curve is hidden
Methods
### Func **GetSHMViewFDBeadBTLFeatInfo**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `ioAdminLevel`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `ioLocked`) As boolean

   Retrieves information about the SHMViewFDBeadBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDCircStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDCircStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDCurveStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDCurveStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgCutBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgCutBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgCutIMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgCutIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgCutOMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgCutOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgHoleBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgHoleBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgHoleIMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgHoleIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDFlgHoleOMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDFlgHoleOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDOtherStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDOtherStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDStiffStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDStiffStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgBTLFeatBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgBTLFeatBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgBTLFeatHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgBTLFeatHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgBTLSuppBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgBTLSuppBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgBTLSuppHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgBTLSuppHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgIMLBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgIMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgIMLHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgIMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgOMLBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgOMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfFlgOMLHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfFlgOMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDSurfStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDSurfStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFDUserStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFDUserStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPBeadBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPBeadBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPCircStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPCircStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPCurveStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPCurveStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgCutBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgCutBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgCutIMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgCutIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgCutOMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgCutOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgHoleBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgHoleBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgHoleIMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgHoleIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPFlgHoleOMLInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPFlgHoleOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPOtherStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPOtherStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPStiffStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPStiffStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgBTLFeatBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgBTLFeatBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgBTLFeatHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgBTLFeatHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgBTLSuppBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgBTLSuppBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgBTLSuppHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgBTLSuppHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgCLBBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgCLBBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgCLBHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgCLBHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgIMLBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgIMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgIMLHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgIMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgOML2BFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgOML2BF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgOML2HFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgOML2HF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgOMLBFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgOMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfFlgOMLHFInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfFlgOMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPSurfStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPSurfStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSHMViewFPUserStampBTLFeatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the SHMViewFPUserStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDBeadBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDBeadBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDCircStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDCircStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDCurveStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDCurveStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgCutBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgCutBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgCutIMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgCutIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgCutOMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgCutOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgHoleBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgHoleBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgHoleIMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgHoleIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDFlgHoleOMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDFlgHoleOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDOtherStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDOtherStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDStiffStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDStiffStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgBTLFeatBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgBTLFeatBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgBTLFeatHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgBTLFeatHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgBTLSuppBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgBTLSuppBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgBTLSuppHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgBTLSuppHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgIMLBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgIMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgIMLHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgIMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgOMLBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgOMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfFlgOMLHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfFlgOMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDSurfStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDSurfStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFDUserStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFDUserStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPBeadBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPBeadBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPCircStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPCircStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPCurveStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPCurveStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgCutBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgCutBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgCutIMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgCutIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgCutOMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgCutOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgHoleBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgHoleBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgHoleIMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgHoleIML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPFlgHoleOMLLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPFlgHoleOML setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPOtherStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPOtherStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPStiffStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPStiffStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgBTLFeatBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgBTLFeatBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgBTLFeatHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgBTLFeatHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgBTLSuppBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgBTLSuppBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgBTLSuppHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgBTLSuppHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgCLBBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgCLBBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgCLBHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgCLBHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgIMLBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgIMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgIMLHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgIMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgOML2BFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgOML2BF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgOML2HFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgOML2HF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgOMLBFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgOMLBF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfFlgOMLHFLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfFlgOMLHF setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPSurfStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPSurfStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSHMViewFPUserStampBTLFeatLock**( boolean  `iLocked`)

   Locks or unlocks the SHMViewFPUserStampBTLFeat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.