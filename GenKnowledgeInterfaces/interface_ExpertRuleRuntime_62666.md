# ExpertRuleRuntime (Object)

**_Represents the ExpertRuleRuntime object._**

## Properties

### Property **Priority**( ) As double

Returns or sets the priority of the rule. The priority of expert rules indicates the order in which the rules are evaluated. Rules with the same priority are evaluated in the order of their creation.  
### Property **RuleEdition**( ) As [CATIAExpertRule](../GenKnowledgeInterfaces/interface_ExpertRule_22014.md) (Read Only)

Returns the editable object corresponding to this rule. Be careful that, according to your licence, or the type of rule you're handling, you may not have the right to edit the rule. Dim aRuleEdition As ExpertRule Set aRuleEdition = aRuleRuntime.RuleEdition If not(aRuleEdition is Nothing) Then CATIA.SystemService.Print aRuleEdition.Body End if