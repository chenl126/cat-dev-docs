# StepSettingAtt (Object)

**_The interface to access a CATIAStepSettingAtt._**

## Properties

### Property **AttAP**( ) As short

Returns or sets the AttAP parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttASM**( ) As short

Returns or sets the AttASM parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttASMGVP**( ) As short

Returns or sets the AttASMGVP parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttAngleDefFiting**( ) As float

Returns or sets the AttAngleDefFiting parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttAnnotation**( ) As short

Returns or sets the AttAnnotation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttFitting**( ) As short

Returns or sets the AttFitting parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVP**( ) As short

Returns or sets the AttGVP parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVPCOPS**( ) As short

Returns or sets the AttGVPCOPS parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVPCOPSSAG**( ) As double

Returns or sets the AttGVPCOPSSAG parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVPCOPSTol**( ) As double

Returns or sets the AttGVPCOPSSAG parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVPCdG**( ) As double

Returns or sets the AttGVPCdG parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGVPVA**( ) As double

Returns or sets the AttGVPVA parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttGroupMode**( ) As short

Returns or sets the AttGroupMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttHeaderAuthor**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the AttHeaderAuthor parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttHeaderAuthorisation**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the AttHeaderAuthorisation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttHeaderDescription**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the AttHeaderDescription parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttHeaderOrganisation**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the AttHeaderOrganisation parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttIASM**( ) As short

Returns or sets the AttIASM parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttLayersFilters**( ) As short

Returns or sets the AttLayersFilters parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttMultiCAD**( ) As short

Returns or sets the AttMultiCAD parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttOptimizeC2**( ) As short

Returns or sets the AttOptimizeC2 parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttReport**( ) As short

Returns or sets the AttReport parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttShow**( ) As short

Returns or sets the AttShow parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttTolDefOptFit**( ) As float

Returns or sets the AttTolDefOptFit parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **AttUnits**( ) As short

Returns or sets the AttUnits parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetAttAPInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttAP parameter.
**Role** :Retrieves the state of the AttAP parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttASMGVPInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttASMGVP parameter.
**Role** :Retrieves the state of the AttASMGVP parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttASMInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttASM parameter.
**Role** :Retrieves the state of the AttASM parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttAngleDefFitingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttAngleDefFiting parameter.
**Role** :Retrieves the state of the AttAngleDefFiting parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttAnnotationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttAnnotation parameter.
**Role** :Retrieves the state of the AttAnnotation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttFittingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttFitting parameter.
**Role** :Retrieves the state of the AttFitting parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPCOPSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVP parameter.
**Role** :Retrieves the state of the AttGVP parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPCOPSSAGInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVPVA parameter.
**Role** :Retrieves the state of the AttGVPVA parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPCOPSTolInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVPVA parameter.
**Role** :Retrieves the state of the AttGVPVA parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPCdGInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVPCdG parameter.
**Role** :Retrieves the state of the AttGVPCdG parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVP parameter.
**Role** :Retrieves the state of the AttGVP parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGVPVAInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGVPVA parameter.
**Role** :Retrieves the state of the AttGVPVA parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttGroupModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttGroupMode parameter.
**Role** :Retrieves the state of the AttGroupMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttHeaderAuthorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttHeaderAuthor parameter.
**Role** :Retrieves the state of the AttHeaderAuthor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttHeaderAuthorisationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttHeaderAuthorisation parameter.
**Role** :Retrieves the state of the AttHeaderAuthorisation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttHeaderDescriptionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttHeaderDescription parameter.
**Role** :Retrieves the state of the AttHeaderDescription parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttHeaderOrganisationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttHeaderOrganisation parameter.
**Role** :Retrieves the state of the AttHeaderOrganisation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttIASMInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttIASM parameter.
**Role** :Retrieves the state of the AttIASM parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttLayersFiltersInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttLayersFilters parameter.
**Role** :Retrieves the state of the AttLayersFilters parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttMultiCADInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttMultiCAD parameter.
**Role** :Retrieves the state of the AttMultiCAD parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttOptimizeC2Info**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttOptimizeC2 parameter.
**Role** :Retrieves the state of the AttOptimizeC2 parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttReportInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttReport parameter.
**Role** :Retrieves the state of the AttReport parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttShowInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttShow parameter.
**Role** :Retrieves the state of the AttShow parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttTolDefOptFitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttTolDefOptFit parameter.
**Role** :Retrieves the state of the AttTolDefOptFit parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttUnitsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the AttUnits parameter.
**Role** :Retrieves the state of the AttUnits parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAttAPLock**( boolean  `iLocked`)

