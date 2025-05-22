# VisualizationSettingAtt (Object)

**_The interface to access a CATIAVisualizationSettingAtt._**

## Properties

### Property **AccuratePickingMode**( ) As boolean

Returns the AccuratePickingMode parameter.  
### Property **AccuratePickingWindowSize**( ) As long

Returns the AccuratePickingWindowSize parameter.  
### Property **AllZBufferElementMode**( ) As boolean

Returns the AllZBufferElementMode parameter.  
### Property **AmbientActivation**( ) As long

Returns the AmbientActivation parameter.  
### Property **AntiAliasingMode**( ) As boolean

Returns the AntiAliasingMode parameter.  
### Property **AntiAliasingOffset**( ) As double

Returns the AntiAliasingOffset parameter.  
### Property **AuxiliaryDrillViewer**( ) As boolean

Returns the AuxiliaryDrillViewer parameter.  
### Property **BackFaceCullingMode**( ) As boolean

**Deprecated:**      V5R16. Returns the BackFaceCullingMode parameter.  
### Property **BorderEdgesMode**( ) As boolean

Returns the BorderEdgesMode parameter.  
### Property **BorderEdgesThickness**( ) As long

Returns the BorderEdgesThickness parameter.  
### Property **BoundingBoxSelectionMode**( ) As boolean

Returns the BoundingBoxSelectionMode parameter.  
### Property **ColorBackgroundMode**( ) As boolean

Returns the ColorBackgroundMode parameter.  
### Property **DefaultDiffuseAmbientCoefficient**( ) As double

Returns the AmbientActivation parameter.  
### Property **DefaultShininess**( ) As double

Returns the AmbientActivation parameter.  
### Property **DefaultSpecularCoefficient**( ) As double

Returns the AmbientActivation parameter.  
### Property **DisplayCurrentScale**( ) As boolean

Returns the SetStereoModeLock parameter.  
### Property **DisplayDrillList**( ) As boolean

Returns the DisplayDrillList parameter.  
### Property **DisplayImmersiveDrillViewer**( ) As boolean

Returns the DisplayImmersiveDrillViewer parameter.  
### Property **DynamicCull**( ) As long

Returns the DynamicCull parameter.  
### Property **DynamicLOD**( ) As double

Returns the DynamicLOD parameter.  
### Property **FaceHLDrill**( ) As boolean

Returns the FaceHLDrill parameter.  
### Property **FlyCollisionMode**( ) As boolean

Returns the FlyCollisionMode parameter.  
### Property **FlyCollisionSphereRadius**( ) As double

Returns the FlyCollisionSphereRadius parameter.  
### Property **FlyCollisionType**( ) As long

Returns the FlyCollisionType parameter.  
### Property **FlySensitivity**( ) As long

Returns the FlySensitivity parameter.  
### Property **FlySpeed**( ) As long

Returns the FlySpeed parameter.  
### Property **FlySpeedMode**( ) As long

Returns the FlySpeedMode parameter.  
### Property **FollowGroundAltitude**( ) As double

Returns the FollowGroundAltitude parameter.  
### Property **FollowGroundMode**( ) As boolean

Returns the FollowGroundMode parameter.  
### Property **FullSceneAntiAliasingMode**( ) As [CATFullSceneAntiAliasingMode](../InfInterfaces/enum_CATFullSceneAntiAliasingMode_156888.md)

Returns the AntiAliasingMode parameter.  
### Property **Gravity**( ) As boolean

Returns the Gravity parameter.  
### Property **GravityAxis**( ) As long

Returns the GravityAxis parameter.  
### Property **HaloMode**( ) As boolean

Returns the HaloMode parameter.  
### Property **IsoparGenerationMode**( ) As boolean

Returns the IsoparGenerationMode parameter.  
### Property **KeyboardRotationAngleValue**( ) As long

Retrieves the angle value for rotations operated through key combinations.  
### Property **LightViewerMode**( ) As boolean

Returns the LightViewerMode parameter.  
### Property **LineicCgrMode**( ) As boolean

