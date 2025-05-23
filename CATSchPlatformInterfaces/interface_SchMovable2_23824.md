# SchMovable2 (Object)

**_Manage rotation of a schematic object._**

## Methods

### Sub **RotateAtPoint**(| double | `iDb1RotationAngleInRadian`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb2CenterPoint`)

   Rotate a schematic object with an angle in radian at a point.

**Parameters:**

` iDb1RotationAngleInRadian`      Rotation angle (from x-axis) in radian.
` iDb2CenterPoint`      X-Y components of a center point of rotation.

**Example:**

```VBScript
     Dim objThisIntf As SchMovable2

     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.RotateAtPoint,dbVar2

```