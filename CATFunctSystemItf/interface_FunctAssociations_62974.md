# FunctAssociations (Collection)

**_The interface to access a set of Functional Associations._**

It is managed on a Functional Element, thru the MultiRep Facet Manager (MRM).

## Methods

### Func **Create**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`) As [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)

   Create a FunctAssociation.  
### Sub **Delete**( [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)  `iAssociation`)

   Delete a FunctAssociation.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)

   Returns an association using its index or its name from the associations collection.

**Parameters:**

` iIndex`      The index or the name of the association to retrieve from the collection of associations. As a numerics, this index is the rank of the association in the collection. The index of the first association in the collection is 1, and the index of the last association is Count. As a string, it is the name you assigned to the association using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved association **Example:**      This example retrieves in `Act1` the fifth association in the collection and in `Act2` the association named `Moves`.

```VBScript
     Dim FunctElem As FunctionalObject
     Set FunctElem = FunctDoc.CurrentDescription.Objects.Elem("Valve")
     Dim FacetMRM As FunctionalMultiRepMgr
     Set FacetMRM = FunctElem.GetFacetByName("MRM")
     Dim Assoc1 As FunctAssociation
     Set Assoc1 = FacetMRM.Associations.Elem(5)
     Dim Assoc2 As FunctAssociation
     Set Assoc2 = FacetMRM.Associations.Elem("Skeleton 2D")

```