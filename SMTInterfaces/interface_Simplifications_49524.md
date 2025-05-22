# Simplifications (Collection)

**_Interface to compute Simplifications._**

## Methods

### Func **ComputeSimplification**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes a simplification on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the simplification.
` iAccuracy`      Accuracy for simplification.
**Returns:**      SimplificationDocument: Document containing the result.  
### Func **ComputeSimplificationWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  double  `iAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes a simplification on the selected products, according to a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the simplification.
` iReferenceProduct`      Product taken as a reference.
` iAccuracy`      Accuracy for simplification.
**Returns:**      SimplificationDocument: Document containing the result.  
### Func **SimplificationShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of the associated shape.