# Parabola2D (Object)

**_Class defining an parabola in 2D Space._**

## Properties

### Property **FocalDistance**(| ) As double (Read Only)

   Returns the focal distance of the parabola in 2D space

**Parameters:**

` oFocal`      The focal distance of the parabola
Methods

### Sub **GetAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAxis`)

   Returns the axis vector direction of the parabola in 2D space

**Parameters:**

` oAxis[0]`      The X coordinate of the axis vector direction
` oAxis[1]`      The Y coordinate of the axis vector direction

### Sub **GetCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCenter`)

   Returns the center of the parabola in 2D space

**Parameters:**

` oCenter[0]`      The X Coordinate of the center point of the parabola
` oCenter[1]`      The Y Coordinate of the center point of the parabola

### Sub **SetData**( double  `iCenterX`,  double  `iCenterY`,  double  `iAxisX`,  double  `iAxisY`,  double  `iFocalDistance`)

   Modifies the caracteristics of the parabola

**Parameters:**

` iCenterX`      The X Coordinate of the parabola center
` iCenterY`      The Y Coordinate of the parabola center
` iAxisX`      The X coordinate of the axis vector direction
` iAxisY`      The Y coordinate of the axis vector direction
` iFocalDistance`      The focal distance of the parabola