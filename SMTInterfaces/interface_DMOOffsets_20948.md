# DMOOffsets (Collection)

**_Interface to access a CATIADMOOffsets and compute Offsets_**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductToOffset`,  double  `iOffset1`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIADMOOffset](../SMTInterfaces/interface_DMOOffset_16659.md)

Creates a new Offset and adds it to the DMOOffsets collection. **This function is deprecated.**

**Returns:**      The created offset  **Example:**      The following example creates an offset `newOffset` in the Offset collection.

```VBScript
Set newOffset = DMOOffsets.Add

```

### Func **AddOffsetFromVectors**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductToOffset`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetVectors`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetValues`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIADMOOffset](../SMTInterfaces/interface_DMOOffset_16659.md)

Creates a new Offset from a set of vectors, and adds it to the DMOOffsets collection. **This function is deprecated.**

**Returns:**      The created offset  **Example:**      The following example creates an offset `newOffset` in the Offset collection.

```VBScript
Set newOffset = DMOOffsets.Add

```

### Sub **CleanUp**( )

Cleans up.  
### Func **ComputeAnOffset**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iOffset`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute a offset on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the offset.
` iOffset`      Offset value.
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      OffsetDocument: Document containing the result.  
### Func **ComputeAnOffsetFromVectors**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetVectors`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetValues`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute an offset on the selected products, according to some vectors

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the offset.
` iOffsetVectors`      Vectors taken into account for the computation
` iOffsetValues`      Offset values.
**Returns:**      OffsetDocument: Document containing the result.  
### Func **ComputeAnOffsetFromVectorsWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetVectors`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOffsetValues`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute an offset on the selected products, according to some vectors and a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the offset.
` iReferenceProduct`      The reference product.
` iOffsetVectors`      Vectors taken into account for the computation
` iOffsetValues`      Offset values.
**Returns:**      OffsetDocument: Document containing the result.  
### Func **ComputeAnOffsetWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  double  `iOffset`,  long  `iUseConstraints`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iConstraints`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Compute an offset on the selected products, according to a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the offset.
` iReferenceProduct`      The reference product.
` iOffset`      Offset value.
` iUseConstraints`      Do we use normals constraints or not ?
` iConstraints`      Constraints array.
**Returns:**      OffsetDocument: Document containing the result.  
### Func **OffsetShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of the associated shape.