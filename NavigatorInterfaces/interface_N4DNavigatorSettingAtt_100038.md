# N4DNavigatorSettingAtt (Object)

**_Interface to handle the settings of the DMU Navigator workbench._**

The different settings are:

DMUClashPreview:
Display of the preview viewer when editing an interference.

DMUDistancePreview:
Display of the preview viewer when editing a distance.

DMUGroupPreview:
Display of the preview viewer when editing a group.

DMUSectionPreview:
Display of the preview viewer when editing a section.

DMUShuttlePreview:
Display of the preview viewer when editing a shuttle.

DMUThicknessPreview:
Display of the preview viewer for the thickness command.

DMUOffsetPreview:
Display of the preview viewer for the offset command.

DMUSweptVolPreview:
Display of the preview viewer for the swept volume command.

DMUSilhouettePreview:
Display of the preview viewer for the silhouette command.

DMUWrappingPreview:
Display of the preview viewer for the wrapping command.

DMUFreeSpacePreview:
Display of the preview viewer for the free space command.

DMUSimplifPreview:
Display of the preview viewer for the simplification command.

DMUVibrationVolPreview:
Display of the preview viewer for the vibration volume command.

DMUCut3DPreview:
Display of the preview viewer for the 3D cut command.

DMUMergerPreview:
Display of the preview viewer for the merger command.

NumUrlName:
Display of the hyperlink name.

MarkerAutoUpdate:
Update on product structure modifications and scenes activation.

MarkerDefaultsColor:
Default color of an annotation.

SceneDefaultsColor:
Default background color for scene environment.

MarkerTextColor:
Default color of a text annotation.

MarkerDefaultsWeight:
Default weight value of an annotation.

MarkerDefaultsDashed:
Default dashed value of an annotation.

MarkerDefaultsSize:
Default size value of an annotation.

MarkerDefaultsFont:
Default font of an annotation.

MarkerTextDashed:
Default dashed value of a text annotation.

MarkerTextWeight:
Default weight value of a text annotation.

PublishAutoLaunchBrowser:
Automatic launching of publish results in a browser.

Marker2DAutoNaming:
Automatically use a Part's name as the default for the creation of text annotations.

Marker3DAutoNaming:
Activation of the mechanism that enables to transform temporary markers into persistent 3D annotations.

DMUReviewName:
The desired default name for DMU Reviews

ForceVoxel:
Force users of the Spatial Query command to use the defined Released Accuracy.

ClearanceVoxel:
Definition of the Clearance value.

ForceClearanceVoxel:
Force users of the Spatial Query command to use the defined Clearance value.

InsertMode:
Mode for the Import applicative data command.

DMUGroupPreviewHiddenObjectsDisplayMode:
Display mode for hidden objects of a DMU Group in its preview: visualized as in main 3D viewer or visualized with customized graphic properties

DMUGroupPreviewHiddenObjectsColor:
Color for hidden objects in DMU Group Preview.

DMUGroupPreviewHiddenObjectsOpacity:
Opacity for hidden objects in DMU Group Preview.

DMUGroupPreviewHiddenObjectsLowIntMode:
Hidden objects are low intensified or not in DMU Group Preview.

DMUGroupPreviewHiddenObjectsPickMode:
Hidden objects can be picked or not in DMU Group Preview.

## Properties

### Property **ClearanceVoxel**(| ) As float

   Returns or sets the clearance value (oValue the clearance value in mm).  
