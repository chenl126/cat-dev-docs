# SchMovable (Object)

**_Manage the transformation of a schematic component._**

## Methods

### Sub **Rotate**( double  `iDb1RotationAngleInRadian`)

Rotate a schematic object with an angle in radian.

**Parameters:**

` iDb1RotationAngleInRadian`      Rotation angle (from x-axis) in radian.
**Example:**

```VBScript
Dim objThisIntf As SchMovable

 ...
objThisIntf.Rotate

```

### Sub **Scale**( double  `iDb1ScaleFactor`)

Scale a schematic object with a scale factor.

**Parameters:**

` oDb1ScaleFactor`      The current scale factor of the component.
**Example:**

```VBScript
Dim objThisIntf As SchMovable

 ...
objThisIntf.Scale

```

### Sub **ScaleSelectedObjects**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLCntblToScale`,  double  `iDb1ScaleFactor`)

Scale a list of schematic objects with a scale factor.

**Parameters:**

` iLCntblToScale`      List of selected objects to scale.
` oDb1ScaleFactor`      The current scale factor.
**Example:**

```VBScript
Dim objThisIntf As SchMovable
Dim objArg1 As SchListOfObjects

 ...
objThisIntf.ScaleSelectedObjectsobjArg1,objArg1

```

### Sub **Transform**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb6TransMatrix`)

Transform a schematic object with a transformation matrix.

**Parameters:**

` iDb6TransMatrix`      Transformation matrix. See
[SchGRRComp.GetTransformation2D](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.htm#GetTransformation2D) for explanation of this argument.  **Example:**

```VBScript
Dim objThisIntf As SchMovable
Dim dbVar1(6) As CATSafeArrayVariant
 ...
objThisIntf.TransformdbVar1

```

### Sub **Translate**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Vector`)

Translate a schematic object with a vector.

**Parameters:**

` iDb2Vector`      X-Y components of a translation vector.
**Example:**

```VBScript
Dim objThisIntf As SchMovable
Dim dbVar1(2) As CATSafeArrayVariant
 ...
objThisIntf.TranslatedbVar1

```