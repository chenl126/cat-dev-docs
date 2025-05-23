# Face (Object)

**_2-D boundary._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the lateral face of cylinder. You will create a Face object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewFaceFillet](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewFaceFillet) ). The lifetime of a Face object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md) .

**Example:**      This example asks the end user to select two faces, and creates a face-face fillet on these faces:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select the first face
     InputObjectType(0)="Face"
     Status=Selection.SelectElement2(InputObjectType,"Select the first face",true)
     if (Status = "cancel") then Exit Sub
     Set FirstFace = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the second face
     InputObjectType(0)="Face"
     Status=Selection.SelectElement2(InputObjectType,"Select the second face",true)
     if (Status = "cancel") then Exit Sub
     Set SecondFace = Selection.Item(1).Value
     Set FaceFillet = ShapeFactory.AddNewFaceFillet(FirstFace,SecondFace,5.0)
     Document.Part.Update

```