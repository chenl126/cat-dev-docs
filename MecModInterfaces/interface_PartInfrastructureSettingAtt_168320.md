# PartInfrastructureSettingAtt (Object)

**_Setting controller for all the Part Infrastructure property tab pages._**

**Role** : This interface is implemented by a component representing the controller for the Part Infrastructure settings.

## Properties

### Property **AlsoDeleteExclusiveParents**(| ) As boolean

   Returns or sets the "AlsoDeleteExclusiveParents" parameter.

**Role:** This parameter defines if a exclusive parents of an object will also be deleted when the object is deleted.
This option is effective only when the "Deletion warning box" is displayed.

**Parameters:**

` oDeleted`      Current "AlsoDeleteExclusiveParents" parameter's value:

  * TRUE or 1 if exclusive parents are also deleted,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **AxisSystemSize**( ) As short

   Returns or sets the "AxisSystemSize" parameter.

**Role:** This parameter determines the size of axis systems.

**Parameters:**

` oSize`      Current size of axis systems

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **BodiesUnderOperationsInTree**( ) As boolean

   Returns or sets the "BodiesUnderOperationsInTree" parameter.

**Role:** This parameter determines if a Body node is displayed when it is being aggregated under a boolean operation (Add, Assemble, Remove, Intersect, Union Trim).
Its value can be changed even after a boolean operation has been created. Simply collapse and expand the federating boolean operation node for the specification tree to be refreshed.

**Parameters:**

` oNodeDisplayed`      Current "BodiesUnderOperationsInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ColorSynchronizationEditability**( ) As boolean

   Returns or sets the "ColorSynchronizationEditability" parameter.

**Role:** This parameter determines whether color synchronization property on Part is editable or not.
Color synchronization editability defines whether the property of synchronization on Part can be interactively editable If it is valuated to 1, user will be able to interactively modify the Part property of Color management tab for synchronization. If it is defined to 0, user will not be able to interactively modify the Part property of Color management tab for synchronization. This option cannot be changed after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorSynchronizationEditability" parameter's value:

  * TRUE or 1, Part property option for synchronization is editable
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ColorSynchronizationMode**( ) As boolean

   Returns or sets the "ColorSynchronizationMode" parameter.

**Role:** This parameter determines color synchronization mode for imported features in a part.
Color synchronization mode defines whether the imported feature, created through copy/paste as result with link mechanism, copies reference feature colors on its faces or not. If it is valuated to 1, synchronization will be effective and referece feature colors will be reported. If it is defined to 0, nothing will be copied(default mode). This option cannot be changed after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorSynchronizationMode" parameter's value:

  * TRUE or 1 if reference feature colors are reported on imported feature,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ConstraintsInGeometry**( ) As boolean

   Returns or sets the "ConstraintsInGeometry" parameter.

**Role:** This parameter enables constraints to be visualized in the 3D view.

**Parameters:**

` oDisplayed`      Current "Display constraints within 3D" parameter's value:

  * TRUE or 1 if constraints are displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ConstraintsNodeInTree**( ) As boolean

   Returns or sets the "ConstraintsNodeInTree" parameter.

**Role:** This parameter determines if a node called "Constraints" is created to contain all constraints.
Its value can be changed even after constraints have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ConstraintsNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ContextualFeaturesSelectableAtCreation**( ) As boolean

   Returns or sets the "ContextualFeaturesSelectableAtCreation" parameter.

**Role:** This parameter determines if contextual features can be selected during the creation of an other feature.

**Parameters:**

` oContextualFeaturesSelectable`      Current "ContextualFeaturesSelectableAtCreation" parameter's value:

  * TRUE or 1 if contextual features can be selected,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **DeleteWarningBox**( ) As boolean

   Returns or sets the "DeleteWarningBox" parameter.

**Role:** This parameter defines if a warning box is displayed when an element is deleted.

**Parameters:**

` oDisplayed`      Current "DeleteWarningBox" parameter's value:

  * TRUE or 1 if a warning box is displayed at deletion,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **DisplayGeometryAfterCurrent**( ) As boolean

   Returns or sets the "DisplayGeometryAfterCurrent" parameter.

