# SchGRRComp (Object)

**_Manage the graphical representation of a schematic component._**

## Methods

### Sub **GetPosition**(| [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md) | `oDb2Position`)

   Get the current position of the component.

**Parameters:**

` oDb2Position`      The current position of the component.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetPositionobjArg1

```

### Sub **GetRotationAngle**( double  `oDb1RotationAngleInRad`)

   Get the current rotation angle (from x-axis in radian) of the component.

**Parameters:**

` oDb1RotationAngleInRad`      The current angle of the component in radian.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar As Double;

      ...
     objThisIntf.GetRotationAngledbVar

```

### Sub **GetScale**( double  `oDb1ScaleFactor`)

   Get the current scale factor of the component.

**Parameters:**

` oDb1ScaleFactor`      The current scale factor of the component.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar As Double;
      ...
     objThisIntf.GetScaledbVar

```

### Sub **GetTransformation2D**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb6TransMatrix`)

   Get the local coordinate reference frame (with respect to absolute coordinate system) of the component.

**Parameters:**

` oDb6TransMatrix`      An double array of 6 members. Transformation matrix that defines the local coordinate reference frame of the component member 1, 2 - defines the x-axis of the local coordinate reference frame. member 3, 4 - defines the y-axis of the local coordinate reference frame. member 5, 6 - defines the origin of the local coordinate reference frame One can also interpret this as the transformation matrix that would move the component from the absolute coordinate frame to the current position and orientation. As such, the member 5,6 define the translational vector Furthemore, rotation angle and scale factor can be calculated from member 1 to 4.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetTransformation2DobjArg1

```

### Sub **SetPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDb2Position`)

   Set the current position of the component.

**Parameters:**

` iDb2Position`      The position of the component to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar1(x) As CATSafeArrayVariant
      ...
     objThisIntf.SetPositiondbVar1

```

### Sub **SetRotationAngle**( double  `iDb1RotationAngleInRad`)

   Set the current rotation angle (from x-axis in radian) of the component.

**Parameters:**

` iDb1RotationAngleInRad`      The rotation angle of the component in radian to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar As Double;
      ...
     objThisIntf.SetRotationAngledbVar

```

### Sub **SetScale**( double  `iDb1ScaleFactor`)

   Set the current scale factor of the component.

**Parameters:**

` iDb1ScaleFactor`      The scale factor of the component to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar As Double;

      ...
     objThisIntf.SetScaledbVar

```

### Sub **SetTransformation2D**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb6TransMatrix`)

   Set the local coordinate reference frame (with respect to absolute coordinate system) of the component.

**Parameters:**

` iDb6TransMatrix`      Transformation matrix to be set. See
GetTransformation2D for explanation of this argument.  **Example:**

```VBScript
     Dim objThisIntf As SchGRRComp
     Dim dbVar1(6) As CATSafeArrayVariant
      ...
     objThisIntf.SetTransformation2DdbVar1

```