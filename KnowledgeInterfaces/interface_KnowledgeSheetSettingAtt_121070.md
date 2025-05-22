# KnowledgeSheetSettingAtt (Object)

**_The interface to access a CATIAKnowledgeSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Knowledge sheet.

## Properties

### Property **DesignTablesCopyData**( ) As short

Returns or sets the DesignTablesCopyData parameter.
**Role** :Return or Set the DesignTablesCopyData parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDesignTablesCopyData`      **Legal values** :
`0 :` default mode for design table : copy data into models
`1 :` default mode for design table : do not copy data into models.

### Property **DesignTablesSynchronization**( ) As short

Returns or sets the DesignTablesSynchronization parameter.
**Role** :Return or Set the DesignTablesSynchronization parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDesignTablesSynchronization`      **Legal values** :
`0 :` automatic synchronization at load for design table
`1 :` interactive synchronization at load for design table
`2 :` manual synchronization for design table.

### Property **ParameterNameSurroundedByTheSymbol**( ) As short

Returns or sets the ParameterNameSurroundedByTheSymbol parameter.
**Role** :Return or Set the ParameterNameSurroundedByTheSymbol parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterNameSurroundedByTheSymbol`      **Legal values** :
`0 :` to see parameter name not surrounded by the symbol "'"
`1 :` to see parameter name surrounded by the symbol "'".

### Property **ParameterTreeViewWithFormula**( ) As short

Returns or sets the ParameterTreeViewWithFormula parameter.
**Role** :Return or Set the ParameterTreeViewWithFormula parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterTreeViewWithFormula`      **Legal values** :
`0 :` to see parameter tree view without formula
`1 :` to see parameter tree view with formula.

### Property **ParameterTreeViewWithValue**( ) As short

Returns or sets the ParameterTreeViewWithValue parameter.
**Role** :Return or Set the ParameterTreeViewWithValue parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oParameterTreeViewWithValue`      **Legal values** :
`0 :` to see parameter tree view without value
`1 :` to see parameter tree view with value.

### Property **RelationsUpdateInPartContextEvaluateDuringUpdate**( ) As short

Returns or sets the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.
**Role** :Return or Set the RelationsUpdateInPartContextEvaluateDuringUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oRelationsUpdateInPartContextEvaluateDuringUpdate`      **Legal values** :
`0 :` creation of relations not evaluate during update
`1 :` creation of relations evaluate during update.

### Property **RelationsUpdateInPartContextSynchronousRelations**( ) As short

Returns or sets the RelationsUpdateInPartContextSynchronousRelations parameter.
**Role** :Return or Set the RelationsUpdateInPartContextSynchronousRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oRelationsUpdateInPartContextSynchronousRelations`      **Legal values** :
`0 :` creation of unsynchronous relations
`1 :` creation of synchronous relations.
Methods

### Func **GetDesignTablesCopyDataInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the DesignTablesCopyData parameter.
**Role** :Retrieves the state of the DesignTablesCopyData parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDesignTablesSynchronizationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the DesignTablesSynchronization parameter.
**Role** :Retrieves the state of the DesignTablesSynchronization parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterNameSurroundedByTheSymbolInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ParameterNameSurroundedByTheSymbol parameter.
**Role** :Retrieves the state of the ParameterNameSurroundedByTheSymbol parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterTreeViewWithFormulaInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ParameterTreeViewWithFormula parameter.
**Role** :Retrieves the state of the ParameterTreeViewWithFormula parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParameterTreeViewWithValueInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the ParameterTreeViewWithValue parameter.
**Role** :Retrieves the state of the ParameterTreeViewWithValue parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsUpdateInPartContextEvaluateDuringUpdateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.
**Role** :Retrieves the state of the RelationsUpdateInPartContextEvaluateDuringUpdate parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsUpdateInPartContextSynchronousRelationsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the RelationsUpdateInPartContextSynchronousRelations parameter.
**Role** :Retrieves the state of the RelationsUpdateInPartContextSynchronousRelations parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetDesignTablesCopyDataLock**( boolean  `iLocked`)

Locks or unlocks the DesignTablesCopyData parameter.
**Role** :Locks or unlocks the DesignTablesCopyData parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDesignTablesSynchronizationLock**( boolean  `iLocked`)

Locks or unlocks the DesignTablesSynchronization parameter.
**Role** :Locks or unlocks the DesignTablesSynchronization parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterNameSurroundedByTheSymbolLock**( boolean  `iLocked`)

Locks or unlocks the ParameterNameSurroundedByTheSymbol parameter.
**Role** :Locks or unlocks the ParameterNameSurroundedByTheSymbol parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterTreeViewWithFormulaLock**( boolean  `iLocked`)

Locks or unlocks the ParameterTreeViewWithFormula parameter.
**Role** :Locks or unlocks the ParameterTreeViewWithFormula parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParameterTreeViewWithValueLock**( boolean  `iLocked`)

Locks or unlocks the ParameterTreeViewWithValue parameter.
**Role** :Locks or unlocks the ParameterTreeViewWithValue parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsUpdateInPartContextEvaluateDuringUpdateLock**( boolean  `iLocked`)

Locks or unlocks the RelationsUpdateInPartContextEvaluateDuringUpdate parameter.
**Role** :Locks or unlocks the RelationsUpdateInPartContextEvaluateDuringUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsUpdateInPartContextSynchronousRelationsLock**( boolean  `iLocked`)

Locks or unlocks the RelationsUpdateInPartContextSynchronousRelations parameter.
**Role** :Locks or unlocks the RelationsUpdateInPartContextSynchronousRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.