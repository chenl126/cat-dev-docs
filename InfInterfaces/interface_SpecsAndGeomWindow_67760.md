# SpecsAndGeomWindow (Object)

**_Represents a window featuring a specification viewer and a geometry viewer._**
The specification viewer is located in the left part of the window and displays the document's specification tree. The geometry viewer is located in the right part of the window and displays the document's geometry, and can thus be a Viewer2D or a Viewer3D, according to the document type. Even if generally the two viewers are simultaneously displayed, one viewer or the other can be hidden thanks to the CatSpecsAndGeomWindowLayout enumeration.

**See also:**      [CatSpecsAndGeomWindowLayout](../InfInterfaces/enum_CatSpecsAndGeomWindowLayout_152411.md)

## Properties

### Property **Layout**(| ) As [CatSpecsAndGeomWindowLayout](../InfInterfaces/enum_CatSpecsAndGeomWindowLayout_152411.md)

   Returns or sets the specification and geometry window layout.

**Example:**      This example sets the specification and geometry window layout for the `MyCADWindow` window to `catWindowGeomOnly`.

```VBScript
     MyCADWindow.Layout = catWindowGeomOnly

```

### Property **SpecsViewer**( ) As [CATIASpecsViewer](../InfInterfaces/interface_SpecsViewer_26446.md) (Read Only)

   Returns the specifications viewer.

**Example:**      This example retrieves the specification viewer for the `MyCADWindow` window.

```VBScript
     Dim MyViewer As Viewer
     Set MyViewer = MyCADWindow.SpecsViewer

```