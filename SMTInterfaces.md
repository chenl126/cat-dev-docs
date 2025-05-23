# SMTInterfaces Framework

## Object Index

  * [DMOOffset](SMTInterfaces/interface_DMOOffset_16659.md)
  * [DMOOffsets](SMTInterfaces/interface_DMOOffsets_20948.md)
  * [DMOThickness](SMTInterfaces/interface_DMOThickness_30246.md)
  * [DMOThicknesses](SMTInterfaces/interface_DMOThicknesses_41444.md)
  * [FreeSpace](SMTInterfaces/interface_FreeSpace_16846.md)
  * [FreeSpaces](SMTInterfaces/interface_FreeSpaces_21174.md)
  * [Merges](SMTInterfaces/interface_Merges_8122.md)
  * [OptimizerWorkBench](SMTInterfaces/interface_OptimizerWorkBench_68592.md)
  * [PartComp](SMTInterfaces/interface_PartComp_13928.md)
  * [PartComps](SMTInterfaces/interface_PartComps_17839.md)
  * [Silhouette](SMTInterfaces/interface_Silhouette_22578.md)
  * [Silhouettes](SMTInterfaces/interface_Silhouettes_27435.md)
  * [Simplifications](SMTInterfaces/interface_Simplifications_49524.md)
  * [SweptVolume](SMTInterfaces/interface_SweptVolume_26919.md)
  * [SweptVolumes](SMTInterfaces/interface_SweptVolumes_32222.md)
  * [ThreeDCuts](SMTInterfaces/interface_ThreeDCuts_20970.md)
  * [VibrationVolumes](SMTInterfaces/interface_VibrationVolumes_56262.md)
  * [Wrapping](SMTInterfaces/interface_Wrapping_14396.md)
  * [Wrappings](SMTInterfaces/interface_Wrappings_18341.md)

---

# DMOOffset (Object)

**_Interface to access a CATIADMOOffset_**

---

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

---

# DMOThickness (Object)

**_Interface to access a CATIADMOThickness_**

---

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

---

# FreeSpace (Object)

**_Interface to access a CATIAFreeSpace_**

## Properties

### Property **Volume**( ) As double (Read Only)

   Returns the volume.  Methods

### Sub **GetGravityCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oGravityCenterCoordinatesArray`)

   Returns the gravity center.

---

# FreeSpaces (Collection)

**_Interface to compute Free Spaces._**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductForFreeSpace`,  double  `iAccuracy`,  double  `iXmin`,  double  `iXmax`,  double  `iYmin`,  double  `iYmax`,  double  `iZmin`,  double  `iZmax`,  long  `iTypeFreeSpace`,  double  `iXpt`,  double  `iYpt`,  double  `iZpt`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iHoles`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute a free space around a selected product.  
### Func **AddAroundAny**( double  `iAccuracy`,  double  `iXmin`,  double  `iXmax`,  double  `iYmin`,  double  `iYmax`,  double  `iZmin`,  double  `iZmax`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iTypeFreeSpace`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iHoles`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute a free space around any products.  
### Func **AddAroundProducts**( double  `iAccuracy`,  double  `iXmin`,  double  `iXmax`,  double  `iYmin`,  double  `iYmax`,  double  `iZmin`,  double  `iZmax`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iTypeFreeSpace`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iHoles`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferenceSelection`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute a free space around a reference selection  
### Func **AddFromFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute a free space from a file.  
### Func **AddInflatingFromFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute an inflating free space from a file.  
### Func **AddSplitFromFile**( double  `iX`,  double  `iY`,  double  `iZ`,  double  `iNx`,  double  `iNy`,  double  `iNz`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

   Compute a split free space from a file.

---

# Merges (Collection)

**_Interface to compute CATIAMerges_**

## Methods

### Sub **CleanUp**( )

   Performs some clean-up.  
### Func **ComputeMerge**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  double  `iAccuracyForSimplification`,  long  `iKeepEdges`,  long  `iDecoration`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes the merge on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iAccuracyForSimplification`      Set this to a non null value to have the simplification activated.
` iKeepEdges`      Do you want edges in the result?
` iDecoration`      Do you want decorations in the result?

**Returns:**      MergeDocument: Document containing the result.  
### Func **MergeShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the name of the associated shape.

---

# OptimizerWorkBench (Object)

**_Interface to access a CATIAOptimizerWorkBench_**

## Properties

### Property **FreeSpaces**( ) As [CATIAFreeSpaces](../SMTInterfaces/interface_FreeSpaces_21174.md) (Read Only)

   Returns FreeSpaces.  
### Property **Offsets**( ) As [CATIADMOOffsets](../SMTInterfaces/interface_DMOOffsets_20948.md) (Read Only)

   Returns Offsets.  
