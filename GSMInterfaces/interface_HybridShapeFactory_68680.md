# HybridShapeFactory (Object)

**_Interface to create all kinds of HybridShape objects that may be needed in wireframe and surface design._**

Note:
This interface concern GSD/GSO/DL1 feature creation via VB
Use of the creation methods requires to have granted license configuration for feature creation
i.e:
\- Bump, Develop,WrapCurve,WrapSurface require GSO license.
\- Unfold, Develop require DL1 license.
\- Other require GSD license.

## Methods

### Func **AddNew3DCorner**(| [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iElement1`,| | [CATIAReference](../InfInterfaces/interface_Reference_17481.md) | `iElement2`,| | [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) | `iDirection`,| | double | `iRadius`,| | long | `iOrientation1`,| | long | `iOrientation2`,| | boolean | `iTrim`) As [CATIAHybridShapeCorner](../GSMInterfaces/interface_HybridShapeCorner_60814.md)

   Creates a new 3D Corner within the current body.
Create a 3D corner curve between a point and a curve or 2 curves along a direction.

**Parameters:**

` iElement1`      First reference curve.
` iElement2`      Second reference curve.
` iDirection`      Direction.
` iRadius`      Radius of the corner.
` iOrientation1`      Manage the corner center position. Value can be 1 or -1
` iOrientation2`      Manage the corner center position. Value can be 1 or -1
` iTrim`      Value can be FALSE or TRUE
if TRUE the 2 curves are trimed and asembled with the corner.
` oCorner`      Created corner.

### Func **AddNew3DCurveOffset**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurveToOffset`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  double  `iOffset`,  double  `iCornerRadius`,  double  `iCornerTension`) As [CATIAHybridShape3DCurveOffset](../GSMInterfaces/interface_HybridShape3DCurveOffset_116318.md)

   Creates a 3D Curve Offset.

**Parameters:**

` iCurve`      The curve to offset
` iDirection`      Offset pulling direction.
` iOffsetValue`      Offset Value.
` iCornerRadius`      Radius of the 3D corners.
` iCornerTension`      Tension of the 3D corners.

**Returns:**      CATIGSM3DCurveOffset_var created 3DCurveOffset.  
### Func **AddNewAffinity**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`,  double  `iXRatio`,  double  `iYRatio`,  double  `iZRatio`) As [CATIAHybridShapeAffinity](../GSMInterfaces/interface_HybridShapeAffinity_76221.md)

   Creates a new Affinity within the current body.

**Parameters:**

` iElement`      point, curve, surface or solid.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iXRatio`      Ratio of affinity in iX direction.
` iYRatio`      Ratio of affinity in iY direction.
` iZRatio`      Ratio of affinity in iZ direction.
` oAffinity`      Created affinity

### Func **AddNewAxisLine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`) As [CATIAHybridShapeAxisLine](../GSMInterfaces/interface_HybridShapeAxisLine_74458.md)

   Creates a new AxisLine within the current body.

**Parameters:**

` iElement`      Circle, Ellipse, Oblong, Sphere, Revolution surface. Axis is computed for this element
` oAxisLine`      Created axis line

### Func **AddNewAxisToAxis**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferenceAxis`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTargetAxis`) As [CATIAHybridShapeAxisToAxis](../GSMInterfaces/interface_HybridShapeAxisToAxis_91226.md)

   Creates a new axis to axis transformation within the current body.

**Parameters:**

` iObject`      Point, curve, surface or solid to transform.
` iReferenceAxis`      reference axis system
` iTargetAxis`      target axis system
` oAxisToAxis`      Created axis to axis transformation.

### Func **AddNewBlend**( ) As [CATIAHybridShapeBlend](../GSMInterfaces/interface_HybridShapeBlend_52604.md)

   Creates a new blend surface within the current body.

**Parameters:**

` oBlend`      The Blend object if succeded

### Func **AddNewBoundary**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iInitialElement`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iTypedePropagation`) As [CATIAHybridShapeBoundary](../GSMInterfaces/interface_HybridShapeBoundary_76575.md)

   Creates a new Boundary within the current body.

**Parameters:**

` iInitialElement`      the element used to initialise the propagation around the surface

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSupport`      the surface used to compute the boundary around it

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iTypedePropagation`      Propagation type the values are: 0 for Boundary for all edges 1 for Boundary propagation for edges on connexe point 2 for Boundary propagation for edges tangent at point breaks 3 for Boundary not propagation from the current edge
` oBoundary`      The computed element

### Func **AddNewBoundaryOfSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Surface`) As [CATIAHybridShapeBoundary](../GSMInterfaces/interface_HybridShapeBoundary_76575.md)

   Creates a Boundary within the current body.

**Parameters:**

` iSurface`      the feature on which all the boundaries will be computed
` oBoundary`      the whole boundary of the Surface given in first parameter

### Func **AddNewBump**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBodyToBump`) As [CATIAHybridShapeBump](../GSMInterfaces/interface_HybridShapeBump_47115.md)

   Creates a new Bump within the current body.
Note: require GSO license.

**Parameters:**

`:`      iBodyToBump Body to deform witn a Bump
`:`      oBump Bump result

### Func **AddNewCircle2PointsRad**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  boolean  `iGeodesic`,  double  `iRadius`,  long  `iOri`) As [CATIAHybridShapeCircle2PointsRad](../GSMInterfaces/interface_HybridShapeCircle2PointsRad_146741.md)

   Creates a new Circle passing through 2 points with a radius within the current body.

**Parameters:**

` iPoint1`      first passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPoint2`      second passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iGeodesic`      Puts the circle on the surface.
` iRadius`      Value specified is considered as radius. To use this value as diameter, set DiameterMode using SetDiameterMode method
` iOri`      circle orientation. Defines the side where circle is computed using the normal direction of line between the 2 passing points.
` oCircle`      The Circle object if succeded

### Func **AddNewCircle3Points**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint3`) As [CATIAHybridShapeCircle3Points](../GSMInterfaces/interface_HybridShapeCircle3Points_117560.md)

   Creates a new circle passing through 3 points within the current body.

**Parameters:**

` iPoint1`      first passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPoint2`      second passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPoint3`      third passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oCircle`      Created circle

### Func **AddNewCircleBitangentPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iOri1`,  long  `iOri2`) As [CATIAHybridShapeCircleBitangentPoint](../GSMInterfaces/interface_HybridShapeCircleBitangentPoint_199815.md)

   Creates a new circle tangent to 2 curves and passing through one point within the current body.

**Parameters:**

` iCurve1`      first curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iCurve2`      second curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPoint`      passing point. This point must lie on second curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iOri1`      first curve orientation for circle computation.
` iOri2`      second curve orientation for circle computation.
` oCircle`      Created circle

### Func **AddNewCircleBitangentRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iRadius`,  long  `iOri1`,  long  `iOri2`) As [CATIAHybridShapeCircleBitangentRadius](../GSMInterfaces/interface_HybridShapeCircleBitangentRadius_212126.md)

   Creates a new circle tangent to 2 curves and with a radius within the current body.

**Parameters:**

` iCurve1`      first curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iCurve2`      second curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iRadius`      Value specified is considered as radius. To use this value as diameter, set DiameterMode using SetDiameterMode method
` iOri1`      first curve orientation for circle computation.
` iOri2`      second curve orientation for circle computation.
` oCircle`      Created circle

