# CATRscInterfaces Framework

## Object Index

  * [RenderingEnvironment](CATRscInterfaces/interface_RenderingEnvironment_87036.md)
  * [RenderingEnvironmentWall](CATRscInterfaces/interface_RenderingEnvironmentWall_123106.md)
  * [RenderingEnvironments](CATRscInterfaces/interface_RenderingEnvironments_96380.md)
  * [RenderingLight](CATRscInterfaces/interface_RenderingLight_41764.md)
  * [RenderingLights](CATRscInterfaces/interface_RenderingLights_48369.md)
  * [RenderingShooting](CATRscInterfaces/interface_RenderingShooting_62481.md)
  * [RenderingShootings](CATRscInterfaces/interface_RenderingShootings_70460.md)

---

# RenderingEnvironment (Object)

**_Represents a Environment object._**

## Properties

### Property **ActiveStatus**( ) As short

   Returns or sets the environment active status.
Only one environment can be active for a product. The active status can be:
* 1: environment is activated
* 0: environment is desactivated

### Property **FaceNumber**( ) As short

   Returns or sets the spherical environment face number.
The default value for a new spherical environment is 2.
If face number is set to 1, a mapped texture image will covered whole environment sphere.
If face number is set to 2, two different texture images can be mapped for upper hemisphere and lower hemisphere.
N.B. This property is useless for cubical and cylindrical environments.  
### Property **Height**( ) As double

   Returns or sets the cubic or cylindrical environment height value.  
### Property **Length**( ) As double

   Returns or sets the cubic environment length value.  
### Property **Radius**( ) As double

   Returns or sets the spherical or cylindrical environment radius value.  
### Property **Width**( ) As double

   Returns or sets the cubic environment width value.  Methods

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the coordinates of the origin of the environment.
These coordinates are set as an array of 3 Variants (double type).  
### Func **GetType**( ) As short

   Returns the environment type.

Possible environment types are:
  * 1: Cubical environment
  * 2: Spherical environment
  * 3: Cylindrical environment

### Sub **GetVerticalAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAxis`)

   Returns the coordinates of the vertical axis vector of the environment.
These coordinates are set as an array of 3 Variants (double type).  
### Func **GetWall**( short  `iType`) As [CATIARenderingEnvironmentWall](../CATRscInterfaces/interface_RenderingEnvironmentWall_123106.md)

   Returns the environment walls.
The environment wall type can be:
* 1: North wall (for cubical and cylindrical environments)
* 2: South wall (for cubical and cylindrical environments)
* 3: East wall (for cubical environments)
* 4: West wall (for cubical environments)
* 5: Top wall (for cubical, cylindrical and shperical environments)
* 6: Bottom wall (for cubical, cylindrical and shperical environments)

### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`)

   Sets the coordinates of the origin of the environment.
These coordinates are set as an array of 3 Variants (double type).

**Example:**      This example sets the origin of the `MyEnvironment` environment. to the point with coordinates (10, 25, 15).

```VBScript
     MyEnvironment.PutOrigin Array(10, 25, 15)

```

### Sub **PutVerticalAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAxis`)

   Sets the coordinates of the vertical axis vector of the environment.
These coordinates are set as an array of 3 Variants (double type).

---

# RenderingEnvironments (Collection)

**_A collection of all the Rendering Environments objects._**

## Methods

### Func **Add**( short  `iEnvironmentType`) As [CATIARenderingEnvironment](../CATRscInterfaces/interface_RenderingEnvironment_87036.md)

   Adds a new environment to the environments collection.

**Parameters:**

` iEnvironmentType`      The type of the environment to create choosen among:

1     For cubical environment 2     For spherical environment 3     For cylindrical environment

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingEnvironment](../CATRscInterfaces/interface_RenderingEnvironment_87036.md)

   Returns an environment index in the environments collection.

**Parameters:**

` iIndex`      The index of the environment to retrieve in the collection of environments. Compared with other collections, you cannot use the name of the environment as argument.

**Returns:**      The retrieved environment  **Example:**      The following example returns in `MyEnvironment` the sixth environment in a environment collection.

