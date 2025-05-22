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