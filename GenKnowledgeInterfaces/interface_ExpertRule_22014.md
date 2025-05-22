# ExpertRule (Object)

**_Represents the edition part of a rule._**
The following example shows how access the Rule Rule1 from an existing RuleSet RS1 of the RuleBase RB1

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
Set RuleSet	 = RuleBase.ExpertRuleBaseComponentRuntimes.Item("RS1")
Dim Rule1 As ExpertRuleRuntime
Set Rule1	 = RuleSet.ExpertRuleBaseComponentRuntimes.Item("Rule1")

```

**See also:**      [Relations](../KnowledgeInterfaces/interface_Relations_18301.md), [ExpertRuleBase](../GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.md)

## Properties

### Property **Body**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the string that defines the body of a Rule. For instance: "if ( H\Diameter > 20mm ) H\Activity = FALSE"  
### Property **Language**( ) As long

Returns or sets the language of a rule.  
### Property **Variables**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the variables scope of the a Rule. For instance: "H:Hole; P: Pad"