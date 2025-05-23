# ControlPoint2D (Object)

**_Class defining a spline control point in 2D Space._**

## Properties

### Property **Curvature**(| ) As double

   Returns the curvature properties of the spline control point

**Parameters:**

` oCurvature`      The curvature of the tangent determined at the control point
Methods

### Sub **GetTangent**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oTangent`)

   Returns the tangent properties of the spline control point

**Parameters:**

` oTangent[0]`      The X Coordinate of the tangent determined at the control point
` oTangent[1]`      The Y Coordinate of the tangent determined at the control point

### Sub **SetTangent**( double  `iTangentX`,  double  `iTangentY`)

   Imposes the tangent properties of the spline control point

**Parameters:**

` iTangentX`      The X Coordinate of the tangent determined at the control point
` iTangentY`      The Y Coordinate of the tangent determined at the control point

### Sub **UnsetCurvature**( )

   Unsets the curvature properties of the spline control point  
### Sub **UnsetTangent**( )

   Unsets the tangent properties of the spline control point