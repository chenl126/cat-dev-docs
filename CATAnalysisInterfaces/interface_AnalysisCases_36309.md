# AnalysisCases (Collection)

**_The collection of analysis case making an Analysis._**

## Methods

### Func **Add**( ) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

Creates a new case and adds it to the case collection. This case will be plugged under the analysis model.

**Returns:**      The created case  **Example:**      The following example creates a case `NewCase` in the case collection of the `ModelAnalysis` Analysis model .

```VBScript
Dim ModelAnalysis As AnalysisModel
Dim NewCase As AnalysisCase
Set NewCase = ModelAnalysis.AnalysisCases.Add()

```

### Sub **AddExistingCase**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iCase`)

Adds an existing analysis case to the analysis cases collection.

**Parameters:**

` iCase`      The Existing Analysis Case.  **Example:**      This example adds `ThisAnalysisCase` in the `analysisCases` analysis cases collection.

```VBScript
Dim ThisAnalysisCase As AnalysisCase
Dim analysisCases As AnalysisCases
...
analysisCases.AddExistingCase(ThisAnalysisCase)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

Returns a case using its index or its name from the case collection.

**Parameters:**

` iIndex`      The index or the name of the case to retrieve from the collection of cases. As a numeric, this index is the rank of the case in the collection. The index of the first case in the collection is 1, and the index of the last case is Count. As a string, it is the name you assigned to the case using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved case. **Example:**      This example retrieves in ` ThisCase` the fifth case in the collection and in ` ThatCase` the case named `"MyCase` in the case collection of the `AnalysisModel` Analysis model.

```VBScript
Set CaseColl = AnalysisModel.AnalysisCases
Set ThisCase = CaseColl.Item(5)
Set ThatCase = CaseColl.Item("MyCase")

```

### Func **NewCase**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

Creates a new case and adds it to the case collection. This case will be plugged under the analysis model.

**Returns:**      The created case  **Example:**      The following example creates a case `NewCase` in the case collection of the `ModelAnalysis` Analysis model .

```VBScript
Dim ModelAnalysis As AnalysisModel
Dim NewCase As AnalysisCase
Set NewCase = ModelAnalysis.AnalysisCases.NewCase("AnalysisPreproCase")()

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a case using its index or its name from the case collection.

**Parameters:**

` iIndex`      The index or the name of the case to retrieve from the collection of cases. As a numeric, this index is the rank of the case in the collection. The index of the first case in the collection is 1, and the index of the last case is Count. As a string, it is the name you assigned to the case using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property. **Example:**      This example removes the fifth case in the collection.

```VBScript
AnalysisModel.AnalysisCases.Remove (5)

```