### Property **PartComps**( ) As [CATIAPartComps](../SMTInterfaces/interface_PartComps_17839.md) (Read Only)

   Returns PartComps.  
### Property **Silhouettes**( ) As [CATIASilhouettes](../SMTInterfaces/interface_Silhouettes_27435.md) (Read Only)

   Returns or sets the constraint driving mode. For constraint types supporting the concept of value, such as distance constraints, the driving mode tells whether the constraint value actually drives the geometry position, or, conversely, is driven by it.

**Example:**     The following example retrieves in `currentSilhouettes` the driving mode for the `distCst` distance constraint:

```VBScript
     currentSilhouettes = distCst.Silhouettes

```

### Property **SweptVolumes**( ) As [CATIASweptVolumes](../SMTInterfaces/interface_SweptVolumes_32222.md) (Read Only)

   Returns SweptVolumes.  
### Property **Thicknesses**( ) As [CATIADMOThicknesses](../SMTInterfaces/interface_DMOThicknesses_41444.md) (Read Only)

   Returns Thicknesses.  
### Property **Wrappings**( ) As [CATIADMOWrappings](../SMTInterfaces/interface_Wrappings_18341.md) (Read Only)

   Returns Wrappings.  Methods

### Func **Check**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iContext`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInstanceID`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLatestShape`) As long

   Check 1 component  
### Func **QueryNeighbours**( double  `iAccuracy`,  double  `iClearance`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferenceSelection`,  long  `iTypeQuery`) As long

   Compute the Neighbours

---

# PartComp (Object)

**_Interface to access a CATIAPartComp_**

---

# PartComps (Collection)

**_Interface to access a CATIAPartComps_**

## Properties

### Property **AddedMaterialPercentage**( ) As double (Read Only)

   Returns the added material percentage.  
### Property **AddedMaterialVolume**( ) As double (Read Only)

   Returns the added material volume.  
### Property **RemovedMaterialPercentage**( ) As double (Read Only)

   Returns the removed material percentage.  
### Property **RemovedMaterialVolume**( ) As double (Read Only)

   Returns the removed material volume.  Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct1`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct2`,  double  `iCompAccuracy`,  double  `iDispAccuracy`,  long  `iComputationType`) As [CATIAPartComp](../SMTInterfaces/interface_PartComp_13928.md)

   Computes a new comparison between products. Documents created are added to the documents in the session. Document containing the added material is called **AddedMaterial.3dmap**. Document containing the removed material is called **RemovedMaterial.3dmap**. Document containing the changed material is called **ChangedMaterial.3dmap**. If the document are meant to be kept they must be renamed, otherwise they should be deleted. Document lifecyle must be managed either with SaveAs or Close.

**Parameters:**

` iCompAccuracy`      Accuracy of the 3dmaps for the computation.
` iDispAccuracy`      Accuracy of the displayed 3dmaps.
` iComputationType`      0 : Added with position taken into account
1 : Removed with position
2 : Added + Removed with positions
3 : Added without position
4 : Removed without position
5 : Added + Removed without positions

**Returns:**      Created PartComp  **Example:**      The following example computes a comparison between two products:

```VBScript
     Dim newPartComp As PartComp
     Set newPartComp = PartComps.Add(product1, product2, 5.0, 5.0, 2)
     Dim documents1 As Documents
     Set documents1 = CATIA.Documents
     Dim document1 As Document
     Set document1 = documents1.Item("AddedMaterial.3dmap")

```

---

# Silhouette (Object)

**_Interface to access a CATIASilhouette._**

---

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

---

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

---

# SweptVolume (Object)

**_Interface to access a CATIASweptVolume_**

---

# SweptVolumes (Collection)

**_Interface to compute swept volumes._**

## Methods

### Func **Add**( [CATIAReplay](../SimulationInterfaces/interface_Replay_8252.md)  `replay`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIASweptVolume](../SMTInterfaces/interface_SweptVolume_26919.md)

   Creates a new SweptVolume and adds it to the SweptVolumes collection. **This function is deprecated.**

**Returns:**      The created SweptVolume  **Example:**      The following example creates a SweptVolume `newSweptVolume` in the SweptVolume collection.

```VBScript
     Set SweptVolume = SweptVolumes.Add

```

### Func **AddFromSweptAble**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iShapeName`,  long  `iActivatedShape`,  long  `iDefaultShape`) As [CATIASweptVolume](../SMTInterfaces/interface_SweptVolume_26919.md)

   Creates a new SweptVolume and adds it to the SweptVolumes collection. **This function is deprecated.**

