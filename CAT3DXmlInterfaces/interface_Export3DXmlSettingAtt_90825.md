# Export3DXmlSettingAtt (Object)

**_Represents a setting controller for the 3D XML export settings._**
**Role** : This interface is implemented by a component which represents the controller of the 3D XML export settings.

## Properties

### Property **AlternateView**( ) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.get_DesignReview](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#get_DesignReview) Returns or sets the alternate view activation flag.

**Example:**      This example activates the alternate view export.

```VBScript

 export3DXmlSettingAtt.AlternateView = True

```

### Property **Animation**( ) As boolean

Returns or sets the animation activation flag.

**Example:**      This example activates the animation export.

```VBScript

 export3DXmlSettingAtt.Animation = True

```

### Property **AnnotatedView**( ) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.get_DesignReview](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#get_DesignReview) Returns or sets the annotated view activation flag.

**Example:**      This example activates the annotated view export.

```VBScript

 export3DXmlSettingAtt.AnnotatedView = True

```

### Property **Annotation3D**( ) As boolean

Returns or sets the 3D annotation activation flag.

**Example:**      This example activates the 3D annotation export.

```VBScript

 export3DXmlSettingAtt.Annotation3D = True

```

### Property **DesignReview**( ) As boolean

Returns or sets the Design Review activation flag.

**Example:**      This example activates the Design Review export.

```VBScript

 export3DXmlSettingAtt.DesignReview = True

```

### Property **GeometryRepresentationFormat**( ) As [Cat3DXmlGeomRepresentationType](../CAT3DXmlInterfaces/enum_Cat3DXmlGeomRepresentationType_187556.md)

Returns or sets the format of geometry representation.

**Example:**      This example sets the representation format to the exact mode.

```VBScript

 export3DXmlSettingAtt.GeometryRepresentationFormat = cat3DXmlExact

```

### Property **Measure**( ) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.get_DesignReview](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#get_DesignReview) Returns or sets the measure activation flag.

**Example:**      This example activates the measure export.

```VBScript

 export3DXmlSettingAtt.Measure = True

```

### Property **PPRSaveConfig**( ) As [Cat3DXmlPPRSaveConfig](../CAT3DXmlInterfaces/enum_Cat3DXmlPPRSaveConfig_85391.md)

Returns or sets the PPR config.

**Example:**      This example sets the PPR config. Product And resources export is acivated.

```VBScript

 export3DXmlSettingAtt.PPRSaveConfig = cat3DXmlProductAndResourceList

```

### Property **Presentation**( ) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.get_DesignReview](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#get_DesignReview) Returns or sets the presentation activation flag.

**Example:**      This example activates the presentation export.

```VBScript

 export3DXmlSettingAtt.Presentation = True

```

### Property **Section**( ) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.get_DesignReview](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#get_DesignReview) Returns or sets the section activation flag.

**Example:**      This example activates the section export.

```VBScript

 export3DXmlSettingAtt.Section = True

```

### Property **SurfaceAccuracy**( ) As float

Returns or sets the surface accuracy.

**Example:**      This example sets the surface accuracy used by the exact mode.

```VBScript

 export3DXmlSettingAtt.SurfaceAccuracy = 0.01

```

### Property **WorkInstructions**( ) As boolean

Returns or sets the Work Instructions activation flag.

**Example:**      This example activates the Work Instructions export.

```VBScript

 export3DXmlSettingAtt.DesignReview = True

```

Methods

### Func **GetAlternateViewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.GetDesignReviewInfo](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#GetDesignReviewInfo) Retrieves environment informations for the alternate view setting.
**Role** :Retrieves the state of the alternate view setting in the current environment.  **Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnimationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the animation setting.
**Role** :Retrieves the state of the animation setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnnotatedViewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.GetDesignReviewInfo](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#GetDesignReviewInfo) Retrieves environment informations for the annotated view setting.
**Role** :Retrieves the state of the annotated view setting in the current environment.  **Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnnotation3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the 3D annotation setting.
**Role** :Retrieves the state of the 3D annotation setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDesignReviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the Design Review setting.
**Role** :Retrieves the state of the Design Review setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetGeometryRepresentationFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the geometry representation format setting.
**Role** :Retrieves the state of the parameter geometry representation format setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetMeasureInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.GetDesignReviewInfo](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#GetDesignReviewInfo) Retrieves environment informations for the measure setting.
**Role** :Retrieves the state of the measure setting in the current environment.  **Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetPPRSaveConfigInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the PPRSaveConfig setting.
**Role** :Retrieves the state of the PPRSaveConfig setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetPresentationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.GetDesignReviewInfo](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#GetDesignReviewInfo) Retrieves environment informations for the presentation setting.
**Role** :Retrieves the state of the presentation setting in the current environment.  **Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetSectionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.GetDesignReviewInfo](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#GetDesignReviewInfo) Retrieves environment informations for the section setting.
**Role** :Retrieves the state of the section setting in the current environment.  **Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetSurfaceAccuracyInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the surface accuracy setting.
**Role** :Retrieves the state of the surface accuracy setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetWorkInstructionsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

Retrieves environment informations for the Work Instructions setting.
**Role** :Retrieves the state of the Work Instructions setting in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAlternateViewLock**( boolean  `iLocked`)

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.SetDesignReviewLock](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#SetDesignReviewLock) Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnimationLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnnotatedViewLock**( boolean  `iLocked`)

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.SetDesignReviewLock](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#SetDesignReviewLock) Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnnotation3DLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDesignReviewLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetGeometryRepresentationFormatLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetMeasureLock**( boolean  `iLocked`)

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.SetDesignReviewLock](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#SetDesignReviewLock) Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetPPRSaveConfigLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetPresentationLock**( boolean  `iLocked`)

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.SetDesignReviewLock](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#SetDesignReviewLock) Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSectionLock**( boolean  `iLocked`)

**Deprecated:**      R19 This method will be replaced by [Export3DXmlSettingAtt.SetDesignReviewLock](../CAT3DXmlInterfaces/interface_Export3DXmlSettingAtt_90825.htm#SetDesignReviewLock) Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSurfaceAccuracyLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetWorkInstructionsLock**( boolean  `iLocked`)

Locks or unlocks the flag.
**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.
**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure