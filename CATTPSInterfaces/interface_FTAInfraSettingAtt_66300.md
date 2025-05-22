# FTAInfraSettingAtt (Object)

**_Represents the FT &A (Functional Tolerancing & Annotation) infrastructure setting controller object._**
**Role** : The FT&A infrastructure setting controller object deals with the setting parameters displayed in:

  * The Tolerancing property page for the Tolerancing Standard and the Leader Associativity setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Tolerancing**
  * The Display property page for the Grid Display, the Grid Snap Point, the Allow Distorsions, the Grid Primary Spacing, the Grid Secondary Step, the GridV Primary Spacing, the GridV Secondary Step, the Under Set Tree Visu, the Under View Tree Visu, and the Under Feature Tree Visu setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Display**
  * The Manipulators property page for the Manipulator Reference Size, the Manipulator Zoom Capability, and the Move After Creation, setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **Manipulators**
  * The View/Annotation Plane property page for the View Associativity, the View Referential, the View Referential Zoomable, and the View Profile setting parameters.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Mechanical Design** to unfold the workbench list
    * Click **Functional Tolerancing & Annotation**
    * Click **View/Annotation Plane**
  * The Cgr Management property page for the Save in CGR setting parameter.
To access this property page:
    * Click the **Options** command in the **Tools** menu
    * Click + left of **Infrastructure** to unfold the workbench list
    * Click **Product Structure**
    * Click **Cgr Management**

The Save in CGR setting parameter represents the state of the check button named: Save FTA 3D Annotation representation in CGR.

## Properties

### Property **AllowDistortions**( ) As boolean

Returns or sets the Allow Distortions setting parameter value.
**True** if the Allow Distortions setting parameter is checked and thus enables distorsions.
**Role** : The Allow Distortions setting parameter defines whether grid spacing and graduations are the same horizontally and vertically (no distorsion) or not (distorsions enabled).  
### Property **GridDisplay**( ) As boolean

Returns or sets the Grid Display setting parameter value.
**True** if the Grid Display setting parameter is checked and thus enables the grid to be displayed.
**Role** : The Grid Display setting parameter displays a grid on the active view.  
### Property **GridPrimarySpacing**( ) As double

Returns or sets the Grid Primary Spacing setting parameter value.
**Role** : The Grid Primary Spacing setting parameter defines the horizontal spacing on the grid, expressed in millimiters. The default value is 100mm.  
### Property **GridSecondaryStep**( ) As long

Returns or sets the Grid Secondary Step setting parameter value.
**Role** : The Grid Secondary Step setting parameter defines the grid's horizontal graduations. The default value is 10.  
### Property **GridSnapPoint**( ) As boolean

Returns or sets the Grid Snap Point setting parameter value.
**True** if the Grid Snap Point setting parameter is checked and thus enables the annotation to be snapped to the nearest grid point. Otherwise, the gris is not used to anchor the annotation.  
### Property **GridVPrimarySpacing**( ) As double

Returns or sets the GridV Primary Spacing setting parameter value.
**Role** : The GridV Primary Spacing setting parameter defines the vertical spacing on the grid, expressed in millimiters. The default value is 100mm. Set this value only if distorsions are allowed thanks to the AllowDistortions property. Otherwise, the value sets to the Grid Primary Spacing setting parameter thanks to the GridPrimarySpacing for horizontal spacing is taken into account.  
### Property **GridVSecondaryStep**( ) As long

Returns or sets the GridV Secondary Step setting parameter value.
**Role** : The GridV Secondary Step setting parameter defines the grid's vertical graduations. The default value is 10. Set this value only if distorsions are allowed thanks to the AllowDistortions property. Otherwise, the value sets to the Grid Secondary Step setting parameter thanks to the GridSecondaryStep for the number of horizontal graduations is taken into account.  
### Property **LeaderAssociativity**( ) As [CATFTALeaderAssociativity](../CATTPSInterfaces/enum_CATFTALeaderAssociativity_128196.md)

Returns or sets the Leader Associativity setting parameter value.
**Role** : The Leader Associativity setting parameter defines the associativity of a leader with the pointed geometrical element.  
### Property **ManRefSiz**( ) As double

Returns or sets the Manipulator Reference Size setting parameter value.
**Role** : The Manipulator Reference Size setting parameter defines the size of the manipulator attached to the end of an annotation leader. The default value is 2mm.  
### Property **ManZooCap**( ) As boolean

Returns or sets the Manipulator Zoom Capability setting parameter value.
**True** if the Manipulator Zoom Capability setting parameter is checked and thus enables the annotation leader end manipulator to be zoomable. Otherwise, it is not zoomable.  
### Property **MoveAfterCreation**( ) As boolean

Returns or sets the Move After Creation setting parameter value.
**True** if the Move After Creation setting parameter is checked and thus enables the annotation leader end manipulator to be moved, after the annotation creation, along lines or curves that represent the intersection between the geometry and the annotation's plane. Otherwise, the annotation leader end manipulator cannot be moved.  
### Property **SaveInCGR**( ) As boolean

Returns or sets the Save In CGR setting parameter value.
**True** if the Save In CGR setting parameter is checked.
**Role** : When set to True, the FT&A 3D Annotation representations are saved in CGR. Otherwise, they are not saved.  
### Property **Standard**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the Tolerancing Standard setting parameter value.
**Role** : The Tolerancing Standard setting parameter defines the standard of the annotation's set.
**Legal values** : five conventional standards are available:

  * **ASME** : American Society for Mechanical Engineers
  * **ASME_3D** : American Society for Mechanical Engineers
  * **ANSI** : American National Standards Institute
  * **JIS** : Japanese Industrial Standard
  * **ISO** : International Organization for Standardization

