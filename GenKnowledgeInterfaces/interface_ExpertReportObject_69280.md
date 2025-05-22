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