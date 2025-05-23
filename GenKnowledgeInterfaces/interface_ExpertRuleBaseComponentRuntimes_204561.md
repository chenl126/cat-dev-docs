# ExpertRuleBaseComponentRuntimes (Collection)

**_Represents the collection of ExpertRuleBase (ExpertChecks, ExpertRules, and ExpertRuleSets) components._**
This collection can be seen flattened (with Item/Count) or hierarchised (with ShallowItem/ShallowCount).

Be careful : the flattened view can be misleading. For instance, if there are two ExpertChecks with the same name, you will be able to access only **one** of them (with the methods [ExpertRuleBaseComponentRuntimes.Item](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.htm#Item) and [ExpertRuleBaseComponentRuntimes.Remove](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.htm#Remove) )

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIAExpertRuleBaseComponentRuntime](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntime_190760.md)

   Returns a RuleBase component using its index or its name from the entire RuleBase collection.  If several Expert components have the same name, the use of name is **unpredicted**.

**Parameters:**

` iIndex`      The index or the name of the Rule Base component to retrieve from the collection of Rule Base Components. As a numerics, this index is the rank of the Rule Base Component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Rule base component.  **Example:**      This example retrieves the last component in a `RuleSet` collection.

```VBScript
      Dim lastRuleBaseComponent as ExpertRuleBaseComponentRuntime
      Set lastRuleBaseComponent = RuleSet.Item(RuleCollection.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an Expert component from the Rule Base collection. If the expert component is a RuleSet all the rules, checks and rulesets embedded in the Ruleset will be also removed.  If several Expert components have the same name, the use of name is **unpredicted**.

**Parameters:**

` iIndex`      The index or the name of the component to retrieve from the collection. As a numerics, this index is the rank of the expert component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Expert component.  **Example:**      This example removes the Expert component named `density` from the `relations` collection.

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
     Set massCheck    = part.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.Remove("density")

```

### Func **ShallowCount**( ) As long

   Returns the number of **first-level-depth** objects in the collection. This is handy to scan the objects in a collection.

**Example:**      This example retrieves in `ObjectNumber` the number of objects currently gathered in `MyCollection`.

```VBScript
     ObjectNumber = MyCollection.ShallowCount

```

### Func **ShallowItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertRuleBaseComponentRuntime](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntime_190760.md)

   Returns a **first-level-depth** RuleBase component using its index or its name from the RuleBase collection.

**Parameters:**

` iIndex`      The index or the name of the Rule Base component to retrieve from the collection of Rule Base Components. As a numerics, this index is the rank of the Rule Base Component in the collection. The index of the first component in the collection is 1, and the index of the last component is ShallowCount. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Rule base component.  **Example:**      This example retrieves the last component in a `RuleSet` collection.

```VBScript
      Dim lastRuleBaseComponent as ExpertRuleBaseComponentRuntime
      Set lastRuleBaseComponent = RuleSet.ShallowItem(RuleCollection.ShallowCount)

```

### Sub **ShallowRemove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an **first-level-depth** Expert component from the Rule Base collection. If the expert component is a RuleSet all the rules, checks and rulesets embedded in the Ruleset will be also removed.

**Parameters:**

` iIndex`      The index or the name of the component to retrieve from the collection. As a numerics, this index is the rank of the expert component in the collection. The index of the first component in the collection is 1, and the index of the last component is `ShallowCount`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Expert component.  **Example:**      This example removes the Expert component named `density` from the `relations` collection.

```VBScript
     Dim CATDocs As Document
     Set CATDocs   = CATIA.Documents
     Dim partdoc As PartDocument
     Set partdoc   = CATDocs.Add("CATPart")
     Dim part As Part
     Set part      = partdoc.Part
     Set massCheck    = part.Relations.Item("RuleBase").RuleSet.ExpertRuleBaseComponentRuntimes.ShallowRemove("density")

```