# AnalysisImage (Object)

**_Represents the analysis image object._**

## Properties

### Property **AnalysisImages**(| ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

   Returns the analysis images collection associated with an analysis image.  Methods

### Sub **ExportData**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportDataWithMeshPartId

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

### Sub **ExportDataInGlobalAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataInManualAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iXDirection`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iYDirection`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iZDirection`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iOrigin`      Origin of Location axis system
` iXDirection`      co-ordinates of a point on X- axis of Location axis system
` iYDirection`      co-ordinates of a point on Y- axis of Location axis system
` iZDirection`      co-ordinates of a point on Z- axis of Location axis system
` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataInUserAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)  `iAxisSystem`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportDataWithMeshPartId

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iAxisSystem`      Reference to the axis system to be used for location transformation.
` iProduct`      Reference to the product, where the above axis system is defined.
` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataWithMeshPartId**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`)

   Extracts image results and location with mesh part name (as identifier).
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportData

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

### Sub **ResetSelection**( )

   Resets all selections in an image.
This is done related to an existing image  
### Sub **SetActivationStatus**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iActivationStatus`)

   Activates oe deactivates an image.
This is done related to an existing image

**Parameters:**

` iActivationStatus`      To activate or not the current image.

### Sub **SetCurrentOccurrence**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iOccurrenceNumber`)

   Sets occurrence number for an image.
This is done related to an existing image

**Parameters:**

` iOccurrenceNumber`      The number to select

**Legal value** : 1 ≤ iOccurrenceNumber ≤ nbOccurrence

### Sub **SetSelection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iReplaceMode`)

   Adds a selection to an image.
This is done related to an existing image

**Parameters:**

` iReference`      The selectionGroup to add
` iReplaceMode`      To replace or not the current selections.

### Sub **Update**( )

   Updates an image.
This is done related to an existing image