```VBScript
     Dim MyEnvironment As RenderingEnvironment
     Set MyEnvironment = RenderingEnvironments.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a environment from the environments collection.  
### Sub **RemoveAll**( )

   Removes all environments.of the collection

---

# RenderingEnvironmentWall (Object)

**_Represents a Environment object._**

## Properties

### Property **ActiveStatus**( ) As short

   Returns or sets the environment wall active status. A wall is visible only when it is active.

The active status can be:
  * 1: wall is visible
  * 0: wall is invisible

### Property **AutoScaleStatus**( ) As short

   Returns or sets the texture automatic scaling status. If status is automatic scaling, the texture fit is locked when the environment size is modified.

The scaling status can be:
  * 1: automatic scaling is on
  * 0: automatic scaling is off

### Property **FlipUStatus**( ) As short

   Returns or sets texture orientation status along the U axis.

The flip status can be:
  * 1: texture is flipped along the U axis
  * 0: texture is not flipped along the U axis

### Property **FlipVStatus**( ) As short

   Returns or sets texture orientation status along the V axis.

The flip status can be:
  * 1: texture is flipped along the V axis
  * 0: texture is not flipped along the V axis

### Property **LinkedScaleStatus**( ) As short

   Returns or sets the texture scaling link status. If scales are linked, modifying one scale will update the other keeping the ratio between U and V constant.

The link status can be:
  * 1: U and V scales are linked
  * 0: U and V scales are not linked

### Property **Rotation**( ) As double

   Returns or sets the texture rotation angle (in degrees). The rotation values must be between -360 and 360 degrees.  
### Property **ScaleU**( ) As double

   Returns or sets the texture scale along the U axis. The scale value should be > 0. Note that the modification of this parameter is useless if automatic scaling is enabled.  
### Property **ScaleV**( ) As double

   Returns or sets the texture scale along the V axis. The scale value should be > 0. Note that the modification of this parameter is useless if automatic scaling is enabled.  
### Property **ShadowsStatus**( ) As short

   Returns or sets the wall shadow status. A wall may or may not be affected by lights depending on this status.

The shadows status can be:
  * 1: wall is affected by active lights and can bear shadows
  * 0: wall is not affected by active lights and is always seen

### Property **Texture**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the wall texture name. To remove the texture, use an empty string.  
### Property **TranslationU**( ) As double

   Returns or sets the texture offset along the U axis. Note that this parameter is useless if automatic scaling is enabled.  
### Property **TranslationV**( ) As double

   Returns or sets the texture offset along the V axis. Note that this parameter is useless if automatic scaling is enabled.  Methods

### Sub **FitAllInWall**( )

   If a texture is mapped on the wall, scale automatically the texture to fit inside the wall.

---

# RenderingLight (Object)

**_Represents a Rendering Light object._**

## Properties

### Property **ActiveStatus**( ) As short

   Returns or sets the light active status.
A light illuminates only when it is active. The active status can be:
* 1: light is on
* 0: light is off

### Property **Ambient**( ) As double

   Returns or sets the light ambient intensity of a light.  
### Property **Angle**( ) As double

   Returns or sets the light angle of a spot light.
The angle ranges from `0.` (directional light) to `360.` (point light).  
### Property **AreaSamplesU**( ) As short

   Changes the number of samples taken in U direction of the area source.  
### Property **AreaSamplesV**( ) As short

   Changes the number of samples taken in V direction of the area source.  
### Property **AreaStatus**( ) As short

   Returns or sets the light area visibility status.
The area visibility status can be:
* 1: light area is rendered
* 0: light area is not rendered

### Property **AttenuationAngleRatio**( ) As double

   Returns or sets the light attenuation angle ratio.
It represents the fraction of the light angle where the illumination starts to attenuate.
The ratio ranges from `0.` (attenuation starts when angle is null) to `1.` (attenuation starts when angle is maximum = no angle attenuation).  
### Property **AttenuationStartRatio**( ) As double

   Returns or sets the light attenuation start ratio.
It represents the fraction of the end distance where the light intensity starts to attenuate.
The ratio ranges from `0.` (attenuation starts at the origin) to `1.` (attenuation starts at the end distance = no attenuation).  
### Property **CausticPhotonsNumber**( ) As long

   Changes the maximum number of caustic photons to emit from the light source.  
### Property **CylinderLightHeight**( ) As double

   Returns or sets the cylinder light area radius.  
### Property **CylinderLightRadius**( ) As double

   Returns or sets the cylinder light area radius.  
### Property **Diffuse**( ) As double

   Returns or sets the light diffuse intensity of a light.  
### Property **DiskLightRadius**( ) As double

   Returns or sets the disk light area radius.  
### Property **EndDistance**( ) As double

   Returns or sets the light maximum distance of illumination.
The light illuminates from its origin to its end distance. Objects farther than this distance are not affected by the light.  
### Property **EnergyFactor**( ) As double

   Changes the factor for indirect illumination energy.  
### Property **FalloffExponent**( ) As short

   Changes the light falloff exponent. Exponent value can be 0, 1 or 2.
An exponent of 0 means that the light energy does not fall off with distance.
An exponent of 1 means that the light energy fall off is linear.
An exponent of 2 is physically correct.  
### Property **GlobalPhotonsNumber**( ) As long

   Changes the maximum number of global illumination photons to emit from the light source.  
### Property **HardwareShadowSmoothing**( ) As short

   Returns or sets the light shadow smoothing.
It is an integer in the scale 0 to 10 It represents the cleanliness of the shadow limits  
### Property **HardwareShadowStatus**( ) As short

   Returns or sets the light shadow status on environmemt.
The shadow status can be:
* 1: light casts shadows on environmemt
* 0: light does not cast shadows on environmemt

The shadow status on environmemt can be activate only with a directional light  
### Property **HardwareShadowTransparency**( ) As double

   Returns or sets the light shadow transparency.
It is a float in the scale 0.0(no transparency) to 1.0(full transparency)  
### Property **IlluminationStatus**( ) As short

   Changes the indirect illumination status.
The indirect illumination status can be:
* 1: indirect illumination is enabled
* 0: indirect illumination is disabled

### Property **Intensity**( ) As double

   Returns or sets the light intensity of a light.  
### Property **LightAreaType**( ) As short

   Returns or sets the light area type.

Possible area light types are:
  * 1: CATNone
  * 2: CATRectangle
  * 3: CATDisk
  * 4: CATSphere
  * 5: CATCylinder

### Property **Mode**( ) As short

   Returns or sets the light mode.

Possible light modes are:
  * 1: Light is linked to the viewpoint
  * 2: Light is linked to the model

### Property **RectangleLightLength**( ) As double

   Returns or sets the light area length.  
### Property **RectangleLightWidth**( ) As double

   Returns or sets the light area width.  
### Property **ShadowFittingMode**( ) As short

   Returns or sets the light shadow fitting mode.
The shadow fitting mode can be:
* 0: Standard
* 1: Good

### Property **ShadowMapSize**( ) As short

   Returns or sets the light shadow map size.
The shadow map size can be:
* 0: Small (512)
* 1: Medium (1024)
* 2: Large (2048)

### Property **ShadowObjectStatus**( ) As short

   Returns or sets the light shadow status on objet.
The shadow status can be:
* 1: light casts shadows on objet
* 0: light does not cast shadows on objet

The shadow status on object can be activate only with a spot light  
### Property **ShadowStatus**( ) As short

   Returns or sets the light shadow status.
The shadow status can be:
* 1: light casts shadows
* 0: light does not cast shadows

### Property **Specular**( ) As double

   Returns or sets the light specular intensity of a light.  
### Property **SphereLightRadius**( ) As double

   Returns or sets the sphere light area radius.  
### Property **Type**( ) As short

   Returns or sets the light type.

Possible light types are:
  * 1: Spot light
  * 2: Point light
  * 3: Directional light

Methods

### Sub **GetColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oColor`)

   Returns the color of a light.
