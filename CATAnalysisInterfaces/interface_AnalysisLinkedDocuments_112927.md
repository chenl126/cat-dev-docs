# AnalysisLinkedDocuments (Collection)

**_The collection of Documents linked by Analysis._**

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Returns a Document by its index or its name from the linked Documents collection.

**Parameters:**

` iIndex`      The index or the name of the linked Document to retrieve from the collection of linked Documents. As a numerics, this index is the rank of the linked Document in the collection. The index of the first linked Document in the collection is 1, and the index of the last linked Document is Count. As a string, it is the name you assigned to the collection by using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved linked Document