### Func **AddNewCircleCenterAxis**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  double  `iValue`,  boolean  `iProjection`) As [CATIAHybridShapeCircleCenterAxis](../GSMInterfaces/interface_HybridShapeCircleCenterAxis_150107.md)

   Creates a circle from point and axis.

**Parameters:**

` iAxis`      Axis of plane in which circle is lying
` iPoint`      Point used for center computation. It will be the center if ProjectionMode is False. If ProjectionMode = True, this point will be projected on to axis/line
` iValue`      Value specified is considered as radius. To use this value as diameter, set DiameterMode property
` iProjection`      Sets Projection Mode. ProjectionMode = TRUE implies point will be projected on to axis/line, ProjectionMode = FALSE implies that point will be center of the circle.
` oCircle`      Created circle

### Func **AddNewCircleCenterAxisWithAngles**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  double  `iValue`,  boolean  `iProjection`,  double  `iStartAngle`,  double  `iEndAngle`) As [CATIAHybridShapeCircleCenterAxis](../GSMInterfaces/interface_HybridShapeCircleCenterAxis_150107.md)

   Creates a circle from point and axis.

**Parameters:**

` iAxis`      Axis of plane in which circle is lying
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): ` iPoint`      Point used for center computation. It will be the center if ProjectionMode is False. If ProjectionMode = True, this point will be projected on to axis/line
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): ` iValue`      Value specified is considered as radius. To use this value as diameter, set DiameterMode property
` iProjection`      Sets Projection Mode. ProjectionMode = TRUE implies point will be projected on to axis/line, ProjectionMode = FALSE implies that point will be center of the circle.
` iStartAngle`      start angle
` iEndAngle`      end angle
` oCircle`      Created circle

### Func **AddNewCircleCenterTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenterElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTangentCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iRadius`) As [CATIAHybridShapeCircleCenterTangent](../GSMInterfaces/interface_HybridShapeCircleCenterTangent_186102.md)

   Creates a new circle with given center element and tangent curve.

**Parameters:**

` iCenterElem`      Can be either curve or point.
` iTangentCurve`      Curve to which the circle will be tangent.
` iSupport`      support surface or plane.
` iRadius`      circle radius, valid only if center element is curve. Value specified is considered as radius. To use this value as diameter, set DiameterMode using SetDiameterMode method
` oCircle`      Created circle

### Func **AddNewCircleCtrPt**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrossingPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  boolean  `iGeodesic`) As [CATIAHybridShapeCircleCtrPt](../GSMInterfaces/interface_HybridShapeCircleCtrPt_98914.md)

   Creates a new whole circle defined by its center, a passing point within the current body.

**Parameters:**

` iCenter`      circle center.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iCrossingPoint`      passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iGeodesic`      Puts the circle on the surface.
` oCircle`      CreatedCircle

### Func **AddNewCircleCtrPtWithAngles**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrossingPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  boolean  `iGeodesic`,  double  `iStartAngle`,  double  `iEndAngle`) As [CATIAHybridShapeCircleCtrPt](../GSMInterfaces/interface_HybridShapeCircleCtrPt_98914.md)

   Creates a new circle defined by its center, a passing point and angles within the current body.

**Parameters:**

` iCenter`      circle center.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iCrossingPoint`      passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iGeodesic`      Puts the circle on the surface.
` iStartAngle`      start angle
` iEndAngle`      end angle
` oCircle`      Created circle

### Func **AddNewCircleCtrRad**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  boolean  `iGeodesic`,  double  `iRadius`) As [CATIAHybridShapeCircleCtrRad](../GSMInterfaces/interface_HybridShapeCircleCtrRad_106865.md)

   Creates a new whole circle defined by its center and a radius within the current body.

**Parameters:**

` iCenter`      circle center.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iGeodesic`      Puts the circle on the surface.
` iRadius`      Value specified is considered as radius. To use this value as diameter, set DiameterMode using SetDiameterMode method
` oCircle`      Created circle

### Func **AddNewCircleCtrRadWithAngles**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  boolean  `iGeodesic`,  double  `iRadius`,  double  `iStartAngle`,  double  `iEndAngle`) As [CATIAHybridShapeCircleCtrRad](../GSMInterfaces/interface_HybridShapeCircleCtrRad_106865.md)

   Creates a new circle defined by its center, a radius and angles within the current body.

**Parameters:**

` iCenter`      circle center.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iGeodesic`      Puts the circle on the surface.
` iRadius`      Value specified is considered as radius. To use this value as diameter, set DiameterMode using SetDiameterMode method
` iStartAngle`      start angle
` iEndAngle`      end angle
` oCircle`      Created circle

### Func **AddNewCircleDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapeCircleExplicit](../GSMInterfaces/interface_HybridShapeCircleExplicit_130251.md)

   Creates a new datum of circle within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oCircle`      Created datum

### Func **AddNewCircleTritangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve3`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iOri1`,  long  `iOri2`,  long  `iOri3`) As [CATIAHybridShapeCircleTritangent](../GSMInterfaces/interface_HybridShapeCircleTritangent_152975.md)

   Creates a new tritangent circle within the current body.

**Parameters:**

` iCurve1`      first curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iCurve2`      second curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iCurve3`      third curve to which the circle will be tangent.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSupport`      support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iOri1`      first curve orientation for circle computation.
` iOri2`      second curve orientation for circle computation.
` iOri3`      third curve orientation for circle computation.
` oCircle`      Created circle

### Func **AddNewCombine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondCurve`,  long  `iNearestSolutions`) As [CATIAHybridShapeCombine](../GSMInterfaces/interface_HybridShapeCombine_67178.md)

   Creates a new Combine within the current body. By default, the combine direction is the normal of each curve. If you want to change see CATIAHybridShapeCombine interfaces.

**Parameters:**

` iFirstCurve`      First curve to combine

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSecondCurve`      Second curve to combine

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iNearestSolution`      If more than one solution, to choose the nearest solution of the first curve
` oCombine`      The combine object if succeded

### Func **AddNewConic**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iStartingPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEndPoint`) As [CATIAHybridShapeConic](../GSMInterfaces/interface_HybridShapeConic_52888.md)

   Creates a new conic within the current body.

**Parameters:**

` iSupport`      The conic support (always a plane).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iStartingPoint`      Starting Point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iEndPoint`      End Point

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oConic`      The Conic object if succeded

### Func **AddNewConicalReflectLineWithType**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOrigin`,  double  `iAngle`,  long  `iOrientationSupport`,  long  `iType`) As [CATIAHybridShapeReflectLine](../GSMInterfaces/interface_HybridShapeReflectLine_99604.md)

   Creates a new conical ReflectLine within the current body.
Create a conical reflectline curve on a support surface from an origin point with an angle.

**Parameters:**

` iSupport`      Support surface.
` iOrigin`      Origin point.
` iAngle`      Angle of the reflectline.
` iOrientationSupport`      Manage the angle used to compute the reflectline. Value can be 1 or -1
` iType`      Manage the type used to compute the reflectline. Value can be 0 or 1 Returns or sets whether the reflectline curve is or should be created with the normal to the support or the tangent plane to the support.

**Role** : The TypeSolution indicates whether the created reflectline curve is compute with the angle between the normale to the support and the direction or with the angle between the tangent plane to the support and the direction..

**Legal values** : 0 for the normal and 1 for the tangent plane.
` oReflectLine`      Created conical reflectline.

