# Camera3D (Object)

**_Represents a 3D camera._**
The 3D camera stores a 3D viewpoint, that is a [Viewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md) object.

## Properties

### Property **Viewpoint3D**( ) As [CATIAViewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md)

Returns or sets the 3D viewpoint of a 3D camera.

**Example:**      Assume the active window is a [SpecsAndGeomWindow](../InfInterfaces/interface_SpecsAndGeomWindow_67760.md) object. This example retrieves the [Viewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md) of the active 3D viewer and creates from it a Camera3D you handle using the `MyCamera` variable. Then the camera zoom is set to 2, and the camera's viewpoint is assigned to the active viewer.

```VBScript
Dim MyCamera As Camera3D
Set MyCamera = CATIA.ActiveWindow.ActiveViewer.NewCamera()
MyCamera.Viewpoint3D.Zoom = 2
CATIA.ActiveWindow.ActiveViewer.Viewpoint3D = MyCamera.Viewpoint3D

```