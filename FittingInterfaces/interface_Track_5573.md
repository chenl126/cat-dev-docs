# Track (Object)

**_The interface to access a CATIATrack._**
**Role:** A CATIATrack (or track) object is an object to define motion to various items (such as a product or a shuttle). These tracks can be simulated which results in them to move along the defined trajectory (with a set speed).

## Properties

### Property **MoveMode**( ) As [DMUTrackMoveMode](../FittingInterfaces/enum_DMUTrackMoveMode_51428.md)

Returns or sets the track's movement mode. Can be speed or time based. In Speed mode, the total time is calculated based on the time need to travel the distance of the track at the given speed. In Time mode, the movement speed to calculated so that the end of the track is reached by the end of the total time. Uses enum DMUTrackMoveMode, which defined is in this interface.  
### Property **Speed**( ) As double

Returns or sets the track speed. Please note that the value of the speed should be greater than zero.

**Example**      This example sets the track speed to `17.54`.

```VBScript
myTrack.Speed =  17.54

```

Methods

### Sub **GetMatrixAll**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMatrixAll`)

GetMatrixAll Gets the base location of the track. The sum of several internal transforms.

**Parameters:**

` oMatrixAll`      An array of 12 doubles. A 3 by 3 rotation matrix followed by a position (x/y/z) vector, in millimeters.
**Returns:**      S_OK if everything was succcessfull  
### Sub **Mirror**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPoint`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iNormal`)

Produces a "mirror image" of the track. **Role:** Determines the "mirror image" of a track. The "mirror" is a 3d plane specified by a point on the plane and the normal to the surface of the plane. The mirror calculation involves going through each shot and projecting it in the space on the other side of the mirror plane. The projection "reflects" the point perpendicularly to the plane.

**Parameters:**

` iPoint`      A point on the plane that will be used to define the mirror.
` iNormal`      A normal to the plane that will be used to define the mirror.

### Sub **Move**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTransfo`)

Moves the track a certain position.

**Parameters:**

` iTransfo`      Specifies a relative amount to move the track.