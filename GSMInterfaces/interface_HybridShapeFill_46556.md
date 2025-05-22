# HybridShapeFill (Object)

**_The Fill feature : an Fill is made up of a face to process and one Fill parameter._**

## Properties

### Property **Constraint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the passing point for the Fill.

**Example** :      This example retrieves in `Element` the passing point for the `Fill` hybrid shape feature.

```VBScript
Dim Element As Reference
Set Element = Fill.Constraint

```

### Property **Continuity**( ) As long

Returns or sets the continuity between the support and fill.
**Legal values** :

0
    Continuity in point (C0)
1
    Continuity in tangency (C1)
2
    Continuity in curvature (C2)

**Example** :      This example retrieves in `oContinuity` the continuity type for the `Fill` hybrid shape feature.

```VBScript
Dim oContinuity
Set oContinuity = Fill.Continuity

```

### Property **MaximumDeviationValue**( ) As double

Sets or Gets the maximum deviation allowed for smoothing operation in fill commnd. This value must be set in SI unit (m).

**Example** : This example retrieves in `DeviationValue` the maximum deviation value for the `Fill` hybrid shape feature.

```VBScript
Dim DeviationValue As double
Set DeviationValue = Fill.MaximumDeviationValue

```

### Property **PlaneOnlyMode**( ) As boolean

Returns or sets whether Planar Boundaries only should be considered during fill operation.
**Legal values** :

TRUE
    Planar boundaries are only considered during Fill operation
FALSE
    Non-Planar boundaries are also considered during Fill operation

### Property **TolerantMode**( ) As boolean

Returns or sets the Tolerant mode option. **Role** : To activate or not the tolerant mode option TRUE : Tolerant mode is active. Uses deviation parameter to do tolerant fill. FALSE : Tolerant mode is not active.

**Example** : This example retrieves in `tolMode` the tolerant mode for the `Fill` hybrid shape feature.

```VBScript
Dim tolMode As boolean
Set tolMode = Fill.TolerantMode

```

Methods

### Sub **AddBound**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`)

Adds an boundary to the hybrid shape fill feature object.

**Parameters:**

` iBoundary`      The boundary(curve) to be added to the hybrid shape fill feature object.  **Example** :      The following example adds the `iBoundary` curve to the `Fill` object.

```VBScript
Fill.AddBound iBoundary

```

### Sub **AddSupportAtBound**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

Inserts the support at specified boundary in the Fill.

**Parameters:**

` iBoundary`      Reference of the boundary object to which support has to be added.
` iSupport`      Reference of the support object to be added.

**Example** :      This example adds supports in the Fill feature `Fill` to specified `iBoundary` boundary

```VBScript
Fill.AddSupportAtBound iBoundary,iSupport

```

### Sub **AppendConstraint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iConstraint`)

Appends an constraint to the hybrid shape fill feature object.

**Parameters:**

` iConstraint`      The constraint to be appended.  **Example** :      The following example appends the `iConstraint` constraint to the `Fill` object.

```VBScript
Fill.AppendConstraint iConstraint

```

### Func **GetBoundAtPosition**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves the boundary at specified position in the hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the boundary to retrieve.  **Example** :      The following example gets the `oBoundary` boundary of the `Fill` object at the position `iPos`.

```VBScript
Dim oBoundary As Reference
Set oBoundary = Fill.GetBoundAtPosition (iPos).

```

### Func **GetBoundPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`) As long

Retrieves the position of a boundary used by the hybrid shape fill feature object.

**Parameters:**

` iBoundary`      The boundary whose position has to be retrieved.  **Example** :      The following example gets the `oPos` position of the `iBoundary` boundary in the `Fill` object.

```VBScript
Dim oPos As  long
oPos = Fill.GetBoundPosition (iBoundary).

```

### Func **GetBoundSize**( ) As long

Returns the number of boundaries in the Fill object.

**Parameters:**

` oSize`      Number of boundaries in the Fill.

**Example** :      This example retrieves the number of boundaries in the `Fill` hybrid shape fill.

```VBScript
Dim oSize As  long
oSize = Fill.GetBoundSize

```

### Func **GetBoundaryContinuity**( long  `iPos`) As long

Returns the continuity mode for a boundary at specified position in the Fill.

**Parameters:**

` iPos`      Position at which the continuity should be retrieved.
` oContinuity`      Continuity retrieved between the support and the fill.
**Legal values** :

0
    Continuity in point (C0)
1
    Continuity in tangency (C1)
2
    Continuity in curvature (C2)
