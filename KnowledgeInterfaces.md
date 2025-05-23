# KnowledgeInterfaces Framework

## Object Index

  * [Angle](KnowledgeInterfaces/interface_Angle_5497.md)
  * [BoolParam](KnowledgeInterfaces/interface_BoolParam_17217.md)
  * [Check](KnowledgeInterfaces/interface_Check_5408.md)
  * [ConstraintSatisfaction](KnowledgeInterfaces/interface_ConstraintSatisfaction_104794.md)
  * [DesignTable](KnowledgeInterfaces/interface_DesignTable_25284.md)
  * [Dimension](KnowledgeInterfaces/interface_Dimension_18130.md)
  * [EnumParam](KnowledgeInterfaces/interface_EnumParam_17344.md)
  * [FeatureGenerator](KnowledgeInterfaces/interface_FeatureGenerator_55282.md)
  * [Formula](KnowledgeInterfaces/interface_Formula_11046.md)
  * [FreeParameter](KnowledgeInterfaces/interface_FreeParameter_36139.md)
  * [FreeParameters](KnowledgeInterfaces/interface_FreeParameters_42284.md)
  * [IntParam](KnowledgeInterfaces/interface_IntParam_13730.md)
  * [KnowledgeActivateObject](KnowledgeInterfaces/interface_KnowledgeActivateObject_110372.md)
  * [KnowledgeObject](KnowledgeInterfaces/interface_KnowledgeObject_47429.md)
  * [KnowledgeSheetSettingAtt](KnowledgeInterfaces/interface_KnowledgeSheetSettingAtt_121070.md)
  * [LanguageSheetSettingAtt](KnowledgeInterfaces/interface_LanguageSheetSettingAtt_110732.md)
  * [Law](KnowledgeInterfaces/interface_Law_2130.md)
  * [Length](KnowledgeInterfaces/interface_Length_8108.md)
  * [List](KnowledgeInterfaces/interface_List_3838.md)
  * [ListParameter](KnowledgeInterfaces/interface_ListParameter_36657.md)
  * [Loop](KnowledgeInterfaces/interface_Loop_3798.md)
  * [Optimization](KnowledgeInterfaces/interface_Optimization_32466.md)
  * [OptimizationConstraint](KnowledgeInterfaces/interface_OptimizationConstraint_106166.md)
  * [OptimizationConstraints](KnowledgeInterfaces/interface_OptimizationConstraints_116449.md)
  * [Optimizations](KnowledgeInterfaces/interface_Optimizations_38238.md)
  * [Parameter](KnowledgeInterfaces/interface_Parameter_17963.md)
  * [ParameterSet](KnowledgeInterfaces/interface_ParameterSet_31016.md)
  * [ParameterSets](KnowledgeInterfaces/interface_ParameterSets_36730.md)
  * [Parameters](KnowledgeInterfaces/interface_Parameters_22342.md)
  * [RealParam](KnowledgeInterfaces/interface_RealParam_17053.md)
  * [Relation](KnowledgeInterfaces/interface_Relation_14366.md)
  * [Relations](KnowledgeInterfaces/interface_Relations_18301.md)
  * [ReportGenerationSheetSettingAtt](KnowledgeInterfaces/interface_ReportGenerationSheetSettingAtt_202432.md)
  * [Rule](KnowledgeInterfaces/interface_Rule_3720.md)
  * [SetOfEquation](KnowledgeInterfaces/interface_SetOfEquation_36247.md)
  * [StrParam](KnowledgeInterfaces/interface_StrParam_13874.md)
  * [ToleranceSheetSettingAtt](KnowledgeInterfaces/interface_ToleranceSheetSettingAtt_120946.md)
  * [Unit](KnowledgeInterfaces/interface_Unit_3832.md)
  * [Units](KnowledgeInterfaces/interface_Units_5973.md)
  * [UnitsSheetSettingAtt](KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.md)

## Enumerated Types Index

  * [CatAlgorithmType](KnowledgeInterfaces/enum_CatAlgorithmType_54838.md)
  * [CatOptimizationType](KnowledgeInterfaces/enum_CatOptimizationType_78349.md)

---

# CatAlgorithmType (Enumeration)

**_Algorithm types._**

**Values:**

` catSimulatedAnnealing`      see Product Engineering Optimizer product help for explanation
` catGradient`      see Product Engineering Optimizer product help for explanation
` catCAAalgorithm`      see Product Engineering Optimizer product help for explanation

---

# CatOptimizationType (Enumeration)

**_Optimization types._**

**Values:**

` catMinimum`      minimum of objective parameter is looked for
` catMaximum`      maximum of objective parameter is looked for
` catTargetValue`      defined target is looked for for objective parameter
` catOnlyBoundedVariation`      no doc.
` catNone`      when the type of the optimization is not defined yet.
` catCstOnly`      when the type of the optimization handles only constraints.

---

# Angle (Object)

**_Represents the angle parameter._**
The following example shows how to create it:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim angle1 As Angle
     Set angle1  = part1.Parameters.CreateDimension("angle1", "ANGLE", 40.)

```

---

# BoolParam (Object)

**_Represents the boolean parameter._**
The following example shows how to create it:

```VBScript
    	Dim CATDocs As Documents
      Set CATDocs      = CATIA.Documents
    	Dim part1 As Document
      Set part1        = CATDocs.Add("CATPart")
    	Dim availability As BooleanParam
      Set availability = part1.Parameters.CreateBoolean("availability", True)

```

## Properties

### Property **Value**( ) As boolean

   Returns or sets the value of the boolean parameter.

**Example:**      This example sets the `availability` boolean parameter value to True if its value is False:

```VBScript
     If (availability.Value = False)  Then
         availability.Value = True
     End If

```

---

# Check (Object)

**_Represents the check relation._**
The following example shows how to create a check which checks if a given mass is less than 10kg. The mass should be defined previously:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim mass As RealParam
     Set mass         = part1.Part.Parameters.CreateReal("mass", 5.)
     Dim maximummass As Check
     Set maximummass = part1.Relations.CreateCheck
                        ("maximummass",
                         "Ensures that mass is less than 10 kg",
                         "mass<10kg")

```

## Properties

### Property **Diagnosis**( ) As boolean (Read Only)

   Returns the check diagnosis. True if the condition of the check is verified. False otherwise.
```

### Property **Severity**( ) As long

   Returns or sets the check severity. The severity is the way the check will manifest itself:
* Silent (1)
* Information (2)
* Warning (3)
```

---

# ConstraintSatisfaction (Object)

**_Represents the set of equation._**

## Methods

### Sub **Solve**( )

   Solves the constraint satisfaction problem.

---

# DesignTable (Object)

**_Represents the DesignTable object._**

## Properties

### Property **ColumnsNb**( ) As short (Read Only)

   Returns the nb of columns in the design table file.  
### Property **Configuration**( ) As short

   Returns or sets the current configuration. Legal values: 1 to ConfigurationsNb.  
### Property **ConfigurationsNb**( ) As short (Read Only)

   Returns the number of design table configurations.  
### Property **CopyMode**( ) As boolean

   Returns or sets whether the data contained in the file must be included inside the CATIA model.  
### Property **FilePath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the design table (read/write property).  Methods

### Sub **AddAssociation**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetColumn`)

   Adds an association between a parameter iParameter and a column of the design table. This method does nothing if the column does not exist or if the type of the parameter isn t compliant with the column type.

**Parameters:**

` iParameter`      The parameter.
` iSheetColumn`      The name of the column to be associated with the parameter.

### Sub **AddNewRow**( )

   Adds a row in the design table source file. The new row is filled in with values of associated parameters. ##### Since V5R14 ##### If the file contains at least one empty row between two not empty rows, the behavior of this method is the same for Excel and Text files : => the new row containing the current parameters values replaces the first empty row found from the beginning of the file. RQ : before R14, for text files, the new row was appended at the end of the file. The empty rows were never filed by this way, so that the new row was not visible in Design Table dialog. ######################

**Returns:**      S_OK if succeeded, E_FAIL else.  
### Func **CellAsString**( short  `iRow`,  short  `iColumn`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the content of a specific cell.

**Parameters:**

` iRow`      the index of the row where the cell is located.
` iColumn`      the index of the column where the cell is located.

### Sub **RemoveAssociation**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetColumn`)

   Removes an existing association. This method does nothing if the column isn t associated or if it doesn t exist.

**Parameters:**

` iSheetColumn`      The name of an associated column.

### Sub **Synchronize**( )

   Synchronizes the design table with its source file. If the file is managed in Enovia LCA, copies this file on local disk, and synchronizes design table content

---

# Dimension (Object)

**_Represents the dimension parameter._**
It is an abstract object which is not intended to be created as such, but from which the length and angle parameters derive.

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md), [Angle](../KnowledgeInterfaces/interface_Angle_5497.md)

## Properties

### Property **Unit**( ) As [CATIAUnit](../KnowledgeInterfaces/interface_Unit_3832.md) (Read Only)

   Returns the unit used for this dimension object.  Methods

### Func **ValueAsString2**( long  `iNbDecimals`,  boolean  `iShowTrailingZeros`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets the value of the parameter as a string, with a given precision.

**Parameters:**

` iNbDecimals`      the maximum number of decimal places to use to generate the string (minimum 0, maximum 9)
` iShowTrailingZeros`      this argument says if trailing zeros have to be shown  **Example:**      This example gets the value of the existing `dimension` parameter and shows it in a message box

```VBScript
     Dim str
     str = dimension.ValueAsString;
     MessageBox str

```

---

