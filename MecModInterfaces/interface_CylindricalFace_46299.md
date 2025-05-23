# CylindricalFace (Object)

**_2-D boundary with a cylindrical geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the lateral face of a cylinder. You will create a CylindricalFace object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewCircPattern](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewCircPattern) ). The lifetime of a CylindricalFace object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a shape to pattern and a cylindrical face, and creates a circular pattern of the shape. The cylindrical face specifies the rotation axis.

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select the shape to pattern
     InputObjectType(0)="SketchBasedShape"
     Status=Selection.SelectElement2(InputObjectType,"Select the shape to pattern",true)
     if (Status = "cancel") then Exit Sub
     Set Shape = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the cylindrical face
     InputObjectType(0)="CylindricalFace"
     Status=Selection.SelectElement2(InputObjectType,"Select the cylindrical face",true)
     if (Status = "cancel") then Exit Sub
     Set CylindricalFace = Selection.Item(1).Value
     Set RotationCenter = Document.Part.CreateReferenceFromName("")
     Set CircPattern = ShapeFactory.AddNewCircPattern(Shape,1,4,20.0,45.0,1,4,RotationCenter,CylindricalFace,True,0.0,True)
     Document.Part.Update

```

## Methods

### Sub **GetDirection**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oDirection`)

   Returns the direction of the cylindrical face axis

**Parameters:**

` oDirection[0]`      The X Coordinate of the axis direction
` oDirection[1]`      The Y Coordinate of the axis direction
` oDirection[2]`      The Z Coordinate of the axis direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the cylindrical face axis.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the axis origin
` oOrigin[1]`      The Y Coordinate of the axis origin
` oOrigin[2]`      The Z Coordinate of the axis origin