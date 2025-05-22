# Wrappings (Collection)

**_Interface to compute Wrappings_**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductToWrapping`,  double  `iAccuracy`,  double  `iRatio`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIADMOWrapping](../SMTInterfaces/interface_Wrapping_14396.md)

Compute a wrapping on the selected products. **This method is deprecated!**

**Parameters:**

` iProductToWrapping`      The selected products on which you want to perform a wrapping.
` iAccuracy`      The grain accuracy.
` iRatio`      The ratio.
` iShapeName`      The associated shape name.
` iActivatedShape`      Do we activate the shape ?
` iDefaultShape`      Do we activate the shape as default shape ?
**Returns:**      oWrapping: Document containing the result.  
### Sub **CleanUp**( )

Cleans up.  
### Func **ComputeAWrapping**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iAccuracy`,  double  `iRation`,  double  `iAccuracyForSimplification`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a wrapping on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform a wrapping.
` iAccuracy`      The grain accuracy.
` iRation`      The ratio.
` iAccuracyForSimplification`      The accuracy for the simplification. equals -1 if no simplification is to be performed.
**Returns:**      WrappingDocument: Document containing the result.  
### Func **ComputeAWrappingWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  double  `iAccuracy`,  double  `iRation`,  double  `iAccuracyForSimplification`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a wrapping on the selected products, according to a reference product.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform a wrapping.
` iReferenceProduct`      Product taken as a reference.
` iAccuracy`      The grain accuracy.
` iRation`      The ratio.
` iAccuracyForSimplification`      The accuracy for the simplification. equals -1 if no simplification is to be performed.
**Returns:**      WrappingDocument: Document containing the result.  
### Func **WrappingShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of the associated shape.