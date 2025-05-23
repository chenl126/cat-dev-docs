# CircPattern (Object)

**_Represents the circular pattern._**
The shape is duplicated along concentric circles to build crowns. A linear repartition object defines the duplication along radial directions, thus determining the number of crowns. An angular repartition object defines the duplication on the crowns.

**See also:**      [LinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md), [AngularRepartition](../PartInterfaces/interface_AngularRepartition_70628.md)

## Properties

### Property **AngularDirectionRow**(| ) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md) (Read Only)

   Returns the position of the shape to be copied along the angular direction.

**Example:**     The following example returns in `AngularDirPos` the position of the shape to be copied along the angular direction.

```VBScript
     Set AngularDirPos = firstPattern.AngularDirectionRow

```

### Property **AngularRepartition**( ) As [CATIAAngularRepartition](../PartInterfaces/interface_AngularRepartition_70628.md) (Read Only)

   Returns the angular repartition. The angular repartition is the repartition on a crown.

**Example:**     The following example returns in `repartA` the angular repartition of the circular pattern `firstPattern`:

```VBScript
     Set repartA = firstPattern.AngularRepartition

```

### Property **CircularPatternParameters**( ) As [CatCircularPatternParameters](../PartInterfaces/enum_CatCircularPatternParameters_166158.md)

   Returns or sets the circular pattern parameters required to define the pattern. These parameters are used when reading the CATIAAngularRepartition properties.

**Example:**     The following example returns in `parameters` the circular pattern parameters of the `firstPattern` circular pattern, and then sets it to `catCompleteCrown`, so that only the number of instances is used to define the Pattern:

```VBScript
     Set parameters = firstPattern.CircularPatternParameters
     Set firstPattern.CircularPatternParameters = catCompleteCrown

```

### Property **RadialAlignment**( ) As boolean

   Returns or sets whether the copied shapes should be rotated or radial aligned with respect to the original one.

**True** if the copied shapes are rotated.

**Example:**     The following example returns in `alignedR` the radial alignment of the circular pattern `firstPattern`, and then sets it to `False`:

```VBScript
     Set alignedR = firstPattern.RadialAlignment
     firstPattern.RadialAlignment = False

```

### Property **RadialDirectionRow**( ) As [CATIAIntParam](../KnowledgeInterfaces/interface_IntParam_13730.md) (Read Only)

   Returns the position of the shape to be copied along the radial direction.

**Example:**     The following example returns in `RadialDirPos` the position of the shape to be copied along the radial direction.

```VBScript
     Set RadialDirPos = firstPattern.RadialDirectionRow

```

### Property **RadialRepartition**( ) As [CATIALinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md) (Read Only)

   Returns the radial repartition. The radial repartition is the repartition along a radius.

**Example:**     The following example returns in `repartR` the radial repartition of the circular pattern `firstPattern`:

```VBScript
     Set repartR = firstPattern.RadialRepartition

```

### Property **RotationOrientation**( ) As boolean

   Returns or sets whether the shapes are copied clockwise on the crowns with respect to the rotation axis direction.

**True** if the shapes are copied counterclockwise when the rotation axis direction goes towards you when you look at the crown.

**Example:**     The following example returns in `alignedAxis` whether the circular pattern `firstPattern` is built clockwise, and then sets it to `True`:

```VBScript
     alignedAxis = firstPattern.RotationOrientation
     firstPattern.RotationOrientation = True

```

Methods

### Sub **GetRotationAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioRotationAxis`)

   Returns the rotation axis. The rotation axis is returned as an array containing the rotation axis vector components. Assume this array is `oRotationAxis`. It contains:

`oRotationAxis[0],oRotationAxis[1],oRotationAxis[2]`     The X, Y, and Z rotation axis vector components

**Example:**     The following example returns in `axisArray` the rotation axis components of the circular pattern `firstPattern`:

```VBScript
     Call firstPattern.GetRotationAxis(axisArray)
     Set x = axisArray[0]
     Set y = axisArray[1]
     Set z = axisArray[2]

```

### Sub **GetRotationCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioRotationCenter`)

   Returns the rotation center if the user defined it. Returns E_FAIL if no rotation center has been defined The rotation center is returned as an array containing the rotation center coordinates. Assume this array is `oRotationCenter`. It contains:

`oRotationCenter[0],oRotationCenter[1],oRotationCenter[2]`     The X, Y, and Z rotation center coordinates

**Example:**     The following example returns in `centerArray` the rotation center coordinates of the circular pattern `firstPattern`, and saves them in variables:

```VBScript
     Call firstPattern.GetRotationCenter(centerArray)
     x = centerArray[0]
     y = centerArray[1]
     z = centerArray[2]

```

### Sub **SetInstanceAngularSpacing**( long  `iInstanceNumber`,  double  `iAngularSpacing`)

   Sets the InstanceAngularSpacing.

**Parameters:**

` iInstanceNumber`      The Instance Number
` iAngularSpacing`      The Angular Spacing  **Example:**     The following example sets the InstanceAngularSpacing of the circular pattern
```

### Sub **SetRotationAxis**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationAxis`)

   Sets the rotation axis.

**Parameters:**

` iRotationAxis`      The rotation axis. It is passed as reference and can be valuated with a line, an edge or a plane reference: in this case the plane normal is taken into account.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md) [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  **Example:**     The following example sets the rotation axis of the circular pattern `firstPattern` with the `refLine1` reference:

```VBScript
     firstPattern.SetRotationAxis refLine1

```

### Sub **SetRotationCenter**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationCenter`)

   Sets the rotation center.

**Parameters:**

` iRotationCenter`      The rotation center  **Example:**     The following example sets the rotation center of the circular pattern `firstPattern` with `point1Ref` point:

```VBScript
     firstPattern.SetRotationCenter point1Ref

```

### Sub **SetUnequalInstanceNumber**( long  `iInstanceNumber`)

   Sets the Instance Number.

**Parameters:**

` iInstanceNumber`      The Instance Number  **Example:**     The following example modifies the instance number for unequal angular spacing
```

### Sub **SetUnequalStep**( long  `iInstanceNumber`)

   This method is deprecated Sets the UnequalStep.

**Parameters:**

` iInstanceNumber`      The Instance Number  **Example:**     The following example creates the number of pattern spacing objects in pattern object
```