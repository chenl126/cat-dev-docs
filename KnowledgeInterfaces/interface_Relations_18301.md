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

### Property **Optimizations**(| ) As [CATIAOptimizations](../KnowledgeInterfaces/interface_Optimizations_38238.md) (Read Only)

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