# EnumParam (Object)

**_Represents the enum parameter._**

## Properties

### Property **ValueEnum**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the value of the EnumParameter object. Units are expressed in the IS unit system, except for lengthes expressed in millimeters, and angles expressed in decimal degrees.

**Example:**      This example sets the `param1` value to 1 if its value is greater than 2.5:

```VBScript
     If (density.Value > 2.5)  Then
         density.Value = 1
     End If

```

---

# FeatureGenerator (Object)

**_The interface to access a CATIAFeatureGenerator._**

## Properties

### Property **NbGeneratedFeatures**( ) As long (Read Only)

   Number of generated features in last generation.  
### Property **Script**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the script that describes what is to be generated.  Methods

### Sub **Generate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iContext`)

   Generates the features.  
### Sub **GenerateInContext**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iInputsArray`)

   Generates the features.  
### Sub **LoadScriptFromFilePath**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilePath`)

   Sets a script from a document file.

---

# Formula (Object)

**_Represents the formula relation._**
The following example shows how to create a formula that computes the mass of a cuboid, given its geometric dimensions and the density of the material it is made of:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim width As RealParam
     Set width        = part1.Part.Parameters.CreateReal("width", 1.)
     Dim height As RealParam
     Set height       = part1.Part.Parameters.CreateReal("height", 2.)
     Dim depth As RealParam
     Set depth        = part1.Part.Parameters.CreateReal("depth", 3.)
     Dim density As RealParam
     Set density      = part1.Part.Parameters.CreateReal("density", 1.5)
     Dim mass As RealParam
     Set mass         = part1.Part.Parameters.CreateReal("mass", 0.)
     Dim computemass As RealParam
     Set computemass = part1.Part.Relations.CreateFormula
                        ("computemass",
                         "Computes the cuboid mass",  mass,
                         "(width*height*depth)*density")

```

---

# FreeParameter (Object)

**_Interface to access a CATIAFreeParameter._**

## Properties

### Property **InfRange**( ) As double

   Returns or sets the inferior bound of the free parameter object. The optimization cannot escape those bounds.  
### Property **Parameter**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns or sets which parameter (CATIAParameter) is linked to this object. The parameter must be real.  
### Property **Step**( ) As double

   Returns or sets the initial step used by the optimisation to look for a better solution. This step is just a preliminary indication. It will vary during the optimisation process.  
### Property **SupRange**( ) As double

   Returns or sets the superior bound of the free parameter object. The optimization cannot escape those bounds.

---

# FreeParameters (Collection)

**_Interface to access a CATIAFreeParameters._**

## Methods

### Func **AddFreeParameter**( [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)  `parameter`) As [CATIAFreeParameter](../KnowledgeInterfaces/interface_FreeParameter_36139.md)

   Adds a free parameter. This parameter must not be read only.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFreeParameter](../KnowledgeInterfaces/interface_FreeParameter_36139.md)

   Retrieves an optimization using its index or its name from the Free Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the free parameter to retrieve from the collection of free parameters. As a numerics, this index is the rank of the free parameter in the collection. The index of the first free parameter in the collection is 1, and the index of the last free parameter is Count. As a string, it is the name you assigned to the free parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the free parameter name by the property panel.  **Returns:**      The retrieved free parameter  **Example:**      This example retrieves the last free parameter in the `free parameters` collection.

```VBScript
     Set lastFreeParameter = freeParameters.Item(freeParameters.Count)

```

### Sub **RemoveFreeParameter**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a free parameter.

---

# IntParam (Object)

**_Represents the integer parameter._**
The following example shows how to create it:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Dccument
     Set part1   = CATDocs.Add("CATPart")
     Dim  year As IntParam
     Set year    = part1.Part.Parameters.CreateInteger("year", 1998)

```

## Properties

### Property **RangeMax**( ) As long

   Returns or sets the value of the upper bound that the parameter object value can take.

**Example:**      This example sets the `RangeMax` value to 0 if its value is smaller than 0:

```VBScript
     If (Length.RangeMax < 0.0 and Length.RangeMaxValidity <> 0)  Then
         Length.RangeMax = 0.0
     End If

```

### Property **RangeMaxValidity**( ) As long

   Returns or sets the type of the upper bound of the parameter.

0    the upper bound is meaningless 1    the upper bound can be reached 2    the upper bound cannot be reached  
### Property **RangeMin**( ) As long

   Returns or sets the value of the lower bound that the parameter object value can take.

**Example:**      This example sets the `RangeMin` value to 0 if its value is bigger than 0:

```VBScript
     If (Length.RangeMin > 0.0 and Length.RangeMinValidity <> 0)  Then
         Length.RangeMin = 0.0
     End If

```

### Property **RangeMinValidity**( ) As long

   Returns or sets the type of the lower bound of the parameter.

0    the lower bound is meaningless 1    the lower bound can be reached 2    the lower bound cannot be reached  
### Property **Value**( ) As long

   Returns or sets the value of the integer parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `year` value to 0 if its value is equal to 2000:

```VBScript
     If (year.Value = 2000)  Then
         year.Value = 0
     End If

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

   Returns an array containing the different values that the int param can take in the case of multiple values.

**Example:**

```VBScript
     Dim enumValues () as Variant
     ReDim enumValues (anIntegerParameter.GetEnumerateValuesSize() - 1)
     anIntegerParameter.GetEnumerateValues(enumValues)
     For i = LBound(enumValues) to UBound(enumValues)
       ...
     Next

```

### Func **GetEnumerateValuesSize**( ) As long

   Returns the number of enumerate values.  
### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

   Sets an array containing the different values that the real param can take in the case of multiple values.  
### Sub **SuppressEnumerateValues**( )

   Resets the status of the object to a single value object.

---

# KnowledgeActivateObject (Object)

**_Interface to access a CATIAKnowledgeActivableObject._**

## Properties

### Property **Activated**( ) As boolean (Read Only)

   Returns whether the relation is activated.

**True** if the relation is activated. An activated relation is processed whenever the value of one of its input parameter is modified.

**Example:**      This example retrieves whether the `maximummass` relation is activated, and if true, displays the result in a message box:

```VBScript
     If ( maximummass.Activated ) Then
          MsgBox "maximummass is activated"
     End If

```

Methods

### Sub **Activate**( )

   Activates the relation. The relation will be processed whenever the value of one of its input parameter is modified.

**Example:**      This example activates the `maximummass` relation:

```VBScript
     maximummass.Activate()

```

### Sub **Deactivate**( )

   Deactivates the relation. The relation will no longer be processed when the value of one of its input parameter is modified.

**Example:**      This example deactivates the `maximummass` relation:

```VBScript
     maximummass.Deactivate()

```

---

# KnowledgeObject (Object)

**_Interface to access a CATIAKnowledgeObject._**

## Properties

### Property **Hidden**( ) As boolean

   Returns or sets wether the relation is hidden or should be hidden. or not.  
### Property **IsConst**( ) As boolean

   Returns or sets wether the relation is Const or should be Const. or not.

---

# KnowledgeSheetSettingAtt (Object)

**_The interface to access a CATIAKnowledgeSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Knowledge sheet.

## Properties

### Property **DesignTablesCopyData**( ) As short

   Returns or sets the DesignTablesCopyData parameter.

**Role** :Return or Set the DesignTablesCopyData parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDesignTablesCopyData`      **Legal values** :
`0 :` default mode for design table : copy data into models
`1 :` default mode for design table : do not copy data into models.

### Property **DesignTablesSynchronization**( ) As short

   Returns or sets the DesignTablesSynchronization parameter.

**Role** :Return or Set the DesignTablesSynchronization parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDesignTablesSynchronization`      **Legal values** :
`0 :` automatic synchronization at load for design table
`1 :` interactive synchronization at load for design table
`2 :` manual synchronization for design table.

### Property **ParameterNameSurroundedByTheSymbol**( ) As short

   Returns or sets the ParameterNameSurroundedByTheSymbol parameter.

**Role** :Return or Set the ParameterNameSurroundedByTheSymbol parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterNameSurroundedByTheSymbol`      **Legal values** :
`0 :` to see parameter name not surrounded by the symbol "'"
`1 :` to see parameter name surrounded by the symbol "'".

### Property **ParameterTreeViewWithFormula**( ) As short

   Returns or sets the ParameterTreeViewWithFormula parameter.

**Role** :Return or Set the ParameterTreeViewWithFormula parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterTreeViewWithFormula`      **Legal values** :
`0 :` to see parameter tree view without formula
`1 :` to see parameter tree view with formula.

### Property **ParameterTreeViewWithValue**( ) As short

   Returns or sets the ParameterTreeViewWithValue parameter.

**Role** :Return or Set the ParameterTreeViewWithValue parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterTreeViewWithValue`      **Legal values** :
`0 :` to see parameter tree view without value
`1 :` to see parameter tree view with value.

### Property **RelationsUpdateInPartContextEvaluateDuringUpdate**( ) As short

   Returns or sets the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.

**Role** :Return or Set the RelationsUpdateInPartContextEvaluateDuringUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oRelationsUpdateInPartContextEvaluateDuringUpdate`      **Legal values** :
`0 :` creation of relations not evaluate during update
`1 :` creation of relations evaluate during update.

### Property **RelationsUpdateInPartContextSynchronousRelations**( ) As short

   Returns or sets the RelationsUpdateInPartContextSynchronousRelations parameter.

**Role** :Return or Set the RelationsUpdateInPartContextSynchronousRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oRelationsUpdateInPartContextSynchronousRelations`      **Legal values** :
`0 :` creation of unsynchronous relations
`1 :` creation of synchronous relations.
Methods

### Func **GetDesignTablesCopyDataInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DesignTablesCopyData parameter.

**Role** :Retrieves the state of the DesignTablesCopyData parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDesignTablesSynchronizationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DesignTablesSynchronization parameter.

**Role** :Retrieves the state of the DesignTablesSynchronization parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterNameSurroundedByTheSymbolInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ParameterNameSurroundedByTheSymbol parameter.

**Role** :Retrieves the state of the ParameterNameSurroundedByTheSymbol parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterTreeViewWithFormulaInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ParameterTreeViewWithFormula parameter.

**Role** :Retrieves the state of the ParameterTreeViewWithFormula parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterTreeViewWithValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ParameterTreeViewWithValue parameter.

**Role** :Retrieves the state of the ParameterTreeViewWithValue parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsUpdateInPartContextEvaluateDuringUpdateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.

**Role** :Retrieves the state of the RelationsUpdateInPartContextEvaluateDuringUpdate parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsUpdateInPartContextSynchronousRelationsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the RelationsUpdateInPartContextSynchronousRelations parameter.

**Role** :Retrieves the state of the RelationsUpdateInPartContextSynchronousRelations parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetDesignTablesCopyDataLock**( boolean  `iLocked`)

   Locks or unlocks the DesignTablesCopyData parameter.

**Role** :Locks or unlocks the DesignTablesCopyData parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDesignTablesSynchronizationLock**( boolean  `iLocked`)

   Locks or unlocks the DesignTablesSynchronization parameter.

**Role** :Locks or unlocks the DesignTablesSynchronization parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterNameSurroundedByTheSymbolLock**( boolean  `iLocked`)

   Locks or unlocks the ParameterNameSurroundedByTheSymbol parameter.

**Role** :Locks or unlocks the ParameterNameSurroundedByTheSymbol parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterTreeViewWithFormulaLock**( boolean  `iLocked`)

   Locks or unlocks the ParameterTreeViewWithFormula parameter.

**Role** :Locks or unlocks the ParameterTreeViewWithFormula parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterTreeViewWithValueLock**( boolean  `iLocked`)

   Locks or unlocks the ParameterTreeViewWithValue parameter.

**Role** :Locks or unlocks the ParameterTreeViewWithValue parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsUpdateInPartContextEvaluateDuringUpdateLock**( boolean  `iLocked`)

   Locks or unlocks the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.

**Role** :Locks or unlocks the RelationsUpdateInPartContextEvaluateDuringUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsUpdateInPartContextSynchronousRelationsLock**( boolean  `iLocked`)

   Locks or unlocks the RelationsUpdateInPartContextSynchronousRelations parameter.

**Role** :Locks or unlocks the RelationsUpdateInPartContextSynchronousRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# LanguageSheetSettingAtt (Object)

**_The interface to access a CATIALanguageSheetSettingAtt._**

## Properties

### Property **KnowledgeBuildPathDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the CATKnowledgeBuildPath setting parameter.

**Role** :Return or Set the CATKnowledgeBuildPath parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oKnowledgeBuildPathDirectory`      The knowledge build path directory: the path where all the resources are located.

### Property **ListOfPackagesToLoad**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ListOfPackagesToLoad parameter.

**Role** :Return or Set the ListOfPackagesToLoad parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oListOfPackagesToLoad`      The list of packages to load.

### Property **LoadAllPackages**( ) As short

   Returns or sets the LoadAllPackages parameter.

**Role** :Return or Set the LoadAllPackages parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLoadAllPackages`      **Legal values** :
`0 :` to not load all packages
`1 :` to load all packages.

### Property **LoadExtendedLanguageLib**( ) As short

   Returns or sets the LoadExtendedLanguageLib parameter.

**Role** :Return or Set the LoadExtendedLanguageLib parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLoadExtendedLanguageLib`      **Legal values** :
`0 :` to not use extended libraries
`1 :` to use extended libraries.

### Property **ReferenceDirectoryForTypes**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ReferenceDirectoryForTypes parameter.

**Role** :Return or Set the ReferenceDirectoryForTypes parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReferenceDirectoryForTypes`      The reference directory for types.
Methods

### Func **GetKnowledgeBuildPathDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the CATKnowledgeBuildPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetListOfPackagesToLoadInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ListOfPackagesToLoad setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLoadAllPackagesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the LoadAllPackages setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetLoadExtendedLanguageLibInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the LoadExtendedLanguageLib setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetReferenceDirectoryForTypesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ReferenceDirectoryForTypes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetKnowledgeBuildPathDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the CATKnowledgeBuildPath setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetListOfPackagesToLoadLock**( boolean  `iLocked`)

   Locks or unlocks the ListOfPackagesToLoad setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLoadAllPackagesLock**( boolean  `iLocked`)

   Locks or unlocks the LoadAllPackages setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetLoadExtendedLanguageLibLock**( boolean  `iLocked`)

   Locks or unlocks the LoadExtendedLanguageLib setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetReferenceDirectoryForTypesLock**( boolean  `iLocked`)

   Locks or unlocks the ReferenceDirectoryForTypes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.

---

# Law (Object)

**_Represents the Law object._**

## Methods

### Sub **AddFormalParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitude`)

   Creates a formal parameter for the law.

**Parameters:**

` iName`      The name of the formal parameter.
` iType`      The type name of the formal parameter.

### Sub **RemoveFormalParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

   Removes a formal parameter of the law.

**Parameters:**

` iName`      The name of the formal parameter.

---

# Length (Object)

**_Represents the length parameter._**
The following example shows how to create it:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim Width As Length
     Set width   = part1.Part.Parameters.CreateDimension("width", "LENGTH", 20.)

```

By default the units are the default units of the IS of units.

---

# List (Collection)

**_Represents a CATIAList._**

## Methods

### Sub **Add**( [CATIABase](../System/interface_AnyObject_17321.md)  `iItemValue`)

   Adds an item at the end of the list. Does an AddRef on the item. Returns E_FAIL if the object type is not correct. Will return E_FAIL if trying to set an already existing element while IsDuplicateElementsAllowed is false.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves a Feature using its index or its name from the Features collection.

**Parameters:**

` iIndex`      The index or the name of the Feature to retrieve from the collection of Features. As a numerics, this index is the rank of the Feature in the collection. The index of the first Feature in the collection is 1, and the index of the last Feature is Count. As a string, it is the name you assigned to the Feature using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Feature.  **Returns:**      The retrieved Feature  **Example:**      This example retrieves the last Feature in the `Features` collection.

```VBScript
     Dim lastFeature As CATIABase
     Set lastFeature = Features.Item(Features.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Feature from the Features collection.

**Parameters:**

` iIndex`      The index or the name of the Feature to retrieve from the collection of Features. As a numerics, this index is the rank of the Feature in the collection. The index of the first Feature in the collection is 1, and the index of the last Feature is Count. As a string, it is the name you assigned to the Feature using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Feature.  **Example:**      This example removes the Feature named `density` from the `Features` collection.

```VBScript
     Features.Remove("density")

```

### Sub **Reorder**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndexCurrent`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndexTarget`)

   Reorders an element by moving it from the current position to the target position. Doesn't change the list if either position is out of the list. Return E_FAIL if cannot reorder.

### Sub **Replace**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iItemValue`)

   Sets an item in the list at a position. Does an AddRef on the item. Returns E_FAIL if the object type is not correct or the index is out of bounds. Returns E_FAIL if trying to set an already existing element while IsDuplicateElementsAllowed is false.

---

# ListParameter (Object)

**_Represents a CATIAListParameter._**

## Properties

### Property **ValueList**( ) As [CATIAList](../KnowledgeInterfaces/interface_List_3838.md) (Read Only)

   Returns or sets the value of the List object.

---

# Loop (Object)

**_The interface to access a CATIALoop._**

---

# Optimization (Object)

**_Represents an Optimization object._**

## Properties

### Property **AlgorithmType**( ) As [CatAlgorithmType](../KnowledgeInterfaces/enum_CatAlgorithmType_54838.md)

   Returns or sets the algorithm type. Currently available algorithms are gradient and simulatedAnnealing

**See also:**      [CatAlgorithmType](../KnowledgeInterfaces/enum_CatAlgorithmType_54838.md) 
### Property **Constraints**( ) As [CATIAOptimizationConstraints](../KnowledgeInterfaces/interface_OptimizationConstraints_116449.md) (Read Only)

   Returns the collection of optimization constraints.  
### Property **ConvSpeed**( ) As long

   Returns or sets the convergence speed for some gradients and the simulated annealing.  
### Property **FreeParameters**( ) As [CATIAFreeParameters](../KnowledgeInterfaces/interface_FreeParameters_42284.md) (Read Only)

   Returns the collection of the free parameters.  
### Property **MaxEvalsNb**( ) As long

   Returns or sets the maximum number of model updates allowed during one run of the optimization.  
### Property **MaxEvalsWoImprovement**( ) As long

   Returns or sets the maximum number of model updates without improvement of the problem solution during one run of the optimization.  
### Property **MaxTime**( ) As long

   Returns or sets the maximum time allowed for one run of the optimization (in minutes).  
### Property **ObjectiveParameter**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns or sets the objective parameter of the optimization. This parameter can not exist (in this case the get_ method returns E_FAIL) when the optimization contains only constraints and uses Simulated Annealing, or if the optimization feature doesn't contain all information necessary to be run.  
### Property **OptimizationType**( ) As [CatOptimizationType](../KnowledgeInterfaces/enum_CatOptimizationType_78349.md)

   Returns or sets the type of the optimization: minimum, maximum or target value searched on the objective parameter.

**See also:**      [CatOptimizationType](../KnowledgeInterfaces/enum_CatOptimizationType_78349.md) 
### Property **TargetValue**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the objective parameter target value. (used only if the optimization type is a target value search)  
### Property **UseMaxEvalsWoImprovement**( ) As boolean

   Returns or sets if the number of updates without improvement of the solution has to be used as a termination criterion.  
### Property **UseMaxTime**( ) As boolean

   Returns or sets if max time has to be used as a termination criterion.  Methods

### Sub **Run**( boolean  `iWithStopDialog`)

   Runs the optimization as it is defined. The stop dialog appears if argument is TRUE
Before running, a check is made to ensure that the optimization feature contains enough information to run the optimization. In the case where some information is missing, this method returns E_FAIL
WARNING : if argument is TRUE, the optimization is launched asynchronously, and you can not run several optimizations in this mode.

---

# OptimizationConstraint (Object)

**_Represents an optimization constraint._**

**See also:**      [OptimizationConstraints](../KnowledgeInterfaces/interface_OptimizationConstraints_116449.md)

## Properties

### Property **DistanceToSatisfaction**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the parameter containing the distance to constraint satisfaction.  
### Property **Precision**( ) As double

   Returns or sets the constraint precision. Only for equality constraints.
The constraint precision allows the system to know when an equality constraint can be declared as satisfied (when : distance to satisfaction < precision).  
### Property **Satisfaction**( ) As boolean (Read Only)

   Returns the constraint satisfaction.

---

# OptimizationConstraints (Collection)

**_Represents a collection of Optimization Constraint._**

## Methods

### Func **AddConstraint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `constraintExpression`) As [CATIAOptimizationConstraint](../KnowledgeInterfaces/interface_OptimizationConstraint_106166.md)

   Adds a optimization constraint. This parameter must not be read only.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAOptimizationConstraint](../KnowledgeInterfaces/interface_OptimizationConstraint_106166.md)

   Returns an optimization constraint using its index or its name from the optimization constraints collection.