The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oColor`      The color as a safe array made up of three doubles: r, g, b
The array must be previously initialized.

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the coordinates of the origin of the light.
These coordinates are set as an array of 3 Variants (double type).  
### Sub **GetShadowColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oShadowColor`)

   Returns the color of a shadow.
The color is expressed with r, g, and b coefficients (between 0 and 255)

**Parameters:**

` oColor`      The color as a safe array made up of three doubles: r, g, b
The array must be previously initialized.

### Sub **GetTarget**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oTarget`)

   Returns the coordinates of the target point of the light.
These coordinates are set as an array of 3 Variants (double type).  
### Sub **PutColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iColor`)

   Sets the color of a light.
The color is expressed with r, g, and b coefficients (between 0 and 255)

### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`)

   Sets the coordinates of the origin of the light.
These coordinates are set as an array of 3 Variants (double type).

**Example:**      This example sets the origin of the `MyLight` light. to the point with coordinates (10, 25, 15).

```VBScript
     MyLight.PutOrigin Array(10, 25, 15)

```

### Sub **PutShadowColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iShadowColor`)

   Sets the color of a shadow.
The color is expressed with r, g, and b coefficients (between 0 and 255)

### Sub **PutTarget**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTarget`)

   Sets the coordinates of the target point of the light.
