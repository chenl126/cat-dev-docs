# Camera (Object)

**_Represents the camera._**
The camera is the object that stores a viewpoint saved from a viewer at a given moment using the [Viewer.NewCamera](../InfInterfaces/interface_Viewer_8284.htm#NewCamera) method of the [Viewer](../InfInterfaces/interface_Viewer_8284.md) object. The viewpoint stored in the camera can then be applied to another viewer to display the document in this viewer according to this viewpoint.

## Properties

### Property **Type**( ) As [CatCameraType](../InfInterfaces/enum_CatCameraType_35351.md) (Read Only)

Returns the camera's type.

**Example:**      This example retrieves in `MyCameraType` the type of the `MyCamera` 3D camera and applies the viewpoint stored in this camera to the active viewer.

```VBScript
MyCameraType = MyCamera.Type
CATIA.ActiveWindow.ActiveViewer.Viewpoint3D = MyCamera.Viewpoint3D

```

The value returned by the Type property in `MyCameraType` is `catCamera3D`