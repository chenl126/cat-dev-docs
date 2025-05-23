# AnalysisDocument (Object)

**_Represents the document object for analysis._**
This objects is used for all CAE applications to defines specifications and managed associated results.
The document for analysis data is typed as ".CATAnalysis".
When an analysis document object is created, an analysis manager is also created.
This analysis manager is the root object at the top of the structure of the Analysis document.

**See also:**      [Document](../InfInterfaces/interface_Document_14456.md)

## Properties

### Property **Analysis**(| ) As [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md) (Read Only)

   Returns the root analysis object from the current analysis document.

**Example:**     The following example returns in `RootAnalysis` the root analysis object of the active document, assumed to be an analysis document:

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis

```