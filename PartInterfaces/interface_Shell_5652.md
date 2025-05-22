# Shell (Object)

**_Represents the shell shape._**
A shell shape is made up of a list of faces to process and two thickness parameters.

## Properties

### Property **ExternalThickness**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the shell external thickness.

**Example:**     The following example returns in `extThick` the external thickness of the shell `firstShell`:

```VBScript
Set extThick = firstShell.ExternalThickness

```

### Property **FacesToRemove**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns the collection of faces to be removed by the shell process.

**Example:**     The following example returns in `list` the faces to be removed from the shell `firstShell`:

```VBScript
Set list = firstShell.FacesToRemove

```

### Property **InternalThickness**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the shell internal thickness.

**Example:**     The following example returns in `intThick` the internal thickness of the shell `firstShell`:

```VBScript
Set intThick = firstShell.InternalThickness

```

Methods

### Sub **AddFaceToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`)

Adds a new face to those to be removed by the shell process.

**Parameters:**

` iFaceToRemove`      The face to be removed
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new `face` face to be removed in the shell `firstShell`:

```VBScript
call firstShell.AddFaceToRemove(face)

```

### Sub **AddFaceWithDifferentThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToThicken`)

Adds a new face to be thicken with different offset values.

**Parameters:**

` iFaceToThicken`      The face to be thicken with different offset values
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new `face` face to be thicken with different offset values in the shell `firstShell`:

```VBScript
call firstShell.AddFaceWithDifferentThickness(face)

```

### Sub **RemoveFaceWithDifferentThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`)

Removes an existing face from those to be thicken with different offset values by the shell process.

**Parameters:**

` iFaceToRemove`      The face to be removed from the shell specifications
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example removes the `face` face from the list of faces in the shell `firstShell`:

```VBScript
call firstShell.RemoveFaceWithDifferentThickness(face)

```

### Sub **SetVolumeSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`)

Set the Support Volume of the faces to modify during Shell operation.  
### Sub **WithdrawFaceToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`)

Withdraws an existing face from those to be removed by the shell process.

**Parameters:**

` iFaceToWithdraw`      The face to be withdrawn from the shell
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example removes the `face` face from the list of faces in the shell `firstShell`:

```VBScript
call firstShell.WithdrawFaceToRemove(face)

```