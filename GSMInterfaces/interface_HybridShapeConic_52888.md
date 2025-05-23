# HybridShapeConic (Object)

**_Represents the hybrid shape conic object._**

**Role** : To access the data of the hybrid shape conic object. This data includes:

  * The start point and its associated tangent contraint
  * The end point and its associated tangent contraint
  * The supporting plane
  * The tangent intersection point
  * The conic parameter: p = 0.5 (parabola), 0<=p<=0.5 (ellipse), 0.5<= p <=1.0 (hyperbola)

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) to create a HybridShapeConic object.

## Properties

### Property **ConicParameter**(| ) As double

   Returns or sets the conic parameter.

**Example** :      This example retrieves in `conicParm` the conic parameter of the conic `hybConic`.

```VBScript
     Dim conicParm As double
     Set conicParm = hybConic.ConicParameter

```

### Property **ConicUserTol**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Gets or sets the conic User Tolerance.

**Example** :      This example retrieves in `conicUserTol` the conic user tolerance of the conic `HybridShapeConic`.

```VBScript
     Dim oConicUserTol As  CATIALength
     Set oConicUserTol = HybridShapeConic.conicUserTol

```

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) 
### Property **EndPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the conic end point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `endPt` the end point of the conic `hybConic`.

```VBScript
     Dim endPt As Reference
     Set endPt = hybConic.EndPoint

```

### Property **EndTangent**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the tangent direction at the conic end point.

**Example** :      This example retrieves in `endTgt` the tangent direction associated with the end point of the conic `hybConic`.

```VBScript
     Dim endTgt As Reference
     Set endTgt = hybConic.EndTangent

```

### Property **StartPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the conic start point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example sets `startPt` as the start point of the conic `hybConic`.

```VBScript
     Dim startPt As Reference
     ... ' Value startPt
     hybConic.StartPoint startPt

```

### Property **StartTangent**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the tangent direction at the conic start point.

**Example** :      This example sets `startTgt` as the tangent direction at the start point of the conic `hybConic`.

```VBScript
     Dim startTgt As Reference
     ... ' Value startTangent
     hybConic.StartTangent startTgt

```

### Property **SupportPlane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the conic supporting plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

**Example** :      This example retrieves in `supportPln` the supporting plane of the conic `hybConic`.

```VBScript
     Dim supportPln As Reference
     Set supportPln = hybConic.SupportPlane

```

### Property **TangentIntPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the conic tangent intersection point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `tgtIntPt` the tangent intersection point of the conic `hybConic`.

```VBScript
     Dim tgtIntPt As Reference
     Set tgtIntPt = hybConic.TangentIntPoint

```

Methods

### Sub **GetEndTangentDirectionFlag**( long  `oOrientation`)

   Retrieves the tangent direction orientation at the conic end point.

**Parameters:**

` oOrientation`      The direction orientation applied to the tangent direction at the conic end point

**Legal values** : 1 if the tangent direction is used as is, and -1 if it is inverted

**Example:**      This example retrieves the direction orientation of the tangent at the end point of the conic `hybConic`.

```VBScript
     Dim endPtTgtOrient As long
     hybConic.GetEndTangentDirectionFlag endPtTgtOrient

```

### Func **GetIntermedTangent**( long  `iIndexPoint`) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Retrieves the tangent direction at one of the conic intermediate passing points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point to retrieve

**Legal values** : 1 for the first passing point, and 2 for the second one
` oTgtDir`      The retrieved tangent direction at the given passing point

**Example:**      This example retrieves in `tgtDir` the tangent direction at point `passingPtIdx` through which the conic `hybConic` passes.

```VBScript
     Dim tgtDir As Reference
     passingPtIdx = 1
     Set tgtDir = hybConic.GetIntermedTangent (passingPtIdx)

```

### Sub **GetIntermediatePoint**( long  `iIndexPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oEndPoint`)

   Retrieves one of the conic intermediate passing points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point to retrieve

**Legal values** : 1 for the first passing point, 2 for the second one, and 3 for the third one
` oEndPoint`      The retrieved passing point

**Example:**      This example retrieves in `passingPt` the second point through which the conic `hybConic` passes.

```VBScript
     Dim passingPt As Reference
     passingPtIdx = 2
     hybConic.GetIntermediatePoint passingPtIdx, passingPt

```

### Sub **GetIntermediateTangentDirectionFlag**( long  `iIndexPoint`,  long  `oOrientation`)

   Retrieves the tangent direction orientation of one of the conic intermediate points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point to retrieve

**Legal values** : 1 for the first passing point, and 2 for the second one
` oOrientation`      The direction orientation applied to the tangent direction at the intermediate passing point

**Legal values** : 1 if the tangent direction is used as is, and -1 if it is inverted

