# Constraint (Object)

**_A geometric constraint set for geometric elements of a part, a sketch, or a product._**

## Properties

### Property **AngleSector**(| ) As [CatConstraintAngleSector](../MecModInterfaces/enum_CatConstraintAngleSector_121214.md)

   Returns or sets the constraint angle (or angular) sector. The geometric elements of an angle constraint (e.g. : 2 lines or 2 planes) divide the sketch or the space in 4 regions which are called angle or angular sectors, numbered from 0 to 3. 1 / 0 \---/--- 2/ 3 By default, the constraint is created in the sector number 0. One angle sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angle sector, the Dimension.Value, Side and Orientation are also modified.

**Parameters:**

` AngleSector=0`      The default sector of a constraint. Dimension.Value = angle Orientation = catCstOrientSame Side = catCstSidePositive
` AngleSector=1`      Dimension.Value = angle-180 if angle>180 abs(angle)+180 otherwise Orientation = catCstOrientOpposite Side = catCstSidePositive
` AngleSector=2`      Dimension.Value = abs(540-angle) if angle>180 180-fabs(angle) otherwise Orientation = catCstOrientOpposite Side = catCstSideNegative
` AngleSector=3`      Dimension.Value = 360-abs(angle) Orientation = catCstOrientSame Side = catCstSideNegative

**Example:**     The following example retrieves in `angleSector` the angle sector of the `angleCst` angle constraint and then changes the angle sector

```VBScript
     angleSector = angleCst.AngleSector
     angleCst.AngleSector = 2

```

### Property **Dimension**( ) As [CATIADimension](../KnowledgeInterfaces/interface_Dimension_18130.md) (Read Only)

   Returns the constraint dimension. The dimension may be meaningless for some types of constraints such as tangency constraints, or if the constraint is not currently satisfied. Use the Status property to check whether the constraint is satisfied.

**Example:**     The following example returns in `cstDimension` the dimension of the `firstCst` constraint:

```VBScript
     Set cstDimension = firstCst.Dimension

```

### Property **DistanceConfig**( ) As [CatConstraintDistConfig](../MecModInterfaces/enum_CatConstraintDistConfig_110847.md)

   Returns or sets the distance constraint configuration. Distance constraints between lines and cylinders offer often more degrees of freedom to geometry than acually desired. This property allows to limit these degrees of freedom without having to redefine additional constraints. This property is useless for constraints whose type is not distance.

**Example:**     The following example retrieves in `distCstConfig` the configuration of the `distCst` distance constraint:

```VBScript
     distCstConfig = distCst.DistanceConfig

```

### Property **DistanceDirection**( ) As [CatConstraintDistDirection](../MecModInterfaces/enum_CatConstraintDistDirection_143052.md)

   Returns or sets the distance constraint direction. This property is useless for constraints whose type is not Distance (1). Distance constraints may be measured along a particular direction. This property will be used if the direction is a reference axis : In 2D, 1 means the horizontal axis, 2 the vertical axis. In 3D, 1 stands for the X axis, 2 for the Y axis, 3 for the Z axis. 0 means that no direction is specified and the distance is measured as usual.

**Example:**     The following example retrieves in `distCstDirection` the configuration of the `distCst` distance constraint:

```VBScript
     distCstConfig = distCst.DistanceDirection

```

### Property **Mode**( ) As [CatConstraintMode](../MecModInterfaces/enum_CatConstraintMode_61138.md)

   Returns or sets the constraint driving mode. For constraint types supporting the concept of value, such as distance constraints, the driving mode tells whether the constraint value actually drives the geometry position, or, conversely, is driven by it.

**Example:**     The following example retrieves in `currentMode` the driving mode for the `distCst` distance constraint:

```VBScript
     currentMode = distCst.Mode

```

### Property **Orientation**( ) As [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md)

   Returns or sets the constraint orientation. This is used for constraints that involve two geometric elements and specifies the orientation for the second geometric element with regard to the first one, when several possible orientations are all satisfying the constraint.

**Example:**     The following example retrieves the in `distCstOrient` the orientation of the `distCst` distance constraint:

```VBScript
     distCstOrient = distCst.Orientation

```

### Property **ReferenceAxis**( ) As [CatConstraintRefAxis](../MecModInterfaces/enum_CatConstraintRefAxis_83938.md)

   Returns or sets the constraint reference axis. AxisParallel or AxisPerpendicular constraint types define which axis they relate to through this property, which makes no sense for constraints of another type.

**Example:**     The following example retrieves in `refAxis` the reference axis for the `axisPerpCst` AxisPerpendicular constraint:

```VBScript
     refAxis = axisPerpCst.ReferenceAxis

```

