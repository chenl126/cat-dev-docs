# AnalysisSets (Collection)

**_The collection of analysis sets._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  [CATAnalysisSetType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.md)  `iSetType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

Creates a new analysis set and adds it to the analysis sets collection.
The analysis set will be aggregated on the Analysis Model

**Parameters:**

` iType`      The type of the set to create.
` iSetType`      The category of the set for update.
**Returns:**      The created Analysis Set  **Example:**      This example create `ThisAnalysisSet` in the `analysisSets`analysis
sets collection. The set to create is supposed to be a load set defined as an input of
the case for the update.

```VBScript
Dim ThisAnalysisSet As AnalysisSet
Set ThisAnalysisSet = analysisSets.Add("LoadSet", 0)

```

### Sub **AddExistingSet**( [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)  `iSet`,  [CATAnalysisSetType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.md)  `iSetType`)

Adds an existing analysis set to the analysis sets collection.

**Parameters:**

` iSet`      The Existing Analysis Set.
` iSetType`      The category of the set for update.
**Example:**      This example adds `ThisAnalysisSet` in the `analysisSets`analysis
sets collection. The set to add is supposed to be a restrain set defined as an input of
the case for the update.

```VBScript
Dim ThisAnalysisSet As AnalysisSet
...
analysisSets.AddExistingSet(ThisAnalysisSet, 0)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATAnalysisSetSearchType](../CATAnalysisInterfaces/enum_CATAnalysisSetSearchType_118426.md)  `iSerachType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

Returns an analysis set using its index or its name from the analysis sets collection.

**Parameters:**

` iIndex`      The index or the name of the analysis set to retrieve from the collection of analysis sets. As a numerics, this index is the rank of the analysis set in the collection. The index of the first analysis set in the collection is 1, and the index of the last analysis set is Count. As a string, it is the name you assigned to the analysis set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method. ` iSerachType`      The criterion of searching the set.
[CATAnalysisSetType.CATAnalysisSetSearchType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.htm#CATAnalysisSetSearchType) **Returns:**      The retrieved analysis set  **Example:**      This example retrieves in `ThisAnalysisSet` the third analysis set, and in `ThatAnalysisSet` the analysis set named `MySet` in the analysis set collection of an Analysis Case of analysis model.

```VBScript
Dim ThisAnalysisSet As AnalysisSet
Set ThisAnalysisSet = analysisCase.AnalysisSets.Item(3,1)
Dim ThatAnalysisSet As AnalysisSet
Set ThatAnalysisSet = analysisCase.AnalysisSets.Item("MySet")

```

### Func **ItemByType**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

Returns an analysis set using its type from the analysis sets collection.

**Parameters:**

` iType`      The type of the set required for the search
**Returns:**      The retrieved analysis set  **Example:**      This example retrieves in `ThisAnalysisSet` the "LoadSet" analysis set in the analysis set collection.

```VBScript
Dim ThisAnalysisSet As AnalysisSet
Set ThisAnalysisSet = analysisCase.AnalysisSets.ItemByType("LoadSet")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a set using its index or its name from the set collection.

**Parameters:**

` iIndex`      The index or the name of the set to retrieve from the collection of sets. As a numeric, this index is the rank of the set in the collection. The index of the first set in the collection is 1, and the index of the last set is Count. As a string, it is the name you assigned to the set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.