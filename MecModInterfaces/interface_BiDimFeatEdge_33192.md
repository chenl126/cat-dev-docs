# BiDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is two dimensional._**
**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a surface obtained through the extrusion of a spline. You will create a BiDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewPointOnCurveFromDistance](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewPointOnCurveFromDistance) ). The lifetime of a BiDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select an edge, and creates a point on this edge. Here, both TriDimFeatEdge and BiDimFeatEdge objects are proposed to the user.

```VBScript
Dim InputObjectType(1)
Set Document = CATIA.ActiveDocument
Set Selection = Document.Selection
Set HybridBodies = Document.Part.HybridBodies
Set HybridBody = HybridBodies.Item("Geometrical Set.1")
'We propose to the user that he select an edge
InputObjectType(0)="TriDimFeatEdge"
InputObjectType(1)="BiDimFeatEdge"
Status=Selection.SelectElement2(InputObjectType,"Select an edge",true)
if (Status = "cancel") then Exit Sub
Set Curve = Selection.Item(1).Value
Set HybridShapePointOnCurve = HybridShapeFactory.AddNewPointOnCurveFromDistance(Curve,18.0,False)
HybridBody.AppendHybridShape HybridShapePointOnCurve
Document.Part.InWorkObject = HybridShapePointOnCurve
Document.Part.Update

```