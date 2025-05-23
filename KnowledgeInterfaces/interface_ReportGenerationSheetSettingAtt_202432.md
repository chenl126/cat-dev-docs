# ReportGenerationSheetSettingAtt (Object)

**_The interface to access a CATIAReportGenerationSheetSettingAtt._**

## Properties

### Property **AllChecksReport**(| ) As short

   Returns or sets the AllChecksReport parameter.

**Role** :Return or Set the AllChecksReport parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oAllChecksReport`      **Legal values** :
`0 :` report of only failed checks
`1 :` report of all checks.

### Property **CheckReportHtml**( ) As short

   Returns or sets the CheckReportHtml parameter.

**Role** :Return or Set the CheckReportHtml parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oCheckReportHtml`      **Legal values** :
`0 :` to have check report in Xml
`1 :` to have check report in Html.

### Property **DirectoryForInputXsl**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the DirectoryForInputXsl parameter.

**Role** :Return or Set the DirectoryForInputXsl parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDirectoryForInputXsl`      Directory for the report file with Xml extension.

### Property **ReportCheckAdvisor**( ) As short

   Returns or sets the ReportCheckAdvisor parameter.

**Role** :Return or Set the ReportCheckAdvisor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportCheckAdvisor`      **Legal values** :
`0 :` not report of check Advisor
`1 :` report of check Advisor.

### Property **ReportCheckExpert**( ) As short

   Returns or sets the ReportCheckExpert parameter.

**Role** :Return or Set the ReportCheckExpert parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportCheckExpert`      **Legal values** :
`0 :` not report of check Advisor
`1 :` report of check Advisor.

### Property **ReportHtmlInCatiaSession**( ) As short

   Returns or sets the ReportHtmlInCatiaSession parameter.

**Role** :Return or Set the ReportHtmlInCatiaSession parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportHtmlInCatiaSession`      **Legal values** :
`0 :` report Html outside CATIA session
`1 :` report Html in CATIA session.

### Property **ReportObjectsInformation**( ) As short

   Returns or sets the ReportObjectsInformation parameter.

**Role** :Return or Set the ReportObjectsInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportObjectsInformation`      **Legal values** :
`0 :` not report objects information
`1 :` report objects information.

### Property **ReportOutputDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the ReportOutputDirectory parameter.

**Role** :Return or Set the ReportOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportOutputDirectory`      The output directory for report of checks expert and checks advisor.

### Property **ReportParametersInformation**( ) As short

   Returns or sets the ReportParametersInformation parameter.

**Role** :Return or Set the ReportParametersInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportParametersInformation`      **Legal values** :
`0 :` not check Advisor parameter information
`1 :` check Advisor parameter information.

### Property **ReportPassedObjects**( ) As short

   Returns or sets the ReportPassedObjects parameter.

**Role** :Return or Set the ReportPassedObjects parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oReportPassedObjects`      **Legal values** :
`0 :` not report passed objects
`1 :` report passed objects.
Methods

### Func **GetAllChecksReportInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AllChecksReport parameter.

**Role** :Retrieves the state of the AllChecksReport parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCheckReportHtmlInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CheckReportHtml parameter.

**Role** :Retrieves the state of the CheckReportHtml parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDirectoryForInputXslInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DirectoryForInputXsl parameter.

**Role** :Retrieves the state of the DirectoryForInputXsl parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportCheckAdvisorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportCheckAdvisor parameter.

**Role** :Retrieves the state of the ReportCheckAdvisor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportCheckExpertInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportCheckExpert parameter.

**Role** :Retrieves the state of the ReportCheckExpert parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportHtmlInCatiaSessionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportHtmlInCatiaSession parameter.

**Role** :Retrieves the state of the ReportHtmlInCatiaSession parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportObjectsInformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportObjectsInformation parameter.

**Role** :Retrieves the state of the ReportObjectsInformation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportOutputDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportOutputDirectory parameter.

**Role** :Retrieves the state of the ReportOutputDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportParametersInformationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportParametersInformation parameter.

**Role** :Retrieves the state of the ReportParametersInformation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReportPassedObjectsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ReportPassedObjects parameter.

**Role** :Retrieves the state of the ReportPassedObjects parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAllChecksReportLock**( boolean  `iLocked`)

   Locks or unlocks the AllChecksReport parameter.

**Role** :Locks or unlocks the AllChecksReport parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCheckReportHtmlLock**( boolean  `iLocked`)

   Locks or unlocks the CheckReportHtml parameter.

**Role** :Locks or unlocks the CheckReportHtml parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDirectoryForInputXslLock**( boolean  `iLocked`)

   Locks or unlocks the DirectoryForInputXsl parameter.

**Role** :Locks or unlocks the DirectoryForInputXsl parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportCheckAdvisorLock**( boolean  `iLocked`)

   Locks or unlocks the ReportCheckAdvisor parameter.

**Role** :Locks or unlocks the ReportCheckAdvisor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportCheckExpertLock**( boolean  `iLocked`)

   Locks or unlocks the ReportCheckExpert parameter.

**Role** :Locks or unlocks the ReportCheckExpert parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportHtmlInCatiaSessionLock**( boolean  `iLocked`)

   Locks or unlocks the ReportHtmlInCatiaSession parameter.

**Role** :Locks or unlocks the ReportHtmlInCatiaSession parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportObjectsInformationLock**( boolean  `iLocked`)

   Locks or unlocks the ReportObjectsInformation parameter.

**Role** :Locks or unlocks the ReportObjectsInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportOutputDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the ReportOutputDirectory parameter.

**Role** :Locks or unlocks the ReportOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportParametersInformationLock**( boolean  `iLocked`)

   Locks or unlocks the ReportParametersInformation parameter.

**Role** :Locks or unlocks the ReportParametersInformation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReportPassedObjectsLock**( boolean  `iLocked`)

   Locks or unlocks the ReportPassedObjects parameter.

**Role** :Locks or unlocks the ReportPassedObjects parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.