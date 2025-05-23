# BasicComponents (Collection)

**_The collection of Basic Components defining and analysis object._**
These components are agregated by another basic component, an entity or a set.

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iVariant`) As [CATIABasicComponent](../CATAnalysisInterfaces/interface_BasicComponent_42336.md)

   Returns an Basic Component using its index or its name from the Basic Components collection.

**Parameters:**

` iIndex`      The index or the name of the Basic Component to retrieve from the collection of Basic Component. As a numerics, this index is the rank of the Basic Component. in the collection. The index of the first Basic Component in the collection is 1, and the index of the last Basic Component is Count. As a string, it is the name you assigned to the Basic Component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Basic Component