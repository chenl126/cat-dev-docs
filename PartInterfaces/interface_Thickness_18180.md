# Thickness (Object)

**_Represents the thickness shape._**
The thickness shape is made up of a collection of faces to process and an offset parameter.

## Properties

### Property **FacesToThicken**(| ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the collection of faces to be thickened.

**Example:**     The following example returns in `list` the list of faces of the thickness `firstThickness`:

```VBScript
     Set list = firstThickness.FacesToThicken

```

### Property **Offset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the thickness offset.

**Example:**     The following example returns in `offset` the offset of the thickness `firstThickness`:

```VBScript
     Set offset = firstThickness.Offset

```

Methods

### Sub **AddFaceToThicken**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToThicken`)

   Adds a new face to be thickened.

**Parameters:**

` iFaceToThicken`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to thicken for the thickness `firstThickness`:

```VBScript
     call firstThickness.AddFaceToThicken(face)

```

### Sub **AddFaceWithDifferentThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToThicken`)

   Adds a new face to thicken with a different offset value.

**Parameters:**

` iFaceToThicken`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to thicken with a different offset value for the thickness `firstThickness`:

```VBScript
     call firstThickness.AddFaceWithDifferentThickness(face)

```

### Sub **RemoveFaceWithDifferentThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`)

   Removes an existing thickened face.

**Parameters:**

` iFaceToRemove`      The face to remove
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example removes the existing `face` thickened face from the thickness `firstThickness`:

```VBScript
     call firstThickness.RemoveFaceWithDifferentThickness(face)(face)

```

### Sub **SetVolumeSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`)

   Set support of Thickness feature.  
### Sub **WithdrawFaceToThicken**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`)

   Withdraws an existing thickened face.

**Parameters:**

` iFaceToWithdraw`      The face to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example withdraws the existing `face` thickened face from the thickness `firstThickness`:

```VBScript
     call firstThickness.WithdrawFaceToThicken(face)

```