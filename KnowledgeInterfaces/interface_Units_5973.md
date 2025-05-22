# Units (Collection)

**_Represents the collection of Units._**
This collection can be retrieved via any collection of parameters (method Units).

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAUnit](../KnowledgeInterfaces/interface_Unit_3832.md)

Returns a unit using its index or its name from the from the Parameters collection.

**Parameters:**

` iIndex`      The index or the name of the unit to retrieve from the collection of parameters. As a numerics, this index is the rank of the unit in the collection. The index of the first unit in the collection is 1, and the index of the last parameter is Count. As a string, it is the name you assigned to the parameter using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the parameter.  **Example:**      This example retrieves the millimeter unit in the `units` collection:

```VBScript
Set unitmm = units.Item("mm")

```