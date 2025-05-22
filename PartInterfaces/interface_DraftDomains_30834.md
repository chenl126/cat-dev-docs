# DraftDomains (Collection)

**_The collection of draft domains used by the draft shape._**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADraftDomain](../PartInterfaces/interface_DraftDomain_25597.md)

Returns a draft domain using its index or its name from the DraftDomains collection.

**Parameters:**

` iIndex`      The index or the name of the draft domain to retrieve from the collection of draft domains. As a numerics, this index is the rank of the draft domain in the collection. The index of the first draft domain in the collection is 1, and the index of the last draft domain is Count. As a string, it is the name you assigned to the draft domain using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved draft domain

**Example:**     The following example returns in `domain` the third draft domain of the `firstDraftDomains` collection:

```VBScript
Set domain = firstDraftDomains.Item(3)

```