# Spline2D (Object)

**_Class defining a spline in 2D Space._**
A 2D spline is defined by its constituting control points.

## Methods

### Sub **GetControlPoints**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `oCtrlPoints`)

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