# Boundary (Object)

**_Topological cell, such as a face, an edge or a vertex._**

**Role** : The Boundary objects are basic topological objects, such as the edge of a Pad. Some of them posess a geometrical feature (_planar_ face, _rectilinear_ edge). You will create a Boundary object (such as the [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) object, which is derived, indirectly, from the Boundary object) using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewEdgeFilletWithConstantRadius](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewEdgeFilletWithConstantRadius) ). Note that, regarding V4 sub-elements, once the data of a CATIA Version 4 Model has been copied to a .CATPart, the sub-elements of the resulting .CATPart are supported by the [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. The lifetime of a Boundary object is limited. In particular, after having call [Part.Update](../MecModInterfaces/interface_Part_3788.htm#Update) , the Boundary objects are usually no more valid. **See also:**

  * [Face](../MecModInterfaces/interface_Face_3398.md) , [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md)
  * [Edge](../MecModInterfaces/interface_Edge_3456.md) , [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) , [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) , [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) , [MonoDimFeatEdge](../MecModInterfaces/interface_MonoDimFeatEdge_44932.md) , [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md)
  * [Vertex](../MecModInterfaces/interface_Vertex_8466.md) , [TriDimFeatVertexOrBiDimFeatVertex](../MecModInterfaces/interface_TriDimFeatVertexOrBiDimFeatVertex_221087.md) , [NotWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_NotWireBoundaryMonoDimFeatVertex_212840.md), [ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex_474398.md)

**Note:** [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects cannot be selected into the specification tree.

**Note:** For a [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object, the object returned by the [AnyObject.Parent](../System/interface_AnyObject_17321.htm#Parent) property is the master shape. For example, if we have:

```VBScript
                             Pad.2
                              !
                              !
     +                        V
     !                      +---+
     !                    /   / !
     +-- Pad.1          /   /   !
     !                /   / one +------+
     !               +---+    /       /! <--- Pad.1
     !               !   !  /       /  +
     +-- Pad.2       !   !/       /   /
                     !   +------+   /
                     !          ! /
                     +----------+

```

then, for the [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) number "one", the [AnyObject.Parent](../System/interface_AnyObject_17321.htm#Parent) property returns the Pad.2 automation object (see [Pad](../PartInterfaces/interface_Pad_1979.md) ).

**Example:**      This example asks the end user to select an edge (using the [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) object), and creates an edge fillet on this edge:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select an edge
     InputObjectType(0)="TriDimFeatEdge"
     Status=Selection.SelectElement2(InputObjectType,"Select an edge",true)
     if (Status = "cancel") then Exit Sub
     Set EdgeFillet = ShapeFactory.AddNewEdgeFilletWithConstantRadius(Selection.Item(1).Value,1,5.0)
     EdgeFillet.EdgePropagation = 1
     Document.Part.Update

```