### Func **AddNewConnect**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint1`,  long  `iOrient1`,  long  `iContinuity1`,  double  `iTension1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint2`,  long  `iOrient2`,  long  `iContinuity2`,  double  `iTension2`,  boolean  `Trim`) As [CATIAHybridShapeConnect](../GSMInterfaces/interface_HybridShapeConnect_67838.md)

   Creates a new Connect within the current body.

**Parameters:**

` iCurve1`      First curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPoint1`      First point (lying on the first curve)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iOrient1`      Orientation on the first curve
` iContinuity1`      Continuity on first curve
` iTension1`      Tension on first curve
` iCurve2`      Second curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPoint2`      Second point (lying on the second curve)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iOrient2`      Orientation on the second curve
` iContinuity2`      Continuity on second curve
` iTension2`      Tension on second curve
` iTrim`      Trim the two curves with the connect
` oConnect`      The connect object

### Func **AddNewCorner**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iRadius`,  long  `iOrientation1`,  long  `iOrientation2`,  boolean  `iTrim`) As [CATIAHybridShapeCorner](../GSMInterfaces/interface_HybridShapeCorner_60814.md)

   Creates a new Corner within the current body.
Create a corner curve between a point and a curve or 2 curves on a support surface.

**Parameters:**

` iElement1`      First reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iElement2`      Second reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      Support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iRadius`      Radius of the corner.
` iOrientation1`      Manage the corner center position. Value can be 1 or -1
` iOrientation2`      Manage the corner center position. Value can be 1 or -1
` iTrim`      Value can be FALSE or TRUE
if TRUE the 2 curves are trimed and asembled with the corner.
` oCorner`      Created corner.

### Func **AddNewCurveDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapeCurveExplicit](../GSMInterfaces/interface_HybridShapeCurveExplicit_121424.md)

   Creates a new datum of curve within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oCurve`      Created curve

### Func **AddNewCurvePar**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Curve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Support`,  double  `Distance`,  boolean  `InvertDirection`,  boolean  `Geodesic`) As [CATIAHybridShapeCurvePar](../GSMInterfaces/interface_HybridShapeCurvePar_74955.md)

   Creates a new CurvePar within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSupport`      Support on which the curve is lying on

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iDistance`      Distance value
` iInvertDirection`      Orientation
` iGeodesic`      Geodesic mode
` oCurvePar`      Parallel curve

### Func **AddNewCurveSmooth**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIACurve`) As [CATIAHybridShapeCurveSmooth](../GSMInterfaces/interface_HybridShapeCurveSmooth_102554.md)

   Creates a new CurveSmooth within the current body.

**Parameters:**

` iCurve`      Reference curve to be smoothened
` oCurveSmooth`      Smoothened curve

### Func **AddNewCylinder**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  double  `iRadius`,  double  `iFirstLength`,  double  `iSecondLength`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`) As [CATIAHybridShapeCylinder](../GSMInterfaces/interface_HybridShapeCylinder_75955.md)

   Creates a new Cylinder within the current body.

**Parameters:**

` iCenter`      Center of the Cylinder - Can be Point or Vertex.
Sub-element(s) supported (see
[Vertex](../MecModInterfaces/interface_Vertex_8466.md) object): ` iRadius`      Radius of Cylinder.
` iFirstLength`      Length of Cylinder in the given direction.
` iSecondLength`      Length of Cylinder in the opposite direction.
` iDirection`      Direction of extrusion for Cylinder.
` oCylinderObject`      Created CylinderObjct.

### Func **AddNewDatums**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Creates datums from a multi-domain result feature, one datum is created by object domain.
Note; Available only for a shape design feature as input ( not for datum feature ).

**Parameters:**

` iElem`      Reference element
` oArrayOfDatum`      List of datum objects , one datum is created per omain
Level of availability = V5R14

**Example** :      This example converts a hybrid shape object in as much as datums that the original hybrid shape features contains of domain

```VBScript
      Dim HShape
      Set reference   = part.CreateReferenceFromObject(hybridShapeObject)
      ' Convert to Datums
      HShape = hybridShapeFactory.AddNewDatums reference
      Num =UBound(HShape)
      For i = 0 to Num
            hybridBody1.AppendHybridShape HShape (i)
      Next
      part.InWorkObject = HShape(num)
      part.Update
      ' Delete original feature
      hybridShapeFactory.DeleteObjectForDatum reference

```

### Func **AddNewDevelop**( long  `iMode`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iToDevelop`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAHybridShapeDevelop](../GSMInterfaces/interface_HybridShapeDevelop_68134.md)

   Creates a new Develop within the current body.
Note: require either DL1 or GSO license.

**Parameters:**

` iMode`      Develop method.
` iToDevelop`      Wire to be developed.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSupport`      Revolution support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` oExt`      Created developed wire.

### Func **AddNewDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Creates a new direction specified by an element within the current body.

**Parameters:**

` iElement`      Line or plane specifying the direction. In case of plane, the plane normal vector is the direction

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` oDirection`      Created direction.

### Func **AddNewDirectionByCoord**( double  `iX`,  double  `iY`,  double  `iZ`) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Creates a new Direction specifed by coordinates within the current body.

**Parameters:**

` iX`      X component
` iY`      Y component
` iZ`      Z component
` oDirection`      Created direction

### Func **AddNewEmptyRotate**( ) As [CATIAHybridShapeRotate](../GSMInterfaces/interface_HybridShapeRotate_60980.md)

   Creates a new empty Rotate within the current body.  
### Func **AddNewEmptyTranslate**( ) As [CATIAHybridShapeTranslate](../GSMInterfaces/interface_HybridShapeTranslate_84680.md)

   Creates a new empty Translate within the current body.  
### Func **AddNewExtract**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Element`) As [CATIAHybridShapeExtract](../GSMInterfaces/interface_HybridShapeExtract_68586.md)

   Creates a new Extract within the current body.

**Parameters:**

` iElement`      Initial element used to start the extraction

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` oExt`      The extracted object

### Func **AddNewExtractMulti**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Element`) As [CATIAHybridShapeExtractMulti](../GSMInterfaces/interface_HybridShapeExtractMulti_111881.md)

   Creates a new Multiple Extract within the current body.

**Parameters:**

` iElement`      Initial element used to start the extraction

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` oExt`      The extracted object

### Func **AddNewExtrapolLength**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iToExtrapol`,  double  `iLength`) As [CATIAHybridShapeExtrapol](../GSMInterfaces/interface_HybridShapeExtrapol_76994.md)

   Creates a new Extrapol (specified by length) within the current body.

**Parameters:**

` iBoundary`      Boundary point of curve to extrapolate or boundary curve of surface to extrapolate.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iToExtrapol`      Curve or surface to extrapolate.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iLength`      Extrapolation length.
` oExtrapol`      Created Extrapolation.

### Func **AddNewExtrapolUntil**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBoundary`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iToExtrapol`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iUntil`) As [CATIAHybridShapeExtrapol](../GSMInterfaces/interface_HybridShapeExtrapol_76994.md)

   Creates a new Extrapol (until an element) within the current body.

**Parameters:**

` iBoundary`      Boundary point of curve to extrapolate or boundary curve of surface to extrapolate.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iToExtrapol`      Curve or surface to extrapolate.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iUntil`      Extrapolation limit surface.
` oExtrapol`      Created Extrapolation.

### Func **AddNewExtremum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjet`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDir`,  long  `iMinMax`) As [CATIAHybridShapeExtremum](../GSMInterfaces/interface_HybridShapeExtremum_77426.md)

   Creates a new Extremum within the current body.

