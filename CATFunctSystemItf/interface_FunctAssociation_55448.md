# FunctAssociation (Object)

**_The interface to access a Functional Association._**

It is managed on a Functional Element, thru the MultiRep Facet Manager (MRM).

## Properties

### Property **LinkedCount**( ) As long (Read Only)

Get count of linked objects.  Methods

### Sub **DetachFrom**( [CATIABase](../System/interface_AnyObject_17321.md)  `iLinked`)

Delete a link to a linked object.  
### Sub **LinkTo**( [CATIABase](../System/interface_AnyObject_17321.md)  `iLinked`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iKind`)

Create a link to another object.  
### Func **RetrieveKindOfLinked**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieve the kind of linked object.  
### Func **RetrieveLinked**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

Retrieve a linked object.