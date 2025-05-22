# Revolution (Object)

**_Represents the revolution-based shapes._**
It is the base objects for shaft and grooves.

**See also:**      [Shaft](../PartInterfaces/interface_Shaft_5650.md), [Groove](../PartInterfaces/interface_Groove_8300.md)

## Properties

### Property **FirstAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the revolution first angle. This angle is computed around the revolution axis, starting from the sketch plane trace on the plane perpendicular to the revolution axis, and is counted positive clockwise when looking at this plane in the revolution axis direction.

**Example:**     The following example returns in `firstAngle` the first angle of the `MyRevolution` revolution object:

```VBScript
Set firstAngle = MyRevolution.FirstAngle

```

### Property **IsThin**( ) As boolean

Returns the Revol thin flag.
It returns TRUE if the Revol is a thin Revol , FALSE if not.

**Returns:**      oIsThin The thin flag as a boolean

**Example:**     The following example saves in `thinFlag` the thin flag of Revol `firstRevol`, and then sets it so that it will be now thin :

```VBScript
Set thinFlag = firstRevol.IsThin
firstRevol.IsThin = TRUE

```

### Property **MergeEnd**( ) As boolean

Returns the Revol merge end flag (for thin Revol only).
It returns TRUE if merge ends is required , FALSE if not.

**Returns:**      oIsMergeEnd The merge end flag as a boolean

**Example:**     The following example saves in `MergeEndFlag` the merge end flag of Revol `firstRevol`, and then sets it so that merge end will be required :

```VBScript
Set MergeEndFlag = firstRevol.IsMergeEnd
firstRevol.IsMergeEnd = TRUE

```

### Property **NeutralFiber**( ) As boolean

Returns the Revol neutral fiber flag (for thin Revol only).
It returns TRUE if the Revol is a neutral fiber Revol , FALSE if not.

**Returns:**      oIsNeutralFiber The neutral fiber flag as a boolean

**Example:**     The following example saves in `NeutralFiberFlag` the neutral fiber flag of Revol `firstRevol`, and then sets it so that it will be now neutral fiber :

```VBScript
Set NeutralFiberFlag = firstRevol.IsNeutralFiber
firstRevol.IsNeutralFiber = TRUE

```

### Property **RevoluteAxis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the rotation axis for Revol.
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).

**Example** : This example retrieves in `RevoluteAxis` the rotation axis for the `Rotate axis` of the Revol feature Dim RevoluteAxis As Reference Set RevoluteAxis = Rotate.Axis
```

### Property **SecondAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the revolution second angle. This angle is computed around the revolution axis, starting from the sketch plane trace on the plane perpendicular to the revolution axis, and is counted positive counterclockwise when looking at this plane in the revolution axis direction. Its default value is 0.

**Example:**     The following example returns in `secondAngle` the second angle of the `MyRevolution` revolution object:

```VBScript
Set secondAngle = MyRevolution.SecondAngle

```