Locks or unlocks the AttAP parameter.
**Role** :Locks or unlocks the AttAP parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttASMGVPLock**( boolean  `iLocked`)

Locks or unlocks the AttASMGVP parameter.
**Role** :Locks or unlocks the AttASMGVP parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttASMLock**( boolean  `iLocked`)

Locks or unlocks the AttASM parameter.
**Role** :Locks or unlocks the AttASM parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttAngleDefFitingLock**( boolean  `iLocked`)

Locks or unlocks the AttAngleDefFiting parameter.
**Role** :Locks or unlocks the AttAngleDefFiting parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttAnnotationLock**( boolean  `iLocked`)

Locks or unlocks the AttAnnotation parameter.
**Role** :Locks or unlocks the AttAnnotation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttFittingLock**( boolean  `iLocked`)

Locks or unlocks the AttFitting parameter.
**Role** :Locks or unlocks the AttFitting parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPCOPSLock**( boolean  `iLocked`)

Locks or unlocks the AttGVP parameter.
**Role** :Locks or unlocks the AttGVP parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPCOPSSAGLock**( boolean  `iLocked`)

Locks or unlocks the AttGVPVA parameter.
**Role** :Locks or unlocks the AttGVPVA parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPCOPSTolLock**( boolean  `iLocked`)

Locks or unlocks the AttGVPVA parameter.
**Role** :Locks or unlocks the AttGVPVA parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPCdGLock**( boolean  `iLocked`)

Locks or unlocks the AttGVPCdG parameter.
**Role** :Locks or unlocks the AttGVPCdG parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPLock**( boolean  `iLocked`)

Locks or unlocks the AttGVP parameter.
**Role** :Locks or unlocks the AttGVP parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGVPVALock**( boolean  `iLocked`)

Locks or unlocks the AttGVPVA parameter.
**Role** :Locks or unlocks the AttGVPVA parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttGroupModeLock**( boolean  `iLocked`)

Locks or unlocks the AttGroupMode parameter.
**Role** :Locks or unlocks the AttGroupMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttHeaderAuthorLock**( boolean  `iLocked`)

Locks or unlocks the AttHeaderAuthor parameter.
**Role** :Locks or unlocks the AttHeaderAuthor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttHeaderAuthorisationLock**( boolean  `iLocked`)

Locks or unlocks the AttHeaderAuthorisation parameter.
**Role** :Locks or unlocks the AttHeaderAuthorisation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttHeaderDescriptionLock**( boolean  `iLocked`)

Locks or unlocks the AttHeaderDescription parameter.
**Role** :Locks or unlocks the AttHeaderDescription parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttHeaderOrganisationLock**( boolean  `iLocked`)

Locks or unlocks the AttHeaderOrganisation parameter.
**Role** :Locks or unlocks the AttHeaderOrganisation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttIASMLock**( boolean  `iLocked`)

Locks or unlocks the AttIASM parameter.
**Role** :Locks or unlocks the AttIASM parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttLayersFiltersLock**( boolean  `iLocked`)

Locks or unlocks the AttLayersFilters parameter.
**Role** :Locks or unlocks the AttLayersFilters parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttMultiCADLock**( boolean  `iLocked`)

Locks or unlocks the AttMultiCAD parameter.
**Role** :Locks or unlocks the AttMultiCAD parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttOptimizeC2Lock**( boolean  `iLocked`)

Locks or unlocks the AttOptimizeC2 parameter.
**Role** :Locks or unlocks the AttOptimizeC2 parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttReportLock**( boolean  `iLocked`)

Locks or unlocks the AttReport parameter.
**Role** :Locks or unlocks the AttReport parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttShowLock**( boolean  `iLocked`)

Locks or unlocks the AttShow parameter.
**Role** :Locks or unlocks the AttShow parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttTolDefOptFitLock**( boolean  `iLocked`)

Locks or unlocks the AttTolDefOptFit parameter.
**Role** :Locks or unlocks the AttTolDefOptFit parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttUnitsLock**( boolean  `iLocked`)

Locks or unlocks the AttUnits parameter.
**Role** :Locks or unlocks the AttUnits parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.