# CATAssemblyInterfaces Framework

## Object Index

  * [AsmConstraintSettingAtt](CATAssemblyInterfaces/interface_AsmConstraintSettingAtt_112657.md)
  * [AsmGeneralSettingAtt](CATAssemblyInterfaces/interface_AsmGeneralSettingAtt_83800.md)
  * [AssemblyBoolean](CATAssemblyInterfaces/interface_AssemblyBoolean_47926.md)
  * [AssemblyFeature](CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)
  * [AssemblyFeatures](CATAssemblyInterfaces/interface_AssemblyFeatures_55552.md)
  * [AssemblyHole](CATAssemblyInterfaces/interface_AssemblyHole_30806.md)
  * [AssemblyPocket](CATAssemblyInterfaces/interface_AssemblyPocket_42326.md)
  * [AssemblySplit](CATAssemblyInterfaces/interface_AssemblySplit_37076.md)

## Enumerated Types Index

  * [CatAsmAutoSwitchToDesignMode](CATAssemblyInterfaces/enum_CatAsmAutoSwitchToDesignMode_159986.md)
  * [CatAsmConstraintCreationMode](CATAssemblyInterfaces/enum_CatAsmConstraintCreationMode_163128.md)
  * [CatAsmExtendMoveToFixT](CATAssemblyInterfaces/enum_CatAsmExtendMoveToFixT_97992.md)
  * [CatAsmPasteComponentMode](CATAssemblyInterfaces/enum_CatAsmPasteComponentMode_119636.md)
  * [CatAsmQuickConstraintMode](CATAssemblyInterfaces/enum_CatAsmQuickConstraintMode_130336.md)
  * [CatAsmRedundancyMode](CATAssemblyInterfaces/enum_CatAsmRedundancyMode_82718.md)
  * [CatAsmUpdateMode](CATAssemblyInterfaces/enum_CatAsmUpdateMode_52340.md)
  * [CatAsmUpdateStatusComputeMode](CATAssemblyInterfaces/enum_CatAsmUpdateStatusComputeMode_175422.md)

---

# CatAsmAutoSwitchToDesignMode (Enumeration)

**_Option managing the implicit switch from visualization mode to design mode._**

**Values:**

` catSwitchAvailable`      Parts are being switched to necessary design mode when needed.
` catSwitchUnavailable`      No automatic switch to design mode.

---

# CatAsmConstraintCreationMode (Enumeration)

**_Constraint creation mode._**

**Values:**

` catUseAnyGeometry`      The constraint can be created on any kind of geometry.
` catUsePublishedGeometryChildLevel`      The constraint can only be created on geometry published on the direct child level.
` catUsePublishedGeometryAnyLevel`      The constraint can only be created on geometry published on any assembly level.

---

# CatAsmExtendMoveToFixT (Enumeration)

**_Option managing the extension of a move to the components involved in a FixTogether._**

**Values:**

` catNeverExtendMoveToFixT`      Never extend move to all components involved in a FixTogether
` catAskIfExtendMoveToFixT`      Ask question to extend move to all component involved in a FixTogether
` catAlwaysExtendMoveToFixT`      always extend move to all component involved in a FixTogether

---

# CatAsmPasteComponentMode (Enumeration)

**_Component Paste mode._**

**Values:**

` catPasteWithoutCsts`      The component's constraints will not be recreated.
` catPasteWithCstOnCopy`      The component's constraints will only be recreated after a Copy.
` catPasteWithCstOnCut`      The component's constraints will only be recreated after a Cut.
` catPasteWithCstOnCopyAndCut`      The component's constraints will be recreated after a Copy or a Cut.

---

# CatAsmQuickConstraintMode (Enumeration)

**_Quick constraint mode._**

**Values:**

` catSpecifiedOrder`      Use the specified order.
` catVerifiedConstraintFirst`      Create verified constraint first.

---

# CatAsmRedundancyMode (Enumeration)

**_Redundancy check mode._**

**Values:**

` catUnChecked`      Check for redundancy for constraint creation.
` catChecked`      Does not Check for redundancy for constraint creation.

---

# CatAsmUpdateMode (Enumeration)

**_Update command mode._**

**Values:**

` catManualUpdate`      The user will need to launch the Update command.
` catAutomaticUpdate`      Update The Update command will be automatically launched

---

# CatAsmUpdateStatusComputeMode (Enumeration)

