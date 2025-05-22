# Viewer (Object)

**_Represents the viewer._**
The viewer is the object that makes your objects display on the screen.

## Properties

### Property **FullScreen**( ) As boolean

Returns or sets the state of a viewer to occupy the whole screen.
**True** if the viewer occupies the whole screen.

**Example:**      This example retrieves in `IsFullScreen` whether the `MyViewer` viewer occupies the whole screen.

```VBScript
IsFullScreen = MyViewer.FullScreen

```

### Property **Height**( ) As long (Read Only)

Returns the viewer's height, in pixels.

**Example:**      This example retrieves the height of the `MyViewer` viewer.

```VBScript
h = MyViewer.Height

```

### Property **Width**( ) As long (Read Only)

Returns the viewer's width, in pixels.

**Example:**      This example retrieves the width of the `MyViewer` viewer.

```VBScript
w = MyViewer.Width

```

Methods

### Sub **Activate**( )

Activates the viewer in the window.

**Example:**      This example activates `Viewers(1)` in the window `MyWindow`.

```VBScript
MyWindow.Viewers(1).Activate()

```

### Sub **CaptureToFile**( [CatCaptureFormat](../InfInterfaces/enum_CatCaptureFormat_54414.md)  `iFormat`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFile`)

Captures the actually displayed scene by the viewer as an image, and stores the image in a file. Clipped parts of the scene are also clipped in the captured image. Images can be captured as CGM, EMF, TIFF, TIFF Greyscale, BMP, and JPEG images.

**Parameters:**

` iFormat`      The format in which the image will be created
` iFile`      The full pathname of the file into which you want to store the captured image  **Example:**      This example captures the displayed part of the `MyViewer` viewer as a BMP image, and stores it in the `e:\MyImage.bmp` file.

```VBScript
MyViewer.CaptureToFile catCaptureFormatBMP, "e:\MyImage.bmp"

```

### Sub **GetBackgroundColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `color`)

Gets the viewer's background color. The color is expressed in the RGB color mode, as a triplet of coordinates ranging from 0 to 1 for the red, green, and blue colors respectively.

**Example:**      This example gets the background color of the `MyViewer` viewer.

```VBScript
Dim color(2)
MyViewer.GetBackgroundColor color

```

### Func **NewCamera**( ) As [CATIACamera](../InfInterfaces/interface_Camera_7798.md)

Creates a new camera from the viewpoint of the viewer.

**Example:**      This example creates the `MyCamera` new camera by using the current viewpoint of the `MyViewer` viewer.

```VBScript
Dim MyCamera As Camera
Set MyCamera = MyViewer.NewCamera()

```

### Sub **PutBackgroundColor**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `color`)

Sets the viewer's background color. The color is expressed in the RGB color mode, as a triplet of coordinates ranging from 0 to 1 for the red, green, and blue colors respectively.

**Example:**      This example sets the background color of the `MyViewer` viewer to blue, that is the color with (0.,0.,1.) coordinates

```VBScript
MyViewer.PutBackgroundColor Array(0, 0, 1)

```

### Sub **Reframe**( )

Reframes the viewer's contents (Fits all in). Reframing means that the viewer's contents is zoomed in or out to enable every object of the scene to be displayed in such a way that most of the space available in the viewer is used, just leaving a thin empty strip around the scene.

**Example:**      This example reframes the contents of the `MyViewer` viewer.

```VBScript
MyViewer.Reframe()

```

### Sub **Update**( )

Updates the viewer's contents. Since the viewer is not automatically updated after a viewpoint modification (for performance reasons), it must be explicitely redrawn when needed.

**Example:**      This example updates the contents of the `MyViewer` viewer.

```VBScript
MyViewer.Update()

```

### Sub **ZoomIn**( )

Zooms in the viewer's contents.

**Example:**      This example zooms in the contents of the `MyViewer` viewer.

```VBScript
MyViewer.ZoomIn()

```

### Sub **ZoomOut**( )

Zooms out the viewer's contents.

**Example:**      This example zooms out the contents of the `MyViewer` viewer.

```VBScript
MyViewer.ZoomOut()

```