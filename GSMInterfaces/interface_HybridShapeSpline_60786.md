# HybridShapeSpline (Object)

**_Represents the hybrid shape spline feature object._**

**Role** : To access the data of the hybrid shape spline feature object. This data includes:

  * The support surface
  * The control points
  * The tension at each control point
  * The curvature radius at each control point

Use the CATIAHybridShapeFactory to create a HybridShapeAffinity object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Sub **AddPoint**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `ipIAPoint`)

   Add a new point .

**Parameters:**

` iPoint`      Point element.

### Sub **AddPointWithConstraintExplicit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAPoint`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `ipIADirTangency`,  double  `iTangencyNorm`,  long  `iInverseTangency`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `ipIADirCurvature`,  double  `iCurvatureRadius`)

   Add a new point with explicit tangency and curvature.

**Parameters:**

` ipIAPoint`      Point element.
` ipIADirTangency`      Tangent direction.
` iTangencyNorm`      Tension.
` iInverseTangency`      Flag to reverse tangent direction (value can be 1 or -1).
` ipIADirCurvature`      Curvature direction.
` iCurvatureRadius`      Curvature radius value.

### Sub **AddPointWithConstraintFromCurve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIACurveCst`,  double  `iTangencyNorm`,  long  `iInvertValue`,  long  `iCrvCstType`)

   Add a new point with tangency/curvature from a curve.

**Parameters:**

` ipIAPoint`      Point element.
` ipIACurveCst`      Curvature direction.
` iTangencyNorm`      tension factor for tangency.
` iInvertValue`      Orientation for tangent
` iCrvCstType`      Continuity type for Curve Constraint (1=Tangency , 2-= Curvature).

### Func **GetClosure**( ) As long

   Gets whether the curve is closed.

**Parameters:**

` oClosed`      Closing flag

1
   for a closed curve
0
   for an open curve

### Func **GetConstraintType**( long  `iPos`) As long

   Returns the ControlPoint type at the given position.

**Parameters:**

` iPos`      The poistion of the point to retrieve
` oCstType`      Type of Control point (CstType=0 : not defined / CstType=1 : Explicit / CstType=2 : FromCurve)

### Func **GetCurvatureRadius**( long  `iPos`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

   Returns the curvature radius value for each point of the spline.

**Parameters:**

` iPos`      The position of the point in the spline.

**Legal values** : first position is 1. The position cannot be 0.
` oRadius`      The curvature radius value at this point

### Func **GetDirectionInversion**( long  `iPos`) As long

   Gets the orientation of the tangent direction .

**Parameters:**

` oInvertFlag`      invert flag = 1 No Inversion = -1 Invert
` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Func **GetNbControlPoint**( ) As long

   Returns the number of control points.

**Parameters:**

` oNbCtrPt`      The number of control points.

### Func **GetPoint**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the Point at the given position.

**Parameters:**

` iPos`      The poistion of the point to retrieve
` opIAPoint`      Type of Control point (TypeCtrPoint =1 : Explicit / TypeCtrPoint =2 : FromCurve)

### Sub **GetPointConstraintExplicit**( long  `iPos`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `opIADirTangency`,  double  `oTangencyNorm`,  long  `oInverseTangency`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `opIADirCurvature`,  double  `oCurvatureRadius`)

   Returns the Constraint of the point at iPos.
Available for Explicit Point Constraint type (CstType =1 from GetContraintType)

**Parameters:**

` iPos`      The position of the point to retrieve
` opIADirTangency`      Tangent direction.
` oTangencyNorm`      Tension.
` oInverseTangency`      Flag to reverse tangent direction (value can be 1 or -1).
` opIADirCurvature`      Curvature direction.
` oCurvatureRadius`      Curvature radius value.

### Sub **GetPointConstraintFromCurve**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIACurveCst`,  double  `oTangencyNorm`,  long  `oInvertValue`,  long  `oCrvCstType`)

   Returns the Constraint of the point at iPos.
Available for FromCurve Point Constraint type (CstType =2 from GetContraintType)

**Parameters:**

` iPos`      The position of the point to retrieve
` opIACurveCst`      Curvature direction.
` oTangencyNorm`      tension factor for tangency.
` oInvertValue`      Orientation for tangent
` oCrvCstType`      Continuity type for Curve Constraint (1=Tangency , 2-= Curvature).

