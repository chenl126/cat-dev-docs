# Constraints (Collection)

**_A collection of all geometric constraints set on a part, a sketch, or a product._**
A constraint collection is created with default values for its properties (such as value, orientation, etc.). Use the constraint properties edition services to set them to appropriate values after constraint creation.

**See also:**      [Constraint](../MecModInterfaces/interface_Constraint_22634.md)

## Properties

### Property **BrokenConstraintsCount**(| ) As long (Read Only)

   Returns the number of broken constraints from the Constraints collection.

**Example:**     The following example retrieves in `BknCstNum` the number of broken constraints from the `myListofConstraints` collection of constraints:

```VBScript
     BknCstNum = myListofConstraints.BrokenConstraintsCount

```

### Property **UnUpdatedConstraintsCount**( ) As long (Read Only)

   Returns the number of unupdated constraints from the Constraints collection.

**Example:**     The following example retrieves in `UnUpdCstNum` the number of unupdated constraints from the `myListofConstraints` collection of constraints:

```VBScript
     UnUpdCstNum = myListofConstraints.UnUpdatedConstraintsCount

```

Methods

### Func **AddBiEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to two geometric elements and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iFirstElem`      The first constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iSecondElem`      The second constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example adds the `NewCst` tangency constraint in a sketch, between the two circles `c1` and `c2` using the value 4 for `catCstTypeTangency`.

```VBScript
     Set newCst = skCstList.AddBiEltCst(4, c1, c2)

```

### Func **AddMonoEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to a single geometric element and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iElem`      The constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example creates the reference constraint `NewCst` to a part, stating that the `P1` point should remain fixed with respect to the part's origin elements using the value 0 for `catCstTypeReference`, and adds it to the `cstList` collection.

```VBScript
     Set NewCst = cstList.AddMonoEltCst(0, P1)

```

### Func **AddTriEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iThirdElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to three geometric elements and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iFirstElem`      The first constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iSecondElem`      The second constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iThirdElem`      The third constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example adds `symCst` symmetry constraint in a part, stating that the cylinders `cyl1` and `cyl2` are symmetric with respect to the plane `symPlane` using the value 15 for `catCstTypeSymmetry`.

```VBScript
     Set symCst = prtCstList.AddTriEltCst(15, cyl1, cyl2, symPlane)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Returns a constraint using its index or its name from the Constraints collection.

**Parameters:**

` iIndex`      The index or the name of the constraint to retrieve frm the collection of constraints. As a numerics, this index is the rank of the constraint in the collection. The index of the first constraint in the collection is 1, and the index of the last constraint is Count. As a string, it is the name you assigned to the constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved constraint  **Example:**      This example retrieves in `cst1` the first constraint in the collection and in `cst2` the constraint Constraint.2.

```VBScript
     Set cst1 = cstList.Item(1)
     Set cst2 = cstList.Item("Constraint.2")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a constraint from the Constraints collection.

**Parameters:**

` iIndex`      The index or the name of the constraint to remove from the Constraints collection. As a numerics, this index is the rank of the constraint in the collection. The index of the first constraint in the collection is 1, and the index of the last constraint is Count. As a string, it is the name you assigned to the constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last constraint in the collection.

```VBScript
     cstList.Remove(cstList.Count)

```