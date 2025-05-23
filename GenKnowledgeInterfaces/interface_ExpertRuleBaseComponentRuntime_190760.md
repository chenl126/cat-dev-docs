# ExpertRuleBaseComponentRuntime (Object)

**_Represents a rule base component in a ruleset._**

## Properties

### Property **Comment**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the comment of a rulebase component.  Methods

### Func **AccurateType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns as a string the type of component. Returns a string among ("ExpertCheck", "ExpertCheckRuntime", "ExpertRule", "ExpertRuleRuntime", "ExpertRuleSet", "ExpertRuleSetRuntime").

**Returns:**      Type name of the rule base component  
### Sub **Activate**( )

   Activates the RuleBaseComponent.

**Example:**      This example activates the `SolidActivity` ExpertCheck:

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
      part.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.Item("SolidActivity").Activate()

```

### Sub **Deactivate**( )

   Desactivates the RuleBaseComponent.

**Example:**      This example Desactivates the `SolidActivity` ExpertCheck:

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
      part.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.Item("SolidActivity").Deactivate()

```

### Func **IsUseOnly**( ) As boolean

   Retrieves the use-only status of the component.

**Returns:**      Use only status of the component  
### Func **Isactivate**( ) As boolean

   Tells if the RuleBaseComponent is active.

**Example:**      This example tells if the `SolidActivity` ExpertCheck is active :

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
     status = part.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.Item("SolidActivity").Isactivate()

```

**Returns:**      Activity of the rule base component  
### Func **Parse**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Syntactically analyses (ie parses) the component.

**Returns:**      Empty string if the parse is correct, otherwise comments on the errors  
### Sub **SetUseOnly**( )

   Prevents any access to the component for reading or deleting. Be careful : this operation is not reversible.