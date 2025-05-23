# TreeTabSettingAtt (Object)

**__**

## Properties

### Property **ApplicativeDataFilter**(| ) As long

   Returns of sets the value to signify Whether "Applicative Data" created by an application is visible in the PPR tree

**Role** : Returns or sets the value of "Applicative Data" option to signify whether the applicative containers are visualized in the PPR tree  
### Property **AssignedViewer**( ) As long

   Returns or sets the value to signify whether the 3D Assigned Viewer is default viewer or not

**Role** : Returns or sets the value to signify whether 3D Assigned Viewer is default viewer or not  
### Property **AttributesFilter**( ) As long

   Returns or sets the value for "Attributes" option

**Role** : Returns or sets the value of "Attributes" option to signify whether the 'User Attributes' of an Activity is visualized in the PPR tree  
### Property **CollapseExpandFilter**( ) As long

   Returns or sets the value to signify Whether the double clicking on an activity expands/collapses a given activity in the PPR tree

**Role** : Returns or sets the value to signify Whether the double clicking on an activity expands/collapses a given activity in the PPR tree  
### Property **DisplayNameMode**( ) As long

   Returns or sets the value to signify whether the E5 Configured Name is to be displayed

**Role** : Returns or sets the value to signify whether the E5 Configured Name is to be displayed  
### Property **DisplayOrder**( ) As long

   Returns or sets the value for 'Display Order'

**Role** : Returns or sets the value of 'Display Order' to signify which order the product/resource list are in the PPR tree  
### Property **ItemsFilter**( ) As long

   Returns or sets the value for 'Items Folder'

**Role** : Returns or sets the value of 'Items Folder' to signify whether the 'Assigned Items' are visualized in the PPR tree  
### Property **ItemsPerRelationFilter**( ) As long

   Returns or sets the value for 'Items Folder (Per Relation Type)'

**Role** : Returns or sets the value of 'Items Folder(Per Relation Type)' to signify whether the 'Assigned Items'with proper relations ( like First Processes Product) are visualized in the PPR tree  
### Property **LogicalActFilter**( ) As long

   Returns or sets the value to signify Whether the logical activites are visible in the PPR tree

**Role** : Returns or sets the value of "Logical Activities" option to signify whether the logical activites are visible in the PPR tree  
### Property **OutputProductFilter**( ) As long

   Returns of sets the value to signify Whether "Output Products" assigned to a given activity is visible in the PPR tree

**Role** : Returns or sets the value of "Output Products Folder" option to signify whether the output products associated with an activity are visualized in the PPR tree  
### Property **RenderStyle**( ) As long

   Returns or sets the value to signify whether the 3D Render Style is Parallel or Perspective

**Role** : Returns or sets the value to signify whether the 3D Render Style is Parallel or Perspective  
### Property **ResourceFilter**( ) As long

   Returns or sets the value for 'Resources Folder'

**Role** : Returns or sets the value of 'Resources Folder' to signify whether the 'Assigned Resources' are visualized in the PPR tree  Methods

### Func **GetApplicativeDataFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Applicative Data" parameter.

**Role** :Retrieves the state of the "Applicative Data" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAssignedViewerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Assigned Viewer" parameter.

**Role** :Retrieves the state of the "Assigned Viewer" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttributesFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Attributes" parameter.

**Role** :Retrieves the state of the "Attributes" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCollapseExpandFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Disable Collapse/Expand" parameter.

**Role** :Retrieves the state of the "Disable Collapse/Expand" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayNameModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Display Name Mode" parameter.

**Role** :Retrieves the state of the "Display Name Mode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayOrderInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Display Order' parameter.

**Role** :Retrieves the state of the 'Display Order' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetItemsFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Items Folder' parameter.

**Role** :Retrieves the state of the 'Items Folder' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetItemsPerRelationFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Items Folder(Per Relation Type)' parameter.

**Role** :Retrieves the state of the 'Items Folder(Per Relation Type)' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLogicalActFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Logical Activities" parameter.

**Role** :Retrieves the state of the "Logical Activities" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputProductFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Output Products Folder" parameter.

**Role** :Retrieves the state of the "Output Products Folder" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRenderStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Render Style" parameter.

**Role** :Retrieves the state of the "Render Style" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Resource Folder' parameter.

**Role** :Retrieves the state of the 'Resource Folder' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetApplicativeDataFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Applicative Data" parameter.

**Role** :Locks or unlocks the "Attributes" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAssignedViewerLock**( boolean  `iLocked`)

   Locks or unlocks the "Assigned Viewer" parameter.

**Role** :Locks or unlocks the "Assigned Viewer" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttributesFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Attributes" parameter.

**Role** :Locks or unlocks the "Attributes" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCollapseExpandFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Disable Collapse/Expand" parameter.

**Role** :Locks or unlocks the "Disable Collapse/Expand" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayNameModeLock**( boolean  `iLocked`)

   Locks or unlocks the "Display Name Mode" parameter.

**Role** :Locks or unlocks the "Display Name Mode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayOrderLock**( boolean  `iLocked`)

   Locks or unlocks the 'Display Order' parameter.

**Role** :Locks or unlocks the 'Display Order' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetItemsFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Items Folder' parameter.

**Role** :Locks or unlocks the 'Items Folder' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetItemsPerRelationFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Items Folde(Per Relation Type)r' parameter.

**Role** :Locks or unlocks the 'Items Folder(Per Relation Type)' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLogicalActFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Logical Activities" parameter.

**Role** :Locks or unlocks the "Logical Activities" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputProductFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Output Products Folder" parameter.

**Role** :Locks or unlocks the "Output Products Folder" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRenderStyleLock**( boolean  `iLocked`)

   Locks or unlocks the "Render Style" parameter.

**Role** :Locks or unlocks the "Render Style" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Resource Folder' parameter.

**Role** :Locks or unlocks the 'Resource Folder' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.