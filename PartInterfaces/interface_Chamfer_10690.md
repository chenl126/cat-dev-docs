# Chamfer (Object)

**_Represents the chamfer shape._**
A chamfer is made up of a list of geometrical elements to process, such as faces, and is defined using a couple of parameters, such as two lengthes, or a length and an angle.

## Properties

### Property **Angle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the chamfer angle. This is valid only if the chamfer is defined using a length and an angle, that is if the chamfer definition mode [CatChamferMode](../PartInterfaces/enum_CatChamferMode_40082.md) is set to `catLengthAngleChamfer`.

**Example:**     The following example returns in `angle` the angle of the `firstChamfer` chamfer:

```VBScript
Set angle = firstChamfer.Angle

```

### Property **ElementsToChamfer**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns the collection of geometrical elements to be chamfered.

**Example:**     The following example returns in `list` the list of elements of the `firstChamfer` chamfer:

```VBScript
Set list = firstChamfer.ElementsToChamfer

```

### Property **Length1**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the chamfer first length. This is the first length if the chamfer is defined by two lengthes, or the chamfer if the chamfer is defined by a length and an angle.

**Example:**     The following example returns in `length1` the first length of the `firstChamfer` chamfer:

```VBScript
Set length1 = firstChamfer.Length1

```

### Property **Length2**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the chamfer second length. This is valid only if the chamfer is defined using two lengthes, that is if the chamfer definition mode [CatChamferMode](../PartInterfaces/enum_CatChamferMode_40082.md) is set to `catTwoLengthChamfer`.

**Example:**     The following example returns in `length2` the second length of the `firstChamfer` chamfer:

```VBScript
Set length2 = firstChamfer.Length2

```

### Property **Mode**( ) As [CatChamferMode](../PartInterfaces/enum_CatChamferMode_40082.md)

Returns or sets the chamfer definition mode. The chamfer definition mode enables the chamfer to be defined using either two lengthes or a length and an angle.

**Example:**     The following example returns in `mode` how the parameters of the `firstChamfer` chamfer are defined, and then sets it to `catTwoLengthChamfer`:

```VBScript
Set mode = firstChamfer.Mode
firstChamfer.Mode = catTwoLengthChamfer

```

### Property **Orientation**( ) As [CatChamferOrientation](../PartInterfaces/enum_CatChamferOrientation_93680.md)

Returns or sets the chamfer orientation.

**Example:**     The following example returns in `orient` the orientation mode of the `firstChamfer` chamfer, and then sets it to `catReverseChamfer`:

```VBScript
Set orient = firstChamfer.Orientation
firstChamfer.Orientation = catReverseChamfer

```

### Property **Propagation**( ) As [CatChamferPropagation](../PartInterfaces/enum_CatChamferPropagation_93192.md)

Returns or sets the propagation mode of the geometrical elements to be chamfered.

**Example:**     The following example returns in `prop` the propagation mode of the `firstChamfer` chamfer, and then sets it to `catMinimalChamfer`:

```VBScript
Set prop = firstChamfer.Propagation
firstChamfer.Propagation = catMinimalChamfer

```

Methods

### Sub **AddElementToChamfer**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElementToChamfer`)

Adds a new geometrical element to be chamfered.

**Parameters:**

` iElementToChamfer`      The new element to be chamfered
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example adds the new element `element` to be chamfered for the `firstChamfer` chamfer:

```VBScript
firstChamfer.AddElementToChamfer(element)

```

### Sub **WithdrawElementToChamfer**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElementToWithdraw`)

Withdraws a geometrical element from those to be chamfered.

**Parameters:**

` iElementToWithdraw`      The existing element to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example withdraws an existing element `element` to be chamfered from the `firstChamfer` chamfer:

```VBScript
firstChamfer.WithdrawElementToChamfer(element)

```