**Example** :      This example retrieves in `oContinuity` the continuity at the specified position of `Fill` hybrid shape fill feature.

```VBScript
oContinuity = Fill.GetBoundaryContinuity iPos

```

### Func **GetConstraintAtPosition**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves the constraint at specified position in the hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the constraint to retrieve.  **Example** :      The following example gets the `oConstraint` constraint of the `Fill` object at the position `iPos`.

```VBScript
Dim oConstraint As Reference
Set oConstraint = Fill.GetConstraintAtPosition (iPos).

```

### Func **GetConstraintsSize**( ) As long

Returns the number of constraints in the Fill object.

**Parameters:**

` oSize`      Number of constraints in the Fill.

**Example** :      This example retrieves the number of constraints in the `Fill` hybrid shape fill.

```VBScript
Dim oSize As  long
oSize = Fill.GetConstraintsSize

```

### Func **GetSupportAtPosition**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Retrieves the support at specified position in the hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the support to retrieve.  **Example** :      The following example gets the `oSupport` support of the `Fill` object at the position `iPos`.

```VBScript
Dim oSupport As Reference
Set oSupport = Fill.GetSupportAtPosition (iPos).

```

### Sub **InsertBoundAfterPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`,  long  `iPos`)

Inserts the boundary after specified position in the Fill.

**Parameters:**

` iBoundary`      Reference of the boundary object to be inserted.
` iPos`      Position after which the element should be inserted.

**Example** :      This example inserts the boundary in the Fill feature `Fill` after position `iPos`

```VBScript
Fill.InsertBoundAfterPosition iBoundary,iPos

```

### Sub **RemoveAllBound**( )

Removes all boundaries of the hybrid shape fill feature object.  **Example** :      The following example removes all boundaries of the `Fill` object.

```VBScript
Fill.RemoveAllBound

```

### Sub **RemoveBoundAtPosition**( long  `iPos`)

Removes boundary at specified position in hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the boundary to remove.  **Example** :      The following example removes the boundary object from the `Fill` object at the position `iPos`.

```VBScript
Fill.RemoveBoundAtPosition iPos.

```

### Sub **RemoveConstraint**( long  `iPos`)

Removes constraint at specified position in hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the constraint to remove.  **Example** :      The following example removes the constraint object from the `Fill` object at the position `iPos`.

```VBScript
Fill.RemoveConstraint iPos.

```

### Sub **RemoveSupportAtPosition**( long  `iPos`)

Removes support at specified position in hybrid shape fill feature object.

**Parameters:**

` iPos`      The position of the support to remove.  **Example** :      The following example removes the support object from the `Fill` object at the position `iPos`.

```VBScript
Fill.RemoveSupportAtPosition iPos.

```

### Sub **ReplaceBoundAtPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`,  long  `iPos`)

Replaces the boundary at specified position in the Fill.

**Parameters:**

` iBoundary`      Reference of the boundary object to be replaced.
` iPos`      Position at which the boundary should be replaced.

**Example** :      This example replaces the boundary in the Fill feature `Fill` at specified position `iPos`

```VBScript
Fill.ReplaceBoundAtPosition iBoundary,iPos

```

### Sub **ReplaceConstraint**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iConstraint`)

Replaces the constraint at specified position in the Fill.

**Parameters:**

` iPos`      Position at which the constraint should be replaced.
` iConstraint`      Reference of the constraint object to be replaced.

**Example** :      This example replaces the constraint in the Fill feature `Fill` at specified position `iPos`

```VBScript
Fill.ReplaceConstraint iPos,iConstraint

```

### Sub **ReplaceSupportAtPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iPos`)

Replaces the support at specified position in the Fill.

**Parameters:**

` iSupport`      Reference of the support object to be replaced.
` iPos`      Position at which the support should be replaced.

**Example** :      This example replaces the support in the Fill feature `Fill` at specified position `iPos`

```VBScript
Fill.ReplaceSupportAtPosition iSupport,iPos

```

### Sub **SetBoundaryContinuity**( long  `iContinuity`,  long  `iPos`)

Sets the continuity mode for a boundary at specified position in the Fill.

**Parameters:**

` iContinuity`      Continuity between the support and the fill.
**Legal values** :

0
    Continuity in point (C0)
1
    Continuity in tangency (C1)
2
    Continuity in curvature (C2)
` iPos`      Position at which the continuity should be set.

**Example** :      This example sets the continuity in the Fill feature `Fill` at specified position `iPos`

```VBScript
Fill.SetBoundaryContinuity iContinuity,iPos

```