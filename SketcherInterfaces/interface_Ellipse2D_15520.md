# Ellipse2D (Object)

**_Class defining an ellipse in 2D Space._**

## Properties

### Property **CenterPoint**(| ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

   Returns the center point of the ellipse.

**Parameters:**

` iCenterPoint`      The center point of the ellipse

### Property **MajorRadius**( ) As double (Read Only)

   Returns the radius of the ellipse major axis

**Parameters:**

` oMajorRadius`      The radius of the major axis

### Property **MinorRadius**( ) As double (Read Only)

   Returns the radius of the ellipse minor axis

**Parameters:**

` oMinorRadius`      The radius of the minor axis
Methods

### Sub **GetCenter**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCenter`)

   Returns the center of the ellipse in 2D space

**Parameters:**

` oCenter[0]`      The X Coordinate of the center point of the ellipse
` oCenter[1]`      The Y Coordinate of the center point of the ellipse

### Sub **GetMajorAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMajorAxis`)

   Returns the unit vector of the major axis of the ellipse in 2D space

**Parameters:**

` oMajorAxis[0]`      The length of the major axis
` oMajorAxis[1]`      The length of the major axis

### Sub **GetMinorAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMajorAxis`)

   Returns the unit vector of the minor axis of the ellipse in 2D space

**Parameters:**

` oMinorAxis[0]`      The length of the major axis
` oMinorAxis[1]`      The length of the major axis

### Sub **SetData**( double  `iCenterX`,  double  `iCenterY`,  double  `iMajorX`,  double  `iMajorY`,  double  `iMajorRadius`,  double  `iMinorRadius`)

   Modifies the caracteristics of the ellipse

**Parameters:**

` iCenterX`      The X Coordinate of the ellipse center
` iCenterY`      The Y Coordinate of the ellipse center
` iMajorX`      The X coordinate of the Major axis direction
` iMajorY`      The Y coordinate of the Major axis direction
` iMajorRadius`      The length of the major axis
` iMinorRadius`      The length of the minor axis