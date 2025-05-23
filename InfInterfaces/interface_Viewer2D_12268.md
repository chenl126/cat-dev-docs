# Viewer2D (Object)

**_Represents a 2D viewer._**
The 2D viewer aggregates a 2D viewpoint to display a 2D scene.

## Properties

### Property **Viewpoint2D**(| ) As [CATIAViewpoint2D](../InfInterfaces/interface_Viewpoint2D_24329.md)

   Returns or sets the 2D viewpoint of a 2D viewer.

**Example:**      This example retrieves the `Nice2DViewpoint` 2D viewpoint from the `My2DViewer` 2D viewer.

```VBScript
     Dim Nice2DViewpoint As Viewpoint2D
     Set Nice2DViewpoint = My2DViewer.Viewpoint2D

```