# RenderingLights (Collection)

**_A collection of all the Rendering Lights objects._**

## Methods

### Func **Add**( ) As [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)

Adds a new light to the lights collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingLight](../CATRscInterfaces/interface_RenderingLight_41764.md)

Returns a rendering light index in the rendering light collection.

**Parameters:**

` iIndex`      The index of the light to retrieve in the collection of lights. Compared with other collections, you cannot use the name of the light as argument.
**Returns:**      The retrieved light  **Example:**      The following example returns in `MyLight` the sixth light in a lights collection.

```VBScript
Dim MyLight As RenderingLight
Set MyLight = RenderingLights.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a light from the lights collection.  
### Sub **RemoveAll**( )

Removes all lights from the collection.