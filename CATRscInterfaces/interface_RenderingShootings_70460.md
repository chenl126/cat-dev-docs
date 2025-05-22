# RenderingShootings (Collection)

**_A collection of all the Rendering Shootings objects._**

## Methods

### Func **Add**( ) As [CATIARenderingShooting](../CATRscInterfaces/interface_RenderingShooting_62481.md)

Adds a new shooting to the shootings collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIARenderingShooting](../CATRscInterfaces/interface_RenderingShooting_62481.md)

Returns a renderingshooting index in the renderingshootings collection.

**Parameters:**

` iIndex`      The index of the shooting to retrieve in the collection of shootings. Compared with other collections, you cannot use the name of the shooting as argument.
**Returns:**      The retrieved shooting  **Example:**      The following example returns in `MyShooting` the sixth shooting in a shootings collection.

```VBScript
Dim MyShooting As RenderingShooting
Set MyShooting = RenderingShootings.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a shooting from the shootings collection.  
### Sub **RemoveAll**( )

Removes all shootings from the collection.