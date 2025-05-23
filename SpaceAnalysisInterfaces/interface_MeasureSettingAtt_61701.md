# MeasureSettingAtt (Object)

**_The interface to access a CATIAMeasureSettingAtt._**

## Properties

### Property **BoxDisplay**(| ) As boolean

   Returns or sets the BoxDisplay parameter .  Measure label background is filled if BoxDisplay is True ; there are only borders if BoxDisplay is False.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **LineWidth**( ) As short

   Returns or sets the LineWidth parameter.  The line width index, which ranges from 1 to 63.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PartUpdateStatus**( ) As boolean

   Returns or sets the PartUpdateStatus parameter .  Part is automatically updated if PartUpdateStatus is true.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ProductUpdateStatus**( ) As boolean

   Returns or sets the ProductUpdateStatus parameter .  Product is automatically updated if PartUpdateStatus is true.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **TildeDisplay**( ) As boolean

   Returns or sets the TildeDisplay parameter.  If TildeDisplay is TRUE, a tilde displayed for approximate measurement.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetBoxDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the BoxDisplay parameter.

**Role** :Retrieves the state of the BoxDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetLabelColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the LabelColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Func **GetLabelColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LabelColor parameter.

**Role** :Retrieves the state of the LabelColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLineWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LineWidth parameter.

**Role** :Retrieves the state of the LineWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPartUpdateStatusInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PartUpdateStatus parameter.

**Role** :Retrieves the state of the PartUpdateStatus parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetProductUpdateStatusInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ProductUpdateStatus parameter.

**Role** :Retrieves the state of the ProductUpdateStatus parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetTextColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the TextColor parameter .  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetTextColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TextColor parameter.

**Role** :Retrieves the state of the TextColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTildeDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TildeDisplay parameter.

**Role** :Retrieves the state of the TildeDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetBoxDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the BoxDisplay parameter.

**Role** :Locks or unlocks the BoxDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLabelColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the LabelColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Sub **SetLabelColorLock**( boolean  `iLocked`)

   Locks or unlocks the LabelColor parameter.

**Role** :Locks or unlocks the LabelColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLineWidthLock**( boolean  `iLocked`)

   Locks or unlocks the LineWidth parameter.

**Role** :Locks or unlocks the LineWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPartUpdateStatusLock**( boolean  `iLocked`)

   Locks or unlocks the PartUpdateStatus parameter.

**Role** :Locks or unlocks the PartUpdateStatus parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetProductUpdateStatusLock**( boolean  `iLocked`)

   Locks or unlocks the ProductUpdateStatus parameter.

**Role** :Locks or unlocks the Xxx parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTextColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the TextColor parameter .  Ensure consistency with the C++ interface to which the work is delegated.  
### Sub **SetTextColorLock**( boolean  `iLocked`)

   Locks or unlocks the TextColor parameter.

**Role** :Locks or unlocks the TextColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTildeDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the TildeDisplay parameter.

**Role** :Locks or unlocks the TildeDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.