# OptimizationConstraints (Collection)

**_Represents a collection of Optimization Constraint._**

## Methods

### Func **AddConstraint**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `constraintExpression`) As [CATIAOptimizationConstraint](../KnowledgeInterfaces/interface_OptimizationConstraint_106166.md)

   Adds a optimization constraint. This parameter must not be read only.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAOptimizationConstraint](../KnowledgeInterfaces/interface_OptimizationConstraint_106166.md)

   Returns an optimization constraint using its index or its name from the optimization constraints collection.

**Parameters:**

` iIndex`      The index or the name of the optimization constraint to retrieve from the collection of optimization constraints. As a numerics, this index is the rank of the optimization constraint in the collection. The index of the first optimization constraint in the collection is 1, and the index of the last optimization constraint is Count. As a string, it is the name you assigned to the optimization constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the optimization constraint name by the property panel.  **Returns:**      The retrieved optimization constraint  **Example:**      This example retrieves the last optimization constraint in the `optimization constraints` collection.

```VBScript
     Set lastConstraint = constraints.Item(constraints.Count)

```

### Sub **RemoveConstraint**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a given optimization constraint using its index or its name from the optimization constraints collection.

**Parameters:**

` iIndex`      the name of the constraint if argument is a string or the index of the constraint if argument is an integer.