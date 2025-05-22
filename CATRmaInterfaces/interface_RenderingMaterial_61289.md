# RenderingMaterial (Object)

**_Represents an RenderingMaterial object._**
This object is used to manage the Rendering properties of a material.

## Properties

### Property **AdaptiveCoeff**( ) As short

Returns or sets the adaptive coeffcient of a material. Adaptive coeffcient value is between 1 an 8.  
### Property **AmbientCoefficient**( ) As double

Returns or sets the ambient coefficient of a material. Ambient coefficient value is between 0 to 1.  
### Property **Bump**( ) As double

Returns or sets the texture bump. Image texture bump value is between -10 to 10.  
### Property **ChessboardJointHeight**( ) As double

Returns or sets the height of the join of a chessboard texture. Height value is between 0 to 100. N.B. Parameter use for CHESSBOARD texture type only.  
### Property **ChessboardJointWidth**( ) As double

Returns or sets the width of the join of a chessboard texture. Width value is between 0 to 100. N.B. Parameter use for CHESSBOARD texture type only.  
### Property **ChessboardOffset**( ) As double

Returns or sets the offset coefficient for a chessboard texture. It indicates the offset between each line of the chessboard texture. Offset value is between 0 to 0.5. N.B. Parameter use for CHESSBOARD texture type only.  
### Property **ChessboardTileHeight**( ) As double

Returns or sets the height of the tile of a chessboard texture. Height value is between 0 to 100. N.B. Parameter use for CHESSBOARD texture type only.  
### Property **ChessboardTileWidth**( ) As double

Returns or sets the width of the tile of a chessboard texture. Width value is between 0 to 100. N.B. Parameter use for CHESSBOARD texture type only.  
### Property **ColorNumber**( ) As short

Returns or sets the 3d texture color number. Possible color numbers are: \- From 2 to 5 for marble, vein and chessboard texture types \- From 1 to 5 for alternate vein texture types N.B. Parameter useless for ROCK textures (color number is fixed) and IMAGE texture  
### Property **DiffuseCoefficient**( ) As double

Returns or sets the diffuse coefficient of a material. Diffuse coefficient value is between 0 to 1.  
### Property **EnvironmentImage**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the environment image pathname of a material.  
### Property **FlipU**( ) As boolean

Returns or sets the texture flip status along U axis. N.B. Parameter use for IMAGE texture type only  
### Property **FlipV**( ) As boolean

Returns or sets the texture flip status along V axis. N.B. Parameter use for IMAGE texture type only  
### Property **MappingType**( ) As short

Returns or sets the mapping type of a material.

Possible types are:
  * 0: Planar mapping
  * 1: Spherical mapping
  * 2: Cylindrical mapping
  * 3: Cubical mapping
  * 4: Auto mapping
  * 5: Manual mapping

### Property **Orientation**( ) As double

Returns or sets the texture orientation. Orientation value should be between -360 to +360 degrees N.B. Parameter use for IMAGE texture type only  
### Property **PositionU**( ) As double

Returns or sets the texture position along U axis. N.B. Parameter use for IMAGE texture type only  
### Property **PositionV**( ) As double

Returns or sets the texture position along V axis. N.B. Parameter use for IMAGE texture type only  
### Property **PreviewSize**( ) As double

Returns or sets the preview size of a material. Preview size value is 0.1mm minimum.  
### Property **ReflectionHeight**( ) As double

Returns or sets the non-linear reflection height of a material. Non-linear reflection height value is between 0 to 1. N.B. Parameter use for CUSTOM reflection mode only.  
### Property **ReflectionLength**( ) As double

Returns or sets the non-linear reflection length of a material. Non-linear reflection length value is between 0 to 1. N.B. Parameter use for CUSTOM reflection mode only.  
### Property **ReflectionMode**( ) As short

Returns or sets the non-linear reflection mode of a material.

Possible reflection mode values are:
  * 0: CHROMA reflection mode
  * 1: PAINT reflection mode
  * 2: MATTE_METAL reflection mode
  * 3: BRIGHT_PLASTIC reflection mode
  * 4: CUSTOM reflection mode

### Property **ReflectivityCoefficient**( ) As double

