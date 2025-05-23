# ExpertRuleSet (Object)

**_Represents the ExpertRuleSet object which is the editable part of a RuleSet or a RuleBase._**
The following example shows how to access the RuleSet of the rule Base RB1

```VBScript
     Dim CATDocs As Documents
     Set CATDocs   = CATIA.Documents
     Dim partdoc As Document
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part as Part
     Set part      = partdoc.Part
     Dim relations as Relations
     Set relations = part.Relations
     Dim RuleBase as ExpertRuleBaseRuntime
     Set RuleBase  = relations.Item("RB1")
     Dim RuleSet as ExpertRuleSet
     Set RuleSet	 = RuleBase.RuleSet

```

## Methods

### Func **CreateCheck**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iCheckVariables`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iCheckBody`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iRuleSet`) As [CATIAExpertCheck](../GenKnowledgeInterfaces/interface_ExpertCheck_25594.md)

   Creates a check and adds it to the RuleSet.

**Parameters:**

` iName`      The check name
` iCheckVariables`      define variables of the check.
` iCheckBody`      The check definition
` iRuleSet`      The ruleset name where the check is to be aggregated. If this macro is used from the RuleSet where we want to create the check, the param must be equal to value : "".

**Returns:**      The created check  **Example:**      This example creates the `SolidActivity` check and adds it to the newly created `RuleSet.1` RuleSet then creates the `HoleActivity` check and adds it to the newly created `RuleSet.2` RuleSet

```VBScript
      Dim CATDocs As Documents
      Set CATDocs   = CATIA.Documents
      Dim partdoc As Document
      Dim part as Part
      Dim CheckSolid as ExpertCheck
      Dim ruleset as ExpertRuleSet
      Dim CheckHole as ExpertCheck

      Set partdoc      = CATDocs.Add("CATPart")
      Set part         = partdoc.Part
      Set CheckSolid   = part.Relations.Item("RuleBase").RuleSet.CreateCheck
                         ("SolidActivity",
                          "Sol : Solid",
                          "Sol.Activity == True",
                          "RuleSet.1")
      Set ruleset      = part.Relations.Item("RuleBase").RuleSet.CreateRuleSet
                         ("RuleSet.2",
                          "")
      Set CheckHole    = ruleset.CreateCheck
                         ("HoleActivity",
                          "H : Hole",
                          "H.Activity == True",
                          "")

```

### Func **CreateRule**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRuleVariables`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRuleBody`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRuleSet`) As [CATIAExpertRule](../GenKnowledgeInterfaces/interface_ExpertRule_22014.md)

   Creates a rule and adds it to the RuleSet.

**Parameters:**

` iName`      The rule name
` iRuleVariables`      define variables of the rule.
` iRuleBody`      The check definition
` iRuleSet`      The RuleSet name where this rule aggregated. If this macro is used from the ruleset where we want to aggregate the rule, the param must be equal to value : "".

**Returns:**      The created rule  **Example:**      This example creates the `DesactivateIfActivatedOnSolid` rule and adds it to the newly created `RuleSet.1` RuleSet then creates the `DesactivateIfActivatedOnHole` rule and adds it to the newly created `RuleSet.2` RuleSet

```VBScript
      Dim CATDocs As Documents
      Set CATDocs   = CATIA.Documents

      Dim partdoc As Document
      Set partdoc   = CATDocs.Add("CATPart")

      Dim part as Part
      Set part         = partdoc.Part

      Dim rulesolid as ExpertRule
      Set rulesolid    = part.Relations.Item("RuleBase").RuleSet.CreateRule
                         ("DesactivateIfActivatedOnSolid",
                          "Sol : Solid",
                          "Sol.Activity == True then Sol.Activity = False",
    						"RuleSet.1")
      Dim ruleset as ExpertRuleSet
      Set ruleset      = part.Relations.Item("RuleBase").RuleSet.CreateRuleSet
                         ("RuleSet.2",
                          "")
      Dim rulehole as ExpertRule
      Set rulehole     = ruleset.CreateRule
                         ("DesactivateIfActivatedOnHole",
                          "H : Hole",
                          "H.Activity == True then H.Activity = False",
                          "")

```

### Func **CreateRuleSet**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRuleSet`) As [CATIAExpertRuleSet](../GenKnowledgeInterfaces/interface_ExpertRuleSet_36300.md)

   Creates a RuleSet and adds it to the RuleSet.

**Parameters:**

` iName`      The ruleset name
` iRuleSet`      The ruleset name where this ruleset is to be aggregated. If this macro is used from the ruleset or the rulebase where we want to aggregate the ruleset, the param must be equal to value : "".

**Returns:**      The created ruleset  **Example:**      This example, firstly, creates the `RuleSet.1` RuleSet and adds it to the newly created RuleBase. Secondly, it creates `RuleSet.2` RuleSet and adds it to the ruleset `RuleSet.1`

```VBScript
      Dim CATDocs As Documents
      Set CATDocs   = CATIA.Documents
      Dim partdoc As Document
      Set partdoc   = CATDocs.Add("CATPart")
      Dim part as Part
      Set part         = partdoc.Part
      Dim RS1 as ExpertRuleSet
      RS1 = part.Relations.Item("RuleBase").RuleSet.CreateRuleSet
                         ("RuleSet.1",
                          "")
      Dim RS2 as ExpertRuleSet
      RS2 = part.Relations.Item("RuleBase").RuleSet.CreateRuleSet
                         ("RuleSet.2",
                          "RuleSet.1")

```