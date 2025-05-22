# Factory2D (Object)

**_Interface to the factory for 2D objects._**

## Methods

### Func **CreateCircle**( double  `iCenterX`,  double  `iCenterY`,  double  `iRadius`,  double  `iStartParam`,  double  `iEndParam`) As [CATIACircle2D](../SketcherInterfaces/interface_Circle2D_11806.md)

Creates and returns a 2D circle arc.

**Parameters:**

` iCenterX`      The X coordinate of the circle center
` iCenterY`      The Y coordinate of the circle center
` iRadius`      The radius of the circle
` iStartParam`      The beginning parameter of the circle.
This parameter is an angle value between 0 included and 2PI excluded. Parameter values are computed from the axis horizontal direction in the trigonometrical direction.
` iEndParam`      The end parameter of the circle.
This parameter may take any value between iStartParam excluded and 4PI included.

### Func **CreateClosedCircle**( double  `iCenterX`,  double  `iCenterY`,  double  `iRadius`) As [CATIACircle2D](../SketcherInterfaces/interface_Circle2D_11806.md)

Creates and returns a closed 2D circle.

**Parameters:**

` iCenterX`      The X coordinate of the circle center
` iCenterY`      The Y coordinate of the circle center
` iRadius`      The radius of the circle

### Func **CreateClosedEllipse**( double  `iCenterX`,  double  `iCenterY`,  double  `iMajorX`,  double  `iMajorY`,  double  `iMajorRadius`,  double  `iMinorRadius`) As [CATIAEllipse2D](../SketcherInterfaces/interface_Ellipse2D_15520.md)

Creates and returns a closed 2D ellipse.

**Parameters:**

` iCenterX`      The X coordinate of the ellipse center
` iCenterY`      The Y coordinate of the ellipse center
` iMajorX`      The X component of the major axis direction
` iMajorY`      The Y component of the Major axis direction
` iMajorRadius`      The length of the major axis
` iMinorRadius`      The length of the minor axis

### Func **CreateControlPoint**( double  `iX`,  double  `iY`) As [CATIAControlPoint2D](../SketcherInterfaces/interface_ControlPoint2D_39214.md)

Creates and returns a 2D spline control point.

**Parameters:**

` iX`      The X coordinate of point to create
` iY`      The Y coordinate of point to create

### Func **CreateEllipse**( double  `iCenterX`,  double  `iCenterY`,  double  `iMajorX`,  double  `iMajorY`,  double  `iMajorRadius`,  double  `iMinorRadius`,  double  `iStartParam`,  double  `iEndParam`) As [CATIAEllipse2D](../SketcherInterfaces/interface_Ellipse2D_15520.md)

Creates and returns a 2D ellipse arc.

**Parameters:**

` iCenterX`      The X coordinate of the ellipse center
` iCenterY`      The Y coordinate of the ellipse center
` iMajorX`      The X component of the major axis direction
` iMajorY`      The Y component of the major axis direction
` iMajorRadius`      The length of the major axis
` iMinorRadius`      The length of the minor axis
` iStartParam`      The beginning parameter of the ellipse.
This parameter is an angle value between 0 included and 2PI excluded. Parameter values are computed from the major axis direction in the trigonometrical direction.
` iEndParam`      The end parameter of the ellipse.
This parameter may take any value between iStartParam excluded and 4PI included.

### Func **CreateHyperbola**( double  `iCenterX`,  double  `iCenterY`,  double  `iAxisX`,  double  `iAxisY`,  double  `iMajorRadius`,  double  `iMinorRadius`) As [CATIAHyperbola2D](../SketcherInterfaces/interface_Hyperbola2D_23520.md)

Creates and returns a hyperbola.

**Parameters:**

` iCenterX`      The X coordinate of the hyperbola center
` iCenterY`      The Y coordinate of the hyperbola center
` iAxisX`      The X coordinate of the major axis direction
` iAxisY`      The Y coordinate of the major axis direction
` iMajorRadius`      The length of the major axis
` iMinorRadius`      The length of the minor axis

### Func **CreateIntersection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAGeometry2D](../SketcherInterfaces/interface_Geometry2D_19898.md)

Creates and returns the intersection of an object with the sketch.

**Parameters:**

` iGeometry`      The object to intersect with the sketch

### Func **CreateIntersections**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md)

Creates and returns the possible intersections of an object with the sketch.

**Parameters:**

` iGeometry`      The object to intersect with the sketch

### Func **CreateLine**( double  `iX1`,  double  `iY1`,  double  `iX2`,  double  `iY2`) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md)

Creates and returns a 2D line.

**Parameters:**

` iX1`      The X coordinate of line first extremity
` iY1`      The Y coordinate of line first extremity
` iX2`      The X coordinate of line second extremity
` iY2`      The Y coordinate of line second extremity

### Func **CreateLineFromVector**( double  `iX1`,  double  `iY1`,  double  `iUX`,  double  `iUY`) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md)

Creates and returns a 2D line.

**Parameters:**

` iX1`      The X coordinate of the line origin
` iY1`      The Y coordinate of the line origin
` iUX`      The X component of the line vector
` iUY`      The Y component of the line vector

### Func **CreateParabola**( double  `iCenterX`,  double  `iCenterY`,  double  `iAxisX`,  double  `iAxisY`,  double  `iFocalDistance`) As [CATIAParabola2D](../SketcherInterfaces/interface_Parabola2D_18844.md)

Creates and returns a parabola.

**Parameters:**

` iCenterX`      The X coordinate of the parabola center
` iCenterY`      The Y coordinate of the parabola center
` iAxisX`      The X coordinate of the major axis direction
` iAxisY`      The Y coordinate of the major axis direction
` iFocalDistance`      The parabola focal distance

### Func **CreatePoint**( double  `iX`,  double  `iY`) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

Creates and returns a 2D point.

**Parameters:**

` iX`      The X coordinate of point to create
` iY`      The Y coordinate of point to create

### Func **CreateProjection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAGeometry2D](../SketcherInterfaces/interface_Geometry2D_19898.md)

Creates and returns the projection of an object on the sketch.

**Parameters:**

` iGeometry`      The object to project on the sketch

### Func **CreateProjections**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md)

Creates and returns the possible projections of an object on the sketch.

**Parameters:**

` iGeometry`      The object to project on the sketch

### Func **CreateSpline**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPoles`) As [CATIASpline2D](../SketcherInterfaces/interface_Spline2D_12098.md)

Creates and returns a 2D b-spline.

**Parameters:**

` iPoles`      An array of CATIAPoint2D forming the poles of the b-spline.