Returns the LineicCgrMode parameter.  
### Property **MaxSelectionMove**( ) As long

Returns the MaxSelectionMove parameter.  
### Property **MinimumFPSMode**( ) As boolean

Returns the MinimumFPSMode parameter.  
### Property **MinimumSpaceFPSMode**( ) As boolean

Returns the MinimumSpaceFPSMode parameter.  
### Property **MouseDoubleClicDelay**( ) As long

Returns the MouseDoubleClicDelay parameter.  
### Property **MouseSpeedValue**( ) As long

Returns the MouseSpeedValue parameter.  
### Property **NbIsopars**( ) As long

Returns the NbIsopars parameter.  
### Property **NoZBufferSelectionMode**( ) As boolean

Returns the NoZBufferSelectionMode parameter.  
### Property **NumberOfMinimumFPS**( ) As long

Returns the NumberOfMinimumFPS parameter.  
### Property **NumberOfMinimumSpaceFPS**( ) As long

Returns the NumberOfMinimumSpaceFPS parameter.  
### Property **OcclusionCullingMode**( ) As boolean

Returns the OcclusionCullingMode parameter.  
### Property **OpaqueFaces**( ) As boolean

Returns the SetStereoModeLock parameter.  
### Property **OtherSelectionTimeout**( ) As double

Returns the OtherSelectionTimeout parameter.  
### Property **OtherSelectionTimeoutActivity**( ) As boolean

Returns the OtherSelectionTimeoutActivity parameter.  
### Property **PickingWindowSize**( ) As long

Returns the PickingWindowSize parameter.  
### Property **PreSelectionMode**( ) As boolean

Returns the PreSelectionMode parameter.  
### Property **PreselectedElementLinetype**( ) As long

Returns the PreselectedElementLinetype parameter.  
### Property **RotationSphereMode**( ) As boolean

Returns the RotationSphereMode parameter.  
### Property **ShaderMode**( ) As boolean

Returns the ShaderMode parameter.  
### Property **StaticCull**( ) As long

Returns the StaticCull parameter.  
### Property **StaticLOD**( ) As double

Returns the StaticLOD parameter.  
### Property **StereoMode**( ) As boolean

Returns the StereoMode parameter.  
### Property **TransparencyMode**( ) As boolean

Returns the TransparencyMode parameter.  
### Property **TwoSideLightingMode**( ) As boolean

Returns the TwoSideLightingMode parameter.  
### Property **ViewpointAnimationMode**( ) As boolean

Returns the ViewpointAnimationMode parameter.  
### Property **Viz2DAccuracyMode**( ) As boolean

Returns the 2DAccuracyMode parameter.  
### Property **Viz2DFixedAccuracy**( ) As double

Returns the 2DFixedAccuracy parameter.  
### Property **Viz2DProportionnalAccuracy**( ) As double

Returns the 2DProportionnalAccuracy parameter.  
### Property **Viz3DAccuracyMode**( ) As boolean

Returns the Viz3DAccuracyMode parameter.  
### Property **Viz3DCurveAccuracy**( ) As double

Returns the 3DCurveAccuracy parameter.  
### Property **Viz3DFixedAccuracy**( ) As double

Returns the 3DFixedAccuracy parameter.  
### Property **Viz3DProportionnalAccuracy**( ) As double

Returns the Viz3DProportionnalAccuracy parameter.  Methods

### Func **GetAccuratePickingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AccuratePickingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAccuratePickingWindowSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AccuratePickingWindowSize setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAllZBufferElementModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AllZBufferElementMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAmbientActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AmbientActivation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAntiAliasingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AntiAliasingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAntiAliasingOffsetInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AntiAliasingOffset setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAuxiliaryDrillViewerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AuxiliaryDrillViewer setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetBackFaceCullingMode**( ) As [CATBackFaceCullingMode](../InfInterfaces/enum_CATBackFaceCullingMode_95180.md)

Retrieves the BackFaceCullingMode parameter.

**Parameters:**