**_Real Update status computation mode._**

**Values:**

` catManualCompute`      The user chooses when he want to compute the exact Update status.
` catAutomaticCompute`      Additional data are being loaded to compute an exact Update status.

---

# AsmConstraintSettingAtt (Object)

**_Represents the Assembly Constraints setting controller object._**

**Role** : the Assembly Constraints setting controller object deals with the setting parameters displayed in the Assembly Constraints property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **Mechanical Design** to unfold the workbench list
  * Click **Assembly Design: Constraints tab**

## Properties

### Property **ConstraintCreationMode**( ) As [CatAsmConstraintCreationMode](../CATAssemblyInterfaces/enum_CatAsmConstraintCreationMode_163128.md)

   Returns or sets the constraint creation setting parameter.

**Role** : The constraint creation setting parameter manages the determination of the kind of elements to constraint.

**Legal values** :  | catUseAnyGeometry | The constraint can be created on any kind of geometry
---|---
catUsePublishedGeometryChildLevel | The constraint can only be created on geometry published on the direct child level
catUsePublishedGeometryAnyLevel | The constraint can only be created on geometry published on any assembly level

**Example:**      The following example retrieves the constraint creation setting parameter of `AsmConstraintSettingAtt1` in `CreationMode` and sets the mode to catUsePublishedGeometryAnyLevel.

```VBScript
     Set CreationMode = AsmConstraintSettingAtt1.ConstraintCreationMode
     AsmConstraintSettingAtt1.ConstraintCreationMode = catUsePublishedGeometryAnyLevel

```

### Property **PasteComponentMode**( ) As [CatAsmPasteComponentMode](../CATAssemblyInterfaces/enum_CatAsmPasteComponentMode_119636.md)

   Returns or sets the component paste setting parameter.

**Role** : The component paste setting parameter manages the keeping of the contraints of a component after a Copy/Paste or a Cut/Paste.

**Legal values** :  | catPasteWithoutCsts | The component's constraints will not be recreated
---|---
catPasteWithCstOnCopy | The component's constraints will only be recreated after a Copy
catPasteWithCstOnCut | The component's constraints will only be recreated after a Cut
catPasteWithCstOnCopyAndCut | The component's constraints will be recreated after a Copy or a Cut

**Example:**      The following example retrieves the component paste setting parameter of `AsmConstraintSettingAtt1` in `PasteMode` and sets the mode to With Cut Only.

```VBScript
     Set PasteMode = AsmConstraintSettingAtt1.PasteComponentMode
     AsmConstraintSettingAtt1.PasteComponentMode = catPasteWithCstOnCut

```

### Property **QuickConstraintMode**( ) As [CatAsmQuickConstraintMode](../CATAssemblyInterfaces/enum_CatAsmQuickConstraintMode_130336.md)

   Returns or sets the quick constraint setting parameter.

**Role** : The quick constraint setting parameter manages the type of contraint that will be created by tue Quick Constraint command.

**Legal values** :  | catSpecifiedOrder | Use the specified order
---|---
catVerifiedConstraintFirst | Create verified constraint first

**Example:**      The following example retrieves the quick constraint setting parameter of `AsmConstraintSettingAtt1` in `QuickMode` and sets the mode to catSpecifiedOrder.

```VBScript
     Set QuickMode = AsmConstraintSettingAtt1.QuickConstraintMode
     AsmConstraintSettingAtt1.QuickConstraintMode = catSpecifiedOrder

```

### Property **RedundancyMode**( [CatAsmRedundancyMode](../CATAssemblyInterfaces/enum_CatAsmRedundancyMode_82718.md)  `iRedundancyMode`)

   Sets redundancy check option for constraint creation.

**Role** : The Redundancy of the constraint is decided to be checked or not to be checked, for constraint creation.

**Legal values** :  | catUnChecked | Redundancy of constraint will be checked while constraint creation.
---|---
catChecked | Redundancy of constraint will not be checked while constraint creation.
Methods
### Func **GetConstraintCreationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves informations about the constraint creation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetPasteComponentModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves informations about the component paste setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetQuickConstraintModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves informations about the quick constraint setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetQuickConstraintOrderedList**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns the quick constraint ordered list setting parameter.

**Role** : The quick constraint ordered list setting parameter manages the determination of the kind of elements to constraint.

**Parameters:**

