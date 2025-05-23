# ExpertRuleBaseRuntime (Object)

**_Represents the Runtime part of the RuleBase._**
The following example shows how to create the Rule Base RB1 from a newly created part document:

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
     Dim relations As Relations
     Set relations = part.Relations
     Dim Rulebase As ExpertRuleBaseRuntime
     Set RuleBase  = relations.CreateRuleBase("RB1")

```

**See also:**      [Relations](../KnowledgeInterfaces/interface_Relations_18301.md)

## Properties

### Property **ReportDescriptionLength**(| ) As [CatDescriptionLengthType](../GenKnowledgeInterfaces/enum_CatDescriptionLengthType_122046.md)

   Returns or sets the Report Description Length (For Text option only).

0    ShortText 1    LongText  
### Property **ReportOutPutFormat**( ) As [CatOutPutFormatType](../GenKnowledgeInterfaces/enum_CatOutPutFormatType_76632.md)

   Returns or sets the Report OutPut Format.

0    Html 1    Text 2    Print 3    Email  
### Property **ReportPath**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Report output path.  
### Property **ReportShowResult**( ) As [CatShowResultType](../GenKnowledgeInterfaces/enum_CatShowResultType_62350.md)

   Returns or sets the option for sorting the report.

0    ByRule 1    ByObject 2    ByState  
### Property **RuleBaseEdition**( ) As [CATIAExpertRuleBase](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.md) (Read Only)

   Returns the editable object corresponding to this rulebase. Be careful that, according to your licence, or the type of rulebase you're handling, you may not have the right to edit the rulebase.  **Example:**

```VBScript
     Dim aRBEdition As CATIAExpertRuleBase
     Set aRBEdition = aRBRuntime.RuleBaseEdition

     If not(aRBEdition is Nothing) Then
       ' .. action on the editable rulebase
     End if

```

### Property **RuleSet**( ) As [CATIAExpertRuleSet](../GenKnowledgeInterfaces/interface_ExpertRuleSet_36300.md) (Read Only)

   Returns the Set linked to the RuleBase. This is the main RuleSet that contains all the RuleBase components.  
### Property **SolveType**( ) As [CatSolveType](../GenKnowledgeInterfaces/enum_CatSolveType_31004.md)

   Returns or sets the solve option.  
### Property **TextVisualization**( ) As [CatVisualizationType](../GenKnowledgeInterfaces/enum_CatVisualizationType_86736.md)

   Returns or sets the Report option for visualization.

0    Passed 1    Failed 2    Both  Methods

### Func **AccurateType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns as a string the type of component.

**Returns:**      A string among ("ExpertRuleBase", "ExpertRuleBaseRuntime")  
### Sub **AddFact**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFact`)

   Adds new fact to the rule base resolution.

**Parameters:**

` iFact`      Fact to be added  **Example:**

```VBScript
      Dim pad3 as Shape
      Dim rulebase as ExpertRuleBase

      Set pad3 = part.MainBody.Shapes.Item("Pad3")
      Set rulebase = part.Relations.Item("RuleBase")
      rulebase.AddFact (pad3)

```

### Sub **AddRootOfFacts**( [CATIABase](../System/interface_AnyObject_17321.md)  `iRootFacts`)

   Adds a new root of facts to the rule base.

**Parameters:**

` iRootFacts`      root of facts to be added.

### Sub **Deduce**( )

   Launch a Forward chaining Solve on the current RuleBase.  **Example:**

```VBScript
      Dim rulebase as ExpertRuleBase

      Set rulebase = part.Relations.Item("RuleBase")
      rulebase.Deduce ()

```

### Func **Fingerprint**( ) As boolean

   Returns the Fingerprint information. The fingerprint indicates if the last result of the rulebase is relevant regarding to the objects the rule base has checked. In other words, if the part has evolved since last `Deduce`, the fingerprint is false. Be careful : on volatile rulebases ( [ExpertRuleBase.VolatileCopy](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.htm#VolatileCopy) ), it raises an error.

**Example:**

```VBScript
      on error resume next
      part.Relations.Item("RuleBase").Fingerprint ()
      on error goto 0

```

**Returns:**      Fingerprint information  
### Func **GetNumberOfRootsOfFacts**( ) As long

   Retrieves the number of roots of facts of the rule base.

**Returns:**      Number of roots of facts.  
### Sub **GetRootsOfFacts**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oRootsOfFacts`)

   Retrieves all the roots of facts from the rule base.

**Parameters:**

` oRootsOfFacts`      array of roots of facts.

### Sub **Import**( [CATIAExpertRuleSet](../GenKnowledgeInterfaces/interface_ExpertRuleSet_36300.md)  `iRuleSet`,  boolean  `iForce`)

   Import from RuleSet.

**Parameters:**

` iRuleSet`      CATIAExpertRuleSet : the RuleSet user want to import.
` iForce`      Boolean : if True (= 1), then if imported rules allready exist in target document, rules of target document are replaced.  **Example:**

```VBScript
     Dim CATDocs As Documents
     Set CATDocs   = CATIA.Documents
     Dim partdoc As Document
     Set partdoc = CATDocs.Open("e:\TargetDocument.CATPart")
     Dim part As Part
     Set part      = partdoc.Part
     Dim productdoc As Document
     Set productdoc = CATDocs.Open("e:\ImportedDocument.CATProduct")
     Dim product As Product
     Set product      = productdoc.Product
     Dim ruleset As ExpertRuleSet
     Set ruleset    = product.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.ShallowItem(1)
     part.Relations.Item("RuleBase").Import (ruleset,0)

```

### Sub **ImportFromFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`,  boolean  `iForce`)

   Import from file.

**Parameters:**

` iPath`      CATBSTR : the path of the document user want to import.
` iForce`      Boolean : if True (= 1), then if imported rules allready exist in target document, rules of target document are replaced. if False (= 0), then if imported rules allready exist in target document, rules of imported document are ignored.*  **Example:**

```VBScript
      part.Relations.Item("RuleBase").ImportFromFile ("e:\importeddocument.CATProduct",0)

```

### Sub **ImportWithLink**( [CATIABase](../System/interface_AnyObject_17321.md)  `iRoot`,  boolean  `iForce`)

   Import with link to a document.

**Parameters:**

` iRoot`      CATIABase : the root user want to import into.
` iForce`      Boolean : if True (= 1), then if imported rules allready exist in target document, rules of target document are replaced. if False (= 0), then if imported rules allready exist in target document, rules of imported document are ignored.*  **Example:**

```VBScript
      part.Relations.Item("RuleBase").ImportWithLink (root,0)

```

### Sub **RemoveRootOfFacts**( [CATIABase](../System/interface_AnyObject_17321.md)  `iRootFacts`)

   Removes a root of facts from the rule base.

**Parameters:**

` iRootFacts`      root of facts to be removed.

### Sub **Report**( boolean  `reallyStartBrowser`)

   Launch a Report. The default output format is HTML

**Parameters:**

` reallyStartBrowser`      Boolean : if True (= 1), then the browser is started on the report  **Example:**

```VBScript
      part.Relations.Item("RuleBase").Report (0)

```

### Func **SynchronizeStatus**( ) As boolean

   Returns the Synchronize information. The synchronize status indicates for a linked rule base if the rulebase is synchronized. Be careful : on volatile rulebases ( [ExpertRuleBase.VolatileCopy](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.htm#VolatileCopy) ), it raises an error.

**Example:**

```VBScript
      on error resume next
      part.Relations.Item("RuleBase").SynchronizeStatus ()
      on error goto 0

```

**Returns:**      Synchronize status