**Returns:**      The created SweptVolume  
### Sub **CleanUp**( )

   Cleans up.  
### Func **ComputeASweptVolume**( [CATIAReplay](../SimulationInterfaces/interface_Replay_8252.md)  `iReplay`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a swept volume. **This function is deprecated.**

**Returns:**      The created SweptVolume  
### Func **ComputeASweptVolumeFromReplay**( [CATIAReplay](../SimulationInterfaces/interface_Replay_8252.md)  `iReplay`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a swept volume. **This function is deprecated.**

**Returns:**      The created SweptVolume  
### Func **ComputeASweptVolumeFromSweptable**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a swept volume. **This function is deprecated.**

**Returns:**      The created SweptVolume  
### Sub **ComputeSweptVolumes**( [CATIAReplay](../SimulationInterfaces/interface_Replay_8252.md)  `iReplay`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  long  `iPerformWrapping`,  long  `iPerformSimplif`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSweptVolumeDocuments`)

   Computes a swept volume, from a replay or a track.

**Parameters:**

` iReplay`      Replay on which we perfom the swept volume. Can be NULL.
` iSweptAble`      Track (or any other thing that implements CATISweptAble) on which we perfom the swept volume. Can be NULL.
` iProductsToSwept`      Selection of products to sweep.
` iProductReference`      Product taken as a reference.
` iLODMode`      Do we want levels of details or not?
` iAccuracy`      Filtering positions parameter.
` iPerformWrapping`      Do we perform a wrapping?
` iPerformSimplif`      Do we perform a simplification?
` iWrappingGrain`      Grain for wrapping.
` iWrappingRatio`      Offset ratio for wrapping.
` iSimplifAccuracy`      Accuracy for simplification.

**Returns:**      oSweptVolumeDocuments: Documents containing the results.  
### Sub **ComputeSweptVolumesFromReplay**( [CATIAReplay](../SimulationInterfaces/interface_Replay_8252.md)  `iReplay`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  long  `iPerformWrapping`,  long  `iPerformSimplif`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSweptVolumeDocuments`)

   Computes a swept volume from a replay.

**Parameters:**

` iReplay`      Replay on which we perfom the swept volume.
` iProductsToSwept`      Selection of products to sweep.
` iProductReference`      Product taken as a reference.
` iLODMode`      Do we want levels of details or not?
` iAccuracy`      Filtering positions parameter.
` iPerformWrapping`      Do we perform a wrapping?
` iPerformSimplif`      Do we perform a simplification?
` iWrappingGrain`      Grain for wrapping.
` iWrappingRatio`      Offset ratio for wrapping.
` iSimplifAccuracy`      Accuracy for simplification.

**Returns:**      oSweptVolumeDocuments: Documents containing the results.  
### Sub **ComputeSweptVolumesFromSweptable**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iProductsToSwept`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductReference`,  long  `iLODMode`,  double  `iAccuracy`,  long  `iPerformWrapping`,  long  `iPerformSimplif`,  double  `iWrappingGrain`,  double  `iWrappingRatio`,  double  `iSimplifAccuracy`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSweptVolumeDocuments`)

   Computes a swept volume from a track.

**Parameters:**

` iSweptAble`      Track (or any other thing that implements CATISweptAble) on which we perfom the swept volume.
` iProductsToSwept`      Selection of products to sweep.
` iProductReference`      Product taken as a reference.
` iLODMode`      Do we want levels of details or not?
` iAccuracy`      Filtering positions parameter.
` iPerformWrapping`      Do we perform a wrapping?
` iPerformSimplif`      Do we perform a simplification?
` iWrappingGrain`      Grain for wrapping.
` iWrappingRatio`      Offset ratio for wrapping.
` iSimplifAccuracy`      Accuracy for simplification.

**Returns:**      oSweptVolumeDocuments: Documents containing the results.  
### Sub **SetSilhouette**( long  `OnOff`)

   Adds the possibility to make a silhouette before the swept volume  
### Sub **SetSpatialSplit**( long  `OnOff`)

   Adds the possibility to parallelize swept&wrapping; after a spatial split. This gains in memory but not in CPU usage (takes longer.)

---

# ThreeDCuts (Collection)

**_Interface to compute 3D cuts_**

## Methods

### Sub **Compute3DCut**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `ThreeDCutDocument`)

   Computes the 3DCut on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.

**Returns:**      ThreeDCutDocument: Document containing the result.  
### Sub **Compute3DCutWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `ThreeDCutDocument`)

   Computes the 3DCut on the selected products, according to a reference product.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iReferenceProduct`      Product taken as a reference.

**Returns:**      ThreeDCutDocument: Document containing the result.  
### Func **GetCompute3DCut**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes the 3DCut on the selected products (better signature).

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.

**Returns:**      ThreeDCutDocument: Document containing the result.  
### Func **GetCompute3DCutWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes the 3DCut on the selected products, according to a reference product (better signature).

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iReferenceProduct`      Product taken as a reference.

