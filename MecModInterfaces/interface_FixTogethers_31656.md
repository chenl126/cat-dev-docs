# FixTogethers (Collection)

**_A collection of all the FixTogether objects contained in the product._**

## Methods

### Func **Add**(| ) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

   Creates a new FixTogether and adds it to the FixTogethers collection.

**Returns:**      The created FixTogether  **Example:**      The following example creates a FixTogether `newFixTogether` in the FixTogether collection.

```VBScript
     Set newFixTogether = fixTogethers.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

   Returns a FixTogether using its index or its name from the FixTogethers collection.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to retrieve from the collection of FixTogether. As a numerics, this index is the rank of the FixTogether in the collection. The index of the first FixTogether in the collection is 1, and the index of the last FixTogether is Count. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved FixTogether **Example:**      This example retrieves in `thisFixTogether` the fifth FixTogether in the collection and in `thatFixTogether` the FixTogether named `MyFixTogether` in the FixTogether collection of the `product` product.

```VBScript
     Set fixTogetherColl = product.FixTogethers
     Set thisFixTogether = fixTogetherColl.Item(5)
     Set thatFixTogether = fixTogetherColl.Item("MyFixTogether")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a FixTogether from the FixTogethers collection.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to remove from the FixTogethers collection. As a numerics, this index is the rank of the FixTogether in the collection. The index of the first FixTogether in the collection is 1, and the index of the last FixTogether is Count. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last FixTogether in the collection.

```VBScript
     fixTogetherColl.Remove(fixTogetherColl.Count)

```