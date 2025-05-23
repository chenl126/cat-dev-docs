# RectPattern (Object)

**_Represents the rectangular pattern._**
The shape is copied along two directions. Two linear repartitions control the shape copy.

**See also:**      [LinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md)

## Properties

### Property **FirstDirectionRepartition**(| ) As [CATIALinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md) (Read Only)

   Returns the linear repartition along the first direction.

**Example:**     The following example returns in `repart1` the first linear repartition of the rectangular pattern `firstPattern`:

```VBScript
     Set repart1 = firstPattern.FirstDirectionRepartition

```

### Property **FirstDirectionRow**( ) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md) (Read Only)

   Returns the position of the shape to be copied along the first linear direction.

**Example:**     The following example returns in `FirstDirPos` the position of the shape to be copied along the first linear direction in the rectangular pattern `firstPattern`:

```VBScript
     Set FirstDirPos = firstPattern.FirstDirectionRow

```

### Property **FirstOrientation**( ) As boolean

   Returns or sets whether the pattern is built towards the first direction orientation.

**True** if the pattern is built towards the first direction orientation.

**Example:**     The following example returns in `aligned1` whether the rectangular pattern `firstPattern` is built towards the first direction orientation, and then sets its to `True`:

```VBScript
     Set aligned1 = firstPattern.FirstOrientation
     firstPattern.FirstOrientation = True

```

### Property **FirstRectangularPatternParameters**( ) As [CatRectangularPatternParameters](../PartInterfaces/enum_CatRectangularPatternParameters_203822.md)

   Returns or sets the rectangular pattern parameters required to define the pattern. These parameters are used when reading the CATIALinearRepartition properties.

**Example:**     The following example returns in `parameters` the rectangular pattern parameters of the `firstPattern` rectangular pattern, and then sets it to `catUnequalSpacing`, so that the unqual spacing will be defined in first direction:

```VBScript
     Set parameters = firstPattern.FirstCircularPatternParameters
     Set firstPattern.FirstCircularPatternParameters = catUnequalSpacing

```

### Property **SecondDirectionRepartition**( ) As [CATIALinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md) (Read Only)

   Returns the linear repartition along the second direction.

**Example:**     The following example returns in `repart2` the second linear repartition of the rectangular pattern `firstPattern`:

```VBScript
     Set repart2 = firstPattern.SecondDirectionRepartition

```

### Property **SecondDirectionRow**( ) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md) (Read Only)

   Returns the position of the shape to be copied along the second linear direction.

**Example:**     The following example returns in `SecondDirPos` the position of the shape to be copied along the second linear direction in the rectangular pattern `firstPattern`:

```VBScript
     Set SecondDirPos = firstPattern.SecondDirectionRow

```

### Property **SecondOrientation**( ) As boolean

   Returns or sets whether the pattern is built towards the second direction orientation.

**True** if the pattern is built towards the second direction orientation.

**Example:**     The following example returns in `aligned2` whether the rectangular pattern `firstPattern` is built towards the second direction orientation, and then sets its to `False`, meaning the pattern is built in the opposite direction:

```VBScript
     Set aligned2 = firstPattern.SecondOrientation
     firstPattern.SecondOrientation = False

```

### Property **SecondRectangularPatternParameters**( ) As [CatRectangularPatternParameters](../PartInterfaces/enum_CatRectangularPatternParameters_203822.md)

   Returns or sets the rectangular pattern parameters required to define the pattern. These parameters are used when reading the CATIALinearRepartition properties.

**Example:**     The following example returns in `parameters` the rectangular pattern parameters of the `secondPattern` rectangular pattern, and then sets it to `catUnequalSpacing`, so that the unqual spacing will be defined in second direction:

```VBScript
     Set parameters = secondPattern.SecondCircularPatternParameters
     Set secondPattern.SecondCircularPatternParameters = catUnequalSpacing

```

Methods

### Sub **GetFirstDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioFirstDirection`)

   Returns the first repartition direction. The first repartition direction is returned as an array containing the direction vector components. Assume this array is `o1stDirRep`. It contains:

`o1stDirRep[0],o1stDirRep[1],o1stDirRep[2]`     The X, Y, and Z direction vector components

**Example:**     The following example returns in `FirstDir` the first repartition direction vector components of the rectangular pattern `firstPattern` and saves them in variables:

```VBScript
     Dim FirstDir()
     Call firstPattern.GetFirstDirection(FirstDir)
     x = FirstDir(0)
     y = FirstDir(1)
     z = FirstDir(2)

```

### Sub **GetSecondDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioSecondDirection`)

   Returns the second repartition direction. The second repartition direction is returned as an array containing the direction vector components. Assume this array is `o2ndDirRep`. It contains:

`o2ndDirRep[0],o2ndDirRep[1],o2ndDirRep[2]`     The X, Y, and Z direction vector components

**Example:**     The following example returns in `SecondDir` the second repartition direction vector components of the rectangular pattern `firstPattern` and saves them in variables:

```VBScript
     Call firstPattern.GetSecondDirection(SecondDir)
     x = SecondDir[0]
     y = SecondDir[1]
     z = SecondDir[2]

```

### Sub **SetFirstDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstDirection`)

   Sets the first repartition direction.

**Parameters:**

` iFirstDirection`      The first repartition direction. It is passed as a
[Reference](../InfInterfaces/interface_Reference_17481.md) and can be valuated with a reference to a line or an edge.
The following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  **Example:**     The following example sets the first repartition direction of the rectangular pattern `firstPattern` with the `refToLine1` reference :

```VBScript
     firstPattern.SetFirstDirection refToLine1

```

### Sub **SetInstanceSpacing**( long  `iInstanceNumber`,  double  `iSpacing`,  long  `iDirection`)

   Sets the InstanceSpacing.

**Parameters:**

` iInstanceNumber`      The Instance Number
` iSpacing`      The Spacing
` iDirection`      The Instance direction  **Example:**     The following example sets the InstanceSpacing in a direction for unequal spacing
```

### Sub **SetSecondDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondDirection`)

   Sets the second repartition direction.

**Parameters:**

` iSecondDirection`      The second repartition direction. It is passed as a
[Reference](../InfInterfaces/interface_Reference_17481.md) and can be valuated with a reference to a line or an edge.
The following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  **Example:**     The following example sets the second repartition direction of the rectangular pattern `firstPattern` with the `refToLine2` reference :

```VBScript
     firstPattern.SetSecondDirection refToLine2

```

### Sub **SetUnequalInstanceNumber**( long  `iInstanceNumber`,  long  `iDirection`)

   Sets the Instance Number.

**Parameters:**

` iInstanceNumber`      The Instance Number
` iDirection`      The Instance direction  **Example:**     The following example modifies the instance number for unequal spacing
```