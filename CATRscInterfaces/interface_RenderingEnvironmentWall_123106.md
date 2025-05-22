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