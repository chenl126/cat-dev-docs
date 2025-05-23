# ManufacturingToolAssembly (Object)

**_Represents the tool assembly._**

## Properties

### Property **AssemblyType**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the tool assembly.

**Legal values** : the type of the tool assembly can be either MfgMillAndDrillToolAssembly or MfgLatheToolAssembly.

**Example:**      The following example returns the assembly type `Type` of the assembly `CurrentAssembly`:

```VBScript
     Set Type=CurrentAssembly.AssemblyType

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the default comment of a tool assembly.

**Example:**      The following example returns the comment `Comment` of the tool assembly `CurrentAssembly`:

```VBScript
     Comment=CurrentAssembly.Comment

```

### Property **Insert**( ) As [CATIAManufacturingInsert](../ManufacturingInterfaces/interface_ManufacturingInsert_78415.md) (Read Only)

   Returns the insert of an assembly.

**Example:**      The following example retrieves in `Insert` the insert of the assembly `CurrentAssembly`:

```VBScript
     Set Insert = CurrentAssembly.Insert

```

### Property **NumberOfAttributes**( ) As short (Read Only)

   Returns the number of attributes of a tool assembly.

**Example:**      The following example returns the `Number` of attributes of the tool assembly `CurrentAssembly`:

```VBScript
     Number = CurrentAssembly.NumberOfAttributes

```

### Property **Tool**( ) As [CATIAManufacturingTool](../ManufacturingInterfaces/interface_ManufacturingTool_62710.md) (Read Only)

   Returns the tool of an assembly.

**Example:**      The following example retrieves in `Tool` the manufacturing tool of the assembly `CurrentAssembly`:

```VBScript
     Set Tool = CurrentAssembly.Tool

```

### Property **ToolNumber**( ) As long (Read Only)

   Returns the number linked to a tool assembly.

**Example:**      The following example returns the `Number` linked to the tool assembly `CurrentAssembly`:

```VBScript
     Number = CurrentAssembly.ToolNumber

```

Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribute`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Returns an attribute of a tool assembly.
The attribute is identified using its name, and is retrieved as a [Parameter](../KnowledgeInterfaces/interface_Parameter_17963.md) object.

**Parameters:**

` iAttribute`      The attribute name

**Returns:**      The retrieved attribute  **Example:**      The following example retrieves in `Diameter` the attribute `MfgDiameter` of the tool assembly `CurrentAssembly`:

```VBScript
     Set Diameter = CurrentAssembly.GetAttribute(MfgDiameter)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributeName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the NLS value of an attribute.

**Parameters:**

` iAttributeName`      The attribute name

**Returns:**      The attribute NLS value  **Example:**      The following example gives in `NLSresult` the NLS value of the "MFG_COMMENT" attributes of the tool assembly `CurrentAssembly`:

```VBScript
     NLSresult = CurrentAssembly.GetAttributeNLSName("MFG_COMMENT")

```

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioListOfAttributeUnits`)

   Retrieves the list of attribute units of a tool assembly.
The number of items in the output array is equal to the number of attributes of the assembly. When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Parameters:**

` ioListOfAttributeUnits`      The retrieved list of attributes units

**Example:**      The following example retrieves in `TabAttributeUnits` the list of attribute units of the tool assembly `CurrentAssembly`:

```VBScript
     call CurrentAssembly.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioListOfAttributes`)

   Retrieves the list of attributes of a tool assembly.
Each attribute retrieved as a [Parameter](../KnowledgeInterfaces/interface_Parameter_17963.md) object.

**Parameters:**

` ioListOfAttributes`      The retrieved list of attributes

**Example:**      The following example retrieves in `TabAttributes` the list of attributes of the tool assembly `CurrentAssembly`:

```VBScript
     call CurrentAssembly.GetListOfAttributes(TabAttributes)

```