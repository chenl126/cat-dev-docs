# VibrationVolumes (Collection)

**_Interface to compute vibration volumes_**

## Methods

### Sub **CleanUp**(| )

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