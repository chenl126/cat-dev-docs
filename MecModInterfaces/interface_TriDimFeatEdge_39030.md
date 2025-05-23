# TriDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is three dimensional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a Pad. You will create a TriDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewEdgeFilletWithConstantRadius](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewEdgeFilletWithConstantRadius) ). The lifetime of a TriDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select an edge, and creates an edge fillet on this edge:

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