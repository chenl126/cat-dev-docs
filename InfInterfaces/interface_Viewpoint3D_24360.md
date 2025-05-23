# Viewpoint3D (Object)

**_Represents the 3D viewpoint._**
The 3D viewpoint is the object that stores data which defines how your objects are seen to enable their display by a 3D viewer. This data includes namely the eye location, also named the origin, the distance from the eye to the target, that is to the looked at point in the scene, the sight, up, and right directions, defining a 3D axis system with the eye location as origin, the projection type chosen among perspective (conic) and parallel (cylindric), and the zoom factor. The right direction is not exposed in a property, and is automatically computed from the sight and up directions.

**See also:**      [CatProjectionMode](../InfInterfaces/enum_CatProjectionMode_60760.md)

## Properties

### Property **FieldOfView**(| ) As double

   Returns or sets the field of view associated with the viewpoint. The field of view is half of the vertical angle of the viewpoint, expressed in degrees. This property exists with the perspective (conic) projection type only.

**Example:**      This example retrieves in `HalfAngle` the field of view associated with the `NiceViewpoint` viewpoint.

```VBScript
     HalfAngle = NiceViewpoint.FieldOfView

```

### Property **FocusDistance**( ) As double

   Returns or sets the focus distance of the viewpoint. The focus distance determines the target position, that is the point at which the eye located at the origin and looking towards the sight direction is looking at. It is expressed in model units.

**Example:**      This example sets the focus distance of the `NiceViewpoint` viewpoint to 10.

```VBScript
     NiceViewpoint.FocusDistance = 10

```

### Property **ProjectionMode**( ) As [CatProjectionMode](../InfInterfaces/enum_CatProjectionMode_60760.md)

   Returns or sets the projection mode.

**Example:**      This example sets the projection mode for the `My3DViewer` 3D viewer to `catProjectionConic`.

```VBScript
     My3DViewer.Viewpoint3D.NavigationStyle = catProjectionConic

```

### Property **Zoom**( ) As double

   Returns or sets the zoom factor associated with the viewpoint. This property exists with the parallel (cylindric) projection type only.

**Example:**      This example retrieves in `ZoomFactor` the zoom factor associated with the `NiceViewpoint` viewpoint, tests if it is greater than 2, and if so, sets it to one and applies it.

```VBScript
     ZoomFactor = NiceViewpoint.Zoom
     If ZoomFactor > 2 Then
      ZoomFactor = 1
      NiceViewpoint.Zoom(ZoomFactor)
     End If

```

Methods

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `origin`)

   Retrieves the coordinates of the origin of the viewpoint. These coordinates are returned as an array of 3 Variants (double type).

**Example:**      This example retrieves the origin of the `NiceViewpoint` viewpoint in the `origin` variable.

```VBScript
     Dim origin(2)
     NiceViewpoint.GetOrigin origin

```

### Sub **GetSightDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSight`)

   Gets the components of the sight direction of the viewpoint. The sight direction is the line passes both by the origin of the viewpoint and by the target.

**Example:**      This example gets the sight direction of the `NiceViewpoint`

```VBScript
     Dim sight(2)
     NiceViewpoint.GetSightDirection sight

```

### Sub **GetUpDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oUp`)

   Gets the components of the up direction of the viewpoint.

**Example:**      This example gets the up direction of the `NiceViewpoint`.

```VBScript
     Dim up(2)
     NiceViewpoint.GetUpDirection up

```

### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `origin`)

   Sets the coordinates of the origin of the viewpoint. These coordinates are set as an array of 3 Variants (double type).

**Example:**      This example sets the origin of the `NiceViewpoint` viewpoint. to the point with coordinates (10, 25, 15).

```VBScript
     NiceViewpoint.PutOrigin Array(10, 25, 15)

```

### Sub **PutSightDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSight`)

   Sets the components of the sight direction of the viewpoint. The sight direction is the line passes both by the origin of the viewpoint and by the target.

**Example:**      This example sets the sight direction of the `NiceViewpoint` viewpoint to the direction with components (1.414, 1.414, 0).

```VBScript
     NiceViewpoint.PutSightDirection Array(1.414, 1.414, 0)

```

### Sub **PutUpDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oUp`)

   Sets the components of the up direction of the viewpoint.

**Example:**      This example sets the up direction of the `NiceViewpoint` viewpoint to the direction with components (0, 0, 1).

```VBScript
     NiceViewpoint.PutUpDirection Array(0, 0, 1)

```