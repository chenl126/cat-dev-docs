# AnalysisEntities (Collection)

**_The collection of analysis entities._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

Creates a new analysis entity and adds it to the analysis entities collection.
This collection may be extracted from an analysis set.The Analysis entity will be created on the Analysis Model.

**Parameters:**

` iType`      The type of the entity to create.
**Returns:**      The created analysis entity  **Example:**      This example create `ThisAnalysisEntity` in the `analysisEntities` collection
The entity to create is supposed to be a pressure defined in a load set.

```VBScript
Dim analysisEntities As CATIAAnalysisEntities
Dim ThisAnalysisEntity As AnalysisEntity
Set ThisAnalysisEntity = analysisEntities.Add("SAMPressure")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

Returns an analysis entity using its index or its name from the analysis entities collection.

**Parameters:**

` iIndex`      The index or the name of the analysis entity to retrieve from the collection of analysis entities. As a numerics, this index is the rank of the analysis entity in the collection. The index of the first analysis entity in the collection is 1, and the index of the last analysis entity is Count. As a string, it is the name you assigned to the analysis entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved analysis entity  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a entity using its index or its name from the entity collection.

**Parameters:**

` iIndex`      The index or the name of the entity to retrieve from the collection of entities. As a numeric, this index is the rank of the entity in the collection. The index of the first entity in the collection is 1, and the index of the last entity is Count. As a string, it is the name you assigned to the entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.