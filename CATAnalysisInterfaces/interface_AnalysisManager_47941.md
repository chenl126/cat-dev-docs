# AnalysisManager (Object)

**_Represents the root object inside an analysis document._**
It aggregates all the objects making up an analysis document.

## Properties

### Property **AnalysisModels**( ) As [CATIAAnalysisModels](../CATAnalysisInterfaces/interface_AnalysisModels_42446.md) (Read Only)

Returns the analysis model collection from the current analysis manager.

**Example:**     The following example returns from `RootAnalysis` the root analysis object of the active document, assumed to be an Analysis document, the collection of analysis models.

```VBScript
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
Dim analysisModels As AnalysisModels
Set analysisModels = RootAnalysis.AnalysisModels

```

### Property **AnalysisSets**( ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

Returns the analysis sets collection associated with an analysis manager. This collection allows to access the Analysis Connection Manager that aggregates the Analysis Connection features.

**Returns:**      a collection of CATIAAnalysisSets.  
### Property **LinkedDocuments**( ) As [CATIAAnalysisLinkedDocuments](../CATAnalysisInterfaces/interface_AnalysisLinkedDocuments_112927.md) (Read Only)

Returns the collection containing the documents linked to analysis document. All the CATIA documents that are linked to the different objects (like AnalysisMeshPart of Analysis Entity) might be accessed thru that collection.

**Example:**     The following example returns in `documents` the linked documents of the `AnalysisDocument` :

```VBScript
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
Dim Documents As AnalysisLinkedDocuments
Set Documents = RootAnalysis.LinkedDocuments

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection object containing the analysis parameters. All the parameters that are defined in analysis objects might be accessed thru that collection.

**Example:**     The following example returns in `params` the parameters of the `RootAnalysis` from the `AnalysisDocument` document:

```VBScript
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
Dim params As CATIAParameters
Set params = RootAnalysis.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

Returns the collection object containing the analysis relations. All the relations that are defined in analysis objects might be accessed thru that collection.

**Example:**     The following example returns in `relation` the relations of the `RootAnalysis` from the `AnalysisDocument` document:

```VBScript
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
Dim relation As CATIARelations
Set relation = RootAnalysis.Relations

```

Methods

### Func **CreateReferenceFromGeometry**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from a geometry. This geometry must in defined in a document rerecened in the CATIAAnalysisLinkedDocuments collection.

**Parameters:**

` iProduct`      The product of the geometry to be referenced that defines the instance of the geometry.
` iGeometry`      The geometry to be referenced. As a reference, it can be an CATIABoundary object of a mechanical feature.
**Returns:**      a reference of the couple (iProduct, iGeometry).  
### Func **CreateReferenceFromObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Creates a reference from an analysis object. Use of reference allows a uniform handling of anay objects.

**Parameters:**

` iObject`      The analysis object to be referenced. It can be an `AnalysisEntity` or an `AnalysisSet`
**Returns:**      The reference to the object.  
### Sub **Import**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToImport`)

Import an existing document in an analysis document . This document can of any type that implement the CATIADocument interface. This is implemented for internal document formats. (like Part or Product documents).

**Example:**     The following example imports an opened CATPart document

```VBScript
Dim AnalysisDocument As Document
Dim PartDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
RootAnalysis.Import(PartDocument)

```

### Sub **ImportDefineFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentPath`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeLate`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iValues`)

Import an existing document in an analysis document. This document can of any type that is managed by the CATISamImportDefine interface.

**Example:**     The following example imports an CATPart document stored as FileToOpen file. This example is also use the CATAnalysisImport Object. This object allow to import Part, Product or Analysis documents. As of today no parameters are mandatory for this object.

```VBScript
Dim arrayOfVariant(0)
FileToOpen = "e:\users\Parts\ThisIsANicePart.CATPart"
ObjectForImport = "CATAnalysisImport"
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
RootAnalysis.ImportDefineFile(FileToOpen,CATAnalysisImport,arrayOfVariant)

```

### Sub **ImportFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentPath`)

Import an existing document in an analysis document.

**Deprecated:**      V5R15 use ImportDefineFile instead. This document can of any type that implement the CATISamImportDefine interface.

**Example:**     The following example imports an CATPart document stored as FileToOpen file.

```VBScript
FileToOpen = "e:\users\Parts\ThisIsANicePart.CATPart"
Dim AnalysisDocument As Document
Set AnalysisDocument = CATIA.ActiveDocument
Dim RootAnalysis As AnalysisManager
Set RootAnalysis = AnalysisDocument.Analysis
RootAnalysis.ImportFile(FileToOpen)

```