# Window (Object)

**_Represents the window._**
The window is the object that accommodates one or several viewers to display your objects, and which makes the link with the windowing system.

## Properties

### Property **ActiveViewer**(| ) As [CATIAViewer](../InfInterfaces/interface_Viewer_8284.md) (Read Only)

   Returns the active viewer in the window.

**Example:**      This example retrieves the active viewer in the `CADWindow` window in `ViewerToWorkIn`.

```VBScript
     Dim ViewerToWorkIn As Viewer
     Set ViewerToWorkIn = CADWindow.ActiveViewer

```

### Property **Caption**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the window caption. The window caption is displayed in the title bar.

**Example:**      This example sets the window caption for the `CADWindow` window to: CAD 3D Window.

```VBScript
     CADWindow.Caption = "CAD 3D Window"

```

### Property **Height**( ) As long

   Returns or sets the window height. The window height is expressed in pixels.

**Example:**      This example sets the window height for the `CADWindow` window to 300 pixels.

```VBScript
     CADWindow.Width = 300

```

### Property **Left**( ) As long

   Returns or sets the distance of the window with respect to the inner left side of the frame. This distance is expressed in pixels.

**Example:**      This example sets the distance of the window with respect to the inner left side of the frame for the `CADWindow` window to 150 pixels.

```VBScript
     CADWindow.Left = 150

```

### Property **PageSetup**( ) As [CATIAPageSetup](../InfInterfaces/interface_PageSetup_17718.md)

   Returns or sets the page setup of the window. The page setup includes all parameters to print the window.

**Example:**      This example sets the page setup for the `CADWindow` window to an existing page setup for the A4 paper size `A4PageSetup`.

```VBScript
     CADWindow.PageSetup = A4PageSetup

```

### Property **Top**( ) As long

   Returns or sets the distance of the window with respect to the inner top side of the frame. This distance is expressed in pixels.

**Example:**      This example sets the distance of the window with respect to the inner top side of the frame for the `CADWindow` window to 50 pixels.

```VBScript
     CADWindow.Top = 50

```

### Property **Viewers**( ) As [CATIAViewers](../InfInterfaces/interface_Viewers_11325.md) (Read Only)

   Returns the collection of viewers attached to the window.

**Example:**      This example retrieves the collection of viewers attached to the `CADWindow` window in `ViewerCollection`.

```VBScript
     Dim ViewerCollection As Viewers
     Set ViewerCollection = CADWindow.Viewers

```

### Property **Width**( ) As long

   Returns or sets the window width. The window width is expressed in pixels.

**Example:**      This example sets the window width for the `CADWindow` window to 450 pixels.

```VBScript
     CADWindow.Width = 450

```

### Property **WindowState**( ) As [CatWindowState](../InfInterfaces/enum_CatWindowState_41936.md)

   Returns or sets the window state.

**Example:**      This example sets the window state for the `CADWindow` window to `catWindowStateMaximized`.

```VBScript
     CADWindow.WindowState = catWindowStateMaximized

```

Methods

### Sub **Activate**( )

   Activates a window. The active window is deactivated and the window to which the method applies is activated instead.

**Example:**      This example activates the `CADWindow` window.

```VBScript
     CADWindow.Activate()

```

### Sub **ActivateNext**( )

   Activates the window following the current active one in the window collection.

**Example:**      This example activates the window following the current `CADWindow` window in the window collection.

```VBScript
     CADWindow.ActivateNext()

```

### Sub **ActivatePrevious**( )

   Activates the window preceding the current active one in the window collection.

**Example:**      This example activates the window preceding the current `CADWindow` window in the window collection.

```VBScript
     CADWindow.ActivatePrevious()

```

### Sub **Close**( )

   Closes the window. This method displays the dialog box requesting whether to save the file if the document was modified, except if the [Application.DisplayFileAlerts](../InfInterfaces/interface_Application_26636.htm#DisplayFileAlerts) property was previously set to False.

**Example:**      This example closes the `CADWindow` window.

```VBScript
     CADWindow.Close()

```

### Func **NewWindow**( ) As [CATIAWindow](../InfInterfaces/interface_Window_8384.md)

   Creates a new window. The new window displays the same document with the same viewers and viewpoints than the window to which the method applies, and becomes the active one.

**Example:**      This example creates a new window named `CADNewWindow` from the `CADWindow` window.

```VBScript
     Dim CADNewWindow As Window
     Set CADNewWindow = CADWindow.NewWindow()

```

### Sub **PrintOut**( )

   Prints the active viewer of the window according to the window's page setup on the default printer.

**Example:**      This example prints the `CADWindow` window's active viewer on the default printer.

```VBScript
     CADWindow.PrintOut()

```

### Sub **PrintToFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `fileName`)

   Prints the active viewer of the window according to the window's page setup in a file instead of being sent to a printer.

**Parameters:**

` fileName`      The full pathname of the file receiving the data.  **Example:**      This example prints the `CADWindow` window's active viewer in a file.

```VBScript
     CADWindow.PrintToFile("e:\temp\cadwin.prn")

```