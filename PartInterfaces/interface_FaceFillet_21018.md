# FaceFillet (Object)

**_Represents the face fillet shape._**
A face fillet shape is built between two faces with a fillet radius.

## Properties

### Property **FirstFace**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first limiting face.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [Face](../MecModInterfaces/interface_Face_3398.md).

**Example:**     The following example returns in `face1` the first limiting face of the face fillet `firstFaceFillet`, and then sets it to `NewFace1`:

```VBScript
Set face1 = firstFaceFillet.FirstFace
firstFaceFillet.FirstFace = NewFace1

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the face fillet radius.

**Example:**     The following example returns in `radius` the fillet radius of the face fillet `firstFaceFillet`:

```VBScript
Set radius = firstFaceFillet.Radius

```

### Property **SecondFace**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the second limiting face.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [Face](../MecModInterfaces/interface_Face_3398.md).

**Example:**     The following example returns in `face2` the second limiting face of the face fillet `firstFaceFillet`, and then sets it to `NewFace2`:

```VBScript
Set face2 = firstFaceFillet.SecondFace
firstFaceFillet.SecondFace = NewFace2

```