` oBackFaceCullingMode`      Value of the back face culling mode setting option. The retrieved value can be one of the four possible values defined by the
[CATBackFaceCullingMode](../InfInterfaces/enum_CATBackFaceCullingMode_95180.md) enumeration.  **Returns:**      An HRESULT.
**Legal values** :

S_OK      if the operation succeeded. E_FAIL      if the operation failed.  
### Func **GetBackFaceCullingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BackFaceCullingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetBackgroundRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the BackgroundRGB parameter.  
### Func **GetBackgroundRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BackgroundRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetBorderEdgesModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BorderEdgesMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetBorderEdgesRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the BorderEdgesRGB parameter.  
### Func **GetBorderEdgesRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BorderEdgesRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetBorderEdgesThicknessInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BorderEdgesThickness setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetBoundingBoxSelectionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the BoundingBoxSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetColorBackgroundModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ColorBackgroundMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultDiffuseAmbientCoefficientInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DefaultDiffuseAmbientCoefficient setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultShininessInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DefaultShininess setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDefaultSpecularCoefficientInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DefaultSpecularCoefficient setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayCurrentScaleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the SetStereoModeLock setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayDrillListInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DisplayDrillList setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayImmersiveDrillViewerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DisplayImmersiveDrillViewer setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDynamicCullInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DynamicCull setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDynamicLODInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the DynamicLOD setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFaceHLDrillInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FaceHLDrill setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlyCollisionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlyCollisionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlyCollisionSphereRadiusInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlyCollisionSphereRadius setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlyCollisionTypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlyCollisionType setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlySensitivityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlySensitivity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlySpeedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlySpeed setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFlySpeedModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FlySpeedMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFollowGroundAltitudeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FollowGroundAltitude setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFollowGroundModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the FollowGroundMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetFullSceneAntiAliasingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the AntiAliasingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGravityAxisInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the GravityAxis setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGravityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the Gravity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetHaloModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the HaloMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetHandlesRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the HandlesRGB parameter.  
### Func **GetHandlesRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the HandlesRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetIsoparGenerationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the IsoparGenerationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetKeyboardRotationAngleValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the KeyboardRotationAngleValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLightViewerModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the LightViewerMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLineicCgrModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the LineicCgrMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMaxSelectionMoveInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the MaxSelectionMove setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMinimumFPSModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the MinimumFPSMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMinimumSpaceFPSModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the MinimumSpaceFPSMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMouseDoubleClicDelayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the MouseDoubleClicDelay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMouseSpeedValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the MouseSpeedValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetNbIsoparsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the NbIsopars setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetNoShowBackgroundRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Retrieves the No Show Background Color setting attribute value.
**Role** : The No Show Background Color setting attribute manages the backgraound color of no show space

**Parameters:**

` ioR,`      ioG, ioB [inout] The Red, Green, Blue components of the No Show Background Color setting attribute value
**Returns:**      S_OK if the No Show Background Color setting attribute value is successfully retrieved, and E_FAIL otherwise  
### Func **GetNoShowBackgroundRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves the No Show Background Color setting attribute information.

**Parameters:**

