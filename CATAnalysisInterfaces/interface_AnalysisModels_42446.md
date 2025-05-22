# AnalysisModels (Collection)

**_The collection of analysis models making an analysis document._**
As of today this collection is made of a single analysis model.

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisModel](../CATAnalysisInterfaces/interface_AnalysisModel_36283.md)

Returns an analysis model using its index or its name from the analysis model collection.

**Parameters:**

` iIndex`      The index or the name of the analysis model to retrieve from the collection of analysis model. As a numerics, this index is the rank of the analysis model in the collection. The index of the first analysis model in the collection is 1, and the index of the last analysis model is Count. As a string, it is the name you assigned to the analysis model using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved analysis model  **Example:**      The following example retrieves the first analysis model in the analysis model collection of the ` AnalysisManager` object.

```VBScript
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
Dim analysisModels As AnalysisModels
Set analysisModels = RootAnalysis.AnalysisModels
Dim analysisModel As AnalysisModel
Set AnalysisModel = analysisModel.Item(1)

```