# StrAnchorPoints (Collection)

**_A collection of the anchor points of a section object._**

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIAStrAnchorPoint](../StructureInterfaces/interface_StrAnchorPoint_42208.md)

   Returns an anchor point from its index in the anchor points collection.

**Parameters:**

` iIndex`      The index of the anchor point to retrieve in the collection of anchor points. This index can either be the rank of the anchor point in the collection or the name you assign to the anchor point. As a numerics, this index is the rank of the anchor point in the collection. The index of the first anchor point in the collection is 1, and the index of the last anchor point is Count. As a string, it is the name you assigned to the member using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved anchor point