` ioAdminLevel,`      ioLocked [inout] and oModified [out] The No Show Background Color setting attribute information
**Returns:**      S_OK if the No Show Background Color setting attribute information is successfully retrieved, and E_FAIL otherwise
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetNoZBufferSelectionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the NoZBufferSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetNumberOfMinimumFPSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the NumberOfMinimumFPS setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetNumberOfMinimumSpaceFPSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the NumberOfMinimumSpaceFPS setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetOcclusionCullingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the OcclusionCullingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetOpaqueFacesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the SetStereoModeLock setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetOtherSelectionTimeoutActivityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the OtherSelectionTimeoutActivity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetOtherSelectionTimeoutInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the OtherSelectionTimeout setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetPickingWindowSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the PickingWindowSize setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetPreSelectionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the PreSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetPreselectedElementLinetypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the PreselectedElementLinetype setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetPreselectedElementRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the PreselectedElementRGB parameter.  
### Func **GetPreselectedElementRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the PreselectedElementRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetRotationSphereModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the RotationSphereMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetSelectedEdgeRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the SelectedEdgeRGB parameter.  
### Func **GetSelectedEdgeRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the SelectedEdgeRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetSelectedElementRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the SelectedElementRGB parameter.  
### Func **GetSelectedElementRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the SelectedElementRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetShaderModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ShaderMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStaticCullInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the StaticCull setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStaticLODInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the StaticLOD setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStereoModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the StereoMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetTransparencyModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the TransparencyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetTwoSideLightingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the TwoSideLightingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetUnderIntensifiedRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the UnderIntensifiedRGB parameter.  
### Func **GetUnderIntensifiedRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the UnderIntensifiedRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetUpdateNeededRGB**( long  `ioR`,  long  `ioG`,  long  `ioB`)

Returns the UpdateNeededRGB parameter.  
### Func **GetUpdateNeededRGBInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the UpdateNeededRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewpointAnimationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the ViewpointAnimationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz2DAccuracyModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the 2DAccuracyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz2DFixedAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the 2DFixedAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz2DProportionnalAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the 2DProportionnalAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz3DAccuracyModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the Viz3DAccuracyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz3DCurveAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the 3DCurveAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz3DFixedAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the 3DFixedAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViz3DProportionnalAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves information about the Viz3DProportionnalAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **PutBackFaceCullingMode**( [CATBackFaceCullingMode](../InfInterfaces/enum_CATBackFaceCullingMode_95180.md)  `iBackFaceCullingMode`)

Sets the BackFaceCullingMode attribute.

**Parameters:**

` iBackFaceCullingMode`      Value of the back face culling mode setting option. The value to set can be one of the four possible values defined by the
[CATBackFaceCullingMode](../InfInterfaces/enum_CATBackFaceCullingMode_95180.md) enumeration.  **Returns:**      An HRESULT.
**Legal values** :

S_OK      if the operation succeeded. E_FAIL      if the operation failed.  
### Sub **SetAccuratePickingModeLock**( boolean  `iLocked`)

Locks or unlocks the AccuratePickingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAccuratePickingWindowSizeLock**( boolean  `iLocked`)

Locks or unlocks the AccuratePickingWindowSize setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAllZBufferElementModeLock**( boolean  `iLocked`)

Locks or unlocks the AllZBufferElementMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAmbientActivationLock**( boolean  `iLocked`)

Locks or unlocks the AmbientActivation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAntiAliasingModeLock**( boolean  `iLocked`)

Locks or unlocks the AntiAliasingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAntiAliasingOffsetLock**( boolean  `iLocked`)

Locks or unlocks the AntiAliasingOffset setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAuxiliaryDrillViewerLock**( boolean  `iLocked`)

Locks or unlocks the AuxiliaryDrillViewer setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBackFaceCullingModeLock**( boolean  `iLocked`)

Locks or unlocks the BackFaceCullingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBackgroundRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the BackgroundRGB parameter.  
### Sub **SetBackgroundRGBLock**( boolean  `iLocked`)

Locks or unlocks the BackgroundRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBorderEdgesModeLock**( boolean  `iLocked`)

Locks or unlocks the BorderEdgesMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBorderEdgesRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the BorderEdgesRGB parameter.  
### Sub **SetBorderEdgesRGBLock**( boolean  `iLocked`)

Locks or unlocks the BorderEdgesRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBorderEdgesThicknessLock**( boolean  `iLocked`)

Locks or unlocks the BorderEdgesThickness setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetBoundingBoxSelectionModeLock**( boolean  `iLocked`)

Locks or unlocks the BoundingBoxSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetColorBackgroundModeLock**( boolean  `iLocked`)

Locks or unlocks the ColorBackgroundMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultDiffuseAmbientCoefficientLock**( boolean  `iLocked`)

