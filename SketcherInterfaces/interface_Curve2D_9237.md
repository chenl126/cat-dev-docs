# Curve2D (Object)

**_Class defining a curve in 2D Space._**

## Properties

### Property **Continuity**( ) As short (Read Only)

Returns the highest level of geometric continuity the curve possesses.

**Parameters:**

` oLevel`      The maximum geometric continuity level

### Property **EndPoint**( ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

Returns the end point of the curve. The end point is decided with respect to the logical flow imposed on the curve by the object.

**Parameters:**

` oEndPoint`      The end point of the curve

### Property **Period**( ) As double (Read Only)

Returns the period of a periodic curve.

**Parameters:**

` oPeriod`      The period of the curve.

### Property **StartPoint**( ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

Returns the start point of the curve. The start point is decided with respect to the logical flow imposed on the curve by the object.

**Parameters:**

` oStartPoint`      The start point of the curve
Methods

### Sub **GetCurvature**( double  `iParam`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCurvature`)

Returns the curvature and curvature direction at the parameter specified.

**Parameters:**

` iParam`      The parameter of the chosen point on the curve.
` oCurvature[0]`      The curvature at the specified parameter.
` oCurvature[1;2]`      The unit-vector of curvature direction at the specified parameter.

### Sub **GetDerivatives**( double  `iParam`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDerivative`)

Returns the first, second and third derivatives at the parameter specified.

**Parameters:**

` iParam`      The parameter of the chosen point on the curve.
` oDerivative[0]`      First degree derivative.
` oDerivative[1]`      Second degree derivative.
` oDerivative[2]`      Third degree derivative.

### Sub **GetEndPoints**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oEndPoints`)

Returns the end-points of the curve. The start point and the end point are decided with respect to the logical flow imposed on the curve by the object.

**Parameters:**

` oEndPoints[0]`      The x coordinate of the start point
` oEndPoints[1]`      The y coordinate of the start point
` oEndPoints[2]`      The x coordinate of the end point
` oEndPoints[3]`      The y coordinate of the end point

### Func **GetLengthAtParam**( double  `iFromParam`,  double  `iToParam`) As double

Returns the length, measured along the curve, from a given parameter to a given parameter.

**Parameters:**

` iFromParam`      The parameter from which the length is to be measured.
` iToParam`      The parameter to which the length is to be measured.
` oLength`      The length between the parameters

### Func **GetParamAtLength**( double  `iFromParam`,  double  `iLength`) As double

Returns the parameter at a given length, measured along the curve, starting from a given parameter. The direction of measurement is always in the direction of the logical flow of the curve. If no inherent logical flow can be assigned the direction is the direction of increasing parameterization.

**Parameters:**

` iFromParam`      The parameter from which the length needs to be measured.
` iLength`      The length of the curve to be measured from iFromParam in the logical flow direction of the curve.
` oParam`      The computed parameter.

### Sub **GetParamExtents**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oParams`)

Returns the parametric extents of the curve. This is the parametric equivalent of the end-points.

**Parameters:**

` oParams[0]`      The parameter associated with the start point of the curve
` oParams[1]`      The parameter associated with the end point of the curve

### Sub **GetPointAtParam**( double  `iParam`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPoint`)

Returns a point on the curve computed from an input parameter.

**Parameters:**

` iParam`      The parameter
` oPoint`      The X and Y coordinates of the computed 2D space point.

### Sub **GetRangeBox**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oBoundPoint`)

Returns the range box (or bounding box) of the object
The box is axially aligned within the local coordinate system of the server.

**Parameters:**

` oBoundPoint[0]`      The minimum x point of the box
` oBoundPoint[1]`      The minimum y point of the box
` oBoundPoint[2]`      The maximum x point of the box
` oBoundPoint[3]`      The maximum y point of the box

### Sub **GetTangent**( double  `iParam`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oTangency`)

Returns the unit-vector tangent at the parameter specified.

**Parameters:**

` iParam`      The parameter of the chosen point on the curve.
` oTangency`      The X and Y coordinates of the unit-vector tangent at the specified parameter.

### Func **IsPeriodic**( ) As boolean

Specifies whether a curve is periodic or not.

**Parameters:**

` oPeriodic`      Returns true if the curve is periodic.