**Role:** This parameter enables to visualize in the 3D features after the current object in O.G.S. and "solid and surface set".

**Parameters:**

` oDisplayed`      Current "DisplayGeometryAfterCurrent" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExpandSketchBasedFeaturesNodeAtCreation**( ) As boolean

   Returns or sets the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role:** This parameter determines if specification tree nodes for sketch-based features are expanded when such elements are created. This will enable to view their sketch node.

**Parameters:**

` oNodeExpanded`      Current "ExpandSketchBasedFeaturesNodeAtCreation" parameter's value:

  * TRUE or 1 if such nodes are expanded,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesAsVisible**( ) As boolean

   Returns or sets the "ExternalReferencesAsVisible" parameter.

**Role:** This parameter defines if an external reference is visible when being created.

**Parameters:**

` oVisible`      Current "ExternalReferencesAsVisible" parameter's value:

  * TRUE or 1 if external references are visible when being created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesAssemblyRootContext**( ) As boolean

   Returns or sets the "ExternalReferencesAssemblyRootContext" parameter.

**Role:** This parameter defines if external references are created using the root context of an assembly.

**Parameters:**

` oRootContextUsed`      Current "ExternalReferencesAssemblyRootContext" parameter's value:

  * TRUE or 1 if external references are created using the root context of an assembly,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesNodeInTree**( ) As boolean

   Returns or sets the "ExternalReferencesNodeInTree" parameter.

**Role:** This parameter determines if a node called "External Reference" is created to contain all linked external references.
Its value can be changed even after linked external references have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ExternalReferencesNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **HybridDesignMode**( ) As boolean

   Returns or sets the "HybridDesignMode" parameter.

**Role:** This parameter determines if hybrid design is possible inside Part Bodies and bodies.
This option can be changed even after a document has been opened.

**Parameters:**

` oHybridDesign`      Current "HybridDesignMode" parameter's value:

  * TRUE or 1 if hybrid design is enabled,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **KnowledgeInHybridDesignMode**( ) As boolean

   Returns or sets the "KnowledgeInHybridDesignMode" parameter.

**Role:** This parameter determines if knowledge features (formulas, parameters, rules, ...) can be located inside ordered sets.
This option can be changed even after a document has been opened.

**Parameters:**

` oKnowledgeInHybridDesign`      Current "KnowledgeInHybridDesignMode" parameter's value:

  * TRUE or 1 if hybrid design is enabled,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferences**( ) As boolean

   Returns or sets the "LinkedExternalReferences" parameter.

**Role:** This parameter enables creation of external references with links.

**Parameters:**

` oWithLink`      "LinkedExternalReferences" parameter's value:

  * TRUE or 1 if external references are created with links,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferencesOnlyOnPublication**( ) As boolean

   Returns or sets the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role:** This parameter restricts the creation of external references with links to only published elements.
This option is only used when external references are created with link.

**Parameters:**

` oOnlyForPublishedElements`      Current "LinkedExternalReferencesOnlyOnPublication" parameter's value:

  * TRUE or 1 if external references with link are only allowed on published elements,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferencesWarningAtCreation**( ) As boolean

   Returns or sets the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role:** This parameter defines if a warning panel is displayed each time an external reference with llink is created. The panel enables the user to decide whether the link will be kept or not.
This option is only used when external references are created with link.

**Parameters:**

` oWarningAtCreation`      Current "LinkedExternalReferencesWarningAtCreation" parameter's value:

  * TRUE or 1 if a panel is displayed upon external references with link creation,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NamingMode**( ) As [CatPartElementsNamingMode](../MecModInterfaces/enum_CatPartElementsNamingMode_128721.md)

   Returns or sets the "NamingMode" parameter.

**Role:** This parameter determines how an element can be named through Edit/Properties or any operation creating a feature (Copy-Paste, etc.).
When this option is being changed, it only affects elements whose name is modified afterwards.

**Parameters:**