` ioList`      The ordered list of constraints type The constraints types must be precise strings  **Example:**      The following example retrieves the quick constraint ordered list of `AsmConstraintSettingAtt1` in `QuickList`

```VBScript
     Dim QuickList
     QuickList = AsmConstraintSettingAtt1.GetQuickConstraintOrderedList()

```

### Sub **SetConstraintCreationModeLock**( boolean  `iLocked`)

   Locks or unlocks the constraint creation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetPasteComponentModeLock**( boolean  `iLocked`)

   Locks or unlocks the component paste setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetQuickConstraintModeLock**( boolean  `iLocked`)

   Locks or unlocks the quick constraint setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetQuickConstraintOrderedList**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iList`)

   Sets the quick constraint ordered list setting parameter.

**Role** : The quick constraint ordered list setting parameter manages the determination of the kind of elements to constraint.

**Parameters:**

` iList`      The ordered list of constraints type The constraints types must be precise strings  **Example:**      The following example sets the quick constraint ordered list of `AsmConstraintSettingAtt1`

```VBScript
     Dim QuickList(5)
     QuickList(0) = "CATAsmCoincidenceType"
     QuickList(1) = "CATAsmSurfContactType"
     QuickList(2) = "CATAsmAngleType"
     QuickList(3) = "CATAsmDistanceType"
     QuickList(4) = "CATAsmPerpendType"
     QuickList(5) = "CATAsmParallelType"
     AsmConstraintSettingAtt1.SetQuickConstraintOrderedListQuickList

```

---

# AsmGeneralSettingAtt (Object)

**_Represents the Assembly General setting controller object._**

**Role** : the Assembly General setting controller object deals with the setting parameters displayed in the Assembly General property page. To access this property page:

  * Click the **Options** command in the **Tools** menu
  * Click + left of **Mechanical Design** to unfold the workbench list
  * Click **Assembly Design: General tab**

## Properties

### Property **AutoSwitchToDesignMode**( ) As [CatAsmAutoSwitchToDesignMode](../CATAssemblyInterfaces/enum_CatAsmAutoSwitchToDesignMode_159986.md)

   Returns or sets the implicit switch from visualization mode to design mode setting parameter .

**Role** : The implicit switch from visualization mode to design mode setting parameter manages the loading of necessayr data whenever they are needed. Note that this option is useful only when the Cache option is activated

**Legal values** :  | catAutoSwitchUnavailable | Automatic switch to design mode unavailable
---|---
catAutoSwitchAvailable | Automatic switch to design mode available

**Example:**      The following example retrieves the implicit switch setting parameter of `AsmGeneralSettingAtt1` in `SwitchMode` and enables the switch

```VBScript
     Set SwitchMode = AsmGeneralSettingAtt1.AutoSwitchToDesignMode
     AsmGeneralSettingAtt1.AutoSwitchToDesignMode = catAutoSwitchAvailable

```

### Property **AutoUpdateMode**( ) As [CatAsmUpdateMode](../CATAssemblyInterfaces/enum_CatAsmUpdateMode_52340.md)

   Returns or sets the automatic update setting parameter.

**Role** : The automatic update setting parameter manages the automatic launching of the Update command.

**Legal values** :  | catManualUpdate | Manual update mode
---|---
catAutomaticUpdate | Automatic update mode

**Example:**      The following example retrieves the automatic update setting parameter of `AsmGeneralSettingAtt1` in `UpdateMode` and sets the mode to manual update.

```VBScript
     Set UpdateMode = AsmGeneralSettingAtt1.AutoUpdateMode
     AsmGeneralSettingAtt1.AutoUpdateMode = catManualUpdate

```

### Property **MoveWithFixTExtendMode**( ) As [CatAsmExtendMoveToFixT](../CATAssemblyInterfaces/enum_CatAsmExtendMoveToFixT_97992.md)

   Returns or sets the setting parameter managing the extension of a move to the components involved in a FixTogether.

**Role** : This setting parameter manages whether the components involved in a FixTogether will be moved or not.

**Legal values** :  | catNeverExtendMoveToFixT | Never extend move to all component involved in a FixTogether
---|---
catAskIfExtendMoveToFixT | Ask question to extend move to all component involved in a FixTogether
catAlwaysExtendMoveToFixT | Always extend move to all component involved in a FixTogether

**Example:**      The following example retrieves the move setting parameter of `AsmGeneralSettingAtt1` in `MoveMode` and sets it to Always

```VBScript
     Set MoveMode = AsmGeneralSettingAtt1.MoveWithFixTExtendMode
     AsmGeneralSettingAtt1.MoveWithFixTExtendMode = catAlwaysExtendMoveToFixT

