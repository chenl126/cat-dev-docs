# UnitsSheetSettingAtt (Object)

**_The interface to access a CATIAUnitsSheetSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option the settings values of Units sheet.

## Properties

### Property **DisplayTrailingZeros**(| ) As short

   Returns or sets the DisplayTrailingZeros parameter.

**Role** :Return or Set the DisplayTrailingZeros parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oDisplayTrailingZeros`      **Legal values** :
`0 :` to not display trailing zeros
`1 :` to display trailing zeros.

### Property **ExpNotationValuesGreater**( ) As double

   Returns or sets the ExpNotationValuesGreater parameter.

**Role** :Return or Set the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oExpNotationValuesGreater`      The minimum value for exponential notation values.

### Property **ExpNotationValuesLower**( ) As double

   Returns or sets the ExpNotationValuesLower parameter.

**Role** :Return or Set the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oExpNotationValuesLower`      The maximum value for exponential notation values.

### Property **ListOfMagnitudes**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) (Read Only)

   Returns or sets the ListOfMagnitudes parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ListOfMagnitudesSize**( ) As double (Read Only)

   Returns or sets the ListOfMagnitudesSize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SameDisplay**( ) As short

   Returns or sets the SameDisplay parameter.

**Role** :Return or Set the SameDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` oSameDisplay`      **Legal values** :
`0 :` to not display same display
`1 :` to display same display.
Methods

### Sub **CommitForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.CommitForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#CommitForUnits) 
### Sub **GetDecimalReadOnly**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  double  `oDecimalPlaceReadOnly`)

   Returns the number of decimals for ReadOnly number.  
### Sub **GetDecimalReadWrite**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  double  `oDecimalPlaceReadWrite`)

   Returns the number of decimals for ReadWrite number.  
### Func **GetDimensionsDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the DimensionsDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetDisplayTrailingZerosInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DisplayTrailingZeros parameter.

**Role** :Retrieves the state of the DisplayTrailingZeros parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpNotationValuesGreaterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ExpNotationValuesGreater parameter.

**Role** :Retrieves the state of the ExpNotationValuesGreater parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpNotationValuesLowerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ExpNotationValuesLower parameter.

**Role** :Retrieves the state of the ExpNotationValuesLower parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetListOfMagnitudesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ListOfMagnitudes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **GetMagnitudeValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oUnitName`,  double  `oDecimalPlaceReadWrite`,  double  `oDecimalPlaceReadOnly`)

   Returns the Magnitude parameters.  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetSameDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SameDisplay parameter.

**Role** :Retrieves the state of the SameDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **ResetToAdminValuesForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.ResetToAdminValuesForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#ResetToAdminValuesForUnits) 
### Sub **RollbackForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.RollbackForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#RollbackForUnits) 
### Sub **SaveRepositoryForUnits**( )

   Implements a function from an interface.

**See also:**      [UnitsSheetSettingAtt.SaveRepositoryForUnits](../KnowledgeInterfaces/interface_UnitsSheetSettingAtt_84938.htm#SaveRepositoryForUnits) 
### Sub **SetDimensionsDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the DimensionsDisplay setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetDisplayTrailingZerosLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the DisplayTrailingZeros parameter.

**Role** :Locks or unlocks the DisplayTrailingZeros parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpNotationValuesGreaterLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetSameDisplayLock. Locks or unlocks the ExpNotationValuesGreater parameter.

**Role** :Locks or unlocks the ExpNotationValuesGreater parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpNotationValuesLowerLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the ExpNotationValuesLower parameter.

**Role** :Locks or unlocks the ExpNotationValuesLower parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetListOfMagnitudesLock**( boolean  `iLocked`)

   Locks or unlocks the ListOfMagnitudes setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetMagnitudeValues**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMagnitudeName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iUnitName`,  double  `iDecimalPlaceReadWrite`,  double  `iDecimalPlaceReadOnly`)

   Sets the Magnitude parameters.  Ensure consistency with the C++ interface to which the work is delegated.  
### Sub **SetSameDisplayLock**( boolean  `iLocked`)

**Deprecated:**      V5R15. Use SetDimensionsDisplayLock. Locks or unlocks the SameDisplay parameter.

**Role** :Locks or unlocks the SameDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.