# Pattern (Object)

**_Represents the pattern shape._**
It is the base object for rectangular and circular patterns. A pattern shape is a set of copies of the same shape. The copy is done according to linear and angular repartitions.

**See also:**      [CircPattern](../PartInterfaces/interface_CircPattern_26301.md), [RectPattern](../PartInterfaces/interface_RectPattern_26504.md), [Repartition](../PartInterfaces/interface_Repartition_27263.md), [LinearRepartition](../PartInterfaces/interface_LinearRepartition_62934.md), [AngularRepartition](../PartInterfaces/interface_AngularRepartition_70628.md)

## Properties

### Property **ItemToCopy**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Returns or sets the shape to be copied.

**Example:**     The following example returns in `shape` the copied shape of the pattern `firstPattern`, and then sets it to `pad1`:

```VBScript
Set shape = firstPattern.ItemToCopy
firstPattern.ItemToCopy = pad1

```

### Property **RotationAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the pattern global rotation angle. The rotation is applied to the whole pattern, but not to the shapes themselves. The shape to be copied is used as the rotation center.

**Example:**     The following example returns in `globAng` the rotation of pattern `firstPattern`:

```VBScript
Set globAng = firstPattern.RotationAngle

```

Methods

### Sub **ActivatePosition**( long  `iPosU`,  long  `iPosV`)

Allows user to activate an instance of the pattern.

**Parameters:**

` iPosU`      The position of the instance in the U direction
` iPosV`      The position of the instance in the V direction

### Sub **DesactivatePosition**( long  `iPosU`,  long  `iPosV`)

Allows user to desactivate an instance of the pattern.

**Parameters:**

` iPosU`      The position of the instance in the U direction
` iPosV`      The position of the instance in the V direction