```

### Property **UpdateStatusMode**( ) As [CatAsmUpdateStatusComputeMode](../CATAssemblyInterfaces/enum_CatAsmUpdateStatusComputeMode_175422.md)

   Returns or sets the update status computation setting parameter.

**Role** : The update status computation setting parameter manages the loading at open of the data necessary to the exact update status computation. Note that this option is useful only when the Cache option is activated

**Legal values** :  | catManualCompute | At open the update status is unknown
---|---
catAutomaticCompute | Additional data are being loaded at open to compute an exact Update status

**Example:**      The following example retrieves the update status computation setting parameter of `AsmGeneralSettingAtt1` in `StatusMode` and sets the mode to automatic computation.

```VBScript
     Set StatusMode = AsmGeneralSettingAtt1.UpdateStatusMode
     AsmGeneralSettingAtt1.UpdateStatusMode = catAutomaticCompute

```

Methods
### Func **GetAutoSwitchToDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves the state of the implicit switch from visualization mode to design mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetAutoUpdateModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves informations about the automatic update setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetMoveWithFixTExtendModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves the state of the setting parameter managing the extension of a move to the components involved in a FixTogether.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetUpdateStatusModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `AdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLocked`) As boolean

   Retrieves informations about the update status computation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAutoSwitchToDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the implicit switch from visualization mode to design mode setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetAutoUpdateModeLock**( boolean  `iLocked`)

   Locks or unlocks the automatic update setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMoveWithFixTExtendModeLock**( boolean  `iLocked`)

   Locks or unlocks the setting parameter managing the extension of a move to the components involved in a FixTogether.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetUpdateStatusModeLock**( boolean  `iLocked`)

   Locks or unlocks the update status computation setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

# AssemblyBoolean (Object)

**_Represents the AssemblyBoolean object._**

## Properties

### Property **Body**( ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md) (Read Only)

   Returns the operating body.

**Example:**     The following example retrieves in `opBody` the operating body of the assembly boolean `assemblyBool`.

```VBScript
     Dim opBody As Body
     Set opBody = assemblyBool.Body

```

### Property **BodyComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the operating body.

**Example:**     The following example retrieves in `opBodyComp` the component that contains the operating body of the assembly boolean `assemblyBool`.

```VBScript
     Dim opBodyComp As Product
     Set opBodyComp = assemblyBool.BodyComponent

```

---

# AssemblyFeature (Object)

**_Represents the AssemblyFeature object._**

## Methods

### Sub **AddAffectedComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`)

   Adds a component to the affected component list. An update of the aggregating Product is necessary to apply the Assembly Feature to this component.

**Parameters:**

` iComponent`      The component to affect  **Example:**     The following example adds the component `ProdToAffect` to the affected component list of the AssemblyFeature `assemblyFeat`.

```VBScript
     assemblyFeat.AddAffectedComponent( ProdToAffect )

```

### Func **AffectedComponentsCount**( ) As long

   Returns the affected component list count.

**Example:**     The following example retrieves the affected component list count of the AssemblyFeature `assemblyFeat` in `affectedListSize`.

```VBScript
     affectedListSize = assemblyFeat.AffectedComponentsCount

```

### Sub **ListAffectedComponents**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfComponents`)

   Retrieves the affected component list.

**Parameters:**

` oListOfComponents`      The retrieved list.
The array must be previously initialized using the
AffectedComponentsCount method.  **Example:**     The following example retrieves the affected component list of the AssemblyFeature `assemblyFeat` in `affectedList`.

```VBScript
     affectedListSize = assemblyFeat.AffectedComponentsCount
     Dim affectedList(affectedListSize-1)
     assemblyFeat.ListAffectedComponents(affectedList)

```

### Sub **RemoveAffectedComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`)

   Removes a component from the affected component list. An update of the aggregating Product is necessary to remove the generated feature from this component.

**Parameters:**

` iComponent`      The affected component to remove  **Example:**     The following example removes the component `ProdToRemove` from the affected component list of the AssemblyFeature `assemblyFeat`.