### Property **ReferenceType**( ) As [CatConstraintRefType](../MecModInterfaces/enum_CatConstraintRefType_84586.md)

   Returns or sets the constraint reference type. This property is used only for Reference constraints in the Assembly context.

**Example:**     The following example applies to the reference constraint refCst2 the reference type of the constraint refCst1.

```VBScript
     refCst2.ReferenceType = refCst1.ReferenceType

```

### Property **Side**( ) As [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md)

   Returns or sets the constraint side. Some constraint types need to relatively position the constrained geometries, when several possible configurations are all satisfying the constraint.

**Example:**     The following example retrieves in `distCstSide` the side of the `distCst` distance constraint:

```VBScript
     distCstSide = distCst.Side

```

### Property **Status**( ) As [CatConstraintStatus](../MecModInterfaces/enum_CatConstraintStatus_78757.md) (Read Only)

   Returns the constraint status. The constraint status is a diagnosis on whether the constraint is satisfied.

**Example:**     The following example retrieves the status of the `distCst` distance constraint.

```VBScript
     distCstSts = distCst.Status

```

### Property **Type**( ) As [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md) (Read Only)

   Returns the constraint type.

**Example:**     The following example returns in `cstType` the type of the `firstCst` constraint:

```VBScript
     cstType = firstCst.Type

```

Methods

### Sub **Activate**( )

   Unsuppresses a constraint for the update process. An activated constraint is again taken into account for the calculation of the part or product. **Example:**     The following example es the `pad1` pad: **Example:**     The following example activates the `tangencyCst` constraint :

```VBScript
     tangencyCst.Activate

```

### Sub **Deactivate**( )

   Suppresses the constraint from being updated. A deactivated constraint is not taken into account for the calculation of the part or of the product.  **Example:**     The following example deactivates the `tangencyCst` constraint from being updated:

```VBScript
     tangencyCst.Deactivate

```

### Func **GetConstraintElement**( long  `iElementNumber`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Reads an element of a constraint.

**Parameters:**

` iElementNumber`      The number of the element of the constraint to be read. (1 for the first element,2 for the second, 3 for the third). Notice it must not exceed the total number of elements of the constraint. (eg : not allowed to read the third element of a tangency).
` oCurrentElement`      An element of the constraint.  **Example:**     The following example reads the first element of a constraint

```VBScript
     Dim reference1 As Reference
     reference1=tangencyCst.GetConstraintElement( 1 )

```

### Sub **GetConstraintVisuLocation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAnchorPoint`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAnchorVector`)

   Returns the constraint visualisation location. When displayed on screen, the constraint is visualized as a dimension positioned close to the constrained geometric element(s). This method retrieves the data used to position this representation within the 3D space.

**Parameters:**

` oAnchorPoint`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the point where the constraint value is displayed.
` oAnchorVector`      A Safe Array made up of 3 doubles : X, Y, Z, representing the vector normal to the plane onto which the constraint value is displayed.  **Example:**     The following example retrieves in `anchorPt` the anchor point of the `tangencyCst` tangency constraint:

```VBScript
     Dim anchorPoint(2)
     Dim anchorVector(2)
     tangencyCst.ConstraintVisuLocation anchorPoint,vectorPoint

```

### Func **IsInactive**( ) As boolean

   Indicates whether a constraint is suppressed from the update process. A suppressed constraint is not taken into account for the calculation of part or the product. The method returns True if the constraint is not active, False if the constraint is active. **Example:**     The following example returns in `isInactive` whether the `tangencyCst` constraint is suppressed from the update process:

```VBScript
     Set isInactive = tangencyCst.IsInactive

```

### Sub **SetConstraintElement**( long  `iElementNumber`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewElement`)

   Replaces an element of a constraint.

**Parameters:**

` iElementNumber`      The number of the element of the constraint to replace. (1 for the first element,2 for the second, 3 for the third).
` iNewElement`      A new element of the constraint.  **Example:**     The following example changes the second element of a constraint

```VBScript
     Dim reference1 As Reference
     tangencyCst.SetConstraintElement ( 2, reference1)

```

### Sub **SetConstraintVisuLocation**( double  `iNewX`,  double  `iNewY`,  double  `iNewZ`)

   Sets a new location for the constraint visualization.

**Parameters:**

` iNewX`      The new value for the constraint anchor point X coordinate
` iNewY`      The new value for the constraint anchor point Y coordinate
` iNewZ`      The new value for the constraint anchor point Z coordinate  **Example:**     The following example changes the anchor point coordinates to 10,0,0

```VBScript
     tangencyCst.SetConstraintVisuLocation 10,0,0

```