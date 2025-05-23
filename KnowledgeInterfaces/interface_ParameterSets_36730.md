# ParameterSets (Collection)

**_Represents a collection of parameter sets._**
The ParameterSet object is a neutral object that contains parameters, like the Parameters node in the specification tree.

The following example shows how to retrieve it on a part:

```VBScript
     Dim CATDocs As Documents
     Set CATDocs = CATIA.Documents
     Dim part1 As Document
     Set part1   = CATDocs.Add("CATPart")
     Dim parameters1 As Parameters
     Set parameters1 = part1.Part.Parameters
     Dim ParameterSet1 As ParameterSet
     Set ParameterSet1 = parameters1.RootParameterSet
     Dim parameterSets1 As ParameterSets
     Set parameterSets1 = parameterSet1.ParameterSets

```

This collection is not a collection of all parameter sets of a document, but a collection of all parameter sets in the current parameter set.

## Methods

### Func **CreateSet**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md)

   Creates a set of parameters and appends it to the parameter set which corresponds to this collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAParameterSet](../KnowledgeInterfaces/interface_ParameterSet_31016.md)

   Returns a parameter set using its index or its name from the ParameterSets collection.

**Parameters:**

` iIndex`      The index or the name of the parameter set to retrieve from the collection of parameter sets. As a numerics, this index is the rank of the parameter set in the collection. The index of the first parameter set in the collection is 1, and the index of the last parameter set is Count. As a string, it is the name you assigned to the parameter set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property .  **Example:**      This example retrieves the parameter set named "Parameters.1" in the `parameterSets` collection:

```VBScript
     Set theSet = parameterSets.Item("Parameters.1")

```