Returns or sets the reflectivity coefficient of a material. Reflectivity coefficient value is between 0 to 1.  
### Property **RefractionCoefficient**( ) As double

Returns or sets the refraction coefficient of a material. Refraction coefficient value is between 1 to 2.  
### Property **RepeatU**( ) As boolean

Returns or sets the texture repeat status along U axis. N.B. Parameter use for IMAGE texture type only  
### Property **RepeatV**( ) As boolean

Returns or sets the texture repeat status along V axis. N.B. Parameter use for IMAGE texture type only  
### Property **ScaleU**( ) As double

Returns or sets the texture scale along U axis. U scale value is between 0 to 100. N.B. Parameter use for IMAGE texture type only  
### Property **ScaleV**( ) As double

Returns or sets the texture scale along V axis. V scale value is between 0 to 100. N.B. Parameter use for IMAGE texture type only  
### Property **SpecularCoefficient**( ) As double

Returns or sets the specular coefficient of a material. Specular coefficient value is between 0 to 1.  
### Property **SpecularExponent**( ) As double

Returns or sets the specular exponent of a material. Specular exponent value is between 0 to 1.  
### Property **TextureAmplitude**( ) As double

Returns or sets the 3d texture amplitude coefficient. Amplitude value is between 0 to 1. N.B. Parameter use for MARBLE and ROCK texture type only.  
### Property **TextureComplexity**( ) As short

Returns or sets the 3d texture complexity. Complexity value is between 0 to 10. N.B. Parameter use for MARBLE and ROCK texture types only.  
### Property **TextureGain**( ) As double

Returns or sets the 3d texture gain coefficient. Gain value is between 0 to 2. N.B. Parameter use for ROCK texture type only.  
### Property **TextureImage**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the texture image pathname of a material. N.B. Parameter use for IMAGE texture type only  
### Property **TexturePerturbation**( ) As double

Returns or sets the 3d texture perturbation coefficient. Perturbation value is between 1 to 10. N.B. Parameter use for VEIN, ALTERNATE VEIN and ROCK texture types only.  
### Property **TextureTurbulence**( ) As boolean

Returns or sets the 3d texture turbulence status. N.B. Parameter use for ROCK texture type only.  
### Property **TextureType**( ) As short

Returns or sets the texture type of a material. The possible values for this type can be:

Possible reflection mode values are:
  * 0: NO texture
  * 1: IMAGE texture
  * 2: MARBLE texture
  * 3: VEIN texture
  * 4: ALTERNATE VEIN texture
  * 5: ROCK texture
  * 6: CHESSBOARD texture

### Property **TextureVeinAmplitude**( ) As double

Returns or sets the 3d texture vein amplitude coefficient. Amplitude value is between 0 to 10. N.B. Parameter use for VEIN and ALTERNATE VEIN texture types only.  
### Property **TransparencyCoefficient**( ) As double

Returns or sets the transparency coefficient of a material. Transparency coefficient value is between 0 to 1.  Methods

### Sub **Get3DTextureColor**( short  `iColorIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `o3DTextureColor`)

Returns one color of a 3d texture. The color to access is identified with its index. The color is expressed with r, g, and b coefficients (between 0 and 255).

**Parameters:**

` iColorIndex`      The index of the color to access

**Returns:**      the color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized. N.B. Parameter useless for image textures.  
### Sub **Get3DTextureColorCoefficient**( short  `iColorIndex`,  double  `o3DTextureColorCoefficient`)

Returns one color coefficient of a 3d texture. The color to access is identified with its index.

**Parameters:**

` iColorIndex`      The index of the color to access.

**Returns:**      the color coefficient.
If the color is enable, the color coefficient value should range from 0 to 1.
If color is disable, the color coefficient is equal to -1.
N.B. Parameter useless for rock, chessboard and image textures.  
### Sub **Get3DTextureOrientation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `o3DTextureOrientation`)

Returns the orientation of a texture. The orientation is expressed with 3 coefficients (orientation around X, Y and Z axis). The orientation values must be between -360 and 360 degrees. N.B. Parameter useless for IMAGE textures (use get_Orientation, set_Orientation methods for IMAGE type).

**Returns:**      the orientation as a safe array made up of three doubles: rotationX, rotationY, rotationZ.
The array must be previously initialized.  
### Sub **Get3DTexturePosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `o3DTexturePosition`)