**Parameters:**

` iObjet`      Element onto extremum is computed

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Face](../MecModInterfaces/interface_Face_3398.md). ` iDir`      Extremum direction
` iMinMax`      Maximum (GSMMax) or Minimum (GSMMin)
` oExt`      The extremum object if succeded

### Func **AddNewExtremumPolar**( short  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAContour`) As [CATIAHybridShapeExtremumPolar](../GSMInterfaces/interface_HybridShapeExtremumPolar_122024.md)

   Creates a new Extremum Polar within the current body.

**Parameters:**

` iType`      Type of extremum polar 0-Min Radius 1-Max Radius 2- Min Angle 3- Maximum Angle
` ipIAContour`      Extremum Polar Contour. It should be non convex
` opIAExtPolar`      The extremum polar object if succeded

### Func **AddNewExtrude**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToExtrude`,  double  `iOffsetDebut`,  double  `iOffsetFin`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`) As [CATIAHybridShapeExtrude](../GSMInterfaces/interface_HybridShapeExtrude_68828.md)

   Creates a new extrude within the current body.

**Parameters:**

` iObjectToExtrude`      Object to be extruded (point, line ,curve,or face)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iOffsetDebut`      Length value
` iOffsetFin`      Length value ( iOffsetFin has to be larger than iOffsetDebut)
` iDirection`      Extrusion direction
` oExtrudeObject`      Extruded result

### Func **AddNewFill**( ) As [CATIAHybridShapeFill](../GSMInterfaces/interface_HybridShapeFill_46556.md)

   Creates a new Fill within the current body.

**Parameters:**

` oFill`      Fill object

### Func **AddNewFilletBiTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  double  `iRadius`,  long  `iOrientation1`,  long  `iOrientation2`,  long  `iSupportsTrimMode`,  long  `iRibbonRelimitationMode`) As [CATIAHybridShapeFilletBiTangent](../GSMInterfaces/interface_HybridShapeFilletBiTangent_138802.md)

   Creates a new a sphere bitangent fillet between two skins.

**Parameters:**

` iElement1`      First support of fillet.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iElement2`      Second support of fillet.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iRadius`      Radius of the fillet.
` iOrientation1`      Manage the fillet center position.
` iOrientation2`      Manage the fillet center position.
` iSupportsTrimMode`      The 2 supports can be trimmed and assembled with the fillet. Value can be 0 (No trim ) or 1 (Trim)
` iRibbonRelimitationMode`      Manage the relimition of fillet extremities. Value can be : 0 (Smooth), 1 (Straight), 2 (Maximum) or 3 (Minimum)
` oFillet`      Created fillet.

### Func **AddNewFilletTriTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveElem`,  long  `iOrientation1`,  long  `iOrientation2`,  long  `iRemoveOrientation`,  long  `iSupportsTrimMode`,  long  `iRibbonRelimitationMode`) As [CATIAHybridShapeFilletTriTangent](../GSMInterfaces/interface_HybridShapeFilletTriTangent_151605.md)

   Creates a new a tritangent fillet between three skins.

**Parameters:**

` iElement1`      First support of fillet.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iElement2`      Second support of fillet.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iRemoveElem`      Support to remove of fillet.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iOrientation1`      Manage the fillet center position.
` iOrientation2`      Manage the fillet center position.
` iRemoveOrientation`      Manage the fillet center position.
` iSupportsTrimMode`      The 2 supports can be trimmed and assembled with the fillet. Value can be 0 (No trim ) or 1 (Trim)
` iRibbonRelimitationMode`      Manage the relimition of fillet extremities. Value can be : 0 (Smooth), 1 (Straight), 2 (Maximum) or 3 (Minimum)
` oFillet`      Created fillet.

### Func **AddNewHealing**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBodyToheal`) As [CATIAHybridShapeHealing](../GSMInterfaces/interface_HybridShapeHealing_66984.md)

   Creates a new healing within the current body.

**Parameters:**

` iBodyToHeal`      The body to heal
` oHealing`      The created healing

### Func **AddNewHelix**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`,  boolean  `iInvertAxis`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iStartingPoint`,  double  `iPitch`,  double  `iHeight`,  boolean  `iClockwiseRevolution`,  double  `iStartingAngle`,  double  `iTaperAngle`,  boolean  `iTaperOutward`) As [CATIAHybridShapeHelix](../GSMInterfaces/interface_HybridShapeHelix_53588.md)

   Creates a new Helix within the current body.

**Parameters:**

` iAxis`      The helix axis (always a line).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iInvertAxis`
` iStartingPoint`      Starting Point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPitch`      Pitch.
` iHeight`      Helix height.
` iClockwiseRevolution`      Revolutions are clockwise if TRUE, counterclockwise if FALSE.
` iStartingAngle`      Starting angle from starting point measured on the helix itself. If no starting angle is wanted, set it to 0.0.
` iTaperAngle`      0 <= Taper Angle < Pi/2 If no taper angle is wanted, set it to 0.0 (constant helix radius).
` iTaperOutward`      Helix radius increases if TRUE, decreases if FALSE.
` oHelix`      The Helix object if succeded

### Func **AddNewHybridScaling**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElemToScale`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  double  `iRatio`) As [CATIAHybridShapeScaling](../GSMInterfaces/interface_HybridShapeScaling_67358.md)

   Creates a new scaling within the current body.

**Parameters:**

` iElemToScale`      Point, curve, surface or solid to transform.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iCenter`      Reference point or reference plane.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iRatio`      Scaling ratio.
` oScaling`      Created scaling.

### Func **AddNewHybridSplit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  long  `iOrientation`) As [CATIAHybridShapeSplit](../GSMInterfaces/interface_HybridShapeSplit_54298.md)

   Creates a new Split within the current body.

**Parameters:**

` iElement1`      The feature to cut (curve or surface).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iElement2`      The cutting feature (point, curve, surface).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iOrientation`      Manage the kept side of the feature to cut (value can be 1 or -1)
` oSplit`      Created split

### Func **AddNewHybridTrim**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement1`,  long  `iOrientation1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  long  `iOrientation2`) As [CATIAHybridShapeTrim](../GSMInterfaces/interface_HybridShapeTrim_47387.md)

   Creates a new Trim within the current body by cutting and joining two elements.
You can trim a surface by a surface or a curve by a curve.

**Parameters:**

` iElement1`      The feature to trim (curve or surface).
` iOrientation1`      Manage the kept side of iElement1 (value can be 1 or -1).
` iElement2`      The second feature to trim (curve or surface).
` iOrientation2`      Manage the kept side of iElement2 (value can be 1 or -1).
` oTrim`      Created trim.

### Func **AddNewIntegratedLaw**( long  `iType`) As [CATIAHybridShapeIntegratedLaw](../GSMInterfaces/interface_HybridShapeIntegratedLaw_119452.md)

   Creates Integrated Law.

**Parameters:**

` iType`      Type of law = 0 : None = 1 : Constant = 2 : Linear = 3 : SType = 4 : Advanced = 5 : Implicit

### Func **AddNewIntersection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject2`) As [CATIAHybridShapeIntersection](../GSMInterfaces/interface_HybridShapeIntersection_112946.md)

   Creates a new Intersection within the current body.

**Parameters:**

` iObject1`      First element ( line, curve, plane, surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iObject2`      Second element ( line , curve, plane, surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` oIntersection`      Intersection

### Func **AddNewInverse**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Element`,  long  `Inverse`) As [CATIAHybridShapeInverse](../GSMInterfaces/interface_HybridShapeInverse_68654.md)

   Creates a new Inverse within the current body.

