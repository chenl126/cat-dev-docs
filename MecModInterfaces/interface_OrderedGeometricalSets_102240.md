# OrderedGeometricalSets (Collection)

**_A collection of the OrderedGeometricalSet objects._**

## Methods

### Func **Add**( ) As [CATIAOrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md)

Creates a new ordered geometrical set and adds it to the OrderedGeometricalSets collection. Thisordered geometrical set becomes the current one

**Returns:**      The created ordered geometrical set  **Example:**      The following example creates a ordered geometrical set named `newOrderedGeometricalSet` in the ordered geometrical set collection of the `rootPart` part in the `partDoc` part document. `NewPartBody` becomes the in work object of `partDoc`.

```VBScript
Set NewPartBody = rootPart.OrderedGeometricalSets.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAOrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md)

Returns a ordered geometrical set using its index or its name from the ordered geometrical set collection.

**Parameters:**

` iIndex`      The index or the name of the ordered geometrical set to retrieve from the collection of ordered geometrical sets. As a numerics, this index is the rank of the ordered geometrical set in the collection. The index of the first ordered geometrical set in the collection is 1, and the index of the last ordered geometrical set is Count. As a string, it is the name you assigned to the ordered geometrical set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ordered geometrical set **Example:**      This example retrieves in `ThisOrderedGeometricalSet` the fifth ordered geometrical set in the collection and in `ThatOrderedGeometricalSet` the ordered geometrical set named `MyOrderedGeometricalSet` in the ordered geometrical set collection of the `partDoc` part document.

```VBScript
Set orderedGeometricalSetColl = partDoc.Part.OrderedGeometricalSets
Set ThisOrderedGeometricalSet = orderedGeometricalSetColl.Item(5)
Set ThatOrderedGeometricalSet = orderedGeometricalSetColl.Item("MyOrderedGeometricalSet")

```