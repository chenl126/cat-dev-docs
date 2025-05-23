# List (Collection)

**_Represents a CATIAList._**

## Methods

### Sub **Add**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iItemValue`)

   Adds an item at the end of the list. Does an AddRef on the item. Returns E_FAIL if the object type is not correct. Will return E_FAIL if trying to set an already existing element while IsDuplicateElementsAllowed is false.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves a Feature using its index or its name from the Features collection.

**Parameters:**

` iIndex`      The index or the name of the Feature to retrieve from the collection of Features. As a numerics, this index is the rank of the Feature in the collection. The index of the first Feature in the collection is 1, and the index of the last Feature is Count. As a string, it is the name you assigned to the Feature using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Feature.  **Returns:**      The retrieved Feature  **Example:**      This example retrieves the last Feature in the `Features` collection.

```VBScript
     Dim lastFeature As CATIABase
     Set lastFeature = Features.Item(Features.Count)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Feature from the Features collection.

**Parameters:**

` iIndex`      The index or the name of the Feature to retrieve from the collection of Features. As a numerics, this index is the rank of the Feature in the collection. The index of the first Feature in the collection is 1, and the index of the last Feature is Count. As a string, it is the name you assigned to the Feature using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating the Feature.  **Example:**      This example removes the Feature named `density` from the `Features` collection.

```VBScript
     Features.Remove("density")

```

### Sub **Reorder**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndexCurrent`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndexTarget`)

   Reorders an element by moving it from the current position to the target position. Doesn't change the list if either position is out of the list. Return E_FAIL if cannot reorder.

### Sub **Replace**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iItemValue`)

   Sets an item in the list at a position. Does an AddRef on the item. Returns E_FAIL if the object type is not correct or the index is out of bounds. Returns E_FAIL if trying to set an already existing element while IsDuplicateElementsAllowed is false.