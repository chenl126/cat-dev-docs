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