### Func **GetPointPosition**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAPoint`) As long

   Returns the position of a given point.

**Parameters:**

` ipIAPoint`      Point
` oPos`      The position of the point (=0 Point Not in Spline)

### Func **GetSplineType**( ) As long

   Gets the spline type.

**Parameters:**

` oType`      = 0 : Cubic Type Spline. = 1 : WilsonFowler Type Spline.

### Func **GetSupport**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Gets the support surface.

**Parameters:**

` oSupport`      Supporting surface for spline (if exist)

### Func **GetTangentNorm**( long  `iPos`) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns the tension for each point of the spline.
The tension is the tangent norm at the given point.

**Parameters:**

` iPos`      The position of the point in the spline.

**Legal values** : first position is 1. The position cannot be 0.
` oTension`      The tension at this point

### Sub **InvertDirection**( long  `iPos`)

   Inverts the orientation of the tangent direction .

**Parameters:**

` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Sub **RemoveAll**( )

   Removes all elements in the list of points.  
### Sub **RemoveControlPoint**( long  `iPos`)

   Removes a point at the given position.

**Parameters:**

` iPos`      The position of the point to remove

### Sub **RemoveCurvatureRadiusDirection**( long  `iPos`)

   Removes Curvature Radius Direction for the given point of the spline.

**Parameters:**

` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Sub **RemoveCurvatureRadiusValue**( long  `iPos`)

   Removes Curvature Radius Value for the given point of the spline.

**Parameters:**

` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Sub **RemoveSupport**( )

   Removes the support surface.  
### Sub **RemoveTangentDirection**( long  `iPos`)

   Removes tangent Direction for the given point of the spline.

**Parameters:**

` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Sub **RemoveTension**( long  `iPos`)

   Removes the Tension for the given point of the spline.

**Parameters:**

` iPos`      Position of point in spline First Position is 1 Position 0 return E_FAIL

### Sub **ReplacePointAtPosition**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Replaces a point in the list at the given position.

**Parameters:**

` oPoint`      Point
` iPos`      Replace position

### Sub **SetClosing**( long  `iClosingType`)

   Activates the closing option of the spline.

**Parameters:**

` iClosingType`      The spline closing option

### Sub **SetPointAfter**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAPoint`)

   Sets the Point After a given position.

**Parameters:**

` iPos`      The position reference (0 < position < Nbpt)
` ipIAPoint`      Point

### Sub **SetPointBefore**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAPoint`)

   Sets the Point Before a given position.

**Parameters:**

` iPos`      The position reference (1 < position < Nbpt+1)
` ipIAPoint`      Point

### Sub **SetPointConstraintExplicit**( long  `iPos`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `ipIADirTangency`,  double  `iTangencyNorm`,  long  `iInverseTangency`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `ipIADirCurvature`,  double  `iCurvatureRadius`)

   Sets the Constraint of the point at iPos.
Available for Explicit Point Constraint type (CstType =1 from GetContraintType)

**Parameters:**

` iPos`      The position of the point to retrieve
` ipIADirTangency`      Tangent direction.
` iTangencyNorm`      Tension.
` iInverseTangency`      Flag to reverse tangent direction (value can be 1 or -1).
` ipIADirCurvature`      Curvature direction.
` iCurvatureRadius`      Curvature radius value.

### Sub **SetPointConstraintFromCurve**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIACurveCst`,  double  `iTangencyNorm`,  long  `iInvertValue`,  long  `iCrvCstType`)

   Sets the Constraint of the point at iPos.
Available for From Curve Point Constraint type (CstType =2 from GetContraintType)

**Parameters:**

` iPos`      The position of the point to retrieve
` ipIACurveCst`      Curvature direction.
` iTangencyNorm`      tension factor for tangency.
` iInvertValue`      Orientation for tangent
` iCrvCstType`      Continuity type for Curve Constraint (1=Tangency , 2-= Curvature).

### Sub **SetSplineType**( long  `iSplineType`)

   Sets the spline type.

**Parameters:**

` iSplineType`      The spline type

**Legal values** : Cubic spline (0) or WilsonFowler (1)

### Sub **SetSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Sets the spline support surface.
Have your "tangent direction" tangent to this support is recommended.

**Parameters:**

` iSupport`      The spline support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).