# RenderingLight (Object)

**_Represents a Rendering Light object._**

## Properties

### Property **ActiveStatus**(| ) As short

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