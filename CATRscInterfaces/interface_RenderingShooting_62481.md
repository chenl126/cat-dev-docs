# RenderingShooting (Object)

**_Represents a Material object._**

## Properties

### Property **ActiveCamera**(| ) As [CATIACamera3D](../InfInterfaces/interface_Camera3D_11722.md)

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