**Parameters:**

` iIndex`      The index or the name of the optimization constraint to retrieve from the collection of optimization constraints. As a numerics, this index is the rank of the optimization constraint in the collection. The index of the first optimization constraint in the collection is 1, and the index of the last optimization constraint is Count. As a string, it is the name you assigned to the optimization constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the optimization constraint name by the property panel.  **Returns:**      The retrieved optimization constraint  **Example:**      This example retrieves the last optimization constraint in the `optimization constraints` collection.

```VBScript
     Set lastConstraint = constraints.Item(constraints.Count)

```

### Sub **RemoveConstraint**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a given optimization constraint using its index or its name from the optimization constraints collection.

**Parameters:**

` iIndex`      the name of the constraint if argument is a string or the index of the constraint if argument is an integer.

---

# Optimizations (Collection)

**_Represents a collection of optimization features._**

**See also:**      [Optimization](../KnowledgeInterfaces/interface_Optimization_32466.md)

## Methods

### Func **CreateConstraintsSatisfaction**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFormulaBody`) As [CATIASetOfEquation](../KnowledgeInterfaces/interface_SetOfEquation_36247.md)

   Returns a set of equations.

**Parameters:**

` iName`      The name of the set of equations.
` iComment`      The comment of the set of equations.
` iFormulaBody`      The body of the set of equations " a==b+4; c ≤ 90".

### Func **CreateOptimization**( ) As [CATIAOptimization](../KnowledgeInterfaces/interface_Optimization_32466.md)

   Creates an empty optimization.
This optimization cannot be used while its properties have not been set.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves an optimization using its index or its name from the Optimizations collection.

**Parameters:**

` iIndex`      The index or the name of the item (optimization or constraintSatisfaction) to retrieve from the collection of optimizations. As a numerics, this index is the rank of the item in the collection. The index of the first item in the collection is 1, and the index of the last item is Count. As a string, it is the name you assigned to the item using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the item name by the property panel.  **Returns:**      either the retrieved optimization or the retreived constraintSatisfaction  **Example:**      This example retrieves the last item (optimization or constraintSatisfaction) in the `optimizations` collection.

```VBScript
     Set lastItem = optimizations.Item(optimizations.Count)

```

---

# Parameter (Object)

**_Represents the parameter._**
It can be computed from a relation: formula, program, or check. It is an abstract object which is not intended to be created as such, but from which the integer, bolean, real, and string parameters derive. Here is an example to create one:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim density As RealParam
     Set density = part1.Part.Parameters.CreateReal("density", 2.5)

```

**See also:**      [IntParam](../KnowledgeInterfaces/interface_IntParam_13730.md), [BoolParam](../KnowledgeInterfaces/interface_BoolParam_17217.md), [RealParam](../KnowledgeInterfaces/interface_RealParam_17053.md), [StrParam](../KnowledgeInterfaces/interface_StrParam_13874.md), [Formula](../KnowledgeInterfaces/interface_Formula_11046.md), [Rule](../KnowledgeInterfaces/interface_Rule_3720.md), [Check](../KnowledgeInterfaces/interface_Check_5408.md)

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the parameter object comment.  
### Property **Context**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the context of the parameter : a part, a product, a drafting, a process, depending where the parameter is.  
### Property **Hidden**( ) As boolean

   Returns or sets wether the parameter is hidden or should be hidden. or not.  
### Property **IsTrueParameter**( ) As boolean (Read Only)

   Returns a boolean saying if the parameter is a true one (real, dimension, string, etc.) or a geometrical one (isolated points, curves, surfaces).  
### Property **OptionalRelation**( ) As [CATIARelation](../KnowledgeInterfaces/interface_Relation_14366.md) (Read Only)

   Returns the relation that can be used to compute the parameter. As this relation might not exist, NULL may be returned, so a test is required.

**Example:**      This example checks if there is a relation to compute the `param1` parameter, and if no relation exists, displays a message box:

```VBScript
     Set param1_rel = param1.OptionalRelation
     If param1_rel is Nothing Then
          MsgBox "No relation to compute param1"
     End If

```

### Property **ReadOnly**( ) As boolean (Read Only)

   Returns whether the parameter can be modified.

**Example:**      This example checks if the `param1` parameter can be modified, and if it cannot, displays a message box:

```VBScript
     If ( param1.ReadOnly ) Then
          MsgBox "No way to change param1"
     End If

```

### Property **Renamed**( ) As boolean (Read Only)

   Returns a boolean saying if the parameter is a renamed parameter or not.  
### Property **UserAccessMode**( ) As long (Read Only)

   Returns the user access mode of the parameter.  0    Read only parameter (cannot be destroyed). 1    Read/write parameter (cannot be destroyed). 2    User parameter (can be read, written and destroyed).  Methods

### Sub **Rename**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

   Renames the parameter.

**Parameters:**

` iName`      The new name of the parameter  **Example:**      This example renames the `param1` parameter to `PartSeatbodyMinimumThickness`:

```VBScript
     Call param1.Rename("PartSeatbodyMinimumThickness")

```

### Sub **ValuateFromString**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

   Valuates a parameter using a string as input. The string depends on parameter nature : "True" or "False" for Boolean a numerical value for Integer or Real a numerical value with or without a unit for Dimension

**Parameters:**

` iValue`      The value to assign to the dimension parameter  **Example:**      This example sets the value of the existing `dimension` parameter to a new value:

```VBScript
     dimension.ValuateFromString("300mm");

```

### Func **ValueAsString**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the value of the parameter as a string. **Example:**      This example gets the value of the existing `dimension` parameter and shows it in a message box

```VBScript
     Dim str
     str = dimension.ValueAsString;
     MessageBox str

```

---

# Parameters (Collection)

**_Represents the Parameters collection of the part or the product._**
The following example shows how to retrieve it:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim parameterList As Parameters
      Set parameterList = part1.Part.Parameters

```

## Properties

### Property **RootParameterSet**( ) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md) (Read Only)

   Returns the root parameter set of a document. If it doesn't exist, it is created.  
### Property **Units**( ) As [CATIAUnits](../KnowledgeInterfaces/interface_Units_5973.md) (Read Only)

   Returns the collection of units.  Methods

### Func **CreateBoolean**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  boolean  `iValue`) As [CATIABoolParam](../KnowledgeInterfaces/interface_BoolParam_17217.md)

   Creates a boolean parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `checked` boolean parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim chk As BooleanParam
      Set chk = part1.Part.Parameters.CreateBoolean ("checked", False)

```

### Func **CreateDimension**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitude`,  double  `iValue`) As [CATIADimension](../KnowledgeInterfaces/interface_Dimension_18130.md)

   Creates a user dimension and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The dimension name
` iMagnitude`      The dimension magnitude. Units are those of the IS system. Valid magnitudes are:

  * "LENGTH": the unit is the meter.
  * "ANGLE": the unit is the radian.