**Parameters:**

` iElement`      The objet to inverse
` iInverse`      the type of inversion (see CATGSMOrientation.h) 1 for no inversion -1 for inversion
` oInv`      The inverted object

### Func **AddNewJoin**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Element1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `Element2`) As [CATIAHybridShapeAssemble](../GSMInterfaces/interface_HybridShapeAssemble_75219.md)

   Creates a new Join within the current body.

**Parameters:**

` iElement1`      First element to join ( curve or surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iElement2`      Second element to join ( same type of the first element)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oExt`      Join result The default value used to join element is 0.001mm

### Func **AddNewLawDistProj**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDefinition`) As [CATIAHybridShapeLawDistProj](../GSMInterfaces/interface_HybridShapeLawDistProj_100210.md)

   Creates a new law within the current body.

**Parameters:**

` iReference`      Reference line of the law.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iDefinition`      Definition curve of the law.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oLaw`      The Law object if succeded

### Func **AddNewLineAngle**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  boolean  `iGeodesic`,  double  `iBeginOffset`,  double  `iEndOffset`,  double  `iAngle`,  boolean  `iOrientation`) As [CATIAHybridShapeLineAngle](../GSMInterfaces/interface_HybridShapeLineAngle_81468.md)

   Creates a new angle line within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iSurface`      Reference surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iPoint`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iGeodesic`      Puts the line on the surface
` iBeginOffset`      start offset
` iEndOffset`      end offset
` iAngle`      angle to reference curve
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineBiTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAHybridShapeLineBiTangent](../GSMInterfaces/interface_HybridShapeLineBiTangent_117650.md)

   Creates a new bitangent line within the current body.

**Parameters:**

` iCurve1`      First tangency curve lying on the support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iCurve2`      Second tangency element (point, curve) lying on the support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      The support surface of the two elements.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` oLine`      Created line

### Func **AddNewLineBisecting**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine2`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`,  long  `SolutionNb`) As [CATIAHybridShapeLineBisecting](../GSMInterfaces/interface_HybridShapeLineBisecting_119248.md)

   Creates a new bisecting line within the current body.

**Parameters:**

` iLine1`      First line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iLine2`      Second line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineBisectingOnSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`,  long  `SolutionNb`) As [CATIAHybridShapeLineBisecting](../GSMInterfaces/interface_HybridShapeLineBisecting_119248.md)

   Creates a new bisecting line on a support within the current body.

**Parameters:**

` iLine1`      First line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iLine2`      Second line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iSurface`      Reference surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineBisectingOnSupportWithPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRefPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`,  long  `SolutionNb`) As [CATIAHybridShapeLineBisecting](../GSMInterfaces/interface_HybridShapeLineBisecting_119248.md)

   Creates a new bisecting line on a support with a atarting point within the current body.

**Parameters:**

` iLine1`      First line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iLine2`      Second line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iRefPoint`      Starting point of the bisecting line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSurface`      Reference surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineBisectingWithPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRefPoint`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`,  long  `SolutionNb`) As [CATIAHybridShapeLineBisecting](../GSMInterfaces/interface_HybridShapeLineBisecting_119248.md)

   Creates a new bisecting line with a starting point within the current body.

**Parameters:**

` iLine1`      First line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iLine2`      Second line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iRefPoint`      Starting point of the bisecting line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapeLineExplicit](../GSMInterfaces/interface_HybridShapeLineExplicit_110473.md)

   Creates a new datum of line within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oLine`      Created datum

### Func **AddNewLineNormal**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`) As [CATIAHybridShapeLineNormal](../GSMInterfaces/interface_HybridShapeLineNormal_91444.md)

   Creates a new normal line within the current body.

**Parameters:**

` iSurface`      Reference surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iPoint`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLinePtDir**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`) As [CATIAHybridShapeLinePtDir](../GSMInterfaces/interface_HybridShapeLinePtDir_81218.md)

   Creates a new point-direction line within the current body.

**Parameters:**

` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iDirection`      Direction
` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLinePtDirOnSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`) As [CATIAHybridShapeLinePtDir](../GSMInterfaces/interface_HybridShapeLinePtDir_81218.md)

   Creates a new point-direction line within the current body.

**Parameters:**

` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iDirection`      Direction
` iSupport`      Support element (surface or plane)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLinePtPt**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtOrigine`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtExtremite`) As [CATIAHybridShapeLinePtPt](../GSMInterfaces/interface_HybridShapeLinePtPt_73797.md)

   Creates a new point-point line within the current body.

**Parameters:**

` iPtOrigine`      Origin point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPtExtremite`      Extremity point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oLine`      Created line

### Func **AddNewLinePtPtExtended**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtOrigine`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtExtremite`,  double  `iBeginOffset`,  double  `iEndOffset`) As [CATIAHybridShapeLinePtPt](../GSMInterfaces/interface_HybridShapeLinePtPt_73797.md)

   Creates a new point-point line with extensions within the current body.

**Parameters:**

` iPtOrigine`      Origin point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPtExtremite`      Extremity point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` oLine`      Created line

### Func **AddNewLinePtPtOnSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtOrigine`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtExtremite`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAHybridShapeLinePtPt](../GSMInterfaces/interface_HybridShapeLinePtPt_73797.md)

   Creates a new point-point line with support within the current body.

**Parameters:**

` iPtOrigine`      Origin point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPtExtremite`      Extremity point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      Support element (surface or plane)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` oLine`      Created line

### Func **AddNewLinePtPtOnSupportExtended**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtOrigine`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPtExtremite`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iBeginOffset`,  double  `iEndOffset`) As [CATIAHybridShapeLinePtPt](../GSMInterfaces/interface_HybridShapeLinePtPt_73797.md)

   Creates a new point-point line with extensions and with support within the current body.

**Parameters:**

` iPtOrigine`      Origin point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPtExtremite`      Extremity point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      Support element (surface or plane)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` oLine`      Created line

### Func **AddNewLineTangency**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`) As [CATIAHybridShapeLineTangency](../GSMInterfaces/interface_HybridShapeLineTangency_109970.md)

   Creates a new tangent line within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPoint`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLineTangencyOnSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iBeginOffset`,  double  `iEndOffset`,  boolean  `iOrientation`) As [CATIAHybridShapeLineTangency](../GSMInterfaces/interface_HybridShapeLineTangency_109970.md)

   Creates a new tangent line within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPoint`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      Support element (surface or plane)

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iBeginOffset`      start offset
` iEndOffset`      end offset
` iOrientation`      Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.
` oLine`      Created line

### Func **AddNewLoft**( ) As [CATIAHybridShapeLoft](../GSMInterfaces/interface_HybridShapeLoft_47138.md)

   Creates a new Loft within the current body.

**Parameters:**

` oExt`      CATIAHybridShapeLoft created

### Func **AddNewNear**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `MultiElement`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ReferenceElement`) As [CATIAHybridShapeNear](../GSMInterfaces/interface_HybridShapeNear_46501.md)

   Creates a new Near within the current body.

**Parameters:**

