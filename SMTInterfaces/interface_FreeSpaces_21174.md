# FreeSpaces (Collection)

**_Interface to compute Free Spaces._**

## Methods

### Func **Add**(| [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iProductForFreeSpace`,| | double | `iAccuracy`,| | double | `iXmin`,| | double | `iXmax`,| | double | `iYmin`,| | double | `iYmax`,| | double | `iZmin`,| | double | `iZmax`,| | long | `iTypeFreeSpace`,| | double | `iXpt`,| | double | `iYpt`,| | double | `iZpt`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iHoles`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iShapeName`,| | long | `iActivatedShape`,| | long | `iDefaultShape`) As [CATIAFreeSpace](../SMTInterfaces/interface_FreeSpace_16846.md)

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