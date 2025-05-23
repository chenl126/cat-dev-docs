# AnalysisPostManager (Object)

**_Interface to define the Post Processing Manager._**

**Role** : In the analysis document, an Post Processing is dedicated to Visualization and reporting.

## Methods

### Sub **AddExistingCaseForReport**(| [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md) | `iCase`)

   Adds an existing analysis case to manager. To declare Case which will be taken into account for the HTML report.

**Parameters:**

` iCase`      The Existing Analysis Case.

### Sub **BuildReport**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTitle`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iAddCreatedImages`)

   Extract the HTML Report. The Report is defined related to Analysis cases, using AddExistingCaseForReport and will be stored in a CATIA Folder.

**Parameters:**

` iFolder`      Folder to store the HTML file.
` iTitle`      Title of the report.
` iAddCreatedImages`      To add created images under analysis case in the report.

### Sub **ExtractHTMLReport**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTitle`)

**Deprecated:**      V5R14 use BuildReport instead. Extract the HTML Report. The Report is defined related to Analysis cases, using AddExistingCaseForReport and will be stored in a CATIA Folder.  **Parameters:**

` iFolder`      Folder to store the HTML file.
` iTitle`      Title of the report.