**Example:**      This example retrieves the direction orientation of the tangent at the first point through which the conic `hybConic` passes.

```VBScript
     passingPtIdx = 1
     Dim passingPtTgtOrient As long
     hybConic.GetIntermediateTangentDirectionFlag passingPtIdx, passingPtTgtOrient

```

### Sub **GetStartTangentDirectionFlag**( long  `oOrientation`)

   Retrieves the tangent direction orientation at the conic start point.

**Parameters:**

` oOrientation`      The direction orientation applied to the tangent direction at the conic start point

**Legal values** : 1 if the tangent direction is used as is, and -1 if it is inverted

**Example:**      This example retrieves the direction orientation of the tangent at the start point of the conic `hybConic`.

```VBScript
     Dim startPtTgtOrient As long
     hybConic.GetStartTangentDirectionFlag startPtTgtOrient

```

### Sub **SetEndTangentDirectionFlag**( long  `iOrientation`)

   Sets the tangent direction orientation at the conic end point.

**Parameters:**

` iOrientation`      The direction orientation to be applied to the tangent direction at the conic end point

**Legal values** : 1 if the tangent direction is to be used as is, and -1 if it must be inverted

**Example:**      This example sets the direction orientation of the tangent at the end point of the conic `hybConic` to the one of the direction used for the tangent.

```VBScript
     endPtTgtOrient = 1
     hybConic.SetEndTangentDirectionFlag endPtTgtOrient

```

### Sub **SetIntermediatePoint**( long  `iIndexPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEndPoint`)

   Sets one of the conic intermediate passing points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point to retrieve

**Legal values** : 1 for the first passing point, 2 for the second one, and 3 for the third one
` iEndPoint`      The passing point to set.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  **Example:**      This example sets `passingPt` as the first point through which the conic `hybConic` must pass.

```VBScript
     Dim passingPt As Reference
     ... ' Value passingPt
     passingPtIdx = 1
     hybConic.SetIntermediatePoint passingPtIdx, passingPt

```

### Sub **SetIntermediateTangent**( long  `iIndexPoint`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iTgtDir`)

   Sets the tangent direction at one of the conic intermediate passing points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point where the tangent direction is to be set

**Legal values** : 1 for the first passing point, and 2 for the second one
` iTgtDir`      The direction to set as the tangent direction at the given passing point

**Example:**      This example sets `tgtDir` as the tangent direction at the first point through which the conic `hybConic` passes.

```VBScript
     Dim tgtDir As Reference
     ... ' Value tgtDir
     passingPtIdx = 1
     hybConic.SetIntermediateTangent passingPtIdx, tgtDir

```

### Sub **SetIntermediateTangentDirectionFlag**( long  `iIndexPoint`,  long  `iOrientation`)

   Sets the tangent direction orientation of one of the conic intermediate points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point to retrieve

**Legal values** : 1 for the first passing point, and 2 for the second one
` iOrientation`      The direction orientation to be applied to the tangent direction at the intermediate passing point

**Legal values** : 1 if the tangent direction is to be used as is, and -1 if it must be inverted

**Example:**      This example sets the direction orientation of the tangent at the first point through which the conic `hybConic` passes to the inverse of the one of the direction used for the tangent.

```VBScript
     passingPtIdx = 1
     passingPtTgtOrient = -1
     hybConic.SetIntermediateTangentDirectionFlag passingPtIdx, passingPtTgtOrient

```

### Sub **SetStartAndEndTangentsPlusConicParameter**( [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iStartTgt`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iEndTgt`,  double  `iConicParam`)

   Sets the tangent directions at conic start and end points, and the conic parameter.

**Parameters:**

` iStartTgt`      The tangent direction at the start point
` iEndTgt`      The tangent direction at the end point
` iConicParam`      The conic parameter

**Legal values** : p = 0.5 (parabola), 0<=p<=0.5 (ellipse), 0.5<= p <=1.0 (hyperbola)

**Example:**      This example sets `firstDir` and `secondDir` as the tangent directions at the start and end points of the conic `hybConic`, and `conicParm` as the conic parameter.

```VBScript
     hybConic.SetStartAndEndTangentsPlusConicParameter firstDir, secondDir, conicParm

```

### Sub **SetStartAndEndTangentsPlusPassingPoint**( [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iStartTgt`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iEndTgt`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassingPt`)

   Sets the tangent directions at conic start and end points, and a passing point.

**Parameters:**

` iStartTgt`      The tangent direction at the start point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iEndTgt`      The tangent direction at the end point
` iPassingPt`      A point through which the conic must pass.

**Legal values** : This point must differ from the start and end points.

**Example:**      This example sets `firstDir` and `secondDir` as the tangent directions at the start and end points of the conic `hybConic`, and `passingPoint` as a point through which the conic must pass.

```VBScript
     hybConic.SetStartAndEndTangentsPlusPassingPoint firstDir, secondDir, passingPoint

