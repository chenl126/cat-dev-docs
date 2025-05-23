# SpecsViewer (Object)

**_Represents the specification tree viewer._**
This viewer displays the document's specification tree according to the chosen layout, and can only be included in a SpecsAndGeomWindow object.

**See also:**      [CatSpecsLayout](../InfInterfaces/enum_CatSpecsLayout_42356.md), [SpecsAndGeomWindow](../InfInterfaces/interface_SpecsAndGeomWindow_67760.md)

## Properties

### Property **Layout**(| ) As [CatSpecsLayout](../InfInterfaces/enum_CatSpecsLayout_42356.md)

   Returns or sets the specification tree layout.

**Example:**      This example sets the specification tree layout for the `SpecsTreeViewer` specification tree viewer to `catSpecsViewerHorizontalCentered`.

```VBScript
     SpecsTreeViewer.Layout = catSpecsViewerHorizontalCentered

```