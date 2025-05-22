# Viewer3D (Object)

**_Represents a 3D viewer._**
The 3D viewer aggregates a 3D viewpoint to display a 3D scene. In addition, the Viewer3D object manages the lighting, the depth effects, the navigation style, and the rendering mode.

**See also:**      [Viewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md), [CatLightingMode](../InfInterfaces/enum_CatLightingMode_46709.md), [CatNavigationStyle](../InfInterfaces/enum_CatNavigationStyle_69512.md), [CatRenderingMode](../InfInterfaces/enum_CatRenderingMode_53126.md)

## Properties

### Property **ClippingMode**( ) As [CatClippingMode](../InfInterfaces/enum_CatClippingMode_46739.md)

Returns or sets the clipping mode.

**Example:**      This example sets the depth effect for the `My3DViewer` 3D viewer to `catClippingModeNearAndFar`.

```VBScript
My3DViewer.ClippingMode = catClippingModeNearAndFar

```

### Property **FarLimit**( ) As double

Returns or sets the far limit for the far clipping plane. The distance is measured from the eye location, that is the origin of the viewpoint, and is expressed in model unit. The far clipping plane is available with the `catClippingModeFar` and `catClippingModeNearAndFar` values of the [CatClippingMode](../InfInterfaces/enum_CatClippingMode_46739.md) enumeration only.

**Example:**      This example sets the far limit for the far clipping plane of the `My3DViewer` 3D viewer to 150 model units.

```VBScript
My3DViewer.FarLimit = 150

```

### Property **Foggy**( ) As boolean

Returns or sets the fog mode. Useful when clipping is enabled.

**Example:**      This example sets the fog on for the `My3DViewer` 3D viewer:

```VBScript
My3DViewer.Foggy = True

```

### Property **Ground**( ) As boolean

Returns or sets the ground displaying mode.

**Example:**      This example makes the ground visible for the `My3DViewer` 3D viewer:

```VBScript
My3DViewer.Ground = True

```

### Property **LightSources**( ) As [CATIALightSources](../InfInterfaces/interface_LightSources_31546.md) (Read Only)

Returns the viewer's light source collection.

**Example:**      This example retrieves the light source collection for the `My3DViewer` 3D viewer in `VPLightSources`.

```VBScript
Set VPLightSources = My3DViewer.LightSources

```

### Property **LightingIntensity**( ) As double

Returns or sets the lighting intensity. The lighting intensity ranges between 0 and 1.

**Example:**      This example sets the lighting intensity for the `My3DViewer` 3D viewer to 0.35.

```VBScript
My3DViewer.LightingIntensity = 0.35

```

### Property **LightingMode**( ) As [CatLightingMode](../InfInterfaces/enum_CatLightingMode_46709.md)

Returns or sets the lighting mode.

**Example:**      This example sets the lighting mode for the `My3DViewer` 3D viewer to `catInfiniteLightSource`.

```VBScript
My3DViewer.LightingMode = catInfiniteLightSource

```

### Property **NavigationStyle**( ) As [CatNavigationStyle](../InfInterfaces/enum_CatNavigationStyle_69512.md)

Returns or sets the navigation style.

**Example:**      This example sets the navigation style for the `My3DViewer` 3D viewer to `catNavigationWalk`.

```VBScript
My3DViewer.NavigationStyle = catNavigationWalk

```

### Property **NearLimit**( ) As double

Returns or sets the near limit for the near clipping plane. The distance is measured from the eye location, that is the origin of the viewpoint, and is expressed in model unit. The near clipping plane is available with the `catClippingModeNear` and `catClippingModeNearAndFar` values of the [CatClippingMode](../InfInterfaces/enum_CatClippingMode_46739.md) enumeration only.

**Example:**      This example sets the near limit for the near clipping plane of the `My3DViewer` 3D viewer to 75 model units.

```VBScript
My3DViewer.NearLimit = 75

```

### Property **RenderingMode**( ) As [CatRenderingMode](../InfInterfaces/enum_CatRenderingMode_53126.md)

Returns or sets the rendering mode.

**Example:**      This example sets the rendering mode for the `My3DViewer` 3D viewer to `catRenderShadingWithEdges`.

```VBScript
My3DViewer.RenderingMode = catRenderShadingWithEdges

```

### Property **Viewpoint3D**( ) As [CATIAViewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md)

Returns or sets the 3D viewpoint of a 3D viewer.

**Example:**      This example retrieves the `Nice3DViewpoint` 3D viewpoint from the `My3DViewer` 3D viewer.

```VBScript
Dim Nice3DViewpoint As Viewpoint3D
Set Nice3DViewpoint = My3DViewer.Viewpoint3D

```

Methods

### Sub **Rotate**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAxis`,  double  `iAngle`)

Applies a rotation. The rotation of iAngle degrees is applied to the viewer's contents around the axis iAxis (an array of 3 Variants), the invariant point being the target (ie: Origin + FocusDistance*SightDirection).

**Example:**      This applies a rotation of 10 degrees around the Up Direction to the contents of the `MyViewer3D` viewer.

```VBScript
MyViewer3D.Rotate MyViewer3D.UpDirection, 10

```

### Sub **Translate**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iVector`)

Applies a translation. The translation vector is iVector (an array of 3 Variants).

**Example:**      This applies a translation along (1, 1, 1) to the contents of the `MyViewer3D` viewer.

```VBScript
MyViewer3D.Translate Array(1, 1, 1)

```