` iMultiElement`      Non connex element (point,curve,surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iReferenceElement`      Reference element

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oNear`      The result is the connex component that is the nearest from the reference element

### Func **AddNewOffset**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToOffset`,  double  `iOffset`,  boolean  `iOrientation`,  double  `iPrecision`) As [CATIAHybridShapeOffset](../GSMInterfaces/interface_HybridShapeOffset_60716.md)

   Creates a new offset within the current body.

**Parameters:**

` iObjectToOffset`      Surface to offset.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iOffset`      Offset value
` iOrientation`      Offset orientation
` iPrecision`      Offset users's precision
` oOffsetObject`      Offset Surface

### Func **AddNewPlane1Curve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlanarCurve`) As [CATIAHybridShapePlane1Curve](../GSMInterfaces/interface_HybridShapePlane1Curve_97590.md)

   Creates a new plane passing through one planar curve within the current body.

**Parameters:**

` iPlanarCurve`      passing curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oPlane`      Created plane

### Func **AddNewPlane1Line1Pt**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLn`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`) As [CATIAHybridShapePlane1Line1Pt](../GSMInterfaces/interface_HybridShapePlane1Line1Pt_110762.md)

   Creates a new plane passing through 1 line and 1 point within the current body.

**Parameters:**

` iLn`      passing line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` iPt`      passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPlane`      Created plane

### Func **AddNewPlane2Lines**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLn1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLn2`) As [CATIAHybridShapePlane2Lines](../GSMInterfaces/interface_HybridShapePlane2Lines_97036.md)

   Creates a new plane passing through 2 lines within the current body.

**Parameters:**

` iLn1`      first passing line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` iLn2`      second passing line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` oPlane`      Created line

### Func **AddNewPlane3Points**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt3`) As [CATIAHybridShapePlane3Points](../GSMInterfaces/interface_HybridShapePlane3Points_108127.md)

   Creates a new plane passing through 3 points within the current body.

**Parameters:**

` iPt1`      first passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPt2`      second passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPt3`      third passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPlane`      Created plane

### Func **AddNewPlaneAngle**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRevolAxis`,  double  `iAngle`,  boolean  `iOrientation`) As [CATIAHybridShapePlaneAngle](../GSMInterfaces/interface_HybridShapePlaneAngle_89924.md)

   Creates a new angle plane within the current body.

**Parameters:**

` iPlane`      reference plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iRevolAxis`      rotation axis

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` iAngle`      angle
` iOrientation`      Orientation to reverse the plane from the reference plane.
` oPlane`      Created plane

### Func **AddNewPlaneDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapePlaneExplicit](../GSMInterfaces/interface_HybridShapePlaneExplicit_120282.md)

   Creates a new datum of plane within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oPlane`      Created datum

### Func **AddNewPlaneEquation**( double  `iA_Coeff`,  double  `iB_Coeff`,  double  `iC_Coeff`,  double  `iD_Coeff`) As [CATIAHybridShapePlaneEquation](../GSMInterfaces/interface_HybridShapePlaneEquation_120590.md)

   Creates a new equation plane within the current body. Plane equation is Ax+By+Cz = D.

**Parameters:**

` iA_Coeff`      A coefficient
` iB_Coeff`      B coefficient
` iC_Coeff`      C coefficient
` iD_Coeff`      D coefficient
` oPlane`      Created plane

### Func **AddNewPlaneMean**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListOfPoints`,  long  `NbPoint`) As [CATIAHybridShapePlaneMean](../GSMInterfaces/interface_HybridShapePlaneMean_81488.md)

   Creates a new mean through points plane within the current body.

**Parameters:**

` oIListOfPoints`      list of passing points Warning : Input and Output parameter for CATScript applications, procedural type
` iNbPoint`      Number of points
` oPlane`      Created plane

### Func **AddNewPlaneNormal**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`) As [CATIAHybridShapePlaneNormal](../GSMInterfaces/interface_HybridShapePlaneNormal_100394.md)

   Creates a new normal plane within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPt`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPlane`      Created plane

### Func **AddNewPlaneOffset**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  double  `iOffset`,  boolean  `iOrientation`) As [CATIAHybridShapePlaneOffset](../GSMInterfaces/interface_HybridShapePlaneOffset_100364.md)

   Creates a new offset plane within the current body.

**Parameters:**

` iPlane`      reference plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iOffset`      offset value
` iOrientation`      Orientation to reverse the plane from the reference plane.
` oPlane`      Created plane

### Func **AddNewPlaneOffsetPt**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`) As [CATIAHybridShapePlaneOffsetPt](../GSMInterfaces/interface_HybridShapePlaneOffsetPt_118752.md)

   Creates a new offset trough point plane within the current body.

**Parameters:**

` iPlane`      reference plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iPt`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPlane`      Created plane

### Func **AddNewPlaneTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`) As [CATIAHybridShapePlaneTangent](../GSMInterfaces/interface_HybridShapePlaneTangent_109906.md)

   Creates a new tangent plane within the current body.

**Parameters:**

` iSurface`      reference surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPlane`      Created plane

### Func **AddNewPointBetween**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint2`,  double  `iRatio`,  long  `iOrientation`) As [CATIAHybridShapePointBetween](../GSMInterfaces/interface_HybridShapePointBetween_110853.md)

   Creates a new PointBetween within the current body.

**Parameters:**

` iPoint1`      Reference point to compute the barycenter.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPoint2`      Second point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iRatio`      barycenter parameter
` iOrientation`      To compute the barycenter of the segment [Pt1 - Pt2]
` oPoint`      PointBetween if succeded

### Func **AddNewPointCenter**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`) As [CATIAHybridShapePointCenter](../GSMInterfaces/interface_HybridShapePointCenter_101398.md)

   Creates a new circle center point within the current body.

**Parameters:**

` iCurve`      Reference circle

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Edge](../MecModInterfaces/interface_Edge_3456.md). ` oPoint`      Created point

### Func **AddNewPointCoord**( double  `iX`,  double  `iY`,  double  `iZ`) As [CATIAHybridShapePointCoord](../GSMInterfaces/interface_HybridShapePointCoord_92194.md)

   Creates a new point defined by its cartesian coordinates within the current body.

**Parameters:**

` iX`      X coordinate for the point
` iY`      Y coordinate for the point
` iZ`      Z coordinate for the point
` oPoint`      Created point

### Func **AddNewPointCoordWithReference**( double  `iX`,  double  `iY`,  double  `iZ`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`) As [CATIAHybridShapePointCoord](../GSMInterfaces/interface_HybridShapePointCoord_92194.md)

   Creates a new point defined its the cartesian coordinates regarding a reference point.

**Parameters:**

` iX`      X coordinate for the point
` iY`      Y coordinate for the point
` iZ`      Z coordinate for the point
` iPt`      Reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oPoint`      Created point

### Func **AddNewPointDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapePointExplicit](../GSMInterfaces/interface_HybridShapePointExplicit_121688.md)

   Creates a new datum of point within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oPoint`      Created datum

### Func **AddNewPointOnCurveFromDistance**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  double  `iLong`,  boolean  `iOrientation`) As [CATIAHybridShapePointOnCurve](../GSMInterfaces/interface_HybridShapePointOnCurve_110373.md)

   Creates a new point on a curve from a distance to an extremity within the current body.

**Parameters:**

` iCrv`      support curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iLong`      distance to extremity
` iOrientation`      Orientation = TRUE means that distance is measured in the other orientation of the curve and from the other extremity.
` oPoint`      Created point

### Func **AddNewPointOnCurveFromPercent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  double  `iLong`,  boolean  `iOrientation`) As [CATIAHybridShapePointOnCurve](../GSMInterfaces/interface_HybridShapePointOnCurve_110373.md)

   Creates a new point on a curve from a ratio of distance to an extremity within the current body.

**Parameters:**

` iCrv`      support curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iLong`      Ratio of curve length
` iOrientation`      Orientation = TRUE means that ratio is measured in the other orientation of the curve and from the other extremity.
` oPoint`      Created point

