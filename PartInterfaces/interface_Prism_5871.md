# Prism (Object)

**_Prism-based features in Part Design : base for pad or pocket._**

## Properties

### Property **DirectionOrientation**(| ) As [CatPrismOrientation](../PartInterfaces/enum_CatPrismOrientation_77897.md)

   Returns the prism direction orientation.

**Returns:**      oOrientation The direction orientation (see [CatPrismOrientation](../PartInterfaces/enum_CatPrismOrientation_77897.md) for list of possible types)

**Example:**     The following example saves in `dirOrientation` the direction orientation of prism `firstPrism`, and then sets it so that the direction will be now inversed :

```VBScript
     Set dirOrientation = firstPrism.DirectionOrientation
     firstPrism.DirectionOrientation = catInverseOrientation

```

### Property **DirectionType**( ) As [CatPrismExtrusionDirection](../PartInterfaces/enum_CatPrismExtrusionDirection_144922.md)

   Returns the prism direction type.

**Returns:**      oDirType The direction type (see [CatPrismExtrusionDirection](../PartInterfaces/enum_CatPrismExtrusionDirection_144922.md) for list of possible types)

**Example:**     The following example saves in `dirType` the direction type of prism `firstPrism`, and then sets it so that the direction will be now normal to the sketch :

```VBScript
     Set dirType = firstPrism.DirectionType
     firstPrism.DirectionType = catNormalToSketchDirection

```

### Property **FirstLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the first prism limit (one of the two).
This limit manages the way the prism is ended.

**Returns:**      oFirstLimit The first limit (see [Limit](../PartInterfaces/interface_Limit_5781.md) for more information)

**Example:**     The following example returns in `firstLimit` the first limit of prism `firstPrism`:

```VBScript
     Set firstLimit = firstPrism.FirstLimit

```

### Property **IsSymmetric**( ) As boolean

   Returns the prism symmetry flag.
It returns TRUE if the prism is symmetric (from the base sketch), FALSE if not.

**Returns:**      oIsSymmetric The symmetry flag as a boolean

**Example:**     The following example saves in `symFlag` the symmetry flag of prism `firstPrism`, and then sets it so that it will be now symmetric (from the base sketch) :

```VBScript
     Set symFlag = firstPrism.IsSymmetric
     firstPrism.IsSymmetric = TRUE

```

### Property **IsThin**( ) As boolean

   Returns the prism thin flag.
It returns TRUE if the prism is a thin prism , FALSE if not.

**Returns:**      oIsThin The thin flag as a boolean

**Example:**     The following example saves in `thinFlag` the thin flag of prism `firstPrism`, and then sets it so that it will be now thin :

```VBScript
     Set thinFlag = firstPrism.IsThin
     firstPrism.IsThin = TRUE

```

### Property **MergeEnd**( ) As boolean

   Returns the prism merge end flag (for thin prism only).
It returns TRUE if merge ends is required , FALSE if not.

**Returns:**      oIsMergeEnd The merge end flag as a boolean

**Example:**     The following example saves in `MergeEndFlag` the merge end flag of prism `firstPrism`, and then sets it so that merge end will be required :

```VBScript
     Set MergeEndFlag = firstPrism.IsMergeEnd
     firstPrism.IsMergeEnd = TRUE

```

### Property **NeutralFiber**( ) As boolean

   Returns the prism neutral fiber flag (for thin prism only).
It returns TRUE if the prism is a neutral fiber prism , FALSE if not.

**Returns:**      oIsNeutralFiber The neutral fiber flag as a boolean

**Example:**     The following example saves in `NeutralFiberFlag` the neutral fiber flag of prism `firstPrism`, and then sets it so that it will be now neutral fiber :

```VBScript
     Set NeutralFiberFlag = firstPrism.IsNeutralFiber
     firstPrism.IsNeutralFiber = TRUE

```

### Property **SecondLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the second prism limit (one of the two).
This limit manages the way the prism is ended.

**Returns:**      oSecondLimit The second limit (see [Limit](../PartInterfaces/interface_Limit_5781.md) for more information)

**Example:**     The following example returns in `secondLimit` the second limit of prism `firstPrism`:

```VBScript
     Set secondLimit = firstPrism.SecondLimit

```

Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

   Returns the prism direction with absolute coordinates.
It needs a safe array with 3 elements : X, Y, Z direction coordinates The array must be previously initialized

**Returns:**      ioDirection The direction coordinates

**Example:**     The following example returns in `dirArray` the direction coordinates of prism `firstPrism`:

```VBScript
     Dim dirArray(2)
     Call firstPrism.GetDirection(dirArray)
     Set x = dirArray[1]
     Set y = dirArray[2]
     Set z = dirArray[3]

```

### Sub **ReverseInnerSide**( )

   Reverses the prism inner side when the profile is open. This is useful for finding the shape to reach.

**Example:**     The following example reverses the current inner side of prism `firstPrism` :

```VBScript
     firstPrism.ReverseInnerSide

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine`)

   Sets the prism associative direction.

**Parameters:**

` iLine`      The support direction reference (see
[Reference](../InfInterfaces/interface_Reference_17481.md) for more information)
This reference can be valuated with a reference to a line or an edge.
The following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).

**Example:**     The following example sets the prism direction reference of prism `firstPrism` with `prismDirRef` line :

```VBScript
     firstPrism.SetDirection prismDirRef

```