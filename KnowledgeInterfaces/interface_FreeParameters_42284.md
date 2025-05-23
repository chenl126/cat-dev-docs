# FreeParameters (Collection)

**_Interface to access a CATIAFreeParameters._**

## Methods

### Func **AddFreeParameter**(| [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) | `parameter`) As [CATIAFreeParameter](../KnowledgeInterfaces/interface_FreeParameter_36139.md)

   Adds a free parameter. This parameter must not be read only.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFreeParameter](../KnowledgeInterfaces/interface_FreeParameter_36139.md)

   Retrieves an optimization using its index or its name from the Free Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the free parameter to retrieve from the collection of free parameters. As a numerics, this index is the rank of the free parameter in the collection. The index of the first free parameter in the collection is 1, and the index of the last free parameter is Count. As a string, it is the name you assigned to the free parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when changing the free parameter name by the property panel.  **Returns:**      The retrieved free parameter  **Example:**      This example retrieves the last free parameter in the `free parameters` collection.

```VBScript
     Set lastFreeParameter = freeParameters.Item(freeParameters.Count)

```

### Sub **RemoveFreeParameter**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a free parameter.