# RectilinearTriDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is three dimensional, the boundary having a rectilinear geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a Pad resulting from the extrusion of a square. You will create a RectilinearTriDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [Hole.SetDirection](../PartInterfaces/interface_Hole_3612.htm#SetDirection) ). The lifetime of a RectilinearTriDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a face, a rectilinear edge, and creates a hole. The rectilinear edge specifies the hole direction. It may be a RectilinearTriDimFeatEdge, a RectilinearBiDimFeatEdge or a RectilinearMonoDimFeatEdge.

```VBScript
     Dim EnabledObjectSelection1(0)
     Dim EnabledObjectSelection2(2)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select a face
     EnabledObjectSelection1(0)="Face"
     Status=Selection.SelectElement2(EnabledObjectSelection1,"Select a face",true)
     if (Status = "cancel") then Exit Sub
     Set Face = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the hole direction
     EnabledObjectSelection2(0)="RectilinearTriDimFeatEdge"
     EnabledObjectSelection2(1)="RectilinearBiDimFeatEdge"
     EnabledObjectSelection2(2)="RectilinearMonoDimFeatEdge"
     Status=Selection.SelectElement2(EnabledObjectSelection2,"Select the hole direction",true)
     if (Status = "cancel") then Exit Sub
     Set Hole = ShapeFactory.AddNewHoleFromPoint(20.0,-5.5, 1.07,Face,10.0)
     Hole.ThreadingMode = 1
     Hole.ThreadSide = 0
     Hole.SetDirection Selection.Item(1).Value
     Document.Part.Update

```

## Methods

### Sub **GetDirection**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oDirection`)

   Returns the direction of the rectilinear edge

**Parameters:**

` oDirection[0]`      The X Coordinate of the direction
` oDirection[1]`      The Y Coordinate of the direction
` oDirection[2]`      The Z Coordinate of the direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the the rectilinear edge.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the rectilinear edge origin
` oOrigin[1]`      The Y Coordinate of the rectilinear edge origin
` oOrigin[2]`      The Z Coordinate of the rectilinear edge origin