` oNamingMode`      Current "NamingMode" parameter's value:

  * `catNoCheck` when naming is rule-free,
  * `catNamingCheckUnderSameNode` when 2 elements cannot have the same name under the same node,
  * `catNamingCheckWithinUIActiveObject` when 2 elements cannot have the same name within a defined UIActiveObject.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWith3DSupport**( ) As boolean

   Returns or sets the "NewWith3DSupport" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with 3D working support.

**Parameters:**

` o3DSupportCreated`      Current "NewWith3DSupport" parameter's value:

  * TRUE or 1 if a 3D support is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithAxisSystem**( ) As boolean

   Returns or sets the "NewWithAxisSystem" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with an Axis System.

**Parameters:**

` oAxisSystemCreated`      Current "NewWithAxisSystem" parameter's value:

  * TRUE or 1 if an axis system is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithGS**( ) As boolean

   Returns or sets the "NewWithGS" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with a Geometrical Set.

**Parameters:**

` oGSCreated`      Current "NewWithGS" parameter's value:

  * TRUE or 1 if a G.S. is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithOGS**( ) As boolean

   Returns or sets the "NewWithOGS" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with an Ordered Geometrical Set.

**Parameters:**

` oOGSCreated`      Current "NewWithOGS" parameter's value:

  * TRUE or 1 if an O.G.S. is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithPanel**( ) As boolean

   Returns or sets the "NewWithPanel" parameter.

**Role:** This parameter determines if a dedicated '_New Part_ ' panel is displayed when createing a new .CATPart document.

**Parameters:**

` oNewPartPanelDisplayed`      Current "NewWithPanel" parameter's value:

  * TRUE or 1 if the 'New Part' panel is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **OnlyCurrentOperatedSolidSetInGeometry**( ) As boolean

   Returns or sets the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role:** This parameter enables to visualize in the 3D only the current operated body's feature (operated means being aggregated in a boolean operation), as well as all other bodies and sets direcly inserted under the Part feature.

**Parameters:**

` oDisplayed`      Current "Display in 3D only current operated solid set" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **OnlyCurrentSolidSetInGeometry**( ) As boolean

   Returns or sets the "OnlyCurrentSolidSetInGeometry" parameter.

**Role:** This parameter enables to visualize in the 3D only the current operated body's feature (operated means being aggregated in a boolean operation), as well as all other bodies and sets direcly inserted under the Part feature.

**Parameters:**

` oDisplayed`      Current "Display in 3D only current operated solid set" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ParametersNodeInTree**( ) As boolean

   Returns or sets the "ParametersNodeInTree" parameter.

**Role:** This parameter determines if a node called "Parameters" is created to contain all Knowledgeware parameters.
Its value can be changed even after parameters have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ParametersNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **PublishTopologicalElements**( ) As boolean

   Returns or sets the "PublishTopologicalElements" parameter.

**Role:** This parameter defines if topological elements (faces, edges, vertices, axes extremities) can be published.

**Parameters:**

` oTopologyAllowed`      Current "PublishTopologicalElements" parameter's value:

  * TRUE or 1 if topological elements can be used for publication,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **RelationsNodeInTree**( ) As boolean

   Returns or sets the "RelationsNodeInTree" parameter.

**Role:** This parameter determines if a node called "Relations" is created to contain all Knowledgeware relations (for instance formulas).
Its value can be changed even after parameters have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "RelationsNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ReplaceOnlyAfterCurrent**( ) As boolean

   Returns or sets the "ReplaceOnlyAfterCurrent" parameter.

**Role:** This parameter defines if the replace operation can only apply to components located after the current object.

**Parameters:**

` oOnlyAfterCurrent`      Current "ReplaceOnlyAfterCurrent" parameter's value:

  * TRUE or 1 if the replace operation can only apply to components located after the current object,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **SurfaceElementsLocation**( ) As [CatPartSurfaceElementsLocation](../MecModInterfaces/enum_CatPartSurfaceElementsLocation_188182.md)

   Returns or sets the "SurfaceElementsLocation" parameter.

**Role:** This parameter determines where wireframe and surface elements are created when hybrid design is active.
This option can be changed when hybrid design mode is not active (but useless then), and also even after a document has been opened.

