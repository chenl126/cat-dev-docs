# Vertex (Object)

**_0-D boundary._**
**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the corner of a Pad resulting from the extrusion of a square. You will create an Vertex object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewLinePtPt](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewLinePtPt) ). The lifetime of a Vertex object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[TriDimFeatVertexOrBiDimFeatVertex](../MecModInterfaces/interface_TriDimFeatVertexOrBiDimFeatVertex_221087.md) , [NotWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_NotWireBoundaryMonoDimFeatVertex_212840.md) , [ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex_474398.md) .

**Example:**      This example asks the end user to select successively two vertices. Then, it creates a line between these two vertices.

```VBScript
Dim InputObjectType(0)
Set Document = CATIA.ActiveDocument
Set Selection = Document.Selection
Set HybridBodies = Document.Part.HybridBodies
Set HybridBody = HybridBodies.Item("Geometrical Set.1")
'We propose to the user that he select the first vertex
InputObjectType(0)="Vertex"
Status=Selection.SelectElement2(InputObjectType,"Select the first vertex",true)
if (Status = "cancel") then Exit Sub
Set FirstVertex = Selection.Item(1).Value
Selection.Clear
'We propose to the user that he select the second vertex
InputObjectType(0)="Vertex"
Status=Selection.SelectElement2(InputObjectType,"Select the second vertex",true)
if (Status = "cancel") then Exit Sub
Set SecondVertex = Selection.Item(1).Value
Set hybridShapeLinePtPt = HybridShapeFactory.AddNewLinePtPt(FirstVertex,SecondVertex)
HybridBody.AppendHybridShape hybridShapeLinePtPt
Document.Part.InWorkObject = hybridShapeLinePtPt
Document.Part.Update

```