The
[Dimension](../KnowledgeInterfaces/interface_Dimension_18130.md) object provides the [Dimension.ValuateFromString](../KnowledgeInterfaces/interface_Dimension_18130.htm#ValuateFromString) method with which you may express the value in any unit for a given dimension (see the example below). ` iValue`      The dimension value provided as a real number  **Example:**      This example creates a `LENGTH` dimension and adds it to the newly created part. The initial value is expressed in meters. The new value is expressed in millimeters.

```VBScript
     Dim depth As Dimension
     Set depth = parameters.CreateDimension("depth", "LENGTH", 20)
     depth.ValuateFromString("300mm");

```

### Func **CreateInteger**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  long  `iValue`) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md)

   Creates an integer parameter** and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `RevisionNumber` integer parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim revision As IntParam
      Set revision = part1.Part.Parameters.CreateInteger ("RevisionRumber", 17)

```

### Func **CreateList**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAListParameter](../KnowledgeInterfaces/interface_ListParameter_36657.md)

   Creates a list parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name  **Example:**      This example creates the `ListName` list parameter and adds it to the newly created part:

```VBScript
      Set CATDocs = CATIA.Documents
      Set part1   = CATDocs.Add("CATPart")
      Set list1 = part1.Part.Parameters.CreateList ("ListName")

```

### Func **CreateReal**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  double  `iValue`) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Creates a real parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `ReliabilityRate` real parameter and adds it to the newly created part:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim rate As RealParam
      Set rate = part1.Part.Parameters.CreateReal ("ReliabilityRate", 2.5 )

```

### Sub **CreateSetOfParameters**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFather`)

   Creates a set of parameters and appends it to argument iFather.  
### Func **CreateString**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`) As [CATIAStrParam](../KnowledgeInterfaces/interface_StrParam_13874.md)

   Creates a string parameter and adds it to the part's collection of parameters.

**Parameters:**

` iName`      The parameter name
` iValue`      The parameter value  **Example:**      This example creates the `responsible` string parameter and adds it to the newly created part:

```VBScript
      Set CATDocs = CATIA.Documents
      Set part1   = CATDocs.Add("CATPart")
      Set density = part1.Part.Parameters.CreateString ("responsible", "The Boss")

```

### Func **GetNameToUseInRelation**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns a correct name of a feature to use it in a relation.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Retrieves a parameter using its index or its name from the from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the parameter to retrieve from the collection of parameters. As a numerics, this index is the rank of the parameter in the collection. The index of the first parameter in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example retrieves the last parameter in the `parameters` collection:

```VBScript
     Set lastParameter = parameters.Item(parameters.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a parameter from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the parameter to remove from the collection of parameters. As a numerics, this index is the rank of the parameter in the collection. The index of the first parameter in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example removes the "depth" parameter from the `parameters` collection.

```VBScript
     parameters.Remove("depth")

```

### Func **SubList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`,  boolean  `iRecursively`) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md)

   Returns a sub-collection of parameters aggregated to an object.

**Parameters:**

` iObject`      The object used to filter the whole parameter collection to get the resulting sub-collection.
` iRecursively`      A flag to specify if children parameters are to be searched for in the returned collection  **Example:**      This example shows how to retrieve a collection of parameters that are associated to a Pad.

```VBScript
     Dim Parameters1 As Parameters
     Set Parameters1 = CATIA.ActiveDocument.Part.Parameters gets the collection of parameters in the part
     Dim Body0 As AnyObject
     Set Body0 = CATIA.ActiveDocument.Part.Bodies.Item  ( "MechanicalTool.1" )
     Dim Pad1 As AnyObject
     Set Pad1 = Body0.Shapes.Item  ( "Pad.1" ) gets the pad Pad.1
     Dim Parameters2 As Parameters
     Set Parameters2 = Parameters1.SubList(Pad1,TRUE) gets the collection of parameters that are under the pad Pad.1

```

---

# ParameterSet (Object)

**_Represents parameter set._**
It is the node that contains user parameters.

## Properties

### Property **AllParameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns all parameters under this set of parameter.  
### Property **DirectParameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns directly aggregated parameters.  
### Property **ParameterSets**( ) As [CATIAParameterSets](../KnowledgeInterfaces/interface_ParameterSets_36730.md) (Read Only)

   Returns the children parameter sets.

---

# ParameterSets (Collection)

**_Represents a collection of parameter sets._**
The ParameterSet object is a neutral object that contains parameters, like the Parameters node in the specification tree.

The following example shows how to retrieve it on a part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim parameters1 As Parameters
     Set parameters1 = part1.Part.Parameters
     Dim ParameterSet1 As ParameterSet
     Set ParameterSet1 = parameters1.RootParameterSet
     Dim parameterSets1 As ParameterSets
     Set parameterSets1 = parameterSet1.ParameterSets

```

This collection is not a collection of all parameter sets of a document, but a collection of all parameter sets in the current parameter set.

## Methods

### Func **CreateSet**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md)

   Creates a set of parameters and appends it to the parameter set which corresponds to this collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md)

   Returns a parameter set using its index or its name from the ParameterSets collection.

**Parameters:**

` iIndex`      The index or the name of the parameter set to retrieve from the collection of parameter sets. As a numerics, this index is the rank of the parameter set in the collection. The index of the first parameter set in the collection is 1, and the index of the last parameter set is Count. As a string, it is the name you assigned to the parameter set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property .  **Example:**      This example retrieves the parameter set named "Parameters.1" in the `parameterSets` collection:

```VBScript
     Set theSet = parameterSets.Item("Parameters.1")

```

---

# RealParam (Object)

**_Represents the real parameter._**
The following example shows how to create it:

```VBScript
      Dim CATDocs As Documents
      Set CATDocs = CATIA.Documents
      Dim part1 As Document
      Set part1   = CATDocs.Add("CATPart")
      Dim density As RealParam
      Set density = part1.Part.Parameters.CreateReal("density", 2.5)

```

The real parameter is the base object for dimensions.

**See also:**      [Dimension](../KnowledgeInterfaces/interface_Dimension_18130.md)

## Properties

### Property **MaximumTolerance**( ) As double

   Returns or sets the value of the maximum tolerance of a parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `MaximumTolerance` value to 0 if its value is bigger than 0:

```VBScript
     If (Length.MaximumTolerance < 0.0)  Then
         Length.MaximumTolerance = 0.0
     End If

```

### Property **MinimumTolerance**( ) As double

   Returns or sets the value of the minimum tolerance of a parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `MinumumTolerance` value to 0 if its value is bigger than 0:

```VBScript
     If (Length.MinimumTolerance > 0.0)  Then
         Length.MinimumTolerance = 0.0
     End If

```

### Property **RangeMax**( ) As double

   Returns or sets the value of the upper bound that the parameter object value can take.

**Example:**      This example sets the `RangeMax` value to 0 if its value is smaller than 0:

```VBScript
     If (Length.RangeMax < 0.0 and Length.RangeMaxValidity <> 0)  Then
         Length.RangeMax = 0.0
     End If

```

### Property **RangeMaxValidity**( ) As long

   Returns or sets the type of the upper bound of the parameter.

0    the upper bound is meaningless 1    the upper bound can be reached 2    the upper bound cannot be reached  
### Property **RangeMin**( ) As double

   Returns or sets the value of the lower bound that the parameter object value can take.

**Example:**      This example sets the `RangeMin` value to 0 if its value is bigger than 0:

```VBScript
     If (Length.RangeMin > 0.0 and Length.RangeMinValidity <> 0)  Then
         Length.RangeMin = 0.0
     End If

```

### Property **RangeMinValidity**( ) As long

   Returns or sets the type of the lower bound of the parameter.

0    the lower bound is meaningless 1    the lower bound can be reached 2    the lower bound cannot be reached  
### Property **Value**( ) As double

   Returns or sets the value of the real parameter. Units are expressed in the IS unit system, except for lengthes expressed in millimeters, and angles expressed in decimal degrees.

**Example:**      This example sets the `density` value to 1 if its value is greater than 2.5:

```VBScript
     If (density.Value > 2.5)  Then
         density.Value = 1
     End If

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

   Returns an array containing the different values that the real param can take in the case of multiple values.

**Example:**

```VBScript
     Dim enumValues () as Variant
     ReDim enumValues (aRealParameter.GetEnumerateValuesSize() - 1)
     aRealParameter.GetEnumerateValues(enumValues)
     For i = LBound(enumValues) to UBound(enumValues)
       ...
     Next

```

### Func **GetEnumerateValuesSize**( ) As long

   Returns the number of enumerate values.  
### Func **IsEqualTo**( double  `iValueToCompare`) As boolean

   Tests the equality of the parameter value with a given value.

**Parameters:**

` iValueToCompare`      The value to compare the parameter value with

**Returns:**

True
    If the current value of the parameter (the one get by the get_Value property, for dimensions notice that it is not the MKS value) is equal to the one given in argument. Notice that two values are considered as equal if their difference is insignificant faced with the two compared values. This method allows you to avoid problems due to computation errors.
False
    If the two values are different.

### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

   Sets an array containing the different values that the real param can take in the case of multiple values.  
### Sub **SuppressEnumerateValues**( )

   Resets the status of the object to a single value object.

---

# Relation (Object)

**_Represents the relation object._**
It is an abstract object which is not intended to be created as such, but from which the check, design table, formula, rule, objects derive.

**See also:**      [Check](../KnowledgeInterfaces/interface_Check_5408.md), [DesignTable](../KnowledgeInterfaces/interface_DesignTable_25284.md), [Formula](../KnowledgeInterfaces/interface_Formula_11046.md), [Rule](../KnowledgeInterfaces/interface_Rule_3720.md)

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the comment associated with the relation. The comment explains the relation's purpose. It is passed as the second input argument of the relation creation methods of the [Relations](../KnowledgeInterfaces/interface_Relations_18301.md) collection.

**Example:**      This example retrieves the `maximummass` relation comment and displays it in a message box:

```VBScript
     relcomment = maximummass.Comment
     MsgBox "maximummass comment : " & relcomment

```