**Parameters:**

` oLocation`      Current "SurfaceElementsLocation" parameter's value:

  * `catPartBodyLocation` when elements are created within a PartBody,
  * `catXGSLocation` when elements are created within a G.S. or an O.G.S..

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **TrueColorMode**( ) As boolean

   Returns or sets the "ColorInheritanceMode" parameter.

**Role:** This parameter determines color inheritance mode for absorbing features in a part.
Color inheritance mode defines which mode of propagation will be used to set color on an absorbing feature. If it is valuated to 1, absorbing feature will inherit colors from all their input. If it is defined to 0, absorbing features will inherit colors from their main input only (default mode). This option can be changed even after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorInheritanceMode" parameter's value:

  * TRUE or 1 if absorbing features inherit from all their inputs,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateElementsRefreshed**( ) As boolean

   Returns or sets the "UpdateElementsRefreshed" parameter.

**Role:** This parameter determines if elements visualization has to be refreshed individually during update tasks.

**Parameters:**

` oElementsRefreshed`      Current "UpdateElementsRefreshed" parameter's value:

  * TRUE or 1 if elements visualization is refreshed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateLinkedExternalReferences**( ) As boolean

   Returns or sets the "UpdateLinkedExternalReferences" parameter.

**Role:** This parameter determines if update tasks also apply to linked external references.

**Parameters:**

` oExternalReferencesUpdated`      Current "UpdateLinkedExternalReferences" parameter's value:

  * TRUE or 1 if the update tasks apply to linked external references,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateMode**( ) As [CatPartUpdateMode](../MecModInterfaces/enum_CatPartUpdateMode_59539.md)

   Returns or sets the "UpdateMode" parameter.

**Role:** This parameter determines how the update of a .CATPart document is conducted.

**Parameters:**

` oUpdateMode`      Current update mode:

  * `catAutomaticUpdate` when update is automatically launched,
  * `catManualUpdate` when update has to be launched manually.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateStoppedOnError**( ) As boolean

   Returns or sets the "UpdateStoppedOnError" parameter.

**Role:** This parameter determines if update tasks stop on the first detected error.

**Parameters:**

` oStoppedOnError`      Current "UpdateStoppedOnError" parameter's value:

  * TRUE or 1 if update tasks stop,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  Methods

### Func **GetAlsoDeleteExclusiveParentsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "AlsoDeleteExclusiveParents" parameter.

**Role** :Retrieves the state of the "AlsoDeleteExclusiveParents" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAxisSystemSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "AxisSystemSize" parameter.

**Role** :Retrieves the state of the "AxisSystemSize" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetBodiesUnderOperationsInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "BodiesUnderOperationsInTree" parameter.

**Role** :Retrieves the state of the "BodiesUnderOperationsInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetColorSynchronizationEditabilityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorSynchronizationEditability" parameter.

**Role** :Retrieves the state of the "ColorSynchronizationEditability" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetColorSynchronizationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorSynchronizationMode" parameter.

**Role** :Retrieves the state of the "ColorSynchronizationMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetConstraintsInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ConstraintsInGeometry" parameter.

**Role** :Retrieves the state of the "ConstraintsInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetConstraintsNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ConstraintsNodeInTree" parameter.

**Role** :Retrieves the state of the "ConstraintsNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetContextualFeaturesSelectableAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ContextualFeaturesSelectableAtCreation" parameter.

**Role** :Retrieves the state of the "ContextualFeaturesSelectableAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDeleteWarningBoxInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "DeleteWarningBox" parameter.

**Role** :Retrieves the state of the "DeleteWarningBox" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayGeometryAfterCurrentInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "DisplayGeometryAfterCurrent" parameter.

**Role** :Retrieves the state of the "DisplayGeometryAfterCurrent" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpandSketchBasedFeaturesNodeAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role** :Retrieves the state of the "ExpandSketchBasedFeaturesNodeAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesAsVisibleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesAsVisible" parameter.

