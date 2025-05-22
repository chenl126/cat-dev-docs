# Hyperbola2D (Object)

**_Class defining an hyperbola in 2D Space._**

## Properties

### Property **ImaginaryRadius**( ) As double (Read Only)

Returns the minor radius of the hyperbola in 2D space

**Parameters:**

` oMinorRadius`      The minor radius of the hyperbola

### Property **Radius**( ) As double (Read Only)

Returns the major radius of the hyperbola in 2D space

**Parameters:**

` oMajorRadius`      The major radius of the hyperbola
Methods

### Sub **GetAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAxis`)

Returns the axis vector direction of the hyperbola in 2D space

**Parameters:**

` oAxis[0]`      The X coordinate of the axis vector direction
` oAxis[1]`      The Y coordinate of the axis vector direction

### Sub **GetCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCenter`)

Returns the center point of the hyperbola in 2D space

**Parameters:**

` oCenter[0]`      The X Coordinate of the center point of the hyperbola
` oCenter[1]`      The Y Coordinate of the center point of the hyperbola

### Sub **SetData**( double  `iCenterX`,  double  `iCenterY`,  double  `iAxisX`,  double  `iAxisY`,  double  `iMajorRadius`,  double  `iMinorRadius`)

Modifies the caracteristics of the hyperbola

**Parameters:**

` iCenterX`      The X Coordinate of the hyperbola center
` iCenterY`      The Y Coordinate of the hyperbola center
` iAxisX`      The X coordinate of the axis vector direction
` iAxisY`      The Y coordinate of the axis vector direction
` iMajorRadius`      The length of the major radius
` iMinorRadius`      The length of the minor radius