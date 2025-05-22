# DMUDataFlow (Object)

**_Allows the DMU Data Flow Management within the DMU Navigator environment._**

## Methods

### Sub **CacheExport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`,  long  `iData`)

Exports all documents related to the product in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.
` iData`      To save geometries.

  * 0: no save.
  * 1: save.

### Sub **CacheImport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`)

Imports in the cache of marked documents in a directory.

**Parameters:**

` iDirectory`      The directory that contains marked documents.

### Sub **Collapse**( )

Collapse the product by replacing all sub-product by corresponding components.  
### Sub **ReplaceByCGR**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`)

Replaces all components of the product by the corresponding CGR located in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.

### Sub **SaveAsFrozen**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`,  long  `iData`,  long  `iCache`)

Saves all documents related to the product in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.
` iData`      To save geometries.

  * 0: no save.
  * 1: save.

` iCache`      To cache data.

  * 0: no save.
  * 1: save.