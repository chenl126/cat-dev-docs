# VrmlSettingAtt (Object)

**_The interface to access a CATIAVrmlSettingAtt._**
This interface may be used to read or modify in the CATIA\Tools\Option\General\Compatibility.... the settings values of the VRML sheet.

## Properties

### Property **ExportEdges**(| ) As boolean

   Returns or sets the ExportEdges parameter (exported Vrml files will or will not contains edge informations).

**Parameters:**

` oExportEdges`      \- iExportEdges Value of ExportEdges parameter. **Legal values** :
`TRUE :` exported Vrml files will contain edge informations.
`FALSE :` exported Vrml files will not contain edge informations.

### Property **ExportNormals**( ) As boolean

   Returns or sets the ExportNormals parameter (exported Vrml files will or will not contains normal informations).

**Parameters:**

` oExportNormals`      \- iExportNormals Value of ExportNormals parameter. **Legal values** :
`TRUE :` exported Vrml files will contain normal informations.
`FALSE :` exported Vrml files will not contain normal informations.

### Property **ExportTexture**( ) As boolean

   Returns or sets the ExportTexture parameter (exported Vrml files will or will not contains texture informations).

**Parameters:**

` oExportTexture`      \- iExportTexture Value of ExportTexture parameter. **Legal values** :
`TRUE :` exported Vrml files will contain texture informations.
`FALSE :` exported Vrml files will not contain texture informations.

### Property **ExportTextureFile**( ) As long

   Returns or sets the ExportTextureFile parameter (Textures will be exported in the vrml file containing the geometry or in external files).

**Parameters:**

` oExportTextureFile`      \- iExportTextureFile Value of ExportTextureFile parameter. **Legal values** :
`0 :` Textures are exported in the Vrml file containing the geometry.
`1 :` Texture are exported in external files.

### Property **ExportTextureFormat**( ) As long

   Returns or sets the ExportTextureFormat parameter.

**Parameters:**

` oExportTextureFormat`      \- iExportTextureFormat Value of ExportTextureFormat parameter. **Legal values** :
NOT APPLICABLE

### Property **ExportVersion**( ) As long

   Returns or sets the ExportVersion parameter (version of exported Vrml files).

**Parameters:**

` oExportVersion`      \- iExportVersion Value of Import Unit parameter. **Legal values** :
`1 :` VRML 1.0.
`2 :` VRML 97 (VRML 2.0).

### Property **ImportCreaseAngle**( ) As double

   Returns or sets the ImportCreaseAngle parameter. The crease angle affects how DEFAULT normals are generated. If the angle between the geometric normals of two adjacent faces is less than the crease angle, normals will be calculated so that the faces are smooth-shaded across the edge. Otherwise, normals will be calculated so that a lighting discontinuity across the edge is produce.

**Parameters:**

` oImportCreaseAngle`      \- iImportCreaseAngle Value of ImportCreaseAngle parameter. **Legal values** :
[0,inf]

### Property **ImportUnit**( ) As long

   Returns or sets the ImportUnit parameter (unit of imported Vrml files).

**Parameters:**

` oImportUnit`      \- iImportUnit Value of Import Unit parameter. **Legal values** :
`0 :` Millimeter.
`1 :` Centimeter.
`2 :` Meter.
Methods

### Sub **GetExportBackgroundColor**( long  `ioR`,  long  `ioG`,  long  `ioB`)

   Returns the ExportBackgroundColor parameter (Background color of exported Vrml files). Value of ExportBackgroundColor parameter. **Legal values** :
R [0,255] G [0,255] B [0,255]  
### Func **GetExportBackgroundColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportBackgroundColor setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportEdgesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportEdges setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportNormalsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportNormals setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportTextureFileInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportTextureFile setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportTextureFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportTextureFormat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportTextureInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportTexture setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetExportVersionInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ExportVersion setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetImportCreaseAngleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ImportCreaseAngle setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Func **GetImportUnitInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves information about the ImportUnit setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportBackgroundColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the ExportBackgroundColor parameter (Background color of exported Vrml files). Value of ExportBackgroundColor parameter. **Legal values** :
R [0,255] G [0,255] B [0,255]  
### Sub **SetExportBackgroundColorLock**( boolean  `iLocked`)

   Locks or unlocks the ExportBackgroundColor setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportEdgesLock**( boolean  `iLocked`)

   Locks or unlocks the ExportEdges setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportNormalsLock**( boolean  `iLocked`)

   Locks or unlocks the ExportNormals setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportTextureFileLock**( boolean  `iLocked`)

   Locks or unlocks the ExportTextureFile setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportTextureFormatLock**( boolean  `iLocked`)

   Locks or unlocks the ExportTextureFormat setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportTextureLock**( boolean  `iLocked`)

   Locks or unlocks the ExportTexture setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetExportVersionLock**( boolean  `iLocked`)

   Locks or unlocks the ExportVersion setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetImportCreaseAngleLock**( boolean  `iLocked`)

   Locks or unlocks the ImportCreaseAngle setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.  
### Sub **SetImportUnitLock**( boolean  `iLocked`)

   Locks or unlocks the ImportLock setting parameter.
Refer to [SettingController](../System/interface_SettingController_63320.md) for a detailed description.