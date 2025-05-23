# SketcherInterfaces Framework

## Object Index

  * [Axis2D](SketcherInterfaces/interface_Axis2D_6614.md)
  * [Circle2D](SketcherInterfaces/interface_Circle2D_11806.md)
  * [ControlPoint2D](SketcherInterfaces/interface_ControlPoint2D_39214.md)
  * [Curve2D](SketcherInterfaces/interface_Curve2D_9237.md)
  * [Ellipse2D](SketcherInterfaces/interface_Ellipse2D_15520.md)
  * [Factory2D](SketcherInterfaces/interface_Factory2D_15860.md)
  * [GeometricElement](SketcherInterfaces/interface_GeometricElement_54654.md)
  * [Geometry2D](SketcherInterfaces/interface_Geometry2D_19898.md)
  * [Hyperbola2D](SketcherInterfaces/interface_Hyperbola2D_23520.md)
  * [Line2D](SketcherInterfaces/interface_Line2D_6416.md)
  * [Parabola2D](SketcherInterfaces/interface_Parabola2D_18844.md)
  * [Point2D](SketcherInterfaces/interface_Point2D_9306.md)
  * [Sketch](SketcherInterfaces/interface_Sketch_8026.md)
  * [Spline2D](SketcherInterfaces/interface_Spline2D_12098.md)

## Enumerated Types Index

  * [CatGeometricType](SketcherInterfaces/enum_CatGeometricType_54488.md)

---

# CatGeometricType (Enumeration)

**_Enumeration for all types of possible geometrical elements._**

**Values:**

` catGeoTypeUnknown`      The element does not fit in any of the following types.
` catGeoTypeAxis2D`      The geometrical element is a 2D axis.
` catGeoTypePoint2D`      The geometrical element is a 2D point.
` catGeoTypeLine2D`      The geometrical element is a 2D line.
` catGeoTypeControlPoint2D`      The geometrical element is a 2D spline control point.
` catGeoTypeCircle2D`      The geometrical element is a 2D circle.
` catGeoTypeHyperbola2D`      The geometrical element is a 2D hyperbola.
` catGeoTypeParabola2D`      The geometrical element is a 2D parabola
` catGeoTypeEllipse2D`      The geometrical element is a 2D ellipse.
` catGeoTypeSpline2D`      The geometrical element is a 2D spline.
` catGeoTypePoint`      The geometrical element is a 3D point.
` catGeoTypeLine`      The geometrical element is a 3D line.
` catGeoTypePlane`      The geometrical element is a 3D plane.

---

# Axis2D (Object)

**_Interface defining a coordinate system in the 2D Space._**

## Properties

### Property **HorizontalReference**( ) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md) (Read Only)

   Returns the 2D coordinate system horizontal axis.  
### Property **Origin**( ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md) (Read Only)

   Returns the 2D coordinate system origin.  
### Property **VerticalReference**( ) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md) (Read Only)

   Returns the 2D coordinate system vertical axis.

---

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

---

# ControlPoint2D (Object)

**_Class defining a spline control point in 2D Space._**

## Properties

### Property **Curvature**( ) As double

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

---

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

---

# Ellipse2D (Object)

**_Class defining an ellipse in 2D Space._**

## Properties

### Property **CenterPoint**( ) As [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)

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

---

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

---

# GeometricElement (Object)

**_2D or 3D wireframe geometric element._**

## Properties

### Property **GeometricType**( ) As [CatGeometricType](../SketcherInterfaces/enum_CatGeometricType_54488.md) (Read Only)

   Returns the type of the underlying geometrical element

**Parameters:**

` oType`      Specific type of the geometric interface

---

# Geometry2D (Object)

**_2D wireframe geometric element._**

## Properties

### Property **Construction**( ) As boolean

   Returns the construction mode of the 2D geometry  
### Property **ReportName**( ) As long

   Returns the report name of the 2D geometry

**Parameters:**

` oReportName`      The integer value of the report name

---

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

---

# Line2D (Object)

**_Class defining a line in 2D Space._**

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

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

---

# Parabola2D (Object)

**_Class defining an parabola in 2D Space._**

## Properties

### Property **FocalDistance**( ) As double (Read Only)

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

---

# Point2D (Object)

**_Class defining a point in 2D Space._**

## Methods

### Sub **GetCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPoint`)

   Returns the coordinates of the point

**Parameters:**

` oPoint[0]`      The X Coordinate of the point
` oPoint[1]`      The Y Coordinate of the point

### Sub **SetData**( double  `iX`,  double  `iY`)

   Modifies the coordinates of the point

**Parameters:**

` iX`      The X Coordinate of the point
` iY`      The Y Coordinate of the point

---

# Sketch (Object)

**_The Sketch is a 2D based element comprising constrained 2D geometrical elements._**
The Sketch is created by giving a 2D support.

## Properties

### Property **AbsoluteAxis**( ) As [CATIAAxis2D](../SketcherInterfaces/interface_Axis2D_6614.md) (Read Only)

   Returns the 2D absolute axis of the sketch. The absolute axis is used for constraining the sketch in 3D space, and its constituting horizontal and vertical directions can also be used to constrain horizontally or vertically subsequent geometrical elements in the sketch.

**Returns:**      oAxis The absolute axis of the sketch (@see CATIAAxis2D for more information).

**Example:**     The following example places in `myAxis` the absolute axis
of the sketch `mySketch`:

```VBScript
     Set myAxis = mySketch.**AbsoluteAxis**

```

