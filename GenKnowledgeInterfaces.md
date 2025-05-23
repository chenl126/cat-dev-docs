# GenKnowledgeInterfaces Framework

## Object Index

  * [ExpertCheck](GenKnowledgeInterfaces/interface_ExpertCheck_25594.md)
  * [ExpertCheckRuntime](GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.md)
  * [ExpertReportObject](GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)
  * [ExpertReportObjects](GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.md)
  * [ExpertRule](GenKnowledgeInterfaces/interface_ExpertRule_22014.md)
  * [ExpertRuleBase](GenKnowledgeInterfaces/interface_ExpertRuleBase_41078.md)
  * [ExpertRuleBaseComponentRuntime](GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntime_190760.md)
  * [ExpertRuleBaseComponentRuntimes](GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.md)
  * [ExpertRuleBaseRuntime](GenKnowledgeInterfaces/interface_ExpertRuleBaseRuntime_93263.md)
  * [ExpertRuleRuntime](GenKnowledgeInterfaces/interface_ExpertRuleRuntime_62666.md)
  * [ExpertRuleSet](GenKnowledgeInterfaces/interface_ExpertRuleSet_36300.md)
  * [ExpertRuleSetRuntime](GenKnowledgeInterfaces/interface_ExpertRuleSetRuntime_85712.md)

## Enumerated Types Index

  * [CatDescriptionLengthType](GenKnowledgeInterfaces/enum_CatDescriptionLengthType_122046.md)
  * [CatOutPutFormatType](GenKnowledgeInterfaces/enum_CatOutPutFormatType_76632.md)
  * [CatShowResultType](GenKnowledgeInterfaces/enum_CatShowResultType_62350.md)
  * [CatSolveType](GenKnowledgeInterfaces/enum_CatSolveType_31004.md)
  * [CatVisualizationType](GenKnowledgeInterfaces/enum_CatVisualizationType_86736.md)

---

# CatDescriptionLengthType (Enumeration)

**_Precision of the text report._**

**Values:**

` ShortText`      the report only shows status.
` LongText`      the report shows status and t-uples for each check.

---

# CatOutPutFormatType (Enumeration)

**_Output format of the Knowledge Expert text report._**

**Values:**

` KWEHtml`      HTML format.
` KWEText`      Simple text format.
` KWEPrint`      To the printer.
` KWEEmail`      As an e-mail.

---

# CatShowResultType (Enumeration)

**_Sorting option for the Expert Knowledge text report._**

**Values:**

` ByRule`      Sort by the name of the rules.
` ByObject`      Sort by the name of the objects.
` ByState`      Sort by the status of the rules (failed or succeeded).

---

# CatSolveType (Enumeration)

**_Type for controlling the resolution in Knowledge Expert._**

An optimized resolution is a resolution taking into account only the objects modified since the previous resolution.

A complete resolution is a resolution starting from scratch : nothing from the past is taken into account.

**Values:**

` ManualSolveType`      0 : the complete resolution is not called when the part/product is updated.
` AutomaticOptimizedSolveType`      1 : the optimized resolution is called when the part/product is updated.
` AutomaticCompleteSolveType`      2 : the complete resolution is called when the part/product is updated.

---

# CatVisualizationType (Enumeration)

**_Type of checks to be chosen for the Expert Knowledge Report._**

**Values:**

` Passed`      True checks.
` Failed`      False checks.
` Both`      True and false checks.

---

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

### Property **Body**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

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

---

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

---

# ExpertReportObject (Object)

**_Represents the ExpertReportObject object._**

## Properties

### Property **Validity**( ) As boolean (Read Only)

   Returns the validity of a check for a given tuple. The result depends on the result of the check for a given tuple : "True" or "False" for the tuple.  Methods

### Sub **getTuple**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

   Returns a tuple (a collection of objects) concerned by this report object.

**Example:**

```VBScript
     Dim relations1 As Relations
     Dim RuleBase1 As ExpertRuleBaseRuntime
     Dim ListComponents As ExpertRuleBaseComponentRuntimes
     Dim AComponent As ExpertRuleBaseComponentRuntime
     Dim NupletsList As ExpertReportObjects
     Dim ANuplet As ExpertReportObject
     Dim anArray () as Object
     Dim anElementArray as Object

     Set relations1 = part1.Relations
     Set RuleBase1 = relations1.Item("RuleBase")
     Set ListComponents = RuleBase1.RuleSet.ExpertRuleBaseComponentRuntimes
     ' Let's get a check ..
     Set AComponent = ListComponents.Item("CheckOnHoles")
     ' .. and let's see what makes it true
     Set NupletsList = AComponent.Succeeds
     For i = 1 to AComponent.Succeeds.CountSucceed
       Set ANuplet = AComponent.Succeeds.SucceedItem(i)
       NupletSize = ANuplet.getTupleSize()
       ReDim anArray (NupletSize)
       ANuplet.getTuple(anArray)
       For j = LBound(anArray) to UBound(anArray)
         Set anElementArray = anArray(j) ' a hole

         ' .. some action on the element of the array
       Next
     Next

```

**Parameters:**

` oSafeArray`      The collection of objects.