These coordinates are set as an array of 3 Variants (double type).

---

# RenderingLights (Collection)

**_A collection of all the Rendering Lights objects._**

## Methods

### Func **Add**( ) As [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)

   Adds a new light to the lights collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)

   Returns a rendering light index in the rendering light collection.

**Parameters:**

` iIndex`      The index of the light to retrieve in the collection of lights. Compared with other collections, you cannot use the name of the light as argument.

**Returns:**      The retrieved light  **Example:**      The following example returns in `MyLight` the sixth light in a lights collection.

```VBScript
     Dim MyLight As RenderingLight
     Set MyLight = RenderingLights.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a light from the lights collection.  
### Sub **RemoveAll**( )

   Removes all lights from the collection.

---

# RenderingShooting (Object)

**_Represents a Material object._**

## Properties

### Property **ActiveCamera**( ) As [CATIACamera3D](../InfInterfaces/interface_Camera3D_11722.md)

   Returns or sets the active camera for shooting. A shooting can only have one active camera at a time.  
### Property **ActiveEnvironment**( ) As [CATIARenderingEnvironment](../CATRscInterfaces/interface_RenderingEnvironment_87036.md)

   Returns or sets the active environment for shooting.
A shooting can have one or zero active environment at a time.  
### Property **AmbientFactor**( ) As short

   Returns or sets amount of ambient used for indirect illumination (final gathering or global illumination).
The ambient factor can be:
* 1: Ambient is taken into account
* 0: No ambient used

### Property **AntialiasingContrast**( ) As short

   Returns or sets the antialiasing contrast threshold value.
This value ranges from `0.` to `100.`%. Contrast value sets the contrast threshold for adaptative oversampling, that is, the maximum contrast threshold between pixels, below which no oversampling will be done.
If the contrast of any RGB component between the currently calculated pixel and heighboring pixels weighted by their sum is greater than this threshold, the pixel is oversampled.  
### Property **AntialiasingMaxSample**( ) As short

   Returns or sets the antialiasing maximum sample number for image computation.
This value ranges from `0/code> to `5/code>.
Maximum samples value sets the minimum number of rays casted for 1,4 or 16 pixels.

The possible maximum sample number are:
  * 0 : 1 ray casted for a 4x4 pixel square
  * 1 : 1 ray casted for a 2x2 pixel square
  * 2 : 1 ray casted per pixel
  * 3 : 4 rays casted per pixel
  * 4 : 16 rays casted per pixel
  * 5 : 64 rays casted per pixel

### Property **AntialiasingMinSample**( ) As short

   Returns or sets the antialiasing minimum sample number for image computation.
This value ranges from `0/code> to `5/code>.
Minimum samples value sets the minimum number of rays casted for 1,4 or 16 pixels.  The possible minimum sample number are:
    * 0 : 1 ray casted for a 4x4 pixel square
    * 1 : 1 ray casted for a 2x2 pixel square
    * 2 : 1 ray casted per pixel
    * 3 : 4 rays casted per pixel
    * 4 : 16 rays casted per pixel
    * 5 : 64 rays casted per pixel

### Property **CartoonContourThickness**( ) As double

   Returns or sets the cartoon contour thickness.
The line thickness is given as image size percentage.
The line thickness ranges from `0.0` (none) to `100.0`.  
### Property **CartoonShadingStatus**( ) As short

   Returns or sets the cartoon shading status of shooting.
This status defines if the cartoon shading is activated or not.
If shading is deactivated, only contours are rendered.
The cartoon shading effect status can be:
    * 1: Shading status is active
    * 0: Shading status is deactivated

### Property **CartoonStatus**( ) As short

   Returns or sets the cartoon status of shooting.
This status defines if the cartoon rendering is activated or not.
The cartoon effect status can be:
    * 1: Cartoon status is active
    * 0: Cartoon status is deactivated

### Property **CartoonStrokeStatus**( ) As short

   Returns or sets the cartoon stroke status of shooting.
This status defines if the cartoon stroke effect (ink pen effect) is activated or not.
The stroke status can be:
    * 1: Stroke status is active
    * 0: Stroke status is deactivated

### Property **CausticAccuracy**( ) As short

   Returns or sets the number of photons to use when estimating radiance for caustics.  
### Property **CausticRadius**( ) As double

   Returns or sets the maximum distance in which photons for caustics are located.
If the value is 0.0 an estimate based on the scene extent will be used.  
### Property **CausticStatus**( ) As short

   Returns or sets the caustic status of shooting.
This status defines if caustics are calculated or not.
The caustic status can be:
    * 1: Caustics are enabled
    * 0: Caustics are disabled

### Property **DepthOfFieldRadius**( ) As double

   Returns or sets the depth of field radius of confusion.
The radius of confusion ranges from `1.0` to `10.0`%.  
### Property **DepthOfFieldStatus**( ) As short

   Returns or sets the depth of field status of shooting. This status defines if depth of field effect is activated or not.
The depth of field status can be:
    * 1: Depth of field is active
    * 0: Depth of field is deactivated

### Property **FinalGatheringAccuracy**( ) As short

   Returns or sets the number of rays shot in each final gather.  
### Property **FinalGatheringMaxRadius**( ) As double

   Returns or sets the maximum distance in which a final gather result can be used.
If the value is 0.0 an estimate based on the scene extent will be used.  
### Property **FinalGatheringMinRadius**( ) As double

   Returns or sets the minimum distance in which a final gather result can be used.
If the value is 0.0 it will be set to 10% of maximum distance.  
### Property **FinalGatheringStatus**( ) As short

   Returns or sets the final gathering status of shooting.
This status defines if final gathering is activated or not.
The final gathering status can be:
    * 1: Final gathering is enabled
    * 0: Final gathering is disabled

### Property **GlobalIlluminationAccuracy**( ) As short

   Returns or sets the number of photons to use when estimating radiance for global illumination.  
### Property **GlobalIlluminationRadius**( ) As double

   Returns or sets the maximum distance in which photons for global illumination are located.
If the value is 0.0 an estimate based on the scene extent will be used.  
### Property **GlobalIlluminationStatus**( ) As short

   Returns or sets the global illumination status of shooting.
This status defines if global illumination is used or not.
The global illumination status can be:
    * 1: Global illumination is enabled
    * 0: Global illumination is disabled

### Property **GlowFlareDiffusion**( ) As double

   Returns or sets the glow flare diffusion.
The flare diffusion value ranges from `0.0` to `1.0`%.  
### Property **GlowFlareFactor**( ) As double

   Returns or sets the glow flare factor.
The flare factor ranges from `0.0` to `1.0`%.  
### Property **GlowIntensity**( ) As double

   Returns or sets the glow intensity factor.
The glow intensity factor ranges from `1.0` to `10.0`%.  
### Property **GlowRadialLineSize**( ) As double

   Returns or sets the glow radial lines size.
The lines size ranges from `0.0` (none) to `1.0` (max length).  
### Property **GlowSize**( ) As double

   Returns or sets the glow filter size in percentage of image size.
The filter size ranges from `0.1` to `1.0`%.  
### Property **GlowStarEffect**( ) As double

   Returns or sets the glow star effect.
The effect coefficient ranges from `0.0` (random star) to `1.0` (cross).  
### Property **GlowStatus**( ) As short

   Returns or sets the glow status of shooting. This status defines if the glow effect is activated or not.
The glow status can be:
    * 1: Glow is active
    * 0: Glow is deactivated

### Property **GlowThreshold**( ) As double

   Returns or sets the glow color threshold.
The color threshold ranges from `0.5` to `1.5`%.  
### Property **ImageHeight**( ) As short

   Returns or sets the image height for shooting.
The image height ranges from `10` to `8000` pixels.  
### Property **ImageOutputDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the output directory for image.
This is the place where rendered images are saved.  
### Property **ImageOutputFormat**( ) As short

   Returns or sets the file type used for saved image.  Possible format types
      * 1 TIFF True Color (*.tif)
      * 2 TIFF True Color Packbits (*.tif)
      * 3 SGI Format (*.rgb)
      * 4 Windows Bitmap (*.bmp)
      * 5 JPEG Fair Quality (*.jpg)
      * 6 JPEG Medium Quality (*.jpg)
      * 7 JPEG High Quality (*.jpg)
      * 8 Apple Macintosh Format (*.pic)
      * 9 Adobe Photoshop Format (*.psd)
      * 10 Portable Network Graphics (*.png)
      * 11 Truevision Targa (*.tga)

### Property **ImageOutputName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the output name for image (extension excluded).
This is the name of saved files (with no extension).  
### Property **ImageOutputType**( ) As short

   Returns or sets the image output location.  Output types
      * 1 On screen
      * 2 On disk

### Property **ImagePredefinedRatio**( ) As short

   Returns or sets the image height for shooting.
Sets the image ratio to a standard predefined value. The image size keeps the same height and the image length is recalculated.  Possible predefined ratio.  0 no predefined ratio
      * 1 0.708333 (A4)
      * 2 1.0 (6 x 6)
      * 3 1.25 (Standard)
      * 4 1.333333 (4 / 3)
      * 5 1.5 (24 x 36)
      * 6 1.687331 (16 mm.)
      * 7 1.777777 (16 / 9)
      * 8 1.855072 (HDTV)
      * 9 2.2 (Panavision)
      * 10 3.0 (Panorama)
      * 11 1.32 (CCD 1/2")
      * 12 1.333333 (CCD 1/4")

### Property **ImageWidth**( ) As short

   Returns or sets the image width for shooting.
The image width ranges from `10` to `8000` pixels.  
### Property **RaytracingStatus**( ) As short

   Returns or sets the the raytracing status for shooting.
The raytracing status can be:
    * 1: Raytracing is active
    * 0: Raytracing is deactivated

### Property **ReboundsCount**( ) As short

   Returns or sets the maximum number of rebounds levels to take into account for image computation.
This number ranges from `0` to `18` levels.  
### Property **ReflectionsCount**( ) As short

   Returns or sets the maximum number of reflections levels to take into account for image computation.
This number ranges from `0` to `9` levels.  
### Property **RefractionsCount**( ) As short

   Returns or sets the maximum number of refractions levels to take into account for image computation.
This number ranges from `0` to `9` levels.  
### Property **ShadowsStatus**( ) As short

   Returns or sets the shadows status of shooting. This status defines if shadows are calculated or not.
The shadows status can be:
    * 1: Shadows on
    * 0: Shadows off

### Property **TexturesStatus**( ) As short

   Returns or sets the textures status of shooting. This status defines if textures are taken into account for image computation.
The texture status can be:
    * 1: Textures are taking into account
    * 0: Textures are ignored
Methods

### Sub **AddActiveLight**( [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)  `iActiveLight`)

   Adds a new active light to the shooting active lights list.  
### Func **CountActiveLights**( ) As short

   Returns the number of active light for the shooting.  
### Func **GetActiveLight**( short  `iIndex`) As [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)

   Returns the active light of the shooting using its index.  
### Sub **RemoveActiveLight**( short  `iIndex`)

   Removes a light from the shootings active lights list.  
### Sub **Render**( )

   Render the shooting
Caution: Product involved in rendering calculation should not be closed before the end of computation. If product is closed, calculation is interrupted.

---

# RenderingShootings (Collection)

**_A collection of all the Rendering Shootings objects._**

## Methods

### Func **Add**( ) As [CATIARenderingShooting](../CATRscInterfaces/interface_RenderingShooting_62481.md)

   Adds a new shooting to the shootings collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingShooting](../CATRscInterfaces/interface_RenderingShooting_62481.md)

   Returns a renderingshooting index in the renderingshootings collection.

**Parameters:**

` iIndex`      The index of the shooting to retrieve in the collection of shootings. Compared with other collections, you cannot use the name of the shooting as argument.

**Returns:**      The retrieved shooting  **Example:**      The following example returns in `MyShooting` the sixth shooting in a shootings collection.

```VBScript
     Dim MyShooting As RenderingShooting
     Set MyShooting = RenderingShootings.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a shooting from the shootings collection.  
### Sub **RemoveAll**( )

   Removes all shootings from the collection.