### Property **CenterLine**( ) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md)

   Returns the geometric 2D line defined as the center line of the sketch. Center lines are then used for creating shafts.

**Returns:**      oLine The center line of the sketch(@see CATIALine2D for more information).

**Example:**     The following example returns in `myCenterLine` the center line
in the sketch `mySketch`:

```VBScript
     Set myCenterLine = mySketch.**CenterLine**

```

### Property **Constraints**( ) As [CATIAConstraints](../MecModInterfaces/interface_Constraints_27490.md) (Read Only)

   Returns the list of constraints included in the sketch.

**Returns:**      oConstraints The list of constraints in the sketch (@see CATIAConstraints
for more information).

**Example:**     The following example returns in `colConstraint` the list of constraints
in the sketch `mySketch`:

```VBScript
     Set colConstraint = mySketch.**Constraints**

```

### Property **Factory2D**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md) (Read Only)

   Returns the 2D factory of the sketch. Take care that you must open edition
on a sketch before adding or modifying elements in it.

**Returns:**      oFactory The 2D geometrical factory of the sketch (@see CATIAFactory2D
for more information).

**Example:**     The following example returns in `my2DFactory` the 2D factory
of the sketch `mySketch`:

```VBScript
     Set my2DFactory = mySketch.**Factory2D**

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

   Returns the list of geometrical elements included in the sketch.

**Returns:**      oGeometricElements The list of geometric elements in the sketch (@see CATIAGeometricElements
for more information).

**Example:**     The following example returns in `colGeometry` the list of geometrical
elements in the sketch `mySketch`:

```VBScript
     Set colGeometry = mySketch.**GeometricElements**

```

Methods

### Sub **CloseEdition**( )

   Closes the Sketch Edition. Once you have finished working with the sketch, you
must close its edition before using it for sketch-based shapes.

**Example:**     The following example closes the edition of the sketch `mySketch`:

```VBScript
     mySketch.**CloseEdition**

```

### Sub **Evaluate**( )

   Evaluate the constraint system of the sketch  
### Sub **GetAbsoluteAxisData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAxisData`)

   Returns the sketch axis coordinates in 3D space. The matrix returned comprises 9 doubles, the first 3 being the coordinates
of the axis origin, the next 3 being those of the horizontal axis, and the
last 3 those of the vertical axis.
The sketch horizontal axis is in fact computed from the first non null projection of one of the 3 3D space axes on the sketch plane.

**Returns:**      oAxisData The matrix of the axis in 3D space.

**Example:**     The following example reads the coordinates of the axis
of the sketch `mySketch`:

```VBScript
     Dim myAxisCoordinate (8)
     mySketch.GetAbsoluteAxisData myAxisCoordinate
     Set OriginX = myAxisCoordinate(1)
     Set OriginY = myAxisCoordinate(2)
     Set OriginZ = myAxisCoordinate(3)
     Set HorizontalX = myAxisCoordinate(4)
     Set HorizontalY = myAxisCoordinate(5)
     Set HorizontalZ = myAxisCoordinate(6)
     Set VerticalX = myAxisCoordinate(7)
     Set VerticalY = myAxisCoordinate(8)
     Set VerticalZ = myAxisCoordinate(9)

```

### Sub **InverseOrientation**( )

   Inverse Orientation Of Sketch  
### Func **OpenEdition**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md)

   Opens the Sketch Edition. You must open edition on a sketch before you can add
elements in it. The CATIAFactory2D returned then enables you to create 2D
geometrical elements in the sketch.

**Returns:**      oFactory Returns the 2D FACTORY.

**Example:**     The following example opens edition on the sketch `mySketch`
and places the factory in `my2DFactory`:

```VBScript
     Set my2DFactory = mySketch.**OpenEdition**

```

### Sub **SetAbsoluteAxisData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAxisData`)

   Sets the absolute axis of the sketch in 3D space.

**Parameters:**

` oAxisData`      The matrix comprises 9 doubles, the first 3 being the coordinates
of the axis origin, the next 3 being those of the horizontal axis,
and the last 3 those of the vertical axis of the absolute axis.

---

# Spline2D (Object)

**_Class defining a spline in 2D Space._**
A 2D spline is defined by its constituting control points.

## Methods

### Sub **GetControlPoints**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCtrlPoints`)

   Returns the control points making up the spline.

**Parameters:**

` oCtrlPoints`      The control points of the spline

**Example:**     The following example fetches the list of control points defining the
spline`mySpline`:

```VBScript
     mySpline.GetControlPoints **ControlPoints**

```

### Func **GetNumberOfControlPoints**( ) As double

   Returns the number of Control Points of the Spline

**Parameters:**

` oNumber`      The number of control points*

### Sub **InsertControlPointAfter**( [CATIAPoint2D](../SketcherInterfaces/interface_Point2D_9306.md)  `iCtrlPoint`,  long  `iPosition`)

   Inserts control points in the spline. If a 2D point is given (and not a control
point), a new control point is created and aggregated in the spline.

**Parameters:**

` iCtrlPoint`      The new point to be inserted. (@see CATIAPoint2D and CATIAControlPoint2D
for more information).
` iPosition`      The position at which to insert the point.
To insert a new control point as the first element, set iPosition to 0.

**Example:**     The following example inserts a control point `myCtrlPoint` as the second
element of the spline`mySpline`:

```VBScript
     call mySpline.**InsertControlPointAfter** (myCtrlPoint, 1)

```