Locks or unlocks the DefaultDiffuseAmbientCoefficient setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultShininessLock**( boolean  `iLocked`)

Locks or unlocks the DefaultShininess setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDefaultSpecularCoefficientLock**( boolean  `iLocked`)

Locks or unlocks the DefaultSpecularCoefficient setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayCurrentScaleLock**( boolean  `iLocked`)

Locks or unlocks the SetStereoModeLock setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayDrillListLock**( boolean  `iLocked`)

Locks or unlocks the DisplayDrillList setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayImmersiveDrillViewerLock**( boolean  `iLocked`)

Locks or unlocks the DisplayImmersiveDrillViewer setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDynamicCullLock**( boolean  `iLocked`)

Locks or unlocks the DynamicCull setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDynamicLODLock**( boolean  `iLocked`)

Locks or unlocks the DynamicLOD setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFaceHLDrillLock**( boolean  `iLocked`)

Locks or unlocks the FaceHLDrill setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlyCollisionModeLock**( boolean  `iLocked`)

Locks or unlocks the FlyCollisionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlyCollisionSphereRadiusLock**( boolean  `iLocked`)

Locks or unlocks the FlyCollisionSphereRadius setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlyCollisionTypeLock**( boolean  `iLocked`)

Locks or unlocks the FlyCollisionType setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlySensitivityLock**( boolean  `iLocked`)

Locks or unlocks the FlySensitivity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlySpeedLock**( boolean  `iLocked`)

Locks or unlocks the FlySpeed setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFlySpeedModeLock**( boolean  `iLocked`)

Locks or unlocks the FlySpeedMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFollowGroundAltitudeLock**( boolean  `iLocked`)

Locks or unlocks the FollowGroundAltitude setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFollowGroundModeLock**( boolean  `iLocked`)

Locks or unlocks the FollowGroundMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetFullSceneAntiAliasingModeLock**( boolean  `iLocked`)

Locks or unlocks the AntiAliasingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGravityAxisLock**( boolean  `iLocked`)

Locks or unlocks the GravityAxis setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGravityLock**( boolean  `iLocked`)

Locks or unlocks the Gravity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetHaloModeLock**( boolean  `iLocked`)

Locks or unlocks the HaloMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetHandlesRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the HandlesRGB parameter.  
### Sub **SetHandlesRGBLock**( boolean  `iLocked`)

Locks or unlocks the HandlesRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetIsoparGenerationModeLock**( boolean  `iLocked`)

Locks or unlocks the IsoparGenerationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetKeyboardRotationAngleValueLock**( boolean  `iLocked`)

Locks or unlocks the KeyboardRotationAngleValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLightViewerModeLock**( boolean  `iLocked`)

Locks or unlocks the LightViewerMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLineicCgrModeLock**( boolean  `iLocked`)

Locks or unlocks the v setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMaxSelectionMoveLock**( boolean  `iLocked`)

Locks or unlocks the MaxSelectionMove setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMinimumFPSModeLock**( boolean  `iLocked`)

Locks or unlocks the MinimumFPSMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMinimumSpaceFPSModeLock**( boolean  `iLocked`)

Locks or unlocks the MinimumSpaceFPSMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMouseDoubleClicDelayLock**( boolean  `iLocked`)

Locks or unlocks the MouseDoubleClicDelay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMouseSpeedValueLock**( boolean  `iLocked`)

Locks or unlocks the MouseSpeedValue setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNbIsoparsLock**( boolean  `iLocked`)

Locks or unlocks the NbIsopars setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNoShowBackgroundRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the No Show Background Color setting attribute value.
**Role** : The No Show Background Color setting attribute manages the backgraound color of no show space

**Parameters:**

` iR,`      iG, iB [in] The Red, Green, Blue components of the No Show Background Color setting attribute value
**Legal values** : between 0 and 255
**Returns:**      S_OK if the No Show Background Color setting attribute value is successfully set, and E_FAIL otherwise  
### Sub **SetNoShowBackgroundRGBLock**( boolean  `iLocked`)

