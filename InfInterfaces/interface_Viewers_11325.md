# Viewers (Collection)

**_A collection of all the Viewer objects currently attached to a window._**
For a [SpecsAndGeomWindow](../InfInterfaces/interface_SpecsAndGeomWindow_67760.md) object, the viewer containing the geometry is the first viewer, and the viewer containing the specification tree is the second viewer.

## Methods

### Func **Item**( long  `iIndex`) As [CATIAViewer](../InfInterfaces/interface_Viewer_8284.md)

Returns a viewer using its index from the Viewers collection. The first item has the rank 1 in the collection.

**Parameters:**

` iIndex`      The index or the name of the viewer to retrieve from the collection of viewers. As a numerics, this index is the rank of the viewer in the collection. The index of the first viewer in the collection is 1, and the index of the last viewer is Count. As a string, it is the name you assigned to the viewer using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved viewer  **Example:**      This example returns in `MyViewer` the second viewer in the collection.

```VBScript
Dim MyViewer As Viewer
Set MyViewer = Viewer.Item(2)

```