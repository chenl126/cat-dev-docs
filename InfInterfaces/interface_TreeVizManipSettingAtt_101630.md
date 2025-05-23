# TreeVizManipSettingAtt (Object)

**_The Interface to retrieve and set the visual information on the specification tree._**

## Properties

### Property **ArcSelectionActivation**(| ) As boolean

   Retrieves or Sets the arc-selection mode applied to the specification tree.  
### Property **AutoExpandActivation**( ) As boolean

   Retrieves or Sets the automatic expand mode applied to the specification tree.  
### Property **AutoScrollActivation**( ) As boolean

   Retrieves or Sets the automatic scrolling mode applied to the specification tree.  
### Property **DisplayGeomOnScrolling**( ) As boolean

   Retrieves or Sets the "display geometry on scrolling" mode.  
### Property **Orientation**( ) As [CatTreeOrientationEnum](../InfInterfaces/enum_CatTreeOrientationEnum_102450.md)

   Retrieves or Sets the orientation applied to the specification tree.  
### Property **ShowActivation**( ) As boolean

   Retrieves or Sets the visualization Show/NoShow's mode applied to the specification tree.  
### Property **Size**( ) As long

   Retrieves or Sets the number of characters shown for the text of the specification tree.  
### Property **SizeType**( ) As [CatTreeSizeTypeEnum](../InfInterfaces/enum_CatTreeSizeTypeEnum_75532.md)

   Retrieves or Sets the type of size applied to the text of the specification tree.  
### Property **Type**( ) As [CatTreeTypeEnum](../InfInterfaces/enum_CatTreeTypeEnum_47247.md)

   Retrieves or Sets the type applied to the specification tree.  Methods

### Func **GetArcSelectionActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for arc-selection mode applied to the specification tree.

**Role** :Retrieves the state of arc-selection mode applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAutoExpandActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for automatic expand mode applied to the specification tree.

**Role** :Retrieves the state of automatic expand mode applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAutoScrollActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for automatic scrolling mode applied to the specification tree.

**Role** :Retrieves the state of the automatic scrolling mode applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayGeomOnScrollingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for "display geometry on scrolling" mode.

**Role** :Retrieves the state of "display geometry on scrolling" mode in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOrientationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the orientation applied to the specification tree.

**Role** :Retrieves the state of the orientation applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowActivationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the visualization Show/NoShow's mode applied to the specification tree.

**Role** :Retrieves the state of the visualization Show/NoShow's mode applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSizeTypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the type of size applied to the text of the specification tree.

**Role** :Retrieves the state of the type of size applied to the text of the specification tree in the current environment. Attributes "size" and "SizeType" are linked together by the same lock. So there is no function "GetSizeInfo".

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTypeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the type applied to the specification tree.

**Role** :Retrieves the state of the type applied to the specification tree in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetArcSelectionActivationLock**( boolean  `iLocked`)

   Locks or unlocks the arc-selection mode applied to the specification tree.

**Role** :Locks or unlocks the arc-selection mode applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAutoExpandActivationLock**( boolean  `iLocked`)

   Locks or unlocks the automatic expand mode applied to the specification tree.

**Role** :Locks or unlocks the automatic expand mode applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAutoScrollActivationLock**( boolean  `iLocked`)

   Locks or unlocks the automatic scrolling mode applied to the specification tree.

**Role** :Locks or unlocks the automatic scrolling mode applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayGeomOnScrollingLock**( boolean  `iLocked`)

   Locks or unlocks the "display geometry on scrolling" mode.

**Role** :Locks or unlocks "display geometry on scrolling" mode if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOrientationLock**( boolean  `iLocked`)

   Locks or unlocks the orientation applied to the specification tree.

**Role** :Locks or unlocks the orientation applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetShowActivationLock**( boolean  `iLocked`)

   Locks or unlocks the visualization Show/NoShow's mode applied to the specification tree.

**Role** :Locks or unlocks the visualization Show/NoShow's mode applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSizeTypeLock**( boolean  `iLocked`)

   Locks or unlocks the type of size applied to the text of the specification tree.

**Role** :Locks or unlocks the type of size applied to the text of the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL. Attributs "size" and "SizeType" are linked together by the same lock. So there is no function "SetSizeTypeLock".

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTypeLock**( boolean  `iLocked`)

   Locks or unlocks the type of the specification tree.

**Role** :Locks or unlocks the type applied to the specification tree if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.