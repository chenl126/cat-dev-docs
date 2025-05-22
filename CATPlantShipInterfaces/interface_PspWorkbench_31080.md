# PspWorkbench (Object)

**_Represents the PspWorkbench._**
**Role** : To manage application and Psp interface handlers. From this object all the queries for lists of Distributive system (PSP) objects can be made. Furthermore, all the interface handles can be obtained through this interface.

## Methods

### Sub **ExportProperties**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToExportFrom`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iXMLOutputFileName`)

This method extracts property values of the current document to an output XML file. The format is determined by CATIA PlantShip XML-DTD file.

**Parameters:**

` iDocumentToExportFrom`      Documennt to export from
` iXMLOutputFileName`      The file name to output the data to.
**Example:**

```VBScript
Dim objPspWorkbench As PspWorkbench
Dim objCATIAV5CurDocument As Document
Dim iXMLOutputFileName As String
Set objCATIAV5CurDocument = CATIA.ActiveDocument
Set objProductRoot = objCATIAV5CurDocument.Product
Set objPspWorkbench = objProductRoot.GetTechnologicalObject ("PspWorkbench")
..
objThisIntf.ExportProperties objCATIAV5CurDocument, iXMLOutputFileName

```

### Func **GetApplication**( [CatPspIDLApplicationID](../CATPlantShipInterfaces/enum_CatPspIDLApplicationID_94374.md)  `iApplicationID`) As [CATIAPspApplication](../CATPlantShipInterfaces/interface_PspApplication_42486.md)

Returns the PspApplication associated with the input ApplicationID.

**Parameters:**

` CatPspIDLApplicationID`      Application ID to get.
` oApplication`      PspApplication handle found.
**Example:**

```VBScript
Dim objPspWorkbench As PspWorkbench
Dim objArg1 As CatPspIDLApplicationID
Dim objArg2 As PspApplication
objArg1 = catPspIDLCATPiping
Set objArg2 = objPspWorkbench.GetApplication (objArg1)

```

### Func **GetInterface**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIABase](../System/interface_AnyObject_17321.md)

Returns specific interface handle on a given object.

**Parameters:**

` iInterfaceName`      interface name to search for ("CATIAxxxx")
` iObject`      The object to search for the required interface.
**Returns:**      Interface handle found  **Example:**      This example illustrates how to get a specific interface handle from a given object.

```VBScript
Dim objPspWorkbench As PspWorkbench
Dim objPspApplication As PspApplication
Dim objPspAppFactory As PspAppFactory
Dim objProductRoot As Product
Set objProductRoot = CATIA.ActiveDocument.Product
Set objPspWorkbench = objProductRoot.GetTechnologicalObject ("PspWorkbench")
Set objPspPipApplication = objPspWorkbench.GetApplication(catPspIDLCATPiping)

Set objPspPipAppFactory = objPspWorkbench.GetInterface ("CATIAPspAppFactory",objPspPipApplication)

```