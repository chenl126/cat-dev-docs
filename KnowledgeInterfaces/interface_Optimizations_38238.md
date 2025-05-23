# Optimizations (Collection)

**_Represents a collection of optimization features._**

**See also:**      [Optimization](../KnowledgeInterfaces/interface_Optimization_32466.md)

## Methods

### Func **CreateConstraintsSatisfaction**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iComment`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iFormulaBody`) As [CATIASetOfEquation](../KnowledgeInterfaces/interface_SetOfEquation_36247.md)

   Returns a set of equations.

**Parameters:**

` iName`      The name of the set of equations.
` iComment`      The comment of the set of equations.
` iFormulaBody`      The body of the set of equations " a==b+4; c ≤ 90".

### Func **CreateOptimization**( ) As [CATIAOptimization](../KnowledgeInterfaces/interface_Optimization_32466.md)

   Creates an empty optimization.
This optimization cannot be used while its properties have not been set.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves an optimization using its index or its name from the Optimizations collection.

**Parameters:**

` iIndex`      The index or the name of the item (optimization or constraintSatisfaction) to retrieve from the collection of optimizations. As a numerics, this index is the rank of the item in the collection. The index of the first item in the collection is 1, and the index of the last item is Count. As a string, it is the name you assigned to the item using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the item name by the property panel.  **Returns:**      either the retrieved optimization or the retreived constraintSatisfaction  **Example:**      This example retrieves the last item (optimization or constraintSatisfaction) in the `optimizations` collection.

```VBScript
     Set lastItem = optimizations.Item(optimizations.Count)

```