**Returns:**      ThreeDCutDocument: Document containing the result.  
### Sub **SetBox**( double  `OriginX`,  double  `OriginY`,  double  `OriginZ`,  double  `VX`,  double  `VY`,  double  `VZ`)

   Sets the RELATIVE box used for the 3D cut computation.
Be aware of the behavior:

```VBScript
            Vz
           ^_________________
          /|               /|
         /                / |
        /  |             /  |
       /                /   |
      /----+-----------/    |
      |                |    |
      |    |       *   |    |
      |            O   |    |
      |    |           |    |
      |                |    |
      |    |           |    |
      |    * - - - - - + - -|> Vy
      |    Origin      |   /
      |  /             |  /
      |                | /
      |/               |/
      /----------------/
     <
      Vx

```

In the relative referential, O is (0,0,0)

This method sets the RELATIVE box : the rotation and translation matrix will then set the absolute position of O.
Remember where the center of the relative referential lies !
Can have unexpected results if you don't use it properly.

**Parameters:**

` OriginX`      Origin coordinate (X)
` OriginY`      Origin coordinate (Y)
` OriginZ`      Origin coordinate (Z)
` VX`      Length of the box (along X)
` VY`      Length of the box (along Y)
` VZ`      Length of the box (along Z)

### Sub **SetMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iComponents`)

   Sets the rotation AND translation matrix.
Beware : After a SetBox, the matrix is not changed.

**Parameters:**

` iComponents`      Components of the 4x4 matrix, placed in rows.

### Sub **SetOnBorders**( long  `OnBorders`)

   Sets the behavior on borders.

**Parameters:**

` Type`      0 : We keep partially included triangles
1 : We keep entirely included triangles

### Sub **SetType**( long  `Type`)

   Sets the type of cut we're doing.

**Parameters:**

` Type`      0 : We keep the inner triangles
1 : We keep the outer triangles

### Sub **ThreeDCutShapeName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `Name`)

   Returns the name of the associated shape.

---

# VibrationVolumes (Collection)

**_Interface to compute vibration volumes_**

## Methods

### Sub **CleanUp**( )

   Cleans up.  
### Func **ComputeVibrationVolume**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `PositionsFilePath`,  double  `iAccuracy`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a vibration volume, from a position input file.

**Parameters:**

` GroupOfSelectedProducts`      Selection of products to make vibrate.
` PositionsFilePath`      Positions file path.
` iAccuracy`      Grain for wrapping.
` iSimplifAccuracy`      Accuracy for simplification. A non positive value makes the simplification inactive.

**Returns:**      VibrationVolumeDocument: Document containing the result.  
### Func **ComputeVibrationVolumeFromTrack**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  double  `iAccuracy`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a vibration volume, from a track.

**Parameters:**

` GroupOfSelectedProducts`      Selection of products to make vibrate.
` iSweptAble`      Track containing the positions.
` iAccuracy`      Grain for wrapping.
` iSimplifAccuracy`      Accuracy for simplification. A non positive value makes the simplification inactive.

**Returns:**      VibrationVolumeDocument: Document containing the result.  
### Func **ComputeVibrationVolumeFromTrackWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iSweptAble`,  double  `iAccuracy`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a vibration volume, from a track, according to a reference product.

**Parameters:**

` GroupOfSelectedProducts`      Selection of products to make vibrate.
` iReferenceProduct`      Product taken as a reference.
` iSweptAble`      Track containing the positions.
` iAccuracy`      Grain for wrapping.
` iSimplifAccuracy`      Accuracy for simplification. A non positive value makes the simplification inactive.

**Returns:**      VibrationVolumeDocument: Document containing the result.  
### Func **ComputeVibrationVolumeWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `iGroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `PositionsFilePath`,  double  `iAccuracy`,  double  `iSimplifAccuracy`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Computes a vibration volume, from a position input file, according to a reference product.

**Parameters:**

` iGroupOfSelectedProducts`      Selection of products to make vibrate.
` iReferenceProduct`      Product taken as a reference.
` PositionsFilePath`      Positions file path.
` iAccuracy`      Grain for wrapping.
` iSimplifAccuracy`      Accuracy for simplification. A non positive value makes the simplification inactive.

**Returns:**      VibrationVolumeDocument: Document containing the result.  
### Func **VibrationVolumeShapeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the name of the associated shape.

---

# Wrapping (Object)

**_Interface to access a CATIADMOWrapping_**

---

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