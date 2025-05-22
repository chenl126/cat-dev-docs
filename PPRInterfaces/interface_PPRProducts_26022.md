# PPRProducts (Collection)

**_This interface is used to retrieve and add Products from and to the list of Products._**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Adds the specified Product to the current list of Products.

**Parameters:**

` iProduct`      The Product to be added.
**Returns:**      The added Product.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Retrieves the Product corresponding to the specified index in the list of Products.

**Parameters:**

` iIndex`      The index in the Product list.
**Returns:**      The retrieved Product corresponding to the specified index.