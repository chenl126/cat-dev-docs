# AnalysisMeshLocalSpecifications (Collection)

**_The interface to access a AnalysisMeshLocalSpecifications._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisMeshLocalSpecification](../CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecification_188218.md)

Creates a new local specification and adds it to the local specification collection.
The local specification will be created linked to the AnalysisMeshManager object.

**Parameters:**

` iType`      The type of mesh part to create.
**Returns:**      The created local specification  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a local specification using its index or its name from the local specification collection.

**Parameters:**

` iIndex`      The index or the name of the local specification to retrieve from the collection of local specification . As a numeric, this index is the rank of the local specification in the collection. The index of the first local specification in the collection is 1, and the index of the last local specification is Count. As a string, it is the name you assigned to the local specification using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.