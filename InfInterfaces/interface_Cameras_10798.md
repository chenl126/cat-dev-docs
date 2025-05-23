# Cameras (Collection)

**_A collection of all the Camera objects currently attached to a Document object._**
A camera can be created using the [Viewer.NewCamera](../InfInterfaces/interface_Viewer_8284.htm#NewCamera) method of the [Viewer](../InfInterfaces/interface_Viewer_8284.md) object. The first seventh cameras of the collection are [Camera3D](../InfInterfaces/interface_Camera3D_11722.md) objects and cannot be modified or removed. They can just be retrieved and used "as is". They store the following viewpoints whose sight direction is always toward the 3D-axis system origin:

* iso     The origin is on a line with (1,1,1) as components with positive coordinates * front     The origin is on the x axis with a positive x coordinate * back     The origin is on the x axis with a negative x coordinate * left     The origin is on the y axis with a positive y coordinate * right     The origin is on the y axis with a negative y coordinate * top     The origin is on the z axis with a positive z coordinate * bottom     The origin is on the z axis with a negative z coordinate

The cameras of the Cameras collection are available using the dialog box displayed by clicking the View->Defined Views menu.

## Methods

### Func **Item**(| [CATVariant](../System/typedef_CATVariant_20656.md) | `iIndex`) As [CATIACamera](../InfInterfaces/interface_Camera_7798.md)

   Returns a camera using its index or its name from the Cameras collection.

**Parameters:**

` iIndex`      The index or the name of the camera to retrieve from the collection of cameras. As a numerics, this index is the rank of the camera in the collection. The index of the first camera in the collection is 1, and the index of the last camera is Count. As a string, it is the name you assigned to the camera using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved camera  **Example:**      This example retrieves in `ThisCamera` the ninth camera, and in `ThatCamera` the camera named `MyCamera` in the camera collection of the active document.

```VBScript
     Dim ThisCamera As Camera
     Set ThisCamera = CATIA.ActiveDocument.Cameras.Item(9)
     Dim ThatCamera As Camera
     Set ThatCamera = CATIA.ActiveDocument.Cameras.Item("MyCamera")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a camera from the Cameras collection.

**Parameters:**

` iIndex`      The index or the name of the camera to remove from the collection of cameras. As a numerics, this index is the rank of the camera in the collection. The index of the first camera in the collection is 1, and the index of the last camera is Count. As a string, it is the name you assigned to the camera using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property. You cannot remove the first seventh cameras in the collection.  **Example:**      The following example removes the tenth camera and the camera named `CameraToBeRemoved` in the camera collection of the active document.

```VBScript
     CATIA.ActiveDocument.Cameras.Remove(10)
     CATIA.ActiveDocument.Cameras.Remove("CameraToBeRemoved")

```