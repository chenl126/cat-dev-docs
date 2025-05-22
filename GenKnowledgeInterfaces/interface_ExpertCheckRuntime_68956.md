# ExpertCheckRuntime (Object)

**_Runtime part of a check._**
The following example shows how to access the Check check1 from an existing RuleSet RS1 of the RuleBase RB1.

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

### Property **AutomaticCorrect**( ) As boolean

Returns or sets the status of the automatic correction facility. When set to TRUE, the check automatically calls the user function defined by put_CorrectFunction when it fails.  
### Property **CheckEdition**( ) As [CATIAExpertCheck](../GenKnowledgeInterfaces/interface_ExpertCheck_25594.md) (Read Only)

Returns the editable object corresponding to this check. Be careful that, according to your licence, or the type of check you're handling, you may not have the right to edit the check.

**Example:**

```VBScript
Dim aCheckEdition As ExpertCheck
Set aCheckEdition = aCheckRuntime.CheckEdition

If not(aCheckEdition is Nothing) Then
  CATIA.SystemService.Print aCheckEdition.Body
End if

```

### Property **CorrectFunction**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the body to be called in order to correct the check.  
### Property **CorrectFunctionComment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the comment of the correct function of the check.  
### Property **CorrectFunctionType**( ) As long

Returns or sets the type of the body to be called in order to correct the check.

1    Visual Basic 2    Comment 3    Http 4    User Function  
### Property **Failures**( ) As [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md) (Read Only)

Returns the list of the tuples that don't satisfy this check.  
### Property **Help**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the contextual help of the check object.  
### Property **Justification**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the reason why the check was overridden.  
### Property **Priority**( ) As double

Returns or sets the priority of the check. The priority of expert checks indicates the order in which the checks are evaluated. Checks with the same priority are evaluated in the order of their creation.  
### Property **Succeeds**( ) As [CATIAExpertReportObjects](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md) (Read Only)

Returns the list of the tuples that satisfy this check.  Methods

### Sub **Correct**( )

Applies the "correction" function on failed elements.  
### Sub **Highlight**( )

Highlights the Failures on the check.  
### Func **Status**( ) As long

Returns the Status of the check.

**Example:**

```VBScript
Dim Check1 As ExpertCheck
Set Check1	 = RuleSet.ExpertRuleBaseComponentRuntimes.Item("Check1")
status = Check1.Status ()

```

**Returns:**      1=OK, 0=KO.