# PlanarFace (Object)

**_2-D boundary with a planar geometry._**
**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the face of a cube. You will create a PlanarFace object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewDraft](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewDraft) ). The lifetime of a PlanarFace object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a face and two planar faces, and creates a draft on these faces:

```VBScript
Dim InputObjectType(0)
Set Document = CATIA.ActiveDocument
Set Selection = Document.Selection
'We propose to the user that he select the face to draft
InputObjectType(0)="Face"
Status=Selection.SelectElement2(InputObjectType,"Select the face to draft",true)
if (Status = "cancel") then Exit Sub
Set FaceToDraft = Selection.Item(1).Value
Selection.Clear
'We propose to the user that he select the neutral face
InputObjectType(0)="PlanarFace"
Status=Selection.SelectElement2(InputObjectType,"Select the neutral face",true)
if (Status = "cancel") then Exit Sub
Set NeutralFace = Selection.Item(1).Value
Selection.Clear
'We propose to the user that he select the parting element
InputObjectType(0)="PlanarFace"
Status=Selection.SelectElement2(InputObjectType,"Select the parting element",true)
if (Status = "cancel") then Exit Sub
Set PartingElement = Selection.Item(1).Value
Set Draft = ShapeFactory.AddNewDraft(FaceToDraft,NeutralFace,0,PartingElement,0.0,0.0,1.0,0,5.0,0)
Set DraftDomains = Draft.DraftDomains
Set DraftDomain = DraftDomains.Item(1)
DraftDomain.SetPullingDirection 0.0, 0.0,1.0
Document.Part.Update

```

## Methods

### Sub **GetFirstAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFirstAxis`)

Returns the planar face first axis

**Parameters:**

` oFirstAxis[0]`      The X Coordinate of the planar face first axis
` oFirstAxis[1]`      The Y Coordinate of the planar face first axis
` oFirstAxis[2]`      The Z Coordinate of the planar face first axis

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

Returns the origin of the planar face.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the planar face origin
` oOrigin[1]`      The Y Coordinate of the planar face origin
` oOrigin[2]`      The Z Coordinate of the planar face origin

### Sub **GetSecondAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSecondAxis`)

Returns the planar face second axis.

**Parameters:**

` oSecondAxis[0]`      The X Coordinate of the planar face second axis
` oSecondAxis[1]`      The Y Coordinate of the planar face second axis
` oSecondAxis[2]`      The Z Coordinate of the planar face second axis