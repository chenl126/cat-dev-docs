# References (Collection)

**_A collection of all the references aggregated in an object._**

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md)

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns a reference using its index or its name from the References collection.

**Parameters:**

` iIndex`      The index or the name of the reference to retrieve from the collection of references. As a numerics, this index is the rank of the reference in the collection. The index of the first reference in the collection is 1, and the index of the last reference is Count. As a string, it is the name you assigned to the reference using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved reference  **Example:**      This example retrieves the last item in the `RefList` reference collection by means of the Count property.

```VBScript
Dim LastRef As Reference
Set LastRef = RefList.Item(RefList.Count)

```