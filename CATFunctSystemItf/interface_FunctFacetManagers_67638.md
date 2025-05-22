# FunctFacetManagers (Collection)

**_Represents the Functional Facet's Managers._**

## Methods

### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)

Returns a facet manager using its index or its name from the facet managers collection.

**Parameters:**

` iIndex`      The index or the name of the facet manager to retrieve from the collection of facet managers. As a numerics, this index is the rank of the facet manager in the collection. The index of the first facet manager in the collection is 1, and the index of the last facet manager is Count. As a string, it is the name you assigned to the facet manager using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth facet manager in the collection and in `Obj2` the facet manager named `IMC`.

```VBScript
Dim Obj1 As FunctFacetManager
Set Obj1 = Desc.FacetManagers.Elem(5)
Dim Obj2 As FunctFacetManager
Set Obj2 = Desc.FacetManagers.Elem("IMC")

```