# ExpertRuleSetRuntime (Object)

**_Represents the ExpertRuleSet object in the RelationSet._**

## Properties

### Property **ExpertRuleBaseComponentRuntimes**(| ) As [CATIAExpertRuleBaseComponentRuntimes](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.md) (Read Only)

   Returns the list of the RuleBaseComponent.  
### Property **RuleSetEdition**( ) As [CATIAExpertRuleSet](../GenKnowledgeInterfaces/interface_ExpertRuleSet_36300.md) (Read Only)

   Returns the editable object corresponding to this ruleset. Be careful that, according to your licence, or the type of ruleset you're handling, you may not have the right to edit the ruleset.

**Example:**

```VBScript
     Dim aRuleSetEdition As ExpertRuleSet
     Set aRuleSetEdition = aRuleSetRuntime.RuleSetEdition

     If not(aRuleSetEdition is Nothing) Then
       ' .. some actions
     End if

```

Methods

### Func **Status**( ) As long

   Returns the Status of the ruleset: 1=OK, 0=KO.

**Example:**

```VBScript
     Dim RuleSet1 As ExpertRuleSet
     Set RuleSet1	 = RuleSet.ExpertGenericRuleBaseComponentRuntimes.Item("RuleSet1")
     status = RuleSet1.Status ()

```

**Returns:**      Status of the ruleset