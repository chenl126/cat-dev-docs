# Circle2D (Object)

**_Class defining a circle in 2D Space._**

## Properties

### Property **CenterPoint**( ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

Returns the center point of the circle.

**Parameters:**

` oCenterPoint`      The center point of the circle

### Property **Radius**( ) As double (Read Only)

Returns the radius of the circle

**Parameters:**

` oRadius`      The radius of the circle
Methods

### Sub **GetCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oData`)

Returns the center of the circle

**Parameters:**

` oData[0]`      The X Coordinate of the circle center point
` oData[1]`      The Y Coordinate of the circle center point **Example:**     The following example reads the coordinates of the center
of the circle `myCircle`: double center(1) myCircle.GetCenter center

```VBScript

### Sub **SetData**( double  iCenterX,  double  iCenterY,  double  iRadius)

      Modifies the caracteristics of the circle

  **Parameters:**

    iCenterX
                           The X Coordinate of the circle center

    iCenterY
             The Y Coordinate of the circle center

    iRadius
             The radius of the circle