**Role** :Retrieves the state of the "ExternalReferencesAsVisible" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesAssemblyRootContextInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesAssemblyRootContext" parameter.

**Role** :Retrieves the state of the "ExternalReferencesAssemblyRootContext" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesNodeInTree" parameter.

**Role** :Retrieves the state of the "ExternalReferencesNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHybridDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "HybridDesignMode" parameter.

**Role** :Retrieves the state of the "HybridDesignMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetKnowledgeInHybridDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "KnowledgeInHybridDesignMode" parameter.

**Role** :Retrieves the state of the "KnowledgeInHybridDesignMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferences" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferences" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesOnlyOnPublicationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferencesOnlyOnPublication" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesWarningAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferencesWarningAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNamingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NamingMode" parameter.

**Role** :Retrieves the state of the "NamingMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWith3DSupportInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWith3DSupport" parameter.

**Role** :Retrieves the state of the "NewWith3DSupport" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithAxisSystemInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithAxisSystem" parameter.

**Role** :Retrieves the state of the "NewWithAxisSystem" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithGSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithGS" parameter.

**Role** :Retrieves the state of the "NewWithGS" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithOGSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithOGS" parameter.

**Role** :Retrieves the state of the "NewWithOGS" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithPanelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithPanel" parameter.

**Role** :Retrieves the state of the "NewWithPanel" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOnlyCurrentOperatedSolidSetInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role** :Retrieves the state of the "OnlyCurrentOperatedSolidSetInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOnlyCurrentSolidSetInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "OnlyCurrentSolidSetInGeometry" parameter.

**Role** :Retrieves the state of the "OnlyCurrentSolidSetInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParametersNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ParametersNodeInTree" parameter.

**Role** :Retrieves the state of the "ParametersNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPublishTopologicalElementsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "PublishTopologicalElements" parameter.

**Role** :Retrieves the state of the "PublishTopologicalElements" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "RelationsNodeInTree" parameter.

**Role** :Retrieves the state of the "RelationsNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReplaceOnlyAfterCurrentInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ReplaceOnlyAfterCurrent" parameter.

**Role** :Retrieves the state of the "ReplaceOnlyAfterCurrent" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSurfaceElementsLocationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "SurfaceElementsLocation" parameter.

**Role** :Retrieves the state of the "SurfaceElementsLocation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTrueColorModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorInheritanceMode" parameter.

**Role** :Retrieves the state of the "ColorInheritanceMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateElementsRefreshedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateElementsRefreshed" parameter.

**Role** :Retrieves the state of the "UpdateElementsRefreshed" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateLinkedExternalReferencesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateLinkedExternalReferences" parameter.

**Role** :Retrieves the state of the "UpdateLinkedExternalReferences" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateMode" parameter.

**Role** :Retrieves the state of the "UpdateMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateStoppedOnErrorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateStoppedOnError" parameter.

**Role** :Retrieves the state of the "UpdateStoppedOnError" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAlsoDeleteExclusiveParentsLock**( boolean  `iLocked`)

   Locks or unlocks the "AlsoDeleteExclusiveParents" parameter.

**Role** :Locks or unlocks the "AlsoDeleteExclusiveParents" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAxisSystemSizeLock**( boolean  `iLocked`)

   Locks or unlocks the "AxisSystemSize" parameter.

**Role** :Locks or unlocks the "AxisSystemSize" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetBodiesUnderOperationsInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "BodiesUnderOperationsInTree" parameter.

**Role** :Locks or unlocks the "BodiesUnderOperationsInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetColorSynchronizationEditabilityLock**( boolean  `iLocked`)

   Locks or unlocks the "ColorSynchronizationEditability" parameter.

**Role** :Locks or unlocks the "ColorSynchronizationEditability" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetColorSynchronizationModeLock**( boolean  `iLocked`)

   Locks or unlocks the "ColorSynchronizationMode" parameter.

**Role** :Locks or unlocks the "ColorSynchronizationMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetConstraintsInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "ConstraintsInGeometry" parameter.

**Role** :Locks or unlocks the "ConstraintsInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetConstraintsNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ConstraintsNodeInTree" parameter.

