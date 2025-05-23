# Camera2D (Object)

**_Represents a 2D camera._**
The 2D camera stores a 2D viewpoint, that is a [Viewpoint2D](../InfInterfaces/interface_Viewpoint2D_24329.md) object.

## Properties

### Property **Viewpoint2D**(| ) As [CATIAViewpoint2D](../InfInterfaces/interface_Viewpoint2D_24329.md)

   Returns or sets the 2D viewpoint of a 2D camera.

**Example:**      Assume the active window is a [SpecsAndGeomWindow](../InfInterfaces/interface_SpecsAndGeomWindow_67760.md) object. This example retrieves the [Viewpoint2D](../InfInterfaces/interface_Viewpoint2D_24329.md) of the [SpecsViewer](../InfInterfaces/interface_SpecsViewer_26446.md) and creates from it a Camera2D you handle using the `MyCamera` variable. Then the camera zoom is set to 2, and the camera's viewpoint is assigned to the [SpecsViewer](../InfInterfaces/interface_SpecsViewer_26446.md).

```VBScript
     Dim MyCamera As Camera
     Set MyCamera = CATIA.ActiveWindow.SpecsViewer.NewCamera()
     MyCamera.Viewpoint2D.Zoom = 2
     CATIA.ActiveWindow.SpecsViewer.Viewpoint2D = MyCamera.Viewpoint2D

```