Locks or unlocks the No Show Background Color setting attribute.
**Role** : Locks or unlocks the No Show Background Color setting attribute if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      [in] A flag to indicate whether the No Show Background Color setting attribute should be locked.
**Legal values** :
`TRUE` to lock
`FALSE` to unlock
**Returns:**      S_OK if the No Show Background Color setting attribute is successfully locked or unlocked, and E_FAIL otherwise
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNoZBufferSelectionModeLock**( boolean  `iLocked`)

Locks or unlocks the NoZBufferSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNumberOfMinimumFPSLock**( boolean  `iLocked`)

Locks or unlocks the NumberOfMinimumFPS setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetNumberOfMinimumSpaceFPSLock**( boolean  `iLocked`)

Locks or unlocks the NumberOfMinimumSpaceFPS setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetOcclusionCullingModeLock**( boolean  `iLocked`)

Locks or unlocks the OcclusionCullingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetOpaqueFacesLock**( boolean  `iLocked`)

Locks or unlocks the SetStereoModeLock setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetOtherSelectionTimeoutActivityLock**( boolean  `iLocked`)

Locks or unlocks the OtherSelectionTimeoutActivity setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetOtherSelectionTimeoutLock**( boolean  `iLocked`)

Locks or unlocks the OtherSelectionTimeout setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPickingWindowSizeLock**( boolean  `iLocked`)

Locks or unlocks the PickingWindowSize setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPreSelectionModeLock**( boolean  `iLocked`)

Locks or unlocks the PreSelectionMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPreselectedElementLinetypeLock**( boolean  `iLocked`)

Locks or unlocks the PreselectedElementLinetype setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPreselectedElementRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the PreselectedElementRGB parameter.  
### Sub **SetPreselectedElementRGBLock**( boolean  `iLocked`)

Locks or unlocks the PreselectedElementRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetRotationSphereModeLock**( boolean  `iLocked`)

Locks or unlocks the RotationSphereMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSelectedEdgeRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the SelectedEdgeRGB parameter.  
### Sub **SetSelectedEdgeRGBLock**( boolean  `iLocked`)

Locks or unlocks the SelectedEdgeRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSelectedElementRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the SelectedElementRGB parameter.  
### Sub **SetSelectedElementRGBLock**( boolean  `iLocked`)

Locks or unlocks the SelectedElementRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetShaderModeLock**( boolean  `iLocked`)

Locks or unlocks the ShaderMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStaticCullLock**( boolean  `iLocked`)

Locks or unlocks the StaticCull setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStaticLODLock**( boolean  `iLocked`)

Locks or unlocks the StaticLOD setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStereoModeLock**( boolean  `iLocked`)

Locks or unlocks the StereoMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetTransparencyModeLock**( boolean  `iLocked`)

Locks or unlocks the TransparencyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetTwoSideLightingModeLock**( boolean  `iLocked`)

Locks or unlocks the TwoSideLightingMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderIntensifiedRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the UnderIntensifiedRGB parameter.  
### Sub **SetUnderIntensifiedRGBLock**( boolean  `iLocked`)

Locks or unlocks the UnderIntensifiedRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUpdateNeededRGB**( long  `iR`,  long  `iG`,  long  `iB`)

Sets the UpdateNeededRGB parameter.  
### Sub **SetUpdateNeededRGBLock**( boolean  `iLocked`)

Locks or unlocks the UpdateNeededRGB setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewpointAnimationModeLock**( boolean  `iLocked`)

Locks or unlocks the ViewpointAnimationMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz2DAccuracyModeLock**( boolean  `iLocked`)

Locks or unlocks the 2DAccuracyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz2DFixedAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the 2DFixedAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz2DProportionnalAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the 2DProportionnalAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz3DAccuracyModeLock**( boolean  `iLocked`)

Locks or unlocks the Viz3DAccuracyMode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz3DCurveAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the 3DCurveAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz3DFixedAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the 3DFixedAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViz3DProportionnalAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the Viz3DProportionnalAccuracy setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.