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