```

### Sub **SetStartTangentDirectionFlag**( long  `iOrientation`)

   Sets the tangent direction orientation at the conic start point.

**Parameters:**

` iOrientation`      The direction orientation to be applied to the tangent direction at the conic start point

**Legal values** : 1 if the tangent direction is to be used as is, and -1 if it must be inverted

**Example:**      This example sets the direction orientation of the tangent at the start point of the conic `hybConic` to the inverse of the one of the direction used for the tangent.

```VBScript
     startPtTgtOrient = -1
     hybConic.SetStartTangentDirectionFlag startPtTgtOrient

```

### Sub **SetTangentIntersectPointPlusConicParm**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTgtInt`,  double  `iConicParam`)

   Sets the intersection point of the conic tangents to the start and end points, and the conic parameter.

**Parameters:**

` iTgtInt`      The point intersection of the conic tangents to the start and end point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iConicParam`      The conic parameter

**Legal values** : p = 0.5 (parabola), 0<=p<=0.5 (ellipse), 0.5<= p <=1.0 (hyperbola)

**Example:**      This example sets `tgtIntPoint` as the intersection point of the tangents to the start and end points of the conic `hybConic`, and `conicParm` as the conic parameter.

```VBScript
     hybConic.SetTangentIntersectPointPlusConicParm tgtIntPoint, conicParm

```

### Sub **SetTangentIntersectPointPlusPassingPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTgtInt`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassingPt`)

   Sets the intersection point of the conic tangents to the start and end points, and a passing point.

**Parameters:**

` iTgtInt`      The point intersection of the conic tangents to the start and end point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPassingPt`      A point through which the conic must pass.

**Legal values** : This point must differ from the start and end points.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  **Example:**      This example sets `tgtIntPoint` as the intersection point of the tangents to the start and end points of the conic `hybConic`, and `passingPoint` as a point through which the conic must pass.

```VBScript
     hybConic.SetTangentIntersectPointPlusPassingPoint tgtIntPoint, passingPoint

```

### Sub **SetThreeIntermediatePassingPoints**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassPt1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassPt2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassPt3`)

   Sets three conic intermediate passing points.

**Parameters:**

` iPassPt1`      The first intermediate passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPassPt2`      The second intermediate passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPassPt3`      The third intermediate passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  **Example:**      This example sets `passingPoint1`, `passingPoint2`, and `passingPoint3` as the three intermediate points through which the conic `hybConic` must pass.

```VBScript
     hybConic.SetThreeIntermediatePassingPoints passingPoint1, passingPoint2, passingPoint3

```

### Sub **SetTwoIntermediatePassingPointsPlusOneTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassPt1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPassPt2`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iTgtDir`,  long  `iIndexPoint`)

   Sets two conic intermediate passing points and a tangent at one of the passing points.

**Parameters:**

` iPassPt1`      The first intermediate passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iPassPt2`      The second intermediate passing point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iTgtDir`      The tangent direction at one of the intermediate passing points
` iIndexPoint`      An index indicating the passing point to which the tangent direction applies

**Legal values** : 1 for the first passing point, and 2 for the second one

**Example:**      This example sets `passingPoint1` and `passingPoint2` as two intermediate points through which the conic `hybConic` must pass, `tgtDir` as the tangent direction at the passing point designated by `passingPointIdx`.

```VBScript
     hybConic.SetTwoIntermediatePassingPointsPlusOneTangent passingPoint1, passingPoint2, tgtDir, passingPointIdx

```

### Sub **SwitchEndTangentDirection**( )

   Inverts the tangent direction orientation at the conic end point.

**Example:**      This example inverts the direction orientation of the tangent at the end point of the conic `hybConic`.

```VBScript
     hybConic.SwitchEndTangentDirection

```

### Sub **SwitchIntermediateTangentDirection**( long  `iIndexPoint`)

   Inverts the tangent direction orientation of one of the conic intermediate points.

**Parameters:**

` iIndexPoint`      An index that designates the passing point where the tangent direction is to be inverted

**Legal values** : 1 for the first passing point, and 2 for the second one

**Example:**      This example inverts the direction orientation of the tangent at the first point through which the conic `hybConic` passes.

```VBScript
     passingPtIdx = 1
     hybConic.SwitchIntermediateTangentDirection passingPtIdx

```

### Sub **SwitchStartTangentDirection**( )

   Inverts the tangent direction orientation at the conic start point.

**Example:**      This example inverts the direction orientation of the tangent at the start point of the conic `hybConic`.

```VBScript
     hybConic.SwitchStartTangentDirection

```