```VBScript
     assemblyFeat.RemoveAffectedComponent( ProdToRemove )

```

---

# AssemblyFeatures (Collection)

**_A collection of all the AssemblyFeature objects of a product._**

**See also:**      [AssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

## Methods

### Func **AddAssemblyAdd**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iBodyComp`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Creates a new AssemblyBoolean object by adding a body to the assembly.

**Parameters:**

` iBody`      The body to add
` iBodyComp`      The component that contains the body to add
` iComponent`      The component with respect to which the AssemblyBoolean object to create will be positioned

**Returns:**      The created [AssemblyBoolean](../CATAssemblyInterfaces/interface_AssemblyBoolean_47926.md) object  **Example:**      This example creates the `addBody` AssemblyBoolean object in the `assemblyFeats` collection using a body referenced as `bodyToAdd` contained in the `bodyToAddComp` component, and positioned with respect to the `positioningComp` component.

```VBScript
     Dim addBody As AssemblyBoolean
     Set addBody = assemblyFeats.AddAssemblyAdd(bodyToAdd,     _
                                                bodyToAddComp, _
                                                positioningComp)

```

### Func **AddAssemblyHole**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSketchComp`,  double  `iDepth`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Creates a new AssemblyHole object.

**Parameters:**

` iSketch`      The sketch defining the hole reference plane and anchor point.
This sketch must contain a single point that defines the hole axis: the hole axis in 3D passes through that point and is normal to the sketch plane.
` iSketchComp`      The component that contains the sketch
` iDepth`      The hole depth
` iComponent`      The component with respect to which the AssemblyHole object to create will be positioned

**Returns:**      The created [AssemblyHole](../CATAssemblyInterfaces/interface_AssemblyHole_30806.md) object  **Example:**      This example creates the `hole` AssemblyHole object in the `assemblyFeats` collection using a sketch referenced as `holeSketch` contained in the `holeSketchComp` component, with a depth of 60mm, and positioned with respect to the `positioningComp` component.

```VBScript
     Dim hole As AssemblyHole
     Set hole = assemblyFeats.AddAssemblyHole(holeSketch,     _
                                              holeSketchComp, _
                                              60,             _
                                              positioningComp)

```

### Func **AddAssemblyPocket**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSketchComp`,  double  `iDepth`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Creates a new AssemblyPocket object.

**Parameters:**

` iSketch`      The sketch defining the pocket base
` iSketchComp`      The component that contains the sketch
` iDepth`      The pocket depth
` iComponent`      The component with respect to which the AssemblyPocket object to create will be positioned

**Returns:**      The created [AssemblyPocket](../CATAssemblyInterfaces/interface_AssemblyPocket_42326.md) object  **Example:**      This example creates the `pocket` AssemblyPocket object in the `assemblyFeats` collection using a sketch referenced as `pocketSketch` contained in the `pocketSketchComp` component, with a depth of 20mm, and positioned with respect to the `positioningComp` component.

```VBScript
     Dim pocket As AssemblyPocket
     Set pocket = assemblyFeats.AddAssemblyPocket(pocketSketch,     _
                                                  pocketSketchComp, _
                                                  20,               _
                                                  positioningComp)

```

### Func **AddAssemblyRemove**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iBodyComp`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Creates a new AssemblyBoolean object by removing a body from the assembly.

**Parameters:**

` iBody`      The body to remove
` iBodyComp`      The component that contains the body to remove
` iComponent`      The component with respect to which the AssemblyBoolean object to create will be positioned

**Returns:**      The created [AssemblyBoolean](../CATAssemblyInterfaces/interface_AssemblyBoolean_47926.md) object  **Example:**      This example creates the `removeBody` AssemblyBoolean object in the `assemblyFeats` collection using a body referenced as `bodyToRemove` contained in the `bodyToRemoveComp` component, and positioned with respect to the `positioningComp` component.

```VBScript
     Dim removeBody As AssemblyBoolean
     Set removeBody = assemblyFeats.AddAssemblyRemove(bodyToRemove,     _
                                                      bodyToRemoveComp, _
                                                      positioningComp)

```

### Func **AddAssemblySplit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplittingElement`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSplittingElemComp`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSplitSide`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iComponent`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Creates a new AssemblySplit object.

**Parameters:**

` iSplittingElement`      The face or plane that will split the current body
` iSplittingElemComp`      The component that contains the splitting element
` iSplitSide`      The specification for which side of the current body should be kept at the end of the split operation
` iComponent`      The component with respect to which the AssemblySplit object to create will be positioned

**Returns:**      The created [AssemblySplit](../CATAssemblyInterfaces/interface_AssemblySplit_37076.md) object  **Example:**      This example creates the `splitByPlane` AssemblySplit object in the `assemblyFeats` collection using a plane referenced as `splittingPlane` contained in the `splittingComp` component, in such a way that the material to remove be the one located in the direction of the `splittingPlane` normal vector, and positioned with respect to the `positioningComp` component.

```VBScript
     Dim splitByPlane As AssemblySplit
     Set splitByPlane = assemblyFeats.AddAssemblySplit(splittingPlane,  _
                                                       splittingComp,   _
                                                       catPositiveSide, _
                                                       positioningComp)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAssemblyFeature](../CATAssemblyInterfaces/interface_AssemblyFeature_48484.md)

   Returns an AssemblyFeature object using its index or its name from the AssemblyFeatures collection.

**Parameters:**

` iIndex`      The index or the name of the AssemblyFeature object to retrieve from the AssemblyFeatures collection. As a numerics, this index is the rank of the AssemblyFeature object in the collection. The index of the first AssemblyFeature object in the collection is 1, and the index of the last AssemblyFeature object is Count. As a string, it is the name you assigned to the AssemblyFeature object using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved AssemblyFeature object  **Example:**      This example retrieves the last item in the `assemblyFeats` collection.

```VBScript
     Dim lastAssemblyFeat As AssemblyFeature
     Set lastAssemblyFeat = assemblyFeats.Item(assemblyFeats.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an AssemblyFeature object from the AssemblyFeatures collection.

**Parameters:**

` iIndex`      The index or the name of the AssemblyFeature object to remove from the AssemblyFeatures collection. As a numerics, this index is the rank of the AssemblyFeature object in the collection. The index of the first AssemblyFeature object in the collection is 1, and the index of the last AssemblyFeature object is Count. As a string, it is the name you assigned to the AssemblyFeature object using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last AssemblyFeature object in the `assemblyFeats` collection.

```VBScript
     assemblyFeats.Remove(assemblyFeats.Count)

```

---

# AssemblyHole (Object)

**_Represents the AssemblyHole object._**

## Properties

### Property **AnchorMode**( ) As [CatHoleAnchorMode](../PartInterfaces/enum_CatHoleAnchorMode_58938.md)

   Returns or sets the hole anchor mode.
This property is valid when the hole type is Counterbored or Counterdrilled.

**Example:**     The following example saves in `holeAnchorMode` the anchor mode of the hole `assemblyHole` and sets it so that the anchor mode will now be set to the middle of its head.

```VBScript
     Dim holeAnchorMode
     Set holeAnchorMode = assemblyHole.AnchorMode
     assemblyHole.AnchorMode = catMiddlePointHoleAnchor

```

### Property **BottomAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the hole bottom angle.
This property is valid when the hole bottom type is VBottom. The hole bottom angle is returned as a [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) object.

**Example:**     The following example retrieves in `holeBottomAngle` the bottom angle of the hole `assemblyHole`.

```VBScript
     Dim holeBottomAngle As Angle
     Set holeBottomAngle = assemblyHole.BottomAngle

```

### Property **BottomLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the hole bottom limit.
This limit manages the way the hole is ended. It is returned as a [Limit](../PartInterfaces/interface_Limit_5781.md) object.

**Example:**     The following example retrieves in `limit` the bottom limit of the hole `assemblyHole`.

```VBScript
     Dim limit As Limit
     Set limit = assemblyHole.BottomLimit

```

### Property **BottomType**( ) As [CatHoleBottomType](../PartInterfaces/enum_CatHoleBottomType_61261.md)

   Returns or sets the hole bottom type.

**Example:**     The following example saves in `holeBottomType` the bottom type of the hole `assemblyHole` and sets it so that the bottom will now be a V-like one.

```VBScript
     Dim holeBottomType
     Set holeBottomType = assemblyHole.BottomType
     assemblyHole.BottomType = catVHoleBottom

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole diameter.
It is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeDiam` the diameter of the hole `assemblyHole`.

```VBScript
     Dim holeDiam As Length
     Set holeDiam = assemblyHole.Diameter

```

### Property **HeadAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the hole head angle.
This property is valid when the hole type is Tapered, Counterdrilled or Countersunk. The hole head angle is returned as a [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) object.

**Example:**     The following example retrieves in `holeHeadAngle` the head angle of the hole `assemblyHole`.

```VBScript
     Dim holeHeadAngle As Angle
     Set holeHeadAngle = assemblyHole.HeadAngle

```

### Property **HeadDepth**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole head depth.
This property is valid when the hole type is Counterbored, Counterdrilled or Countersunk. The hole head depth is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeHeadDepth` the head depth of the hole `assemblyHole`.

```VBScript
     Dim holeHeadDepth As Length
     Set holeHeadDepth = assemblyHole.HeadDepth

```

### Property **HeadDiameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole head diameter.
This property is valid when the hole type is Counterbored or Counterdrilled. The hole head diameter is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeHeadDiam` the head diameter of the hole `assemblyHole`.

```VBScript
     Dim holeHeadDiam As Length
     Set holeHeadDiam = assemblyHole.HeadDiameter

```

### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the hole positioning sketch.

**Example:**     The following example retrieves in `sketch` the positioning sketch of the hole `assemblyHole`.

```VBScript
     Dim sketch As Sketch
     Set sketch = assemblyHole.Sketch

```

### Property **SketchComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the hole positioning sketch.

**Example:**     The following example retrieves in `skComp` the component that contains the positioning sketch of the hole `assemblyHole`.

```VBScript
     Dim skComp As Product
     Set skComp = assemblyHole.SketchComponent

```

### Property **Type**( ) As [CatHoleType](../PartInterfaces/enum_CatHoleType_25588.md)

   Returns or sets the hole type.

**Example:**     The following example saves in `holeType` the type of the hole `assemblyHole`, and then sets it so that it will now be a tapered hole.

```VBScript
     Set holeType = assemblyHole.Type
     assemblyHole.Type = catTaperedHole

```

Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

   Retrieves the hole direction vector components.
These components are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioDirection`      The direction vector components, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example returns in `dirArray` the direction vector components of the hole `assemblyHole`.

```VBScript
     Dim dirArray(2)
     Call assemblyHole.GetDirection(dirArray)
     Set x = dirArray[0]
     Set y = dirArray[1]
     Set z = dirArray[2]

```

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioOrigin`)

   Retrieves the origin point to which the hole is anchored.
This point belongs to a plane tangent to the hole. The coordinates are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioOrigin`      The hole origin point coordinates, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example returns in `coordArray` the coordinates of the hole `assemblyHole`.

```VBScript
     Dim coordArray(2)
     Call assemblyHole.GetOrigin coordArray
     Set x = coordArray[0]
     Set y = coordArray[1]
     Set z = coordArray[2]

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLineComp`)

   Sets the hole axis direction.

**Parameters:**

` iLine`      The hole axis direction, as a reference to a line or an edge.
` iLineComp`      The component containing the axis direction  **Example:**     The following example sets the axis direction of the hole `assemblyHole` with the `dirRef` line of the component `dirComp`.

```VBScript
     assemblyHole.SetDirection dirRef, dirComp

```

---

# AssemblyPocket (Object)

**_Represents the AssemblyPocket object._**

## Properties

### Property **DirectionOrientation**( ) As [CatPrismOrientation](../PartInterfaces/enum_CatPrismOrientation_77897.md)

   Returns or sets the pocket direction orientation.

**Example:**     The following example saves in `dirOrientation` the direction orientation of the pocket `assemblyPocket`, and then sets it so that the direction will be now inversed.

```VBScript
     Dim dirOrientation
     Set dirOrientation = assemblyPocket.DirectionOrientation
     assemblyPocket.DirectionOrientation = catInverseOrientation

```

### Property **DirectionType**( ) As [CatPrismExtrusionDirection](../PartInterfaces/enum_CatPrismExtrusionDirection_144922.md)

   Returns or sets the pocket direction type.

**Example:**     The following example saves in `dirType` the direction type of the pocket `assemblyPocket`, and then sets it so that the direction will be now normal to the sketch.

```VBScript
     Dim dirType
     Set dirType = assemblyPocket.DirectionType
     assemblyPocket.DirectionType = catNormalToSketchDirection

```

### Property **FirstLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the first pocket limit.
A pocket has two limits that manage the way the pocket is ended.

**Example:**     The following example returns in `firstLimit` the first limit of the pocket `assemblyPocket`.

```VBScript
     Dim firstLimit As Limit
     Set firstLimit = assemblyPocket.FirstLimit

```

### Property **IsSymmetric**( ) As boolean

   Returns or sets the pocket symmetry flag.

**TRUE** if the pocket is symmetric with respect to the base sketch, and **FALSE** otherwise.

**Example:**     The following example saves in `symFlag` the symmetry flag of the pocket `assemblyPocket`, and then sets it so that it will be now symmetric with respect to the base sketch.

```VBScript
     Dim symFlag As boolean
     Set symFlag = assemblyPocket.IsSymmetric
     assemblyPocket.IsSymmetric = TRUE

```

### Property **SecondLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the second pocket limit.
A pocket has two limits that manage the way the pocket is ended.

**Example:**     The following example returns in `secondLimit` the second limit of the pocket `assemblyPocket`.

```VBScript
     Dim secondLimit As Limit
     Set secondLimit = assemblyPocket.SecondLimit

```

### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the pocket sketch.

**Example:**     The following example retrieves in `sketch` the sketch on which the pocket `assemblyPocket` is built.

```VBScript
     Dim sketch As Sketch
     Set sketch = assemblyPocket.Sketch

```

### Property **SketchComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the pocket sketch.

**Example:**     The following example retrieves in `skComp` the component that contains the sketch of the pocket `assemblyPocket` is built.

```VBScript
     Dim skComp As Product
     Set skComp = assemblyPocket.SketchComponent

```

Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

   Retrieves the pocket direction vector components.
These components are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioDirection`      The pocket direction vector components, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example retrieves in `dirArray` the direction vector components of the pocket `assemblyPocket`.

```VBScript
     Dim dirArray(2)
     Call assemblyPocket.GetDirection(dirArray)
     Set x = dirArray[0]
     Set y = dirArray[1]
     Set z = dirArray[2]

```

### Sub **ReverseInnerSide**( )

   Reverses the pocket inner side when the profile is open.
This is useful for finding the shape to reach.

**Example:**     The following example reverses the current inner side of the pocket `assemblyPocket`.

```VBScript
     assemblyPocket.ReverseInnerSide

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLineComp`)

   Sets the pocket associated direction.