### Func **AddNewPointOnCurveWithReferenceFromDistance**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  double  `iLong`,  boolean  `iOrientation`) As [CATIAHybridShapePointOnCurve](../GSMInterfaces/interface_HybridShapePointOnCurve_110373.md)

   Creates a new point on a curve with a reference point and from a distance within the current body.

**Parameters:**

` iCrv`      support curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iLong`      distance (length) to reference point
` iOrientation`      Orientation = TRUE means that distance is measured in the other orientation of the curve
` oPoint`      Created point

### Func **AddNewPointOnCurveWithReferenceFromPercent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  double  `iLong`,  boolean  `iOrientation`) As [CATIAHybridShapePointOnCurve](../GSMInterfaces/interface_HybridShapePointOnCurve_110373.md)

   Creates a new point on a curve with a reference point and from a ratio of distance within the current body.

**Parameters:**

` iCrv`      Support curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iLong`      Ratio of curve length
` iOrientation`      Orientation = TRUE means that ratio is measured in the other orientation of the curve
` oPoint`      Created point

### Func **AddNewPointOnPlane**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  double  `iX`,  double  `iY`) As [CATIAHybridShapePointOnPlane](../GSMInterfaces/interface_HybridShapePointOnPlane_108958.md)

   Creates a new point on a plane within the current body.

**Parameters:**

` iPlane`      Support plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iX`      X cartesian coordinates in the plane.
` iY`      Y cartesian coordinates in the plane.
` oPoint`      Created point

### Func **AddNewPointOnPlaneWithReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  double  `iX`,  double  `iY`) As [CATIAHybridShapePointOnPlane](../GSMInterfaces/interface_HybridShapePointOnPlane_108958.md)

   Creates a new point on a plane with a reference point within the current body.

**Parameters:**

` iPlane`      Support plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iPt`      Reference plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iX`      X cartesian coordinates in the plane.
` iY`      Y cartesian coordinates in the plane.
` oPoint`      Created point

### Func **AddNewPointOnSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  double  `iX`) As [CATIAHybridShapePointOnSurface](../GSMInterfaces/interface_HybridShapePointOnSurface_129465.md)

   Creates a new point on a surface within the current body.

**Parameters:**

` iSurface`      Support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iDirection`      Direction from the reference point in which the point is computed.
` iX`      geodesic length to reference point
` oPoint`      Created point

### Func **AddNewPointOnSurfaceWithReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSurface`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPt`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  double  `iX`) As [CATIAHybridShapePointOnSurface](../GSMInterfaces/interface_HybridShapePointOnSurface_129465.md)

   Creates a new point on a surface with a reference point within the current body.

**Parameters:**

` iSurface`      Support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iPt`      reference point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iDirection`      Direction from the reference point in which the point is computed.
` iX`      geodesic length to reference point
` oPoint`      Created point

### Func **AddNewPointTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`) As [CATIAHybridShapePointTangent](../GSMInterfaces/interface_HybridShapePointTangent_111286.md)

   Creates a new tangent to curve point within the current body.

**Parameters:**

` iCurve`      Reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Edge](../MecModInterfaces/interface_Edge_3456.md). ` iDirection`      Direction in which tangent points are computed
` oPoint`      Created point

### Func **AddNewPolyline**( ) As [CATIAHybridShapePolyline](../GSMInterfaces/interface_HybridShapePolyline_76765.md)

   Creates a new Polyline within the current body.

**Parameters:**

` oPolyline`      The Polyline object if succeded

### Func **AddNewPositionTransfo**( long  `iMode`) As [CATIAHybridShapePositionTransfo](../GSMInterfaces/interface_HybridShapePositionTransfo_143932.md)

   Creates a new PositionTransfo within the current body.

**Parameters:**

` iMode`      Positioning mode.
` oExt`      Created positioning transformation (i.e. positioned wire / profile).

### Func **AddNewProject**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`) As [CATIAHybridShapeProject](../GSMInterfaces/interface_HybridShapeProject_68370.md)

   Creates a new Project within the current body.

**Parameters:**

` iElement`      Element to project (point, curve).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iSupport`      Curve or surface support for projection.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oProjection`      Created projection

### Func **AddNewReflectLine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDir`,  double  `iAngle`,  long  `iOrientationSupport`,  long  `iOrientationDirection`) As [CATIAHybridShapeReflectLine](../GSMInterfaces/interface_HybridShapeReflectLine_99604.md)

**Deprecated:**      V5R17 CATIAHybridShapeFactory#AddNewReflectLineWithType Creates a new ReflectLine within the current body.
Create a reflectline curve on a support surface along a direction with an angle.  **Parameters:**

` iSupport`      Support surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md). ` iAngle`      Angle of the reflectline.
` iOrientationSupport`      Manage the angle used to compute the reflectline. Value can be 1 or -1
` iOrientationDirection`      Manage the angle used to compute the reflectline. Value can be 1 or -1
` oReflectLine`      Created reflectline.

### Func **AddNewReflectLineWithType**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDir`,  double  `iAngle`,  long  `iOrientationSupport`,  long  `iOrientationDirection`,  long  `iType`) As [CATIAHybridShapeReflectLine](../GSMInterfaces/interface_HybridShapeReflectLine_99604.md)

   Creates a new ReflectLine within the current body.
Create a reflectline curve on a support surface along a direction with an angle.

**Parameters:**

` iSupport`      Support surface.
` iAngle`      Angle of the reflectline.
` iOrientationSupport`      Manage the angle used to compute the reflectline. Value can be 1 or -1
` iOrientationDirection`      Manage the angle used to compute the reflectline. Value can be 1 or -1
` iType`      Manage the type used to compute the reflectline. Value can be 0 or 1 Returns or sets whether the reflectline curve is or should be created with the normal to the support or the tangent plane to the support.

**Role** : The TypeSolution indicates whether the created reflectline curve is compute with the angle between the normale to the support and the direction or with the angle between the tangent plane to the support and the direction..

**Legal values** : 0 for the normal and 1 for the tangent plane.
` oReflectLine`      Created reflectline.

### Func **AddNewRevol**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToExtrude`,  double  `iOffsetDebut`,  double  `iOffsetFin`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`) As [CATIAHybridShapeRevol](../GSMInterfaces/interface_HybridShapeRevol_54128.md)

   Creates a new revolution within the current body.

**Parameters:**

` iObjectToExtrude`      Profile to be revolved

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iOffsetDebut`      Angle value
` iOffsetFin`      Angle value
` iAxis`      Revolution axis ( line that has to be in the profil plane

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md). ` oRevolObject`      Revolved result

### Func **AddNewRotate**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iToRotate`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`,  double  `iAngle`) As [CATIAHybridShapeRotate](../GSMInterfaces/interface_HybridShapeRotate_60980.md)

   Creates a new Rotate within the current body.

**Parameters:**

` iToRotate`      point, curve, surface or solid to transform.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iAxis`      Rotation axis.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Edge](../MecModInterfaces/interface_Edge_3456.md). ` iAngle`      Rotation angle.
` oRotate`      Created rotation.

