# ManufacturingTool (Object)

**_A ManufacturingTool for a Manufacturing Document._**

## Properties

### Property **Comment**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the Default Comment of a Manufacturing Setup.

**Example:**     The following example return the comment `ToolComment` of to the manufacturing tool `CurrentTool`

```VBScript
     ToolComment=CurrentTool.Comment

```

### Property **CorrectorCount**( ) As short (Read Only)

   Retreive the number of correctors of a Manufacturing tool.

**Example:**     The following example retreives in `CorrCount` the number of tool correctors of tool `CurrentTool`

```VBScript
     Set NbCorr = CurrentTool.CorrectorCount

```

### Property **NumberOfAttributes**( ) As short (Read Only)

   Give the Number og attributes of a Manufacturing Tool.

**Example:**     The following example returns the `Number` of attributes of the manufacturing Tool `CurrentTool`

```VBScript
     Number = CurrentTool.NumberOfAttributes

```

### Property **Picture**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the path where a picture of the parametrized tool is stored.

**Example:**     The following example return the path `PicturePath` where can be found the picture of the tool `CurrentTool`

```VBScript
     PicturePath=CurrentTool.Picture

```

### Property **ToolNumber**( ) As long (Read Only)

   Give the Number linked to a Manufacturing Tool.

**Example:**     The following example returns the `Number` linked to the manufacturing Tool `CurrentTool`

```VBScript
     Number = CurrentTool.ToolNumber

```

### Property **ToolType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Return the technological type of a the tool.

**Example:**     The following example return the tool type `ToolType` of to the manufacturing tool `CurrentTool`

```VBScript
     Set ToolType=CurrentTool.ToolType

```

Methods

### Func **AddCorrector**( ) As [CATIAManufacturingToolCorrector](../ManufacturingInterfaces/interface_ManufacturingToolCorrector_145356.md)

   Adds a corrector to a Manufacturing tool.

**Example:**     The following example adds in `Corr` the tool corrector of Tool `CurrentTool`

```VBScript
     Set Corr = CurrentTool.AddCorrector

```

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieve by is name the attribute of a Manufacturing Tool.
Each attribute is a CKE object.

**Example:**     The following example retreives in `Diameter` the attribute `MfgDiameter` of the Manufacturing Tool `firstTool`

```VBScript
     Set Diameter = firstTool.GetAttribute(MfgDiameter)

```

### Func **GetAttributeNLSName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttributName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieve the NLS name from the attribute name of a Manufacturing Tool.

### Func **GetCorrector**( short  `index`) As [CATIAManufacturingToolCorrector](../ManufacturingInterfaces/interface_ManufacturingToolCorrector_145356.md)

   Retreive the corrector (index) of a Manufacturing tool.

**Example:**     The following example retreives in `Corr` the tool corrector of Tool `CurrentTool`

```VBScript
     Set Corr = CurrentTool.GetCorrector(index)

```

### Sub **GetListOfAptParameters**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAptParameters`)

   Retrieve the list of apt definition parameters of a Manufacturing Tool.
Parameters are returned in an array of real values.

### Sub **GetListOfAttributeUnits**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributeUnits`)

   Retrieve the list of attribute units of a Manufacturing Tool.
The number of items in the output array is equal to the number of attributes of the tool.
When an attribute has no unit definition, the corresponding unit item in the output array is a blank string.

**Example:**     The following example retrieves in `TabAttributeUnits` the list of attribute units of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfAttributeUnits(TabAttributeUnits)

```

### Sub **GetListOfAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of attributes of a Manufacturing Tool.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabAttributes` the list of attributes of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfAttributes(TabAttributes)

```

### Sub **GetListOfGeomAttributes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oListOfAttributes`)

   Retrieve the list of geometry attributes of a Manufacturing Tool.
Each attribute is returned as the name of a CKE object.

**Example:**     The following example retrieves in `TabGeomAttributes` the list of geometry attributes of the Manufacturing Tool `firstTool`

```VBScript
     call firstTool.GetListOfGeomAttributes(TabAttributes)

```