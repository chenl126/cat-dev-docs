# DMOThicknesses (Collection)

**_Interface to access a CATIADMOThicknesses and compute Thicknesses_**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductToThickness`,  double  `iThickness1`,  double  `iThickness2`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIADMOThickness](../SMTInterfaces/interface_DMOThickness_30246.md)

Creates a new Silhouette and adds it to the DMOThicknesses collection. **This function is deprecated.** 
### Func **ComputeAThickness**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iThickness1`,  double  `iThickness2`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a thickness on the selected products. **This method is deprecated.**

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the thickness.
` iThickness1`      First thickness value.
` iThickness2`      Second thickness value. **Old way**
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      ThicknessDocument: Document containing the result.  
### Func **ComputeAThicknessWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  double  `iThickness1`,  double  `iThickness2`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a thickness on the selected products, according to a reference product. **This method is deprecated.**

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the thickness.
` iReferenceProduct`      The reference product.
` iThickness1`      First thickness value.
` iThickness2`      Second thickness value. **Old way**
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      ThicknessDocument: Document containing the result.  
### Func **ComputeThickness**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iThickness1`,  double  `iThickness2`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a thickness on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the thickness.
` iThickness1`      First thickness value.
` iThickness2`      Second thickness value.
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      ThicknessDocument: Document containing the result.  
### Func **ComputeThicknessWithReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  double  `iThickness1`,  double  `iThickness2`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a thickness on the selected products, according to a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the thickness.
` iReferenceProduct`      The reference product.
` iThickness1`      First thickness value.
` iThickness2`      Second thickness value.
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      ThicknessDocument: Document containing the result.  
### Func **ThicknessShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of the associated shape.