**Role** :Locks or unlocks the "ConstraintsNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetContextualFeaturesSelectableAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "ContextualFeaturesSelectableAtCreation" parameter.

**Role** :Locks or unlocks the "ContextualFeaturesSelectableAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDeleteWarningBoxLock**( boolean  `iLocked`)

   Locks or unlocks the "DeleteWarningBox" parameter.

**Role** :Locks or unlocks the "DeleteWarningBox" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayGeometryAfterCurrentLock**( boolean  `iLocked`)

   Locks or unlocks the "DisplayGeometryAfterCurrent" parameter.

**Role** :Locks or unlocks the "DisplayGeometryAfterCurrent" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpandSketchBasedFeaturesNodeAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role** :Locks or unlocks the "ExpandSketchBasedFeaturesNodeAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesAsVisibleLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesAsVisible" parameter.

**Role** :Locks or unlocks the "ExternalReferencesAsVisible" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesAssemblyRootContextLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesAssemblyRootContext" parameter.

**Role** :Locks or unlocks the "ExternalReferencesAssemblyRootContext" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesNodeInTree" parameter.

**Role** :Locks or unlocks the "ExternalReferencesNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHybridDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the "HybridDesignMode" parameter.

**Role** :Locks or unlocks the "HybridDesignMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetKnowledgeInHybridDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the "KnowledgeInHybridDesignMode" parameter.

**Role** :Locks or unlocks the "KnowledgeInHybridDesignMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferences" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferences" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesOnlyOnPublicationLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferencesOnlyOnPublication" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesWarningAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferencesWarningAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNamingModeLock**( boolean  `iLocked`)

   Locks or unlocks the "NamingMode" parameter.

**Role** :Locks or unlocks the "NamingMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWith3DSupportLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWith3DSupport" parameter.

**Role** :Locks or unlocks the "NewWith3DSupport" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithAxisSystemLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithAxisSystem" parameter.

**Role** :Locks or unlocks the "NewWithAxisSystem" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithGSLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithGS" parameter.

**Role** :Locks or unlocks the "NewWithGS" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithOGSLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithOGS" parameter.

**Role** :Locks or unlocks the "NewWithOGS" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithPanelLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithPanel" parameter.

**Role** :Locks or unlocks the "NewWithPanel" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOnlyCurrentOperatedSolidSetInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role** :Locks or unlocks the "OnlyCurrentOperatedSolidSetInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOnlyCurrentSolidSetInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "OnlyCurrentSolidSetInGeometry" parameter.

**Role** :Locks or unlocks the "OnlyCurrentSolidSetInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParametersNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ParametersNodeInTree" parameter.

**Role** :Locks or unlocks the "ParametersNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPublishTopologicalElementsLock**( boolean  `iLocked`)

   Locks or unlocks the "PublishTopologicalElements" parameter.

**Role** :Locks or unlocks the "PublishTopologicalElements" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "RelationsNodeInTree" parameter.

**Role** :Locks or unlocks the "RelationsNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReplaceOnlyAfterCurrentLock**( boolean  `iLocked`)

   Locks or unlocks the "ReplaceOnlyAfterCurrent" parameter.

**Role** :Locks or unlocks the "ReplaceOnlyAfterCurrent" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSurfaceElementsLocationLock**( boolean  `iLocked`)

   Locks or unlocks the "SurfaceElementsLocation" parameter.

**Role** :Locks or unlocks the "SurfaceElementsLocation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateElementsRefreshedLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateElementsRefreshed" parameter.

**Role** :Locks or unlocks the "UpdateElementsRefreshed" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateLinkedExternalReferencesLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateLinkedExternalReferences" parameter.

**Role** :Locks or unlocks the "UpdateLinkedExternalReferences" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateModeLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateMode" parameter.

**Role** :Locks or unlocks the "UpdateMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateStoppedOnErrorLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateStoppedOnError" parameter.

**Role** :Locks or unlocks the "UpdateStoppedOnError" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.