**Parameters:**

` iLine`      The pocket associated direction, as a reference to a line or an edge.
` iLineComp`      The component containing the associated direction reference

**Example:**     The following example sets the associated direction of the pocket `assemblyPocket` using the `dirRef` line of the component `dirComp`.

```VBScript
     assemblyPocket.SetDirection dirRef, dirComp

```

---

# AssemblySplit (Object)

**_Represents the AssemblySplit object._**

## Properties

### Property **SplittingComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the splitting element.

**Example:**     The following example retrieves in `sptComponent` the splitting component containing the splitting element of the assembly split `assemblySplit`:

```VBScript
     Dim sptComponent As Product
     Set sptComponent = assemblySplit.SplittingComponent

```

### Property **SplittingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

   Returns the splitting element.

**Example:**     The following example retrieves in `sptElement` the splitting element of the assembly split `assemblySplit`:

```VBScript
     Dim sptElement As Reference
     Set sptElement = assemblySplit.SplittingElement

```

### Property **SplittingSide**( ) As [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)

   Returns or sets the splitting side. The splitting side is the side of the split object kept after the split, with respect to the splitting element. A positive side refers to the split object side shown by the splitting element normal vector.

**Example:**     The following example returns in `sptSide` the splitting side of the assembly split `assemblySplit`, and then sets it to `catPositiveSide`:

```VBScript
     Set sptSide = assemblySplit.SplittingSide
     assemblySplit.SplittingSide = catPositiveSide

```

Methods

### Sub **ModifySplittingElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplittingElement`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSplittingElemComp`)

   Replaces the splitting element by a new one.

**Parameters:**

` iSplittingElement`      The new face or plane that will split the current body
` iSplittingElemComp`      The component that contains the new splitting element  **Example:**     The following example replaces the existing splitting element of the assembly split `assemblySplit` by `sptElem` contained in the `sptComponent` splitting component

```VBScript
     assemblySplit.ModifySplittingElement(sptElem, _
                                          sptComponent)

```