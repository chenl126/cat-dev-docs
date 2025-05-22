# Viewpoint2D (Object)

**_Represents the 2D viewpoint._**
The 2D viewpoint is the object that stores data which defines how your objects are seen to enable their display by a 2D viewer. This data includes namely the origin of the scene, that is the center of the displayed area, and the zoom factor.

## Properties

### Property **Zoom**( ) As double

Returns or sets the zoom factor associated with the viewpoint.

**Example:**      This example retrieves in `ZoomFactor` the zoom factor associated with the `NiceViewpoint` viewpoint, tests if it is less than 1, and if so, sets it to one and applies it to the viewpoint.

```VBScript
ZoomFactor = NiceViewpoint.Zoom
If ZoomFactor < 1 Then
 ZoomFactor = 1
 NiceViewpoint.Zoom(ZoomFactor)
End If

```

Methods

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

Gets the coordinates of the origin of the viewpoint.

**Example:**      This example Gets the origin of the `NiceViewpoint` viewpoint.

```VBScript
Dim origin(1)
NiceViewpoint.GetOrigin origin

```

### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

Sets the coordinates of the origin of the viewpoint.

**Example:**      This example sets the origin of the `NiceViewpoint` viewpoint to the point with coordinates (5, 8).

```VBScript
NiceViewpoint.PutOrigin Array(5, 8)

```