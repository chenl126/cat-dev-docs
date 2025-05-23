# FunctionalObjects (Collection)

**_Interface to access a collection of FunctionalObjects._**

## Methods

### Func **Create**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`) As [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)

   Creates a FunctionalObject.  
### Func **CreateProxy**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md)  `iDesc`) As [CATIAFunctionalObjectProxy](../CATFunctSystemItf/interface_FunctionalObjectProxy_94928.md)

   Creates a FunctionalObjectProxi.  
### Sub **Delete**( [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)  `iObject`)

   Deletes a FunctionalObject.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)

   Returns an action using its index or its name from the actions collection.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the collection of actions. As a numerics, this index is the rank of the action in the collection. The index of the first action in the collection is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth object in the collection and in `Obj2` the action named `Valve`.

```VBScript
     Dim Obj1 As FunctionalObject
     Set Obj1 = Desc.Object(5)
     Dim Obj2 As FunctionalObject
     Set Obj2 = Desc.Object("Valve")

```