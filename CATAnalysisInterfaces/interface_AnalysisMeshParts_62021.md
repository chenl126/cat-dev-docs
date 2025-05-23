# AnalysisMeshParts (Collection)

**_The collection of analysis meshparts._**

## Methods

### Func **Add**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iType`) As [CATIAAnalysisMeshPart](../CATAnalysisInterfaces/interface_AnalysisMeshPart_54516.md)

   Creates a new meshpart and adds it to the meshpart collection.
The meshpart will be created linked to the AnalysisMeshManager object.

**Parameters:**

` iType`      The type of mesh part to create.

**Returns:**      The created meshpart  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisMeshPart](../CATAnalysisInterfaces/interface_AnalysisMeshPart_54516.md)

   Returns a meshpart using its index or its name from the meshpart collection.

**Parameters:**

` iIndex`      The index or the name of the meshpart to retrieve from the collection of meshparts. As a numeric, this index is the rank of the meshpart in the collection. The index of the first meshpart in the collection is 1, and the index of the last meshpart is Count. As a string, it is the name you assigned to the meshpart using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved meshpart.

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a meshpart using its index or its name from the meshpart collection.

**Parameters:**

` iIndex`      The index or the name of the meshpart to retrieve from the collection of meshpart. As a numeric, this index is the rank of the meshpart in the collection. The index of the first meshpart in the collection is 1, and the index of the last meshpart is Count. As a string, it is the name you assigned to the meshpart using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.