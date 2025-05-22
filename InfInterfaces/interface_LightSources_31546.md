# LightSources (Collection)

**_A collection of all the LightSource objects._**
This collection is currently managed by a [Viewer3D](../InfInterfaces/interface_Viewer3D_12290.md) object.

## Methods

### Func **Add**( ) As [CATIALightSource](../InfInterfaces/interface_LightSource_26277.md)

Adds a new light source to the LightSources collection.  **Example:**      The following adds a light source to the collection attached to the active viewer. This viewer must be a @see Viewer3D object.

```VBScript
Dim MyViewer As Viewer
Set MyViewer = CATIA.ActiveWindow.ActiveViewer
Dim MyLightSource As LightSource
Set MyLightSource = MyViewer.LightSources.Add

```

### Func **Item**( long  `iIndex`) As [CATIALightSource](../InfInterfaces/interface_LightSource_26277.md)

Returns a light source from its index in the LightSources collection.

**Parameters:**

` iIndex`      The index of the light source to retrieve in the collection of light sources. Compared with other collections, you cannot use the name of the light source as argument.
**Returns:**      The retrieved light source  **Example:**      The following example returns in `MyLightSource` the sixth light source in the collection.

```VBScript
Dim MyLightSource As LightSource
Set MyLightSource = LightSources.Item(6)

```

### Sub **Remove**( long  `iIndex`)

Removes a light source from the LightSources collection.

**Parameters:**

` iIndex`      The index of the light source to remove. Compared with other collections, you cannot use the name of the light source as argument.  **Example:**      The following example removes the second light source in the collection attached to the active viewer. This viewer must be a
[Viewer3D](../InfInterfaces/interface_Viewer3D_12290.md) object.

```VBScript
Dim MyViewer As Viewer
Set MyViewer = CATIA.ActiveWindow.ActiveViewer
MyViewer.LightSources.Remove(2)

```