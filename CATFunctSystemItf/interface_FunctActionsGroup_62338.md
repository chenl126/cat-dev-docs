# FunctActionsGroup (Object)

**_The interface to access a group of functional actions in a system._**

## Properties

### Property **ActionsCount**(| ) As long (Read Only)

   Get the count of actions referenced by the actions' group.  Methods

### Sub **Add**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

   Adds an action to the actions' group.  Fails if the action :

  * is already in a group
  * has "From" and "To" extremities inconsistent with the existing actions.
In case of an ordered group, the added action will be appended.
(i.e. for flows sequencing actions)

**Parameters:**

` iAction`      The action to be added to the group of actions.

### Sub **GetExtremities**( double  `oInputX`,  double  `oInputY`,  double  `oOutputX`,  double  `oOutputY`)

   Get coordinates of Input and Output extremities.  
### Sub **Remove**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

   Removes an action from the actions' group.

**Parameters:**

` iAction`      The action to be removed from the group of actions.

### Sub **RemovePosition**( long  `iPosition`)

   Removes an action from the actions' group.

**Parameters:**

` iPosition`      The position of the action to be removed from the group of actions.

### Func **Retrieve**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

   Returns an action using its index or its name from the actions group.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the group of actions. As a numerics, this index is the rank of the action in the group. The index of the first action in the group is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth action in the group and in `Obj2` the action named `Valve`.

```VBScript
     Dim Act1 As FunctionalAction
     Set Act1 = ActionsGrp.Retrieve(5)
     Dim Act2 As FunctionalAction
     Set Act2 = ActionsGrp.Retrieve("Reduces noise")

```

### Sub **SetExtremities**( double  `iInputX`,  double  `iInputY`,  double  `iOutputX`,  double  `iOutputY`)

   Set coordinates of Input and Output extremities.