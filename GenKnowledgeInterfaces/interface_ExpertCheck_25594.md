# ExpertCheck (Object)

**_Represents the edition part of a check._**
The following example shows how to access the Check check1 from an existing RuleSet RS1 of the RuleBase RB1

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
     Set RuleBase  = relations.Item("RB1")
     Dim Ruleset As ExpertRuleSetRuntime
     Set RuleSet	 = RuleBase.RuleSet.ExpertRuleBaseComponentRuntimes.Item("RS1")
     Dim Check1 As ExpertCheckRuntime
     Set Check1	 = RuleSet.ExpertRuleBaseComponentRuntimes.Item("Check1")

```

**See also:**      [Relations](../KnowledgeInterfaces/interface_Relations_18301.md), [ExpertRuleBase](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.md)

## Properties

### Property **Body**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the body of a Check.

**Example:**

```VBScript
     Check1.Body = "H.Diameter > 20mm AND GetSubString(P.Name, 1, 6) == ""myPad."""

```

### Property **Language**( ) As long

   Returns or sets the language of a check.

1    KWE language 2    VB Script  
### Property **Variables**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the variable scope of an Expert Check.

**Example:**

```VBScript
     Check1.Variables = "H:Hole; P: Pad"

```