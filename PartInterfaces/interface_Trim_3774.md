# Trim (Object)

**_Represents the Trim, or union trim boolean operation._**
It is performed between a body and the current shape.

## Methods

### Sub **AddFaceToKeep**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iFaceToKeep`)

   Adds a new face to be kept (if face is not divided by operation).

**Parameters:**

` iFaceToKeep`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to Keep for the Trim `firstTrim`:

```VBScript
     call firstTrim.AddFaceToKeep(face)

```

### Sub **AddFaceToKeep2**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToKeep`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceAdjacentForKeep`)

   Adds a new face to be kept (if face is divided by operation).

**Parameters:**

` iFaceToKeep`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iFaceAdjacentForKeep`      An adjacent face of iFaceToKeep belonging to the other operand
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to Keep for the Trim `firstTrim`:

```VBScript
     call firstTrim.AddFaceToKeep(face)

```

### Sub **AddFaceToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`)

   Adds a new face to be Removed (if face not divided by operation).

**Parameters:**

` iFaceToRemove`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to Remove for the Trim `firstTrim`:

```VBScript
     call firstTrim.AddFaceToRemove(face)

```

### Sub **AddFaceToRemove2**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceAdjacentForRemove`)

   Adds a new face to be Removed (if face is divided by operation).

**Parameters:**

` iFaceToRemove`      The new face to process
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iFaceAdjacentForRemove`      An adjacent face of iFaceToRemove belonging to the other operand
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example adds the new face `face` to Remove for the Trim `firstTrim`:

```VBScript
     call firstTrim.AddFaceToRemove(face)

```

### Sub **WithdrawFaceToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`)

   Withdraws an existing Kept face (if face is not divided by operation) .

**Parameters:**

` iFaceToWithdraw`      The face to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example withdraws the existing `face` Kept face from the Trim `firstTrim`:

```VBScript
     call firstTrim.WithdrawFaceToKeep(face)

```

### Sub **WithdrawFaceToKeep2**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceAdjacentForKeep`)

   Withdraws an existing Kept face (if face is divided by operation).

**Parameters:**

` iFaceToWithdraw`      The face to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iFaceAdjacentForKeep`      An adjacent face of iFaceToKeep belonging to the other operand
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example withdraws the existing `face` Kept face from the Trim `firstTrim`:

```VBScript
     call firstTrim.WithdrawFaceToKeep(face)

```

### Sub **WithdrawFaceToRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`)

   Withdraws an existing Removed face (if face not divided by operation).

**Parameters:**

` iFaceToWithdraw`      The face to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example withdraws the existing `face` Removed face from the Trim `firstTrim`:

```VBScript
     call firstTrim.WithdrawFaceToRemove(face)

```

### Sub **WithdrawFaceToRemove2**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToWithdraw`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceAdjacentForRemove`)

   Withdraws an existing Removed face (if face is divided by operation).

**Parameters:**

` iFaceToWithdraw`      The face to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iFaceAdjacentForRemove`      An adjacent face of iFaceToRemove belonging to the other operand
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example withdraws the existing `face` Removed face from the Trim `firstTrim`:

```VBScript
     call firstTrim.WithdrawFaceToRemove(face)

```