Returns the position of a texture. The position is expressed with 3 coefficients (position along X, Y and Z axis). The position values must be between -100 and 100. N.B. Parameter useless for IMAGE textures (use PositionU, PositionV methods for IMAGE type).

**Returns:**      the position as a safe array made up of three doubles: positionX, positionY, positionZ.
The array must be previously initialized.  
### Sub **Get3DTextureScale**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `o3DTextureScale`)

Returns the scale of a texture. The scale is expressed with 3 coefficients (scale along X, Y and Z axis) The scale values must be > 0 and ≤ 100\. N.B. Parameter useless for IMAGE textures. (use get_ScaleU, set_ScaleU, get_ScaleV, set_ScaleV methods for IMAGE type)

**Returns:**      the scale as a safe array made up of three doubles: scaleX, scaleY, scaleZ.
The array must be previously initialized.  
### Sub **GetAmbientColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAmbientColor`)

Returns the ambient color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Returns:**      the color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.  
### Sub **GetDiffuseColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDiffuseColor`)

Returns the diffuse color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Returns:**      the color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.  
### Sub **GetSpecularColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSpecularColor`)

Returns the specular color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Returns:**      the color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.  
### Sub **GetTransparencyColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oTransparencyColor`)

Returns the transparent color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oTransparencyColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.

### Sub **Put3DTextureColor**( short  `iColorIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `i3DTextureColor`)

Sets one color of a 3d texture. The color to access is identified with its index. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` iColorIndex`      The index of the color to access.

` i3DTextureColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized. N.B. Parameter useless for image textures.

### Sub **Put3DTextureColorCoefficient**( short  `iColorIndex`,  double  `i3DTextureColorCoefficient`)

Sets one color coefficient of a 3d texture. The color to access is identified with its index.

**Parameters:**

` iColorIndex`      The index of the color to access.

` i3DTextureColorCoefficient.`      The color coefficient.
If color is enable, the color coefficient value should range from 0 to 1.
If color is disable, the color coefficient should be equal to -1.
N.B. Parameter useless for rock, chessboard and image textures.

### Sub **Put3DTextureOrientation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `i3DTextureOrientation`)

Sets the orientation of a texture. The orientation is expressed with 3 coefficients (orientation around X, Y and Z axis). The orientation values must be between -360 and 360 degrees. N.B. Parameter useless for IMAGE textures (use get_Orientation, set_Orientation methods for IMAGE type).

**Parameters:**

` i3DTextureOrientation`      The orientation as a safe array made up of three doubles: rotationX, rotationY, rotationZ.
The array must be previously initialized.

### Sub **Put3DTexturePosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `i3DTexturePosition`)

Sets the position of a texture. The position is expressed with 3 coefficients (position along X, Y and Z axis). The position values must be between -100 and 100. N.B. Parameter useless for IMAGE textures (use PositionU, PositionV methods for IMAGE type).

**Parameters:**

` i3DTexturePosition`      The position as a safe array made up of three doubles: positionX, positionY, positionZ.
The array must be previously initialized.

### Sub **Put3DTextureScale**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `i3DTextureScale`)

Sets the scale of a texture. The scale is expressed with 3 coefficients (scale along X, Y and Z axis). The scale values must be > 0 and ≤ 100\. N.B. Parameter useless for IMAGE textures (use get_ScaleU, set_ScaleU, get_ScaleV, set_ScaleV methods for IMAGE type).

**Parameters:**

` i3DTextureScale`      The scale as a safe array made up of three doubles: scaleX, scaleY, scaleZ.
The array must be previously initialized.

### Sub **PutAmbientColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAmbientColor`)

Sets the ambient color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oAmbientColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.

### Sub **PutDiffuseColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDiffuseColor`)

Sets the diffuse color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oDiffuseColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.

### Sub **PutSpecularColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSpecularColor`)

Sets the specular color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oSpecularColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.

### Sub **PutTransparencyColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTransparencyColor`)

Sets the transparent color of a material. The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` iTransparencyColor`      The color as a safe array made up of three doubles: r, g, b
The r, g, b values ranges from 0 to 255.
The array must be previously initialized.