### Func **AddNewSection**( ) As [CATIAHybridShapeSection](../GSMInterfaces/interface_HybridShapeSection_68352.md)

   Creates a new section.

**Parameters:**

` oSection`      Created Section

### Func **AddNewSphere**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iAxis`,  double  `iRadius`,  double  `iBeginParallelAngle`,  double  `iEndParallelAngle`,  double  `iBeginMeridianAngle`,  double  `iEndMeridianAngle`) As [CATIAHybridShapeSphere](../GSMInterfaces/interface_HybridShapeSphere_60614.md)

   Creates a new Sphere within the current body.

**Parameters:**

` iCenter`      Sphere center.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iAxis`      Sphere axis
` iRadius`      Radius
` iBeginParallelAngle`      Angle value
` iEndParallelAngle`      Angle value
` iBeginMeridianAngle`      Angle value
` iEndMeridianAngle`      Angle value
` oSphereObject`      Sphere result

### Func **AddNewSpine**( ) As [CATIAHybridShapeSpine](../GSMInterfaces/interface_HybridShapeSpine_53676.md)

   Creates a new spine within the current body.

**Parameters:**

` oExt`      CATIAHybridShapeSpine created

### Func **AddNewSpiral**( long  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenterPoint`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iAxis`,  double  `iStartingRadius`,  boolean  `iClockwiseRevolution`) As [CATIAHybridShapeSpiral](../GSMInterfaces/interface_HybridShapeSpiral_60794.md)

   Creates a new Spiral within the current body.

**Parameters:**

` iType`      Spiral is defined by AngleRadius, AnglePitch or PitchRadius.
` iSupport`      Spiral planar support.
` iCenterPoint`      Center point.
` iAxis`      Axis.
` iStartingRadius`      Defines the starting point: distance from the center point on the axis.
` iClockwiseRevolution`      Revolutions are clockwise if TRUE, counterclockwise if FALSE.
` oSpiral`      The Spiral object if succeded

### Func **AddNewSpline**( ) As [CATIAHybridShapeSpline](../GSMInterfaces/interface_HybridShapeSpline_60786.md)

   Creates a new Spline within the current body.

**Parameters:**

` oSpline`      Created spline.

### Func **AddNewSurfaceDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapeSurfaceExplicit](../GSMInterfaces/interface_HybridShapeSurfaceExplicit_141550.md)

   Creates a new datum of surface within the current body.

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oSurface`      Created surface

### Func **AddNewSweepCircle**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide1`) As [CATIAHybridShapeSweepCircle](../GSMInterfaces/interface_HybridShapeSweepCircle_100044.md)

   Creates a new SweepCircle within the current body.

**Parameters:**

` iGuide1`      First guide or center curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oExt`      Created swept surface.

### Func **AddNewSweepConic**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAGuide1`) As [CATIAHybridShapeSweepConic](../GSMInterfaces/interface_HybridShapeSweepConic_91167.md)

   Creates a new SweepConic within the current body.

**Parameters:**

` iGuide1`      First guide curve.
` opIASweepConic`      Created swept surface.

### Func **AddNewSweepExplicit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfile`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`) As [CATIAHybridShapeSweepExplicit](../GSMInterfaces/interface_HybridShapeSweepExplicit_121314.md)

   Creates a new SweepExplicit within the current body.

**Parameters:**

` iProfile`      Profile.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iGuide`      First guide curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` oExt`      Created swept surface.

### Func **AddNewSweepLine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide1`) As [CATIAHybridShapeSweepLine](../GSMInterfaces/interface_HybridShapeSweepLine_82824.md)

   Creates a new SweepLine within the current body.

**Parameters:**

` iGuide1`      First guide curve.
` oExt`      Created swept surface.

### Func **AddNewSymmetry**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`) As [CATIAHybridShapeSymmetry](../GSMInterfaces/interface_HybridShapeSymmetry_78389.md)

   Creates a new Symmetry within the current body.

**Parameters:**

` iObject`      Point, curve, surface or solid to transform.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iReference`      Point, line or reference plane.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [Edge](../MecModInterfaces/interface_Edge_3456.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` oSymmetry`      Created symmetry.

### Func **AddNewTransfer**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElementToTransfer`,  long  `iTypeOfTransfer`) As [CATIAHybridShapeTransfer](../GSMInterfaces/interface_HybridShapeTransfer_76460.md)

   Creates a new Transfer within the current body.
Note: require DL1 license.

**Parameters:**

` iElementToTransfer`      The element to transfer
` iTypeOfTransfer`      The type of transfer
` oExt`      Created Transfer operation.

### Func **AddNewTranslate**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElement`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`,  double  `iDistance`) As [CATIAHybridShapeTranslate](../GSMInterfaces/interface_HybridShapeTranslate_84680.md)

   Creates a new Translate within the current body.

**Parameters:**

` iElement`      Point, curve, surface or solid to translate.
` iDirection`      Translation direction.
` iDistance`      Translation Distance.
` oTranslate`      Created translation
` oTranslate`      Created Translate (Empty feature)
Note: Then translate mode and inputs has to be initialized

**See also:**      [HybridShapeTranslate](../GSMInterfaces/interface_HybridShapeTranslate_84680.md) 
### Func **AddNewUnfold**( ) As [CATIAHybridShapeUnfold](../GSMInterfaces/interface_HybridShapeUnfold_60645.md)

   Creates a new Unfold within the current body.
Note: require DL1 license.

**Parameters:**

` oExt`      Created unfold operation.

### Func **AddNewVolumeDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`) As [CATIAHybridShapeVolumeExplicit](../GSMInterfaces/interface_HybridShapeVolumeExplicit_132217.md)

   Creates a new datum of volume within the current body.
Note: requires GSO License

**Parameters:**

` iObject`      The object whose topological body will be duplicated and put into created datum
` oVolume`      Created Volume

### Func **AddNewWrapCurve**( ) As [CATIAHybridShapeWrapCurve](../GSMInterfaces/interface_HybridShapeWrapCurve_83970.md)

   Creates a new Wrap Curve Surface within the current body.
Note: require GSO license.

**Parameters:**

` oWrapCurve`      The Wrap Curve object if succeded

### Func **AddNewWrapSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBodyToDeform`) As [CATIAHybridShapeWrapSurface](../GSMInterfaces/interface_HybridShapeWrapSurface_100696.md)

   Creates a new Wrap Surface within the current body.
Note: require GSO license.

**Parameters:**

`:`      iBodyToDeform Body to deform with a Wrap Surface
` oWrapSurface`      The Wrap Surface object if succeded

### Sub **ChangeFeatureName**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `Name`)

   Set display name for Shape Design Features.

**Parameters:**

` iElem`      Element to rename
` Name`      User name

### Sub **DeleteObjectForDatum**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObject`)

   Deletes an object within the current body.

**Parameters:**

` iObject`      Object to delete

### Sub **GSMVisibility**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`,  long  `Show`)

   Set Visibility attribut for Shape Design Features.

**Parameters:**

` iElem`      Element to show/NoShow
` Show`      = 0 NoShow , 1= Show

### Func **GetGeometricalFeatureType**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`) As short

   Returns type of "geometrical" shape Design feature .

**Parameters:**

` iElem`      Reference element
` oType`      Type of feature = 0 , Unknown = 1 , Point = 2 , Curve = 3 , Line = 4 , Circle = 5 , Surface = 6 , Plane = 7 , Solid, Volume
Level of availability = V5R14