### Property **DMUClashPreview**( ) As boolean

   Returns or sets the preview activation state for Interference (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUCut3DPreview**( ) As boolean

   Returns or sets the preview activation state for 3D Cut (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUDistancePreview**( ) As boolean

   Returns or sets the preview activation state for Distance (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUFreeSpacePreview**( ) As boolean

   Returns or sets the preview activation state for Free Space (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUGroupPreview**( ) As boolean

   Returns or sets the preview activation state for Group (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUGroupPreviewHiddenObjectsDisplayMode**( ) As [CatDMUGroupPreviewHiddenObjectsDisplayMode](../NavigatorInterfaces/enum_CatDMUGroupPreviewHiddenObjectsDisplayMode_359864.md)

   Returns or sets the mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsLowInt**( ) As boolean

   Returns or sets the Low Intensity mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsOpacity**( ) As long

   Returns or sets the opacity for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsPick**( ) As boolean

   Returns or sets the pick mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUMergerPreview**( ) As boolean

   Returns or sets the preview activation state for Merger (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUOffsetPreview**( ) As boolean

   Returns or sets the preview activation state for Offset (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUReviewName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the default name for the DMU Reviews (oValue, the DMU Review name).  
### Property **DMUSectionPreview**( ) As boolean

   Returns or sets the preview activation state for Section (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUShuttlePreview**( ) As boolean

   Returns or sets the preview activation state for Shuttle (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSilhouettePreview**( ) As boolean

   Returns or sets the preview activation state for Silhouette (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSimplifPreview**( ) As boolean

   Returns or sets the preview activation state for Simplification (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSweptVolPreview**( ) As boolean

   Returns or sets the preview activation state for Swept Volume (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUThicknessPreview**( ) As boolean

   Returns or sets the preview activation state for Thickness (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUVibrationVolPreview**( ) As boolean

   Returns or sets the preview activation state for Vibration volume (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUWrappingPreview**( ) As boolean

   Returns or sets the preview activation state for Wrapping (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **ForceClearanceVoxel**( ) As boolean

   Returns or sets the activation state for the use of the clearance value (TRUE the clearance value is used, FALSE the clearance value is not used);  
### Property **ForceVoxel**( ) As boolean

   Returns or sets the activation state for the use of the Released accuracy value (TRUE the released accuracy value is used, FALSE the released accuracy value is not used);  
### Property **InsertLevel**( ) As boolean

   Returns or sets the level for the Import Applicative Data command (True : at highest review level, False : in current review).  
### Property **InsertMode**( ) As [CatSacSettingsEnum](../NavigatorInterfaces/enum_CatSacSettingsEnum_68200.md)

   Returns or sets the mode for the Import Applicative Data command (CatSacSettingsEnumNoInsert no import of applicative data, CatSacSettingsEnumAutomatic the import of applicative is automatic, CatSacSettingsEnumUserPrompt the user can select the applicative data to import).  
### Property **Marker2DAutoNaming**( ) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_Marker2DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_Marker2DAutoNaming) This method will be replaced by [MarkerSettingAtt.put_Marker2DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_Marker2DAutoNaming) Returns or sets the activation state for 2D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **Marker3DAutoNaming**( ) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_Marker3DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_Marker3DAutoNaming) This method will be replaced by [MarkerSettingAtt.put_Marker3DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_Marker3DAutoNaming) Returns or sets the activation state for 3D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **MarkerAutoUpdate**( ) As boolean

   Returns or sets the activation of the automatic update on product structure modification (TRUE update is done automatically, FALSE update is done manually).  
### Property **MarkerDefaultsDashed**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerDefaultsDashed](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerDefaultsDashed) This method will be replaced by [MarkerSettingAtt.put_MarkerDefaultsDashed](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerDefaultsDashed) Returns or sets the default dashed value of an annotation (oValue the dashed value).  
### Property **MarkerDefaultsFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDefaultsFont2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDefaultsFont2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDefaultsFont2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDefaultsFont2D) Returns or sets the default font of an annotation (oValue the font name).  
### Property **MarkerDefaultsSize**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDefaultsSize2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDefaultsSize2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDefaultsSize2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDefaultsSize2D) Returns or sets the default size value of an annotation (oValue the size value)..  
### Property **MarkerDefaultsWeight**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerDefaultsWeight](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerDefaultsWeight) This method will be replaced by [MarkerSettingAtt.put_MarkerDefaultsWeight](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerDefaultsWeight) Returns or sets the default weight value of an annotation (oValue the weight value).  
### Property **MarkerTextDashed**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDashed2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDashed2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDashed2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDashed2D) Returns or sets the default dashed value of a text annotation (oValue the dashed value).  
### Property **MarkerTextWeight**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextWeight2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextWeight2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextWeight2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextWeight2D) Returns or sets the default weight value of a text annotation (oValue the weight value).  
### Property **NumUrlName**( ) As boolean

   Returns or sets the name activation state for Hyperlink (TRUE the hyperlink name is displayed, FALSE the hyperlink name is not displayed).  
### Property **PublishAutoLaunchBrowser**( ) As boolean

   Returns or sets the activation state of the automatic launching of the publish browser (TRUE the publish browser is automatically opened, FALSE the publish browser is not automatically opened).  Methods

### Func **GetClearanceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ClearanceVoxel parameter.

**Role** :Retrieves the state of the ClearanceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUClashPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUClashPreview parameter.

**Role** :Retrieves the state of the DMUClashPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUCut3DPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUCut3DPreview parameter.

**Role** :Retrieves the state of the DMUCut3DPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUDistancePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUDistancePreview parameter.

**Role** :Retrieves the state of the DMUDistancePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUFreeSpacePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUFreeSpacePreview parameter.

**Role** :Retrieves the state of the DMUFreeSpacePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetDMUGroupPreviewHiddenObjectsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

   Returns the color for the display of hidden objects in DMU Group Preview.  
### Func **GetDMUGroupPreviewHiddenObjectsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsColor parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsDisplayModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsDisplayMode parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsDisplayMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsLowIntInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsLowInt parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsLowInt parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsOpacityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsOpacity parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsOpacity parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsPickInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsPick parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsPick parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreview parameter.

**Role** :Retrieves the state of the DMUGroupPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUMergerPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUMergerPreview parameter.

**Role** :Retrieves the state of the DMUMergerPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUOffsetPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUOffsetPreview parameter.

**Role** :Retrieves the state of the DMUOffsetPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUReviewNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUReviewName parameter.

**Role** :Retrieves the state of the DMUReviewName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSectionPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSectionPreview parameter.

**Role** :Retrieves the state of the DMUSectionPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUShuttlePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUShuttlePreview parameter.

**Role** :Retrieves the state of the DMUShuttlePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSilhouettePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSilhouettePreview parameter.

**Role** :Retrieves the state of the DMUSilhouettePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSimplifPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSimplifPreview parameter.

**Role** :Retrieves the state of the DMUSimplifPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSweptVolPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSweptVolPreview parameter.

**Role** :Retrieves the state of the DMUSweptVolPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUThicknessPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUThicknessPreview parameter.

**Role** :Retrieves the state of the DMUThicknessPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUVibrationVolPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUVibrationVolPreview parameter.

**Role** :Retrieves the state of the DMUVibrationVolPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUWrappingPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUWrappingPreview parameter.

**Role** :Retrieves the state of the DMUWrappingPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetForceClearanceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ForceClearanceVoxel parameter.

**Role** :Retrieves the state of the ForceClearanceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetForceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ForceVoxel parameter.

**Role** :Retrieves the state of the ForceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetInsertLevelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the InsertLevel parameter.

**Role** :Retrieves the state of the InsertLevel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetInsertModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the InsertMode parameter.

**Role** :Retrieves the state of the InsertMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker2DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarker2DAutoNamingInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarker2DAutoNamingInfo) Retrieves environment informations for the Marker2DAutoNaming parameter.

**Role** :Retrieves the state of the Marker2DAutoNaming parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker3DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarker3DAutoNamingInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarker3DAutoNamingInfo) Retrieves environment informations for the Marker3DAutoNaming parameter.

**Role** :Retrieves the state of the Marker3DAutoNaming parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerAutoUpdateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerAutoUpdate parameter.

**Role** :Retrieves the state of the MarkerAutoUpdate parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerDefaultsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsColor](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsColor) Returns the default color of an annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsColorInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsColorInfo) Retrieves environment informations for the MarkerDefaultsColor parameter.

**Role** :Retrieves the state of the MarkerDefaultsColor parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsDashedInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsDashedInfo) Retrieves environment informations for the MarkerDefaultsDashed parameter.

**Role** :Retrieves the state of the MarkerDefaultsDashed parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsFontInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsFont2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsFont2DInfo) Retrieves environment informations for the MarkerDefaultsFont parameter.

**Role** :Retrieves the state of the MarkerDefaultsFont parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by CATIAmarkerSettingAtt Retrieves environment informations for the MarkerDefaultsSize parameter.

**Role** :Retrieves the state of the MarkerDefaultsSize parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsWeightInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsWeightInfo) Retrieves environment informations for the MarkerDefaultsWeight parameter.

**Role** :Retrieves the state of the MarkerDefaultsWeight parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextColor2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextColor2DInfo) Returns the default color of a text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextColor2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextColor2DInfo) Retrieves environment informations for the MarkerTextColor parameter.

**Role** :Retrieves the state of the MarkerTextColor parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextDashed2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextDashed2DInfo) Retrieves environment informations for the MarkerTextDashed parameter.

**Role** :Retrieves the state of the MarkerTextDashed parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextWeight2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextWeight2DInfo) Retrieves environment informations for the MarkerTextWeight parameter.

**Role** :Retrieves the state of the MarkerTextWeight parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNumUrlNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the NumUrlName parameter.

**Role** :Retrieves the state of the NumUrlName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPublishAutoLaunchBrowserInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PublishAutoLaunchBrowser parameter.

**Role** :Retrieves the state of the PublishAutoLaunchBrowser parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetSceneDefaultsColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the scene background color (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetSceneDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SceneDefaultsColor parameter.

**Role** :Retrieves the state of the SceneDefaultsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetClearanceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ClearanceVoxel parameter.

**Role** :Locks or unlocks the ClearanceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUClashPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUClashPreview parameter.

**Role** :Locks or unlocks the DMUClashPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUCut3DPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUCut3DPreview parameter.

**Role** :Locks or unlocks the DMUCut3DPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUDistancePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUDistancePreview parameter.

**Role** :Locks or unlocks the DMUDistancePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUFreeSpacePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUFreeSpacePreview parameter.

**Role** :Locks or unlocks the DMUFreeSpacePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

   Sets the color for the display of hidden objects in DMU Group Preview.  
### Sub **SetDMUGroupPreviewHiddenObjectsColorLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsColor parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsDisplayModeLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsDisplayMode parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsDisplayMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsLowIntLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsLowInt parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsLowInt parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsOpacityLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsOpacity parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsOpacity parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsPickLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsPick parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsPick parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreview parameter.

**Role** :Locks or unlocks the DMUGroupPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUMergerPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUMergerPreview parameter.

**Role** :Locks or unlocks the DMUMergerPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUOffsetPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUOffsetPreview parameter.

**Role** :Locks or unlocks the DMUOffsetPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUReviewNameLock**( boolean  `iLocked`)

   Locks or unlocks the DMUReviewName parameter.

**Role** :Locks or unlocks the DMUReviewName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSectionPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSectionPreview parameter.

**Role** :Locks or unlocks the DMUSectionPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUShuttlePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUShuttlePreview parameter.

**Role** :Locks or unlocks the DMUShuttlePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSilhouettePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSilhouettePreview parameter.

**Role** :Locks or unlocks the DMUSilhouettePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSimplifPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSimplifPreview parameter.

**Role** :Locks or unlocks the DMUSimplifPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSweptVolPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSweptVolPreview parameter.

**Role** :Locks or unlocks the DMUSweptVolPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUThicknessPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUThicknessPreview parameter.

**Role** :Locks or unlocks the DMUThicknessPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUVibrationVolPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUVibrationVolPreview parameter.

**Role** :Locks or unlocks the DMUVibrationVolPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUWrappingPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUWrappingPreview parameter.

**Role** :Locks or unlocks the DMUWrappingPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetForceClearanceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ForceClearanceVoxel parameter.

**Role** :Locks or unlocks the ForceClearanceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetForceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ForceVoxel parameter.

**Role** :Locks or unlocks the ForceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetInsertLevelLock**( boolean  `iLocked`)

   Locks or unlocks the InsertMode parameter.

**Role** :Locks or unlocks the InsertMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetInsertModeLock**( boolean  `iLocked`)

   Locks or unlocks the InsertMode parameter.

**Role** :Locks or unlocks the InsertMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker2DAutoNamingLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarker2DAutoNamingLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarker2DAutoNamingLock) Locks or unlocks the Marker2DAutoNaming parameter.

**Role** :Locks or unlocks the Marker2DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker3DAutoNamingLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarker3DAutoNamingLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarker3DAutoNamingLock) Locks or unlocks the Marker3DAutoNaming parameter.

**Role** :Locks or unlocks the Marker3DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerAutoUpdateLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerAutoUpdate parameter.

**Role** :Locks or unlocks the MarkerAutoUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsColor](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsColor) Sets the default color of an annotation (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetMarkerDefaultsColorLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsColorLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsColorLock) Locks or unlocks the MarkerDefaultsColor parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsDashedLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsDashedLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsDashedLock) Locks or unlocks the MarkerDefaultsDashed parameter.

**Role** :Locks or unlocks the MarkerDefaultsDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsFontLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsFont2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsFont2DLock) Locks or unlocks the MarkerDefaultsFont parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsSizeLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextDefaultsSize2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextDefaultsSize2DLock) Locks or unlocks the MarkerDefaultsSize parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsWeightLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsWeightLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsWeightLock) Locks or unlocks the MarkerDefaultsWeight parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextColor2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextColor2D) Sets the default color of a text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColorLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextColor2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextColor2DLock) Locks or unlocks the MarkerTextColor parameter.

**Role** :Locks or unlocks the MarkerTextColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashedLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextDashed2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextDashed2DLock) Locks or unlocks the MarkerTextDashed parameter.

**Role** :Locks or unlocks the MarkerTextDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeightLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextWeight2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextWeight2DLock) Locks or unlocks the MarkerTextWeight parameter.

**Role** :Locks or unlocks the MarkerTextWeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNumUrlNameLock**( boolean  `iLocked`)

   Locks or unlocks the NumUrlName parameter.

**Role** :Locks or unlocks the NumUrlName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPublishAutoLaunchBrowserLock**( boolean  `iLocked`)

   Locks or unlocks the PublishAutoLaunchBrowser parameter.

**Role** :Locks or unlocks the PublishAutoLaunchBrowser parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSceneDefaultsColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the scene background color (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetSceneDefaultsColorLock**( boolean  `iLocked`)

   Locks or unlocks the SceneDefaultsColor parameter.

**Role** :Locks or unlocks the SceneDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.