# HybridShapeCircle (Object)

**_Represents the hybrid shape circle object._**
**Role** : To access the data of the hybrid shape circle object.

This data includes:

  * The circle radius
  * Two circle center
  * The circle arc limitation mode
  * The circle start and end angles

All interfaces for different type of circle derivates HybridShapeCircle.

Use the CATIAHybridShapeFactory to create a HybridShapeCircle objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AxisComputation**( ) As boolean

Returns or sets the axis computation mode.

**Example:**      This example retrieves the axis computation mode of the `hybShpCircle`

```VBScript
Dim axisComp As Boolean
axisComp = hybShpCircle.AxisComputation

```

### Property **AxisDirection**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

**Role** : To get_Direction on the object.

**Parameters:**

` oDir`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **EndAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the circle end angle.

**Example** :      This example retrieves in `ShpCircleEndAngle` the end angle of the `ShpCircle` hybrid shape circle.

```VBScript
Dim ShpCircleEndAngle As Angle
ShpCircleEndAngle = ShpCircle.EndAngle

```

### Property **StartAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the circle start angle.

**Example** :      This example retrieves in `ShpCircleStartAngle` the end angle of the `ShpCircle` hybrid shape circle.

```VBScript
Dim ShpCircleStartAngle As Angle
ShpCircleStartAngle = ShpCircle.StartAngle

```

Methods

### Sub **GetAxis**( long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oAxis`)

Returns the axis of the Circle.

**Parameters:**

` iType`      Type of axis to be retrived. 3 - CATGSMAxisLineType_NormalToCircle 2 - CATGSMAxisLineType_NormalToDirection 1 - CATGSMAxisLineType_AlignedWithDirection
` oAxis`      Reference to the element.

**Example** :      This example retrieves the axis of the circle. `HybShpCircle` hybrid shape circle.

```VBScript
Dim AxisRef As Reference
HybShpCircle.GetAxis 1, AxisRef

```

### Sub **GetCenter**( double  `oCenterX`,  double  `oCenterY`,  double  `oCenterZ`)

Gets the mathematical center of the circle. This information is available once the circle has been computed.

**Parameters:**

` oCenterX,`      oCenterY, oCenterZ, circle center

### Sub **GetFreeCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioCenter`)

Returns the circle center.

**Parameters:**

` oCenter`      The circle center. It is returned as an array of three coordinates in SafeArrayVariant  **Example** :      This example retrieves in `HybShpCircleCenter` the center of the `HybShpCircle` hybrid shape circle.

```VBScript
Dim HybShpCircleCenter
ReDim HybShpCircleCenter(2)
ShpCircle.GetFreeRadius(HybShpCircleCenter)

```

You can access each center coordinate as follows:

  * `x` is in `HybShpCircleCenter(0)`
  * `y` is in `HybShpCircleCenter(1)`
  * `z` is in `HybShpCircleCenter(2)`

### Sub **GetFreeRadius**( double  `oRadius`)

Returns the circle radius.

**Parameters:**

` oRadius`      The circle radius  **Example** :      This example retrieves in `HybShpCircleRadius` the radius of the `HybShpCircle` hybrid shape circle.

```VBScript
    ShpCircle.GetFreeRadius(HybShpCircleRadius)

```

### Func **GetLimitation**( ) As long

Gets the limitation type for the circle.

**Parameters:**

` oLimit`      (Angles = 0, Whole = 1, Trimmed = 2, Complementary = 3). circle limitation

### Sub **SetLimitation**( long  `iLimitation`)

Set the circle limitation type.

**Parameters:**

` iLimitation`      The circle limitation type
**Legal values** :

0     Angles 1     Whole 2     Trimmed 3     Complementary  **Example** :      This example sets the limitiation type of the `ShpCircle` hybrid shape circle to trimmed.

```VBScript

```