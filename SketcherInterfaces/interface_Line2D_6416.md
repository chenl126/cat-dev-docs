# Line2D (Object)

**_Class defining a line in 2D Space._**

## Methods

### Sub **GetDirection**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oDirection`)

   Returns the unit-vector pointing in the direction of the line.

**Parameters:**

` oDirection[0]`      The X Coordinate of the unit vector pointing in the direction of the line
` oDirection[1]`      The Y Coordinate of the unit vector pointing in the direction of the line

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns a point lying on the line

**Parameters:**

` oPoint[0]`      The X Coordinate of a point lying on the line
` oPoint[1]`      The Y Coordinate of a point lying on the line

### Sub **SetData**( double  `iX`,  double  `iY`,  double  `iXDirection`,  double  `iYDirection`)

   Modifies the caracteristics of the infinite line

**Parameters:**

` iX`      The X Coordinate of a point lying on the line
` iY`      The Y Coordinate of a point lying on the line
` iXDirection`      The X Coordinate of the unit vector pointing in the direction of the line
` iYDirection`      The Y Coordinate of the unit vector pointing in the direction of the line