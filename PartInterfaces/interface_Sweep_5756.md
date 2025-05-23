# Sweep (Object)

**_Represents the sweep shape._**
It is the base object for ribs and slots.

## Properties

### Property **AnchorDirReverse**(| ) As boolean

   Returns the Sweep AnchorDirReverse flag (for Sweep Move Profile only).
It returns TRUE if Anchor direction is reversed , FALSE if not.

**Returns:**      oAnchorDirReverse The oAnchorDirReverse flag as a boolean

**Example:**

### Property **CenterCurve**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the sketch used as the sweep center curve. The sweep is built along this sketch.

**Example:**     The following example returns in `centerCurve` the sketch used as center curve by the `firstSweep` sweep object:

```VBScript
     Set centerCurve = firstSweep.CenterCurve

```

### Property **CenterCurveElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the center curve .
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  
### Property **IsThin**( ) As boolean

   Returns the Sweep thin flag.
It returns TRUE if the Sweep is a thin Sweep , FALSE if not.

**Returns:**      oIsThin The thin flag as a boolean

**Example:**     The following example saves in `thinFlag` the thin flag of Sweep `firstSweep`, and then sets it so that it will be now thin :

```VBScript
     Set thinFlag = firstSweep.IsThin
     firstSweep.IsThin = TRUE

```

### Property **MergeEnd**( ) As boolean

   Returns the Sweep merge end flag (for thin Sweep only).
It returns TRUE if merge ends is required , FALSE if not.

**Returns:**      oIsMergeEnd The merge end flag as a boolean

**Example:**     The following example saves in `MergeEndFlag` the merge end flag of Sweep `firstSweep`, and then sets it so that merge end will be required :

```VBScript
     Set MergeEndFlag = firstSweep.IsMergeEnd
     firstSweep.IsMergeEnd = TRUE

```

### Property **MergeMode**( ) As [CatMergeMode](../PartInterfaces/enum_CatMergeMode_29480.md)

   Returns or sets the end mode .  
### Property **MoveProfileToPath**( ) As boolean

   Returns the Sweep MoveProfileToPath flag (for Sweep Move Profile only).
It returns TRUE if move profile is required , FALSE if not.

**Returns:**      oIsMoveProfileToPath The MoveProfileToPath flag as a boolean

**Example:**
```

### Property **NeutralFiber**( ) As boolean

   Returns the Sweep neutral fiber flag (for thin Sweep only).
It returns TRUE if the Sweep is a neutral fiber Sweep , FALSE if not.

**Returns:**      oIsNeutralFiber The neutral fiber flag as a boolean

**Example:**     The following example saves in `NeutralFiberFlag` the neutral fiber flag of Sweep `firstSweep`, and then sets it so that it will be now neutral fiber :

```VBScript
     Set NeutralFiberFlag = firstSweep.IsNeutralFiber
     firstSweep.IsNeutralFiber = TRUE

```

### Property **NormalAxisDirReverse**( ) As boolean

   Returns the Sweep NormalAxisDirReverse flag (for Sweep Move Profile only).
It returns TRUE if Normal Axis direction is reversed , FALSE if not.

**Returns:**      oNormalAxisDirReverse The oNormalAxisDirReverse flag as a boolean

**Example:**
```

### Property **PullingDirElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the pulling direction .
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md), [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).  
### Property **ReferenceSurfaceElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the reference surface .
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [Face](../MecModInterfaces/interface_Face_3398.md).  Methods

### Sub **SetKeepAngleOption**( )

   Actives KeepAngleOption.