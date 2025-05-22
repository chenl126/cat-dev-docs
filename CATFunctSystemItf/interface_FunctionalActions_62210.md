# FunctionalActions (Collection)

**_The interface to access a collection of FunctionalActions._**

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)  `iFrom`,  [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)  `iTo`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

Create a FunctionalAction.  
### Sub **Delete**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

Delete a FunctionalAction.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

Returns an action using its index or its name from the actions collection.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the collection of actions. As a numerics, this index is the rank of the action in the collection. The index of the first action in the collection is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Act1` the fifth action in the collection and in `Act2` the action named `Moves`.

```VBScript
Dim Act1 As FunctionalAction
Set Act1 = Desc.Action(5)
Dim Act2 As FunctionalAction
Set Act2 = Desc.Action("Moves")

```