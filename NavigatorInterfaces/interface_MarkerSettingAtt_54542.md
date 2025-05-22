# MarkerSettingAtt (Object)

**_Interface to handle the Marker settings

The different settings are:

MarkerAutoUpdate
Update on product structure modifications and scenes activation._**

MarkerDefaultsColor

MarkerDefaultsWeight

MarkerDefaultsDashed

Marker2DAutoNaming

Marker3DAutoNaming

MarkerTextColor2D

MarkerTextWeight2D

MarkerTextDashed2D

MarkerTextDefaultsFont2D

MarkerTextDefaultsSize2D

MarkerTextColor3D

MarkerTextWeight3D

MarkerTextDashed3D

MarkerTextDefaultsFont3D

MarkerTextDefaultsSize3D

## Properties

### Property **Marker2DAutoNaming**( ) As boolean

Returns or sets the activation state for 2D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **Marker3DAutoNaming**( ) As boolean

Returns or sets the activation state for 3D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **MarkerDefaultsDashed**( ) As long

Returns or sets the default dashed value of an annotation (oValue the dashed value).  
### Property **MarkerDefaultsWeight**( ) As long

Returns or sets the default weight value of an annotation (oValue the weight value).  
### Property **MarkerTextDashed2D**( ) As long

Returns or sets the default dashed value of a 2D text annotation (oValue the dashed value).  
### Property **MarkerTextDashed3D**( ) As long

Returns or sets the default dashed value of a 3D text annotation (oValue the dashed value).  
### Property **MarkerTextDefaultsFont2D**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the default font of a 2D annotation (oValue the font name).  
### Property **MarkerTextDefaultsFont3D**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

Returns or sets the default font of a 3D annotation (oValue the font name).  
### Property **MarkerTextDefaultsSize2D**( ) As long

Returns or sets the default size value of a 2d annotation (oValue the size value)..  
### Property **MarkerTextDefaultsSize3D**( long  `iValue`)

Returns or sets the default size value of a 3d annotation (oValue the size value)..  
### Property **MarkerTextWeight2D**( ) As long

Returns or sets the default weight value of a 2D text annotation (oValue the weight value).  
### Property **MarkerTextWeight3D**( long  `iValue`)

Returns or sets the default weight value of a 3D text annotation (oValue the weight value).  Methods

### Func **GetMarker2DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the Marker2DAutoNaming parameter.
**Role** :Retrieves the state of the Marker2DAutoNaming parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker3DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the Marker3DAutoNaming parameter.
**Role** :Retrieves the state of the Marker3DAutoNaming parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerDefaultsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

Returns the default color of an annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsColor parameter.
**Role** :Retrieves the state of the MarkerDefaultsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsDashed parameter.
**Role** :Retrieves the state of the MarkerDefaultsDashed parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsWeight parameter.
**Role** :Retrieves the state of the MarkerDefaultsWeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor2D**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

Returns the default color of a 2D text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColor2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextColor2D parameter.
**Role** :Retrieves the state of the MarkerTextColor2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor3D**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

Returns the default color of a 3D text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColor3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextColor3D parameter.
**Role** :Retrieves the state of the MarkerTextColor3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashed2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextDashed2D parameter.
**Role** :Retrieves the state of the MarkerTextDashed2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashed3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextDashed3D parameter.
**Role** :Retrieves the state of the MarkerTextDashed3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsFont2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsFont2D parameter.
**Role** :Retrieves the state of the MarkerDefaultsFont2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsFont3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsFont3D parameter.
**Role** :Retrieves the state of the MarkerDefaultsFont3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsSize2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsSize2D parameter.
**Role** :Retrieves the state of the MarkerDefaultsSize2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsSize3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerDefaultsSize3D parameter.
**Role** :Retrieves the state of the MarkerDefaultsSize3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeight2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextWeight2D parameter.
**Role** :Retrieves the state of the MarkerTextWeight2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeight3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the MarkerTextWeight3D parameter.
**Role** :Retrieves the state of the MarkerTextWeight3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.
**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMarker2DAutoNamingLock**( boolean  `iLocked`)

Locks or unlocks the Marker2DAutoNaming parameter.
**Role** :Locks or unlocks the Marker2DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker3DAutoNamingLock**( boolean  `iLocked`)

Locks or unlocks the Marker3DAutoNaming parameter.
**Role** :Locks or unlocks the Marker3DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

Sets the default color of an annotation (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetMarkerDefaultsColorLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsColor parameter.
**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsDashedLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsDashed parameter.
**Role** :Locks or unlocks the MarkerDefaultsDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsWeightLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsWeight parameter.
**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor2D**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

Sets the default color of a 2D text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColor2DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextColor2D parameter.
**Role** :Locks or unlocks the MarkerTextColor2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor3D**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

Sets the default color of a 3D text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColor3DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextColor3D parameter.
**Role** :Locks or unlocks the MarkerTextColor3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashed2DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextDashed parameter.
**Role** :Locks or unlocks the MarkerTextDashed2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashed3DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextDashed3D parameter.
**Role** :Locks or unlocks the MarkerTextDashed3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsFont2DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsFont2D parameter.
**Role** :Locks or unlocks the MarkerDefaultsFont2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsFont3DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsFont3D parameter.
**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsSize2DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsSize2D parameter.
**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsSize3DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerDefaultsSize3D parameter.
**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeight2DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextWeight2D parameter.
**Role** :Locks or unlocks the MarkerTextWeight2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeight3DLock**( boolean  `iLocked`)

Locks or unlocks the MarkerTextWeight3D parameter.
**Role** :Locks or unlocks the MarkerTextWeight3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.