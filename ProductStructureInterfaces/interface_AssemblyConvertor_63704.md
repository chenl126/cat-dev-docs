# AssemblyConvertor (Object)

**_Product conversion object._**
The AssemblyConvertor is the object that allows saving an assembly to a specified format. Two objects exist from now on : `BillOfMaterial`, which creates a bill of material (every sub-assembly is represented, with all the one level depth components), and `ListingReport`, which creates a listing report (shows the product structure as it appears in the graph)

## Methods

### Sub **Print**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFile`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Extracts the product's contents as a specified format. Saves it in a txt, html or xls file (depends of the object).

**Parameters:**

` iFileType`      Type of the resulting file : `TXT` (for text file), `HTML` (for html file), `XLS` (for xls file) or `MOTIF` (do not use).
` iFile`      Path of the resulting file
` iProduct`      Product that will be converted

### Sub **SetCurrentFormat**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ilistProps`)

Defines the properties that will be used in the print method.

**Parameters:**

` ilistProps`      list of properties to display

### Sub **SetSecondaryFormat**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ilistProps`)

Defines the secondary properties that will be used in the print method.

**Parameters:**

` ilistProps`      secondary list of properties to display
```