### Property **Context**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the context of the parameter.
The context of a parameter can be a part, a product, a drafting, or a process document, depending where the parameter is.

**Returns:**      The context  **See also:**      [Part](../MecModInterfaces/interface_Part_3788.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md), CATIADrawing, CATIAProcess  
### Property **NbInParameters**( ) As long (Read Only)

   Returns the number of input parameters of the relation.  
### Property **NbOutParameters**( ) As long (Read Only)

   Returns the number of output parameters of the relation.
The output parameters of the relation are those constrained by the relation.  
### Property **Value**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the definition of the relation. It returns an empty string if the relation is not an expressional one (for example for a design table). The definition is the body to be executed to compute one or several parameters. It is passed as the last input argument of the relation creation methods of the [Relations](../KnowledgeInterfaces/interface_Relations_18301.md) collection.

**Example:**      This example retrieves the `maximummass` relation definition and displays it in a message box:

```VBScript
     reldef = maximummass.Value
     MsgBox "maximummass relation is defined as " & reldef

```

Methods

### Func **GetInParameter**( long  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns an input parameter of the relation.
This method can return an object that is not a parameter, that is, you cannot handle it as a Parameter object. For example, in a relation like

```VBScript
    Area.1 = area(PartBody\Pad.1\Sketch.1)
```

the object PartBody\Pad.1\Sketch.1 is a sketch and not a parameter.
To use such an object, call the Visual Basic `TypeName` function to retrieve its real type.

```VBScript
    Dim objectType
     objectType = TypeName(oParameter)
     If objectType = "Parameter" Then
     ...
```

**Parameters:**

` iIndex`      The searched input parameter index in the relation.

**Legal values** : 1 ≤ iIndex ≤
NbInParameters 
### Func **GetOutParameter**( long  `iIndex`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

   Returns an output parameter of the relation. Use TypeName method on the returned parameter to get the real type of the parameter.

**Parameters:**

` iIndex`      The searched input parameter index in the relation.

**Legal values** : 1 ≤ iIndex ≤
NbOutParameters 
### Sub **Modify**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

   Modifies the relation.

**Parameters:**

` iValue`      The new relation value

### Sub **Rename**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

   Renames the relation.

**Parameters:**

` iName`      The new relation name

---

# Relations (Collection)

**_Represents the collection of relations of the part or the product._**

A relation computes values. A relation can belong to one of the following types:

Formula     It combines parameters to compute the value of one output parameter only. For example, the mass of a cuboid can be the output parameter of a formula, while the value is computed using the following parameters:

```VBScript

     FormulaBody = (height*width*depth)*density

```

Program     It combines conditions and actions on parameters to compute one or several output parameter values. For example, the following is a program:

```VBScript
     ProgramBody = if (mass>2kg) { depth=2mm length=10mm } else { depth=1mm length=5mm }

```

Check     It only contains conditions on parameter values. For example, the following is a check:

```VBScript
     CheckBody = mass<10kg

```

The parameters should be defined previously.

The following example shows how to retrieve the collection of relations from a newly created part document:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part As Document
     Set part  = CATDocs.Add("CATPart")
     Dim relations As Relations
     Set relations = part.Relations

```

**See also:**      [Formula](../KnowledgeInterfaces/interface_Formula_11046.md), [Rule](../KnowledgeInterfaces/interface_Rule_3720.md), [Check](../KnowledgeInterfaces/interface_Check_5408.md), [DesignTable](../KnowledgeInterfaces/interface_DesignTable_25284.md)

## Properties

### Property **Optimizations**( ) As [CATIAOptimizations](../KnowledgeInterfaces/interface_Optimizations_38238.md) (Read Only)

   Returns the optimization collection.
It can be empty if no optimization is defined in the document.
This property is available only when the Product Engineering Optimizer license is available.  Methods

### Func **CreateCheck**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCheckBody`) As [CATIACheck](../KnowledgeInterfaces/interface_Check_5408.md)

   Creates a check relation and adds it to the part's collection of relations.

**Parameters:**

` iName`      The check name
` iComment`      A description of the check
` iCheckBody`      The check definition

**Returns:**      The created check  **Example:**      This example creates the `maximummass` check relation and adds it to the newly created part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim partdoc As Document
     Set partdoc  = CATDocs.Add("CATPart")
     Dim part As Part
     Set part    = partdoc.Part
     Dim massCheck As Check
     Set massCheck    = part.Relations.CreateCheck
                        ("maximummass",
                         "Ensures that the mass is less than 10 kg",
                         "mass<10kg")

```

### Func **CreateDesignTable**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  boolean  `iCopyMode`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetPath`) As [CATIADesignTable](../KnowledgeInterfaces/interface_DesignTable_25284.md)

   Creates a design table based on a file organized in an vertical way and adds it to the part's collection of relations.

**Parameters:**

` iName`      The design table name
` iComment`      A description of the design table
` iCopyMode`

**Returns:**      The created design table  **Example:**      This example creates the `dt` design table and adds it to the newly created part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim partdoc As Document
     Set partdoc  = CATDocs.Add("CATPart")
     Dim part As Part
     Set part    = partdoc.Part
     Dim designtable As DesignTable
     Set designtable    = part.Relations.CreateDesignTable
                         ("dt",
                          "Ensures that the mass is less than 10 kg",
                          TRUE,
                          "/u/users/client/data/sheet.txt")

```

### Func **CreateFormula**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iOutputParameter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFormulaBody`) As [CATIAFormula](../KnowledgeInterfaces/interface_Formula_11046.md)

   Creates a formula relation and adds it to the part's collection of relations.

**Parameters:**

` iName`      The formula name
` iComment`      A description of the formula
` iOutputParameter`      The parameter which stores the result of the formula
` iFormulaBody`      The formula definition

**Returns:**      The created formula  **Example:**      This example creates the `computemass` formula relation and adds it to the newly created part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim partdoc As Document
     Set partdoc  = CATDocs.Add("CATPart")
     Dim part As Part
     Set part    = partdoc.Part
     Dim massFormula As Formula
     Set massFormula = part.Relations.CreateFormula
                       ("computemass",
                       "Computes the cuboid mass",
                        mass,
                       "(height*width*depth)*density")

```

### Func **CreateHorizontalDesignTable**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  boolean  `iCopyMode`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSheetPath`) As [CATIADesignTable](../KnowledgeInterfaces/interface_DesignTable_25284.md)

   Creates a design table based on a file organized in an horizontal way and adds it to the part's collection of relations.

**Parameters:**

` iName`      The design table name
` iComment`      A description of the design table
` iCopyMode`

**Returns:**      The created design table  **Example:**      This example creates the `dt` design table and adds it to the newly created part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim partdoc As Document
     Set partdoc  = CATDocs.Add("CATPart")
     Dim part As Part
     Set part    = partdoc.Part
     Dim designtable As DesignTable
     Set designtable    = part.Relations.CreateHorizontalDesignTable
                        ("dt",
                         "Ensures that the mass is less than 10 kg",
                         TRUE,
                         "/u/users/client/data/horizontalsheet.txt")

```

### Func **CreateLaw**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLawBody`) As [CATIALaw](../KnowledgeInterfaces/interface_Law_2130.md)

   Creates a law relation and adds it to the part's collection of relations.

**Parameters:**

` iName`      The law name
` iComment`      A description of the law
` iLawBody`      The law definition

**Returns:**      The created law  
### Func **CreateProgram**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProgramBody`) As [CATIAProgram](../KnowledgeInterfaces/interface_Rule_3720.md)

   Creates a program relation and adds it to the part's collection of relations.

**Parameters:**

` iName`      The program name
` iComment`      A description of the program
` iProgramBody`      The program definition

**Returns:**      The created program  **Example:**      This example creates the `selectdepth` program relation and adds it to the newly created part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim partdoc As Document
     Set partdoc  = CATDocs.Add("CATPart")
     Dim part As Part
     Set part    = partdoc.Part
     Dim depthProgram As Program
     Set depthProgram = part.Relations.CreateProgram
                        ("selectdepth",
                        "Select depth with respect to mass",
                        "if (mass>2kg) { depth=2mm } else { depth=1 mm }")

```

### Func **CreateRuleBase**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIARelation](../KnowledgeInterfaces/interface_Relation_14366.md)

   Creates a rulebase.

**Parameters:**

` iName`      The name of the rulebase.

**Returns:**      The created rulebase.  **See also:**      [ExpertRuleBase](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.md) 
### Func **CreateSetOfEquations**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComment`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFormulaBody`) As [CATIASetOfEquation](../KnowledgeInterfaces/interface_SetOfEquation_36247.md)

   Creates a set of equations.

**Parameters:**

` iName`      The name of the set of equation.
` iComment`      The comment of the set of equation.
` iFormulaBody`      The body of the set of equation " a==b+4; c ≤ 90".

**Returns:**      The created set of equations  
### Sub **CreateSetOfRelations**( [CATIABase](../System/interface_AnyObject_17321.md)  `iParent`)

   Creates a set of relations and appends it to a parent object.

**Parameters:**

` iParent`      The object to which the set is appended

### Sub **GenerateXMLReportForChecks**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`)

   Generates an XML Report on all checks in the current document.

**Parameters:**

` iName`      The name of the XML file

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARelation](../KnowledgeInterfaces/interface_Relation_14366.md)

   Retrieves a relation using its index or its name from the Relations collection.

**Parameters:**

` iIndex`      The index or the name of the relation to retrieve from the collection of relations. As a numerics, this index is the rank of the relation in the collection. The index of the first relation in the collection is 1, and the index of the last relation is Count. As a string, it is the name you assigned to the relation using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the relation.  **Returns:**      The retrieved relation  **Example:**      This example retrieves the last relation in the `relations` collection.