### Property **UnderFeature**( ) As boolean

Returns or sets the Under Geometric Feature Nodes setting parameter value.
**True** if the Under Geometric Feature Nodes setting parameter is checked and thus enables 3D annotations to be displayed in the specification tree. This lets you view 3D annotations under the Part Design or Generative Shape Design feature nodes to which they are applied.  
### Property **UnderSet**( ) As boolean

Returns or sets the Under Annotation Set Node setting parameter value.
**True** if the Under Annotation Set Node setting parameter is checked and thus enables 3D annotations to be displayed under the annotation set node in the specification tree. Set this parameter to True only if the Under View/Annotation Plane Nodes setting parameter managed by UnderView is set to True.  
### Property **UnderView**( ) As boolean

Returns or sets the Under View/Annotation Plane Nodes setting parameter value.
**True** if the Under View/Annotation Plane Nodes setting parameter is checked and thus enables 3D annotations to be displayed under the view/annotation plane nodes in the specification tree. This lets you view 3D annotations under the view node to which they are linked.  
### Property **ViewAssociativity**( ) As boolean

Returns or sets the View Associativity setting parameter value.
**True** if the View Associativity setting parameter is checked and thus enables the associativity of the view/annotation plane associativity with the pointed geometrical elements.
**Role** : The View Associativity setting parameter defines whether the views created are associative with the geometry. When views are associative to the geometry, any modification applied to the geometry or to the axis system is reflected in the view definition.  
### Property **ViewProfile**( ) As boolean

Returns or sets the View Profile setting parameter value.
**True** if the View Profile setting parameter is checked and thus enables the view/annotation plane profile on the part/product to be displayed.  
### Property **ViewReferential**( ) As boolean

Returns or sets the View Referential setting parameter value.
**True** if the View Referential setting parameter is checked and thus enables the display of the active annotation plane axis system.  
### Property **ViewReferentialZoomable**( ) As boolean

Returns or sets the View Referential Zoomable setting parameter value.
**True** if the View Referential Zoomable setting parameter is checked and thus enables the annotation plane axis to be zoomable.  Methods

### Func **GetAllowDistortionsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Allow Distorsions setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Grid Display setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridPrimarySpacingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Grid Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridSecondaryStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Grid Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridSnapPointInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Grid Snap Point setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridVPrimarySpacingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the GridV Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetGridVSecondaryStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the GridV Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLeaderAssociativityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Leader Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetManRefSizInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Manipulator Reference Size setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetManZooCapInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Manipulator Zoom Capability setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMoveAfterCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Move After Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetSaveInCGRInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Save In CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetStandardInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Tolerancing Standard setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderFeatureInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Under Geometric Feature Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderSetInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Under Annotation Set Node setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUnderViewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the Under View/Annotation Plane Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewAssociativityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the View Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewProfileInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the View Profile setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewReferentialInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the View Referential setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetViewReferentialZoomableInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

Retrieves information about the View Referential Zoomable setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAllowDistortionsLock**( boolean  `iLocked`)

Locks or unlocks the Allow Distorsions setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridDisplayLock**( boolean  `iLocked`)

Locks or unlocks the Grid Display setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridPrimarySpacingLock**( boolean  `iLocked`)

Locks or unlocks the Grid Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridSecondaryStepLock**( boolean  `iLocked`)

Locks or unlocks the Grid Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridSnapPointLock**( boolean  `iLocked`)

Locks or unlocks the Grid Snap Point setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridVPrimarySpacingLock**( boolean  `iLocked`)

Locks or unlocks the GridV Primary Spacing setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetGridVSecondaryStepLock**( boolean  `iLocked`)

Locks or unlocks the GridV Secondary Step setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLeaderAssociativityLock**( boolean  `iLocked`)

Locks or unlocks the Leader Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetManRefSizLock**( boolean  `iLocked`)

Locks or unlocks the Manipulator Reference Size setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetManZooCapLock**( boolean  `iLocked`)

Locks or unlocks the Manipulator Zoom Capability setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMoveAfterCreationLock**( boolean  `iLocked`)

Locks or unlocks the Move After Creation setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetSaveInCGRLock**( boolean  `iLocked`)

Locks or unlocks the Save In CGR setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetStandardLock**( boolean  `iLocked`)

Locks or unlocks the Tolerancing Standard setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderFeatureLock**( boolean  `iLocked`)

Locks or unlocks the Under Geometric Feature Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderSetLock**( boolean  `iLocked`)

Locks or unlocks the Under Annotation Set Node setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUnderViewLock**( boolean  `iLocked`)

Locks or unlocks the Under View/Annotation Plane Nodes setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewAssociativityLock**( boolean  `iLocked`)

Locks or unlocks the View Associativity setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewProfileLock**( boolean  `iLocked`)

Locks or unlocks the View Profile setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewReferentialLock**( boolean  `iLocked`)

Locks or unlocks the View Referential setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetViewReferentialZoomableLock**( boolean  `iLocked`)

Locks or unlocks the View Referential Zoomable setting parameter value.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.