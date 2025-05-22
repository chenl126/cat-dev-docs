# Silhouettes (Collection)

**_Interface to compute Silhouettes._**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductToSilhouette`,  double  `iAccuracy`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAzimuts`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIASilhouette](../SMTInterfaces/interface_Silhouette_22578.md)

Creates a new Silhouette and adds it to the Silhouettes collection. **This function is deprecated.**

**Returns:**      The created Silhouette  **Example:**      The following example creates a Silhouette `newSilhouette` in the Silhouette collection.

```VBScript
Set newSilhouette = Silhouettes.Add

```

### Sub **CleanUp**( )

Performs some clean-up.  
### Func **ComputeASilhouette**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iViewPoints`,  double  `iAccuracy`,  double  `iAccuracyForSimplification`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes a silhouette on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the silhouette.
` iViewPoints`      Array containing the viewpoints (cameras) used to perform the silhouette.
` iAccuracy`      Grain value for the voxels.
` iAccuracyForSimplification`      Accuracy for simplification of the silhouette. Let it null for no simplification.
**Returns:**      SilhouetteDocument: Document containing the result.  
### Func **ComputeASilhouetteWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iViewPoints`,  double  `iAccuracy`,  double  `iAccuracyForSimplification`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes a silhouette on the selected products, according to a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      The selected products on which you want to perform the silhouette.
` iReferenceProduct`      Product taken as a reference.
` iViewPoints`      Array containing the viewpoints (cameras) used to perform the silhouette.
` iAccuracy`      Grain value for the voxels.
` iAccuracyForSimplification`      Accuracy for simplification of the silhouette. Let it null for no simplification.
**Returns:**      SilhouetteDocument: Document containing the result.  
### Func **SilhouetteShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the name of the associated shape.