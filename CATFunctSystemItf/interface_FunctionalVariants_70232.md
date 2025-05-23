# FunctionalVariants (Collection)

**_The interface to access a collection of FunctionalVariants._**

## Methods

### Func **Create**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`) As [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)

   Create a FunctionalVariant.  
### Sub **Delete**( [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)  `iVariant`)

   Delete a FunctionalVariant.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)

   Returns a Variant using its index or its name from the Variants collection.

**Parameters:**

` iIndex`      The index or the name of the Variant to retrieve from the collection of Variants. As a numerics, this index is the rank of the Variant in the collection. The index of the first Variant in the collection is 1, and the index of the last Variant is Count. As a string, it is the name you assigned to the Variant using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Variant **Example:**      This example retrieves in `Act1` the fifth Variant in the collection and in `Act2` the Variant named `Moves`.

```VBScript
     Dim Act1 As FunctionalVariant
     Set Act1 = Desc.Variant(5)
     Dim Act2 As FunctionalVariant
     Set Act2 = Desc.Variant("Adding new substance")

```