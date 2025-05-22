# ClashResult (Object)

**_Represents the ClashResult object._**
The ClashResult object is a set of conflicts resulting from a clash detection.

## Properties

### Property **Conflicts**( ) As [CATIAConflicts](../SpaceAnalysisInterfaces/interface_Conflicts_18103.md) (Read Only)

Returns the collection of computed Conflicts.

**Example:**      This example retrieves the conflicts of `NewClashResult` ClashResult.

```VBScript
   Dim NewConflicts As Conflicts
   Set NewConflicts = NewClashResult.Conflicts

```

Methods

### Sub **Export**( [CatClashExportType](../SpaceAnalysisInterfaces/enum_CatClashExportType_69048.md)  `iType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Exports the results in a XML file.

**Parameters:**

` iType`      The type of export.
` iPath`      The path of the file.
**Example:**      This example exports the results of `NewClashResult` ClashResult.

```VBScript
   Dim ThePath As String
   NewClashResult.Export CatClashExportTypeXMLResultOnly, "c:\tmp\sample.xml"

```