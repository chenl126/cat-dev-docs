# Edge (Object)

**_1-D boundary._**
**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a cylinder. You will create an Edge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewPointTangent](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewPointTangent) ). The lifetime of an Edge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) , [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) , [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) , [MonoDimFeatEdge](../MecModInterfaces/interface_MonoDimFeatEdge_44932.md) , [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md) .

**Example:**      This example asks the end user to select a planar curve, whose plane is parallel to the XY plane. Then, it creates a point on the tangent to the curve in the X direction:

```VBScript
Dim InputObjectType(0)
Set Document = CATIA.ActiveDocument
Set Selection = Document.Selection
Set HybridBodies = Document.Part.HybridBodies
Set HybridBody = HybridBodies.Item("Geometrical Set.1")
'We propose to the user that he select a planar curve whose plane is parallel to the XY plane
InputObjectType(0)="Edge"
Status=Selection.SelectElement2(InputObjectType,"Select a planar curve whose plane is parallel to the XY plane",true)
if (Status = "cancel") then Exit Sub
Set PlanarCurve = Selection.Item(1).Value
Set HybridShapeDirection = HybridShapeFactory.AddNewDirectionByCoord(1.0,0.0,0.0)
Set HybridShapePointTangent = HybridShapeFactory.AddNewPointTangent(PlanarCurve,HybridShapeDirection)
HybridBody.AppendHybridShape HybridShapePointTangent
Document.Part.InWorkObject = HybridShapePointTangent
Document.Part.Update

```