```VBScript
     Dim lastRelation As Relation
     Set lastRelation = relations.Item(relations.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a relation from the Relations collection.

**Parameters:**

` iIndex`      The index or the name of the relation to remove from the collection of relations. As a numerics, this index is the rank of the relation in the collection. The index of the first relation in the collection is 1, and the index of the last relation is Count. As a string, it is the name you assigned to the relation using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the relation.  **Example:**      This example removes the relation named `density` from the `relations` collection.

```VBScript
     relations.Remove("density")

```

### Func **SubList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeature`,  boolean  `iRecursively`) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md)

   Returns a sub-collection of relations aggregated to an object.

**Parameters:**

` iFeature`      The object used to filter the the whole relation collection to get the resulting sub-collection.
` iRecursively`      A flag to specify if children parameters are to be searched for in the returned collection

**Returns:**      The resulting sub-collection  **Example:**      This example shows how to get a collection of relations that are under a Pad

```VBScript
     Dim Relations1 As Relations
     Set Relations1 = CATIA.ActiveDocument.Part.Relations' gets the collection of relations in the part
     Dim Body0 As AnyObject
     Set Body0 = CATIA.ActiveDocument.Part.Bodies.Item  ( "MechanicalTool.1" )
     Dim Pad1 As AnyObject
     Set Pad1 = Body0.Shapes.Item  ( "Pad.1" ) ' gets the pad Pad.1
     Dim Relations2 As Relations
     Set Relations2 = Relations1.SubList(Pad1, TRUE) ' gets the collection of relations that are under the pad Pad.1

```

---

# ReportGenerationSheetSettingAtt (Object)

**_The interface to access a CATIAReportGenerationSheetSettingAtt._**

## Properties

### Property **AllChecksReport**( ) As short

   Returns or sets the AllChecksReport parameter.

**Role** :Return or Set the AllChecksReport parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAllChecksReport`      **Legal values** :
`0 :` report of only failed checks
`1 :` report of all checks.

### Property **CheckReportHtml**( ) As short

   Returns or sets the CheckReportHtml parameter.

**Role** :Return or Set the CheckReportHtml parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oCheckReportHtml`      **Legal values** :
`0 :` to have check report in Xml
`1 :` to have check report in Html.

### Property **DirectoryForInputXsl**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the DirectoryForInputXsl parameter.

**Role** :Return or Set the DirectoryForInputXsl parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDirectoryForInputXsl`      Directory for the report file with Xml extension.

### Property **ReportCheckAdvisor**( ) As short

   Returns or sets the ReportCheckAdvisor parameter.

**Role** :Return or Set the ReportCheckAdvisor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportCheckAdvisor`      **Legal values** :
`0 :` not report of check Advisor
`1 :` report of check Advisor.

### Property **ReportCheckExpert**( ) As short

   Returns or sets the ReportCheckExpert parameter.

**Role** :Return or Set the ReportCheckExpert parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportCheckExpert`      **Legal values** :
`0 :` not report of check Advisor
`1 :` report of check Advisor.

### Property **ReportHtmlInCatiaSession**( ) As short

   Returns or sets the ReportHtmlInCatiaSession parameter.

**Role** :Return or Set the ReportHtmlInCatiaSession parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportHtmlInCatiaSession`      **Legal values** :
`0 :` report Html outside CATIA session
`1 :` report Html in CATIA session.

### Property **ReportObjectsInformation**( ) As short

   Returns or sets the ReportObjectsInformation parameter.

**Role** :Return or Set the ReportObjectsInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportObjectsInformation`      **Legal values** :
`0 :` not report objects information
`1 :` report objects information.

### Property **ReportOutputDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ReportOutputDirectory parameter.

**Role** :Return or Set the ReportOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportOutputDirectory`      The output directory for report of checks expert and checks advisor.

### Property **ReportParametersInformation**( ) As short

   Returns or sets the ReportParametersInformation parameter.

**Role** :Return or Set the ReportParametersInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportParametersInformation`      **Legal values** :
`0 :` not check Advisor parameter information
`1 :` check Advisor parameter information.

### Property **ReportPassedObjects**( ) As short

   Returns or sets the ReportPassedObjects parameter.

**Role** :Return or Set the ReportPassedObjects parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportPassedObjects`      **Legal values** :
`0 :` not report passed objects
`1 :` report passed objects.
Methods

### Func **GetAllChecksReportInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AllChecksReport parameter.

**Role** :Retrieves the state of the AllChecksReport parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCheckReportHtmlInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CheckReportHtml parameter.

**Role** :Retrieves the state of the CheckReportHtml parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDirectoryForInputXslInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DirectoryForInputXsl parameter.

**Role** :Retrieves the state of the DirectoryForInputXsl parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportCheckAdvisorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportCheckAdvisor parameter.

**Role** :Retrieves the state of the ReportCheckAdvisor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportCheckExpertInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportCheckExpert parameter.

**Role** :Retrieves the state of the ReportCheckExpert parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportHtmlInCatiaSessionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportHtmlInCatiaSession parameter.

**Role** :Retrieves the state of the ReportHtmlInCatiaSession parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportObjectsInformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportObjectsInformation parameter.

**Role** :Retrieves the state of the ReportObjectsInformation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportOutputDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportOutputDirectory parameter.

**Role** :Retrieves the state of the ReportOutputDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportParametersInformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportParametersInformation parameter.

**Role** :Retrieves the state of the ReportParametersInformation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportPassedObjectsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportPassedObjects parameter.

**Role** :Retrieves the state of the ReportPassedObjects parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAllChecksReportLock**( boolean  `iLocked`)

   Locks or unlocks the AllChecksReport parameter.

**Role** :Locks or unlocks the AllChecksReport parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCheckReportHtmlLock**( boolean  `iLocked`)

   Locks or unlocks the CheckReportHtml parameter.

**Role** :Locks or unlocks the CheckReportHtml parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDirectoryForInputXslLock**( boolean  `iLocked`)

   Locks or unlocks the DirectoryForInputXsl parameter.

**Role** :Locks or unlocks the DirectoryForInputXsl parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportCheckAdvisorLock**( boolean  `iLocked`)

   Locks or unlocks the ReportCheckAdvisor parameter.

**Role** :Locks or unlocks the ReportCheckAdvisor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportCheckExpertLock**( boolean  `iLocked`)

   Locks or unlocks the ReportCheckExpert parameter.

**Role** :Locks or unlocks the ReportCheckExpert parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportHtmlInCatiaSessionLock**( boolean  `iLocked`)

   Locks or unlocks the ReportHtmlInCatiaSession parameter.

**Role** :Locks or unlocks the ReportHtmlInCatiaSession parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportObjectsInformationLock**( boolean  `iLocked`)

   Locks or unlocks the ReportObjectsInformation parameter.

**Role** :Locks or unlocks the ReportObjectsInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportOutputDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the ReportOutputDirectory parameter.

**Role** :Locks or unlocks the ReportOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportParametersInformationLock**( boolean  `iLocked`)

   Locks or unlocks the ReportParametersInformation parameter.

**Role** :Locks or unlocks the ReportParametersInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportPassedObjectsLock**( boolean  `iLocked`)

   Locks or unlocks the ReportPassedObjects parameter.

**Role** :Locks or unlocks the ReportPassedObjects parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# Rule (Object)

**_Represents the program relation._**
The following example shows how to create a program that selects a depth with respect to a mass value. The depth and mass parameters should exist before the creation of the program (also called Rule) object.

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim mass As RealParam
     Set mass         = part1.Part.Parameters.CreateReal("mass", 5.)
     Dim depth As RealParam
     Set depth        = part1.Part.Parameters.CreateReal("depth", 0.)
     Dim selectdepth As Relation
     Set selectdepth = part1.Part.Relations.CreateProgram
                        ("select_depth",
                         "Select depth with respect to mass",
                         "if (mass>2kg) { depth=2mm } else { depth=1mm }")

```

---

# SetOfEquation (Object)

**_Represents the set of equations object._**

## Methods

### Func **GetMaxCalculationTime**( ) As long

   Returns the maximum time of the model calculations.  
### Func **GetPrecision**( ) As double

   Returns the calculation precision.  
### Func **GetSymbolcTransformations**( ) As boolean

   Returns whether the Gauss method is used during the symbolic transformation.

**TRUE** if the Gauss method is used during the symbolic transformation.  
### Func **IsStopDialog**( ) As boolean

   Returns whether the "Stop Dialog" will be shown during calculations.

**TRUE** if the 'Stop Dialog' will be shown during calculations.  
### Sub **SetMaxCalculationTime**( long  `iMaxTime`)

   Sets a maximum time to the model calculations.  
### Sub **SetParameterAsInput**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`)

   Specifies that the parameter must be considered as input parameter.

**Parameters:**

` iParameter`      The parameter to set up as input of the SetOfEquationObject

### Sub **SetParameterAsOutput**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`)

   Specifies that the parameter must be considered as an output parameter.

**Parameters:**

` iParameter`      The parameter to set up as output of the SetOfEquationObject

### Sub **SetPrecision**( double  `iEps`)

   Sets the calculation precision.

**Parameters:**

` iEps`      a precision

**Legal values** : 1e-10 ≤ iEps ≤ 0.1

### Sub **UseStopDialog**( boolean  `iUsed`)

   Specifies whether the 'Stop Dialog' should be shown during calculations.

