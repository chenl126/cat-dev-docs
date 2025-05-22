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