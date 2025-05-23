# FunctActionsGroups (Collection)

**_The interface to access the groups of functional actions in a system._**

## Methods

### Func **Create**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`,| | double | `iInputX`,| | double | `iInputY`,| | double | `iOutputX`,| | double | `iOutputY`) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)

   Create a Group of Actions.  
### Sub **Delete**( [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)  `iActGrp`)

   Delete a Group of Actions.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)

   Returns an actions'group using its index or its name from the actions' groups collection.

**Parameters:**

` iIndex`      The index or the name of the actions'group to retrieve from the collection of actions' groups. As a numerics, this index is the rank of the actions' group in the collection. The index of the first actions' group in the collection is 1, and the index of the last actions' group is Count. As a string, it is the name you assigned to the actions' group using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `AG1` the fifth actions' group in the collection and in `AG2` the actions' group named `Transmission`.

```VBScript
     Dim AG1 As FunctActionsGroup
     Set AG1 = ActionsGroups.Elem(5)
     Dim AG2 As FunctActionsGroup
     Set AG2 = ActionsGroups.Elem("Transmission")

```