# AnnotatedView (Object)

**_Represents an annotated view._**

## Properties

### Property **BehaviorMode**(| ) As [CatAnnotatedViewBehavior](../NavigatorInterfaces/enum_CatAnnotatedViewBehavior_120528.md)

   Returns or sets the behavior mode of the annotated view. This behavior mode enables the annotated view to be independant from the viewpoint.

**Example:**      This example retrieves the behavior mode of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Mode
        Mode = NewAnnotatedView.BehaviorMode

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the comment associated with the annotated view.

**Example:**      This example retrieves the comment of `NewAnnotatedView` annotated view.

```VBScript
        Dim text As String
        text = NewAnnotatedView.Comment

```

### Property **FieldOfView**( ) As double (Read Only)

   Returns the field of view associated with the annotated view. The field of view is half of the vertical angle of the viewpoint, expressed in degrees. This property exists with the perspective (conic) projection mode only.

**Example:**      This example retrieves the field of view` of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Field As Double
        Field = NewAnnotatedView.FieldOfView

```

### Property **Marker2Ds**( ) As [CATIAMarker2Ds](../NavigatorInterfaces/interface_Marker2Ds_15905.md) (Read Only)

   Returns the Marker2D Collection associated with the annotated view.

**Example:**      This example retrieves the `TheMarker2Ds` collection from the `NewAnnotatedView` annotated view.

```VBScript
        Dim TheMarker2Ds As AnnotatedView
        Set TheMarker2Ds = NewAnnotatedView.Marker2Ds(9)

```

### Property **ProjectionMode**( ) As [CatProjectionMode](../InfInterfaces/enum_CatProjectionMode_60760.md) (Read Only)

   Returns the projection mode of the annotated view. This projection mode is the one of the associated 3D View point.

**Example:**      This example retrieves the projection mode of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Mode
        Mode = NewAnnotatedView.ProjectionMode

```

### Property **Sound**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the sound file associated with the annotated view.

**Parameters:**

` iPath`      The path of the sound file. If this path is not empty, the sound replaces the old associated one (if it exists) or creates a new association (if not). If this path is empty, the sound is removed.

**Returns:**      The path of the sound file. If this path is empty, the annotated view has no associated sound.  **Example:**      This example retrieves the path of the sound file associated with the `NewAnnotatedView` annotated view.

```VBScript
        Dim path As String
        path = NewAnnotatedView.Sound

```

### Property **Zoom**( ) As double (Read Only)

   Returns the zoom factor associated with the annotated view. This property exists with the parallel (cylindric) projection mode only. This zoom factor is the one of the associated 3D View point.

**Example:**      This example retrieves in `ZoomFactor` the zoom of the `NewAnnotatedView` annotated view.

```VBScript
        Dim ZoomFactor As Double
        ZoomFactor = NewAnnotatedView.Zoom

```

Methods

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Retrieves the coordinates of the origin of the 3D viewpoint of the annotated view.

**Parameters:**

` oOrigin`      The coordinates of the view point origin expressed as an array of 3 variants are:

  * oOrigin(0) is the X coordinate of the origin
  * oOrigin(1) is the Y coordinate of the origin
  * oOrigin(2) is the Z coordinate of the origin

**Example:**      This example retrieves the origin of the 3D viewpoint of the `NewAnnotatedView` annotated view.

```VBScript
        Dim origin(2)
        NewAnnotatedView.GetOrigin origin

```

### Sub **GetSightDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSight`)

   Retrieves the components of the sight direction of the 3D viewpoint of the annotated view. The sight direction is the line that passes by the origin of the viewpoint and by the target.

**Parameters:**

` oSight`      The components of the viewpoint sight direction expressed as an array of 3 variants are:

  * oSight(0) is the X component of the sight direction
  * oSight(1) is the Y component of the sight direction
  * oSight(2) is the Z component of the sight direction

**Example:**      This example retrieves the sight direction of the `NewAnnotatedView` annotated view.

```VBScript
        Dim sight(2)
        NewAnnotatedView.GetSightDirection sight

```

### Sub **GetUpDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oUp`)

   Retrieves the components of the up direction of the 3D viewpoint of the annotated view.

**Parameters:**

` oUp`      The components of the viewpoint up direction expressed as an array of 3 variants are:

  * oUp(0) is the X component of the up direction
  * oUp(1) is the Y component of the up direction
  * oUp(2) is the Z component of the up direction

**Example:**      This example retrieves the up direction of the `NewAnnotatedView` annotated view.

```VBScript
        Dim up(2)
        NewAnnotatedView.GetUpDirection up

```

### Sub **Update**( )

   Updates the annotated view: that is to take into account all modifications which occur since last update.

**Example:**      This example updates the `NewAnnotatedView` annotated view.

```VBScript
        NewAnnotatedView.Update

```