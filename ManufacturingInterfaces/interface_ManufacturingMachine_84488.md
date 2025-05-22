# ManufacturingMachine (Object)

**_Machine in machining domain._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Return the Comment of a Machine.

**Example:**     The following example return the comment `MachineComment` of to the manufacturing Machine `CurrentMachine`

```VBScript
MachineComment = CurrentMachine.Comment

```

### Property **MachineType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Return the Type of a Machine.

**Example:**     The following example return the type `MachineType` of to the manufacturing Machine `CurrentMachine`

```VBScript
MachineType = CurrentMachine.Type

```

### Property **NumberOfAttributes**( ) As short (Read Only)

Gives the number of attributes of a ManufacturingMachine.

**Example:**     The following example returns the `Number` of attributes of the ManufacturingMachine `CurrentMachine`

```VBScript
Number = CurrentMachine.NumberOfAttributes

```

### Property **NumberOfNumericalControlAttributes**( ) As short (Read Only)

This property returns the number of Numerical Control attributes of a Manufacturing Machine.  
### Property **NumberOfRotaryTableAttributes**( ) As short (Read Only)

This property returns the number of rotary table attributes of a Manufacturing Machine. The machine is upposed to accept Rotary table (type is Mfg3AxisWithTableRotationMachine).  
### Property **NumberOfSpindleAttributes**( ) As short (Read Only)

This property returns the number of Spindle attributes of a Manufacturing Machine.  
### Property **NumberOfToolChangeAttributes**( ) As short (Read Only)

This property returns the number of Tool change attributes of a Manufacturing Machine.  
### Property **PPTableName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Give the PPTableName linked to a Manufacturing Machine.

**Example:**     The following example returns the PPTableName `ThisPPTable` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
Set ThisPPTable = CurrentMachine.PPTableName

```

### Property **PostProcessorFile**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

This property returns the post processor file of a Manufacturing Machine Machine.PostProcessorFile  
### Property **PreferedToolCatalogName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Give the PreferedToolCatalogName linked to a Manufacturing Machine.

**Example:**     The following example returns the PreferedToolCatalogName `ThisCatalog` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
Set ThisCatalog = CurrentMachine.PreferedToolCatalogName

```

### Property **RotaryAxis**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Give the MfgRotaryAxis linked to a Manufacturing Machine.

**Example:**     The following example returns the MfgRotaryAxis `ThisAxis` linked to the Manufacturing Machine `CurrentMachine`

```VBScript
Set ThisAxis = CurrentMachine.RotaryAxis

```

Methods

### Func **DefaultName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Return the string the Type of a Machine.

**Example:**     The following example return the type `MachineType` of to the manufacturing Machine `CurrentMachine`

```VBScript
MachineType = CurrentMachine.Type

```

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieve the Attribute of a Manufacturing Machine.

**Example:**     The following example retreives in `HomePosX` the attribute `MFG_HOME_POS_X` of Manufacturing Machine `MyMachine`

```VBScript
 Set HomePosX = MyMachine.GetAttribute(MFG_HOME_POS_X)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieve the NLS name from the attribute name of a Manufacturing Machine.

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributeUnits`)

Retrieve the list of attribute units of a ManufacturingMachine.
The number of items in the output array is equal to the number of attributes of the machine.
When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Example:**     The following example retrieves in `TabAttributeUnits` the list of attribute units of the ManufacturingMachine `CurrentMachine`

```VBScript
call CurrentMachine.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of all attributes of a ManufacturingMachine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabAttributes` the list of attributes of the ManufacturingMachine `CurrentMachine`

```VBScript
call CurrentMachine.GetListOfAttributes(TabAttributes)

```

### Sub **GetListOfNumericalControlAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Numerical Control attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Numerical Control attributes of the Manufacturing Machine `myMachine`

```VBScript
call myMachine.GetListOfNumericalControlAttributes(oListOfAttributes)

```

### Sub **GetListOfRotaryTableAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Rotary table attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Tool Change attributes of the Manufacturing Machine `myMachine`

```VBScript
call myMachine.GetListOfRotaryTableAttributes(oListOfAttributes)

```

### Sub **GetListOfSpindleAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Spindle attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Spindle attributes of the Manufacturing Machine `myMachine`

```VBScript
call myMachine.GetListOfSpindleAttributes(oListOfAttributes)

```

### Sub **GetListOfToolChangeAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

Retrieve the list of Tool Change attributes of a Manufacturing Machine.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `oListOfAttributes` the list of Tool Change attributes of the Manufacturing Machine `myMachine`

```VBScript
call myMachine.GetListOfToolChangeAttributes(oListOfAttributes)

```

### Sub **set_DefaultValues**( )

Initialise the Manufacturing Machine parameters.

**Example:**     The following example make the init of the parameter of the Machine `ThisMachine` .

```VBScript
call ThisMachine.set_DefaultValues

```