### Func **getTupleSize**( ) As long

   Returns the size of the tuple concerned by this report object.

**Returns:**      Size of the tuple

---

# ExpertReportObjects (Collection)

**_Represents the collection of (succeeded or failed) report objects._**

## Properties

### Property **CountFail**( ) As long (Read Only)

   Returns the number of failed tuples in the failed tuples collection. It is redundant with [Collection.Count](../System/interface_Collection_22150.htm#Count) for [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collection. For [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collection, it will fail.

**Example:**      This example retrieves in `ObjectNumber` the number of tuples currently gathered in `MyCollection`.

```VBScript
     ObjectNumber = MyCollection.CountFail

```

### Property **CountSucceed**( ) As long (Read Only)

   Returns the number of succeeded tuples in the succeeded tuples collection. It is redundant with [Collection.Count](../System/interface_Collection_22150.htm#Count) for [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collection. For [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collection, it will fail.

**Example:**      This example retrieves in `ObjectNumber` the number of tuples currently gathered in `MyCollection`.

```VBScript
     ObjectNumber = MyCollection.CountSucceed

```

Methods

### Func **FailItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

   Retrieves a report failed component from a failed tuples collection, using its index or its name from the Check collection. It is redundant with [ExpertReportObjects.Item](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.htm#Item) for [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collections. For [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collections, it will fail.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

   Retrieves a Report component using its index or its name from the Check collection.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component  
### Func **SucceedItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertReportObject](../GenKnowledgeInterfaces/interface_ExpertReportObject_69280.md)

   Retrieves a report component from a succeeded tuples collection, using its index or its name from the Check collection. It is redundant with [ExpertReportObjects.Item](../GenKnowledgeInterfaces/interface_ExpertReportObjects_77702.htm#Item) for [ExpertCheckRuntime.Succeeds](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Succeeds) collections. For [ExpertCheckRuntime.Failures](../GenKnowledgeInterfaces/interface_ExpertCheckRuntime_68956.htm#Failures) collections, it will fail.

**Parameters:**

` iIndex`      The index or the name of the Report component to retrieve from the collection of Report Components. As a numerics, this index is the rank of the Report component in the collection. The index of the first component in the collection is 1, and the index of the last component is `Count`. As a string, it is the name you assigned to the component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the component.  **Returns:**      The retrieved Report component

---

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

---

# ExpertRuleBase (Object)

**_Represents the RuleBase object that can be edited._**

## Methods

### Func **VolatileCopy**( ) As [CATIAExpertRuleBaseRuntime](../GenKnowledgeInterfaces/interface_ExpertRuleBaseRuntime_93263.md)

   Copy the persistent rulebase in a unpersistent unchangeable rulebase.

**Returns:**      A volatile copy of the rulebase

---

# ExpertRuleBaseComponentRuntime (Object)

**_Represents a rule base component in a ruleset._**

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

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

---

# ExpertRuleBaseComponentRuntimes (Collection)

**_Represents the collection of ExpertRuleBase (ExpertChecks, ExpertRules, and ExpertRuleSets) components._**
This collection can be seen flattened (with Item/Count) or hierarchised (with ShallowItem/ShallowCount).

Be careful : the flattened view can be misleading. For instance, if there are two ExpertChecks with the same name, you will be able to access only **one** of them (with the methods [ExpertRuleBaseComponentRuntimes.Item](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.htm#Item) and [ExpertRuleBaseComponentRuntimes.Remove](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.htm#Remove) )

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAExpertRuleBaseComponentRuntime](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntime_190760.md)

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

---

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

### Property **ReportDescriptionLength**( ) As [CatDescriptionLengthType](../GenKnowledgeInterfaces/enum_CatDescriptionLengthType_122046.md)

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

---

# ExpertRuleRuntime (Object)

**_Represents the ExpertRuleRuntime object._**

## Properties

### Property **Priority**( ) As double

   Returns or sets the priority of the rule. The priority of expert rules indicates the order in which the rules are evaluated. Rules with the same priority are evaluated in the order of their creation.  
### Property **RuleEdition**( ) As [CATIAExpertRule](../GenKnowledgeInterfaces/interface_ExpertRule_22014.md) (Read Only)

   Returns the editable object corresponding to this rule. Be careful that, according to your licence, or the type of rule you're handling, you may not have the right to edit the rule. Dim aRuleEdition As ExpertRule Set aRuleEdition = aRuleRuntime.RuleEdition If not(aRuleEdition is Nothing) Then CATIA.SystemService.Print aRuleEdition.Body End if

---

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

### Func **CreateCheck**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCheckVariables`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCheckBody`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRuleSet`) As [CATIAExpertCheck](../GenKnowledgeInterfaces/interface_ExpertCheck_25594.md)

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

---

# ExpertRuleSetRuntime (Object)

**_Represents the ExpertRuleSet object in the RelationSet._**

## Properties

### Property **ExpertRuleBaseComponentRuntimes**( ) As [CATIAExpertRuleBaseComponentRuntimes](../GenKnowledgeInterfaces/interface_ExpertRuleBaseComponentRuntimes_204561.md) (Read Only)

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