**TRUE** to show the 'Stop Dialog' during calculations.  
### Sub **UseSymbolcTransformations**( boolean  `iGauss`)

   Specifies whether the Gauss method should be used during the symbolic transformation.

**TRUE** to use the Gauss method during the symbolic transformation.

---

# StrParam (Object)

**_Represents the string parameter._**
The following example shows how to create it:

```VBScript
    	Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim material As String
     Set material = part1.Parameters.CreateString("material", "glass")

```

## Properties

### Property **Value**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the string parameter value.

**Example:**     This example returns in `myValue` the value of the string parameter `material`:

```VBScript

```VBScript
     myValue = material.Value

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

   Returns an array containing the different values that the real param can take in the case of multiple values.

**Example:**

```VBScript
     Dim enumValues () as Variant
     ReDim enumValues (aStrParameter.GetEnumerateValuesSize() - 1)
     aStrParameter.GetEnumerateValues(enumValues)
     For i = LBound(enumValues) to UBound(enumValues)
       ...
     Next

```

### Func **GetEnumerateValuesSize**( ) As long

   Returns the number of enumerate values.  
### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

   Sets an array containing the different values that the StrParam object can take in the case of multiple values.

**Parameters:**

` The`      array of enumerated values.

### Sub **SuppressEnumerateValues**( )

   Resets the status of the object to a single value object.

---

# ToleranceSheetSettingAtt (Object)

**_The interface to access a CATIAToleranceSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Tolerance sheet.

## Properties

### Property **AngleMaxTolerance**( ) As double

   Returns or sets the AngleMaxTolerance parameter.

**Role** :Return or Set the AngleMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAngleMaxTolerance`      The angle maximum tolerance value.

### Property **AngleMinTolerance**( ) As double

   Returns or sets the AngleMinTolerance parameter.

**Role** :Return or Set the AngleMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAngleMinTolerance`      The angle minimum tolerance value.

### Property **DefaultTolerance**( ) As short

   Returns or sets the DefaultTolerance parameter.

**Role** :Return or Set the DefaultTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDefaultTolerance`      **Legal values** :
`0 :` to not accept a default tolerance
`1 :` to accept a default tolerance.

### Property **LengthMaxTolerance**( ) As double

   Returns or sets the LengthMaxTolerance parameter.

**Role** :Return or Set the LengthMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLengthMaxTolerance`      The length maximum tolerance value.

### Property **LengthMinTolerance**( ) As double

   Returns or sets the LengthMinTolerance parameter.

**Role** :Return or Set the LengthMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oLengthMinTolerance`      The length minimum tolerance value.
Methods

### Func **GetAngleMaxToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AngleMaxTolerance parameter.

**Role** :Retrieves the state of the AngleMaxTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAngleMinToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AngleMinTolerance parameter.

**Role** :Retrieves the state of the AngleMinTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDefaultToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DefaultTolerance parameter.

**Role** :Retrieves the state of the DefaultTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLengthMaxToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LengthMaxTolerance parameter.

**Role** :Retrieves the state of the LengthMaxTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLengthMinToleranceInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LengthMinTolerance parameter.

**Role** :Retrieves the state of the LengthMinTolerance parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAngleMaxToleranceLock**( boolean  `iLocked`)

   Locks or unlocks the AngleMaxTolerance parameter.

**Role** :Locks or unlocks the AngleMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAngleMinToleranceLock**( boolean  `iLocked`)

   Locks or unlocks the AngleMinTolerance parameter.

**Role** :Locks or unlocks the AngleMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDefaultToleranceLock**( boolean  `iLocked`)

   Locks or unlocks the DefaultTolerance parameter.

**Role** :Locks or unlocks the DefaultTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLengthMaxToleranceLock**( boolean  `iLocked`)

   Locks or unlocks the LengthMaxTolerance parameter.

**Role** :Locks or unlocks the LengthMaxTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLengthMinToleranceLock**( boolean  `iLocked`)

   Locks or unlocks the LengthMinTolerance parameter.

**Role** :Locks or unlocks the LengthMinTolerance parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# Unit (Object)

**_Represents CATIAUnit object._**
This interface allows convertion.

## Properties

### Property **Magnitude**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the magnitude associated to the unit.  
### Property **Symbol**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the symbol associated to the unit.  Methods

### Func **ConvertFromMKS**( double  `iValueInMKS`) As double

   Convert the initial value (expressed in MKS unit) in its equivalent in the current unit.

**Parameters:**

` iValueInThisUnit`      The initial value in MKS unit.
` oValueInMKS`      The final value in the current unit.

### Func **ConvertFromStorageUnit**( double  `iValueInStorageUnit`) As double

   Convert the initial value (expressed in storage unit) in its equivalent in the current unit.

**Parameters:**

` iValueInStorageUnit`      The initial value in storage unit.
` oValueInThisUnit`      The final value in the current unit.

### Func **ConvertToMKS**( double  `iValueInThisUnit`) As double

   Convert the initial value in its equivalent in MKS unit.

**Parameters:**

` iValueInThisUnit`      The initial value in the current unit.
` oValueInMKS`      The final value in the corresponding MKS unit.

### Func **ConvertToStorageUnit**( double  `iValueInThisUnit`) As double

   Convert the initial value in its equivalent in storage unit.

**Parameters:**

` iValueInThisUnit`      The initial value in the current unit.
` oValueInStorageUnit`      The final value in the corresponding storage unit.

---

# Units (Collection)

**_Represents the collection of Units._**
This collection can be retrieved via any collection of parameters (method Units).

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAUnit](../KnowledgeInterfaces/interface_Unit_3832.md)

   Returns a unit using its index or its name from the from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the unit to retrieve from the collection of parameters. As a numerics, this index is the rank of the unit in the collection. The index of the first unit in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example retrieves the millimeter unit in the `units` collection:

```VBScript
     Set unitmm = units.Item("mm")

```

---

# UnitsSheetSettingAtt (Object)

**_The interface to access a CATIAUnitsSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Units sheet.

## Properties

### Property **DisplayTrailingZeros**( ) As short

   Returns or sets the DisplayTrailingZeros parameter.

**Role** :Return or Set the DisplayTrailingZeros parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDisplayTrailingZeros`      **Legal values** :
`0 :` to not display trailing zeros
`1 :` to display trailing zeros.

### Property **ExpNotationValuesGreater**( ) As double

   Returns or sets the ExpNotationValuesGreater parameter.

**Role** :Return or Set the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oExpNotationValuesGreater`      The minimum value for exponential notation values.

### Property **ExpNotationValuesLower**( ) As double

   Returns or sets the ExpNotationValuesLower parameter.

**Role** :Return or Set the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oExpNotationValuesLower`      The maximum value for exponential notation values.

### Property **ListOfMagnitudes**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) (Read Only)

   Returns or sets the ListOfMagnitudes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ListOfMagnitudesSize**( ) As double (Read Only)

   Returns or sets the ListOfMagnitudesSize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SameDisplay**( ) As short

   Returns or sets the SameDisplay parameter.

**Role** :Return or Set the SameDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oSameDisplay`      **Legal values** :
`0 :` to not display same display
`1 :` to display same display.
Methods

### Sub **CommitForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.CommitForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#CommitForUnits) 
### Sub **GetDecimalReadOnly**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  double  `oDecimalPlaceReadOnly`)

   Returns the number of decimals for ReadOnly number.  
### Sub **GetDecimalReadWrite**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  double  `oDecimalPlaceReadWrite`)

   Returns the number of decimals for ReadWrite number.  
### Func **GetDimensionsDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the DimensionsDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayTrailingZerosInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DisplayTrailingZeros parameter.

**Role** :Retrieves the state of the DisplayTrailingZeros parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpNotationValuesGreaterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ExpNotationValuesGreater parameter.

**Role** :Retrieves the state of the ExpNotationValuesGreater parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpNotationValuesLowerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ExpNotationValuesLower parameter.

**Role** :Retrieves the state of the ExpNotationValuesLower parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetListOfMagnitudesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ListOfMagnitudes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetMagnitudeValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oUnitName`,  double  `oDecimalPlaceReadWrite`,  double  `oDecimalPlaceReadOnly`)

   Returns the Magnitude parameters.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetSameDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SameDisplay parameter.

**Role** :Retrieves the state of the SameDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **ResetToAdminValuesForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.ResetToAdminValuesForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#ResetToAdminValuesForUnits) 
### Sub **RollbackForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.RollbackForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#RollbackForUnits) 
### Sub **SaveRepositoryForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.SaveRepositoryForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#SaveRepositoryForUnits) 
### Sub **SetDimensionsDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the DimensionsDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayTrailingZerosLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the DisplayTrailingZeros parameter.

**Role** :Locks or unlocks the DisplayTrailingZeros parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpNotationValuesGreaterLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetSameDisplayLock. Locks or unlocks the ExpNotationValuesGreater parameter.

**Role** :Locks or unlocks the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpNotationValuesLowerLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the ExpNotationValuesLower parameter.

**Role** :Locks or unlocks the ExpNotationValuesLower parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetListOfMagnitudesLock**( boolean  `iLocked`)

   Locks or unlocks the ListOfMagnitudes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMagnitudeValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iUnitName`,  double  `iDecimalPlaceReadWrite`,  double  `iDecimalPlaceReadOnly`)

   Sets the Magnitude parameters.  Ensure consistency with the C++ interface to which the work is delegated.  
### Sub **SetSameDisplayLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the SameDisplay parameter.

**Role** :Locks or unlocks the SameDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.