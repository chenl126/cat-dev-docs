# HybridShapeBlend (Object)

**_Represents the hybrid shape blended surface object._**

**Role** : To access the data of the hybrid shape blended surface object.

This data includes:

  * Two support surfaces, one at each limit of the blended surface
  * Two curves, one for each support surface
  * The curve closing points

Use the CATIAHybridShapeFactory to create a HybridShapeBlend object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Coupling**(| ) As long

   Returns or sets the type of coupling between the limits of the blend.

**Legal values** : The values representing the type of coupling can be:

1     Ratio: the curves are coupled according to the curvilinear abscissa ratio 2     Tangency: the curves are coupled according to their tangency discontinuity points. If they do not have the same number of tangency discontinuity points, they cannot be coupled and an error message is displayed 3     Tangency then curvature: the curves are coupled according to their tangency discontinuity points first, then according to their curvature discontinuity points. If they do not have the same number of tangency and curvature discontinuity points, they cannot be coupled and an error message is displayed 4     Vertices: the curves are coupled according to their vertices. If they do not have the same number of vertices, they cannot be coupled and an error message is displayed 5     Spine: coupling is completely driven by a curve (called spine)

**Example** :      This example retrieves in `CouplingVal` the coupling value of the `ShpBlend` hybrid shape blended feature.

```VBScript
     CouplingVal = ShpBlend.Coupling

```

### Property **RuledDevelopableSurface**( ) As boolean

   Returns or sets the ruled developable surface mode.
TRUE means that the mode is enabled and FALSE means that it is disabled.  
### Property **SmoothAngleThreshold**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the angular threshold.  
### Property **SmoothAngleThresholdActivity**( ) As boolean

   Returns or sets information whether a blending operation is smoothed or not.
TRUE if the blending operation is smoothed, or FALSE otherwise (FALSE if not specified).  
### Property **SmoothDeviation**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the deviation value (length) from guide curves allowed during a sweeping operation in order to smooth it.  
### Property **SmoothDeviationActivity**( ) As boolean

   Returns or sets information whether a deviation from guide curves is allowed or not.
Gives the information on performing smoothing during blending operation.
TRUE if a deviation from guide curves is allowed, or FALSE otherwise (FALSE if not specified).  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets a curve used as spine for coupling in Blend computation. Setting the spine curve also changes coupling mode to CATGSMSpineCoupling. In order to remove the spine, set another coupling mode.

**Parameters:**

` iSpine`      spine curve
Methods

### Func **GetBorderMode**( long  `iBlendLimit`) As long

   Returns the type of border to a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose type of border is to be retrieved.

**Legal values** : 1 for the first limit, and 2 for the second one

**Returns:**      The type of border

**Legal values** :

1     The border of the blend will be tangent to the border of the support surface, or if the curve ends on the border of a face of the support surface, then the border of the blend will be tangent to the border face. 2     The border of the blend is not constrained.  **Example** :      This example retrieves in `BorderType` the type of border of the first limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     BorderType = ShpBlend.GetBorderMode(1)

```

### Func **GetClosingPoint**( long  `iBlendLimit`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the closing point of a closed curve of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose curve closing point is returned.

**Legal values** : 1 for the first curve, and 2 for the second one

**Returns:**      The retrieved closing point  **Example** :      This example retrieves in `ClosingPoint` the closing point of the curve of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Dim ClosingPoint As Reference
     ClosingPoint = ShpBlend.GetClosingPoint(2)

```

### Func **GetContinuity**( long  `iBlendLimit`) As long

   Retrieves the continuity of a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose continuity is to be retrieved.

**Legal values** : 1 for the first limit, and 2 for the second one

**Returns:**      The retrieved continuity.

**Legal values** :

0     Point continuity 1     Tangency continuity 2     Curvature continuity  **Example** :      This example retrieves in `Continuity` the continuity of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Continuity = ShpBlend.GetContinuity(2)

```

### Func **GetCurve**( long  `iBlendLimit`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns a curve from the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend from which the curve will be retrieved.

**Legal values** : 1 for the first curve, and 2 for the second one

**Returns:**      The retrieved curve  **Example** :      This example retrieves in `BlendCurve` the curve of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Dim BlendCurve As Reference
     BlendCurve = ShpBlend.GetCurve(2)

```

### Func **GetOrientation**( long  `iBlendLimit`) As long

   Returns the orientation of a curve of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose curve orientation is to be retrieved.

**Legal values** : 1 for the first curve, and 2 for the second one

**Returns:**      The orientation to set to the curve.

**Legal values** : 1 for direct and -1 for reverse  **Example** :      This example retrieves in `Orientation` the orientation of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Orientation = ShpBlend.GetOrientation(2)

```

### Func **GetRuledDevelopableSurfaceConnection**( long  `iBlendLimit`) As long

   Returns or sets the ruled developable surface connection type.

**Parameters:**

` iBlendLimit`      The limit of the blend for which the connection type is to be set.

**Legal values** : 1 for the start limit, and 2 for the end one
` oBlendConnection`      The value of connection type

**Legal values** :

1     Connect to both extremities 2     Free first curve 3     Free second curve

### Func **GetSupport**( long  `iBlendLimit`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns a support from the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose support is to be retrieved.

**Legal values** : 1 for the first support, and 2 for the second one

**Returns:**      The retrieved support surface  **Example** :      This example retrieves in `SupportSurf` the support surface of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Dim SupportSurf As Reference
     SupportSurf = ShpBlend.GetSupport(2)

```

### Func **GetTensionInDouble**( long  `iBlendLimit`,  long  `iRank`) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

   Returns the tension values of a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend from which the tension type and values are to be retrieved.

**Legal values** : 1 for the first limit, and 2 for the second one
` iRank`      The rank of the value to retrieve among those available, depending on the tension type.

**Legal values** : `iRank` can take the following values:

1     With default tension and constant tension, for the unique available value, and with linear tension for the first value 2     With linear tension for the second value

**Returns:**      The retrieved tension value  **Example** :      This example retrieves in `TensionVal` the tension value of the tension, supposed to be a constant tension, of the first limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     Dim ConstTensionVal As RealParam
     Set ConstTensionVal = ShpBlend.GetTensionInDouble(1, 1)

```

### Func **GetTensionType**( long  `iBlendLimit`) As long

   Returns the tension type of a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend from which the tension type is to be retrieved.

**Legal values** : 1 for the first limit, and 2 for the second one

**Returns:**      The value of tension type

**Legal values** :

1     Default tension 2     Constant tension 3     Linear tension  **Example** :      This example retrieves in `TensionType` the tension type of the first limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     TensionType.GetTensionType(1)

```

### Func **GetTransition**( long  `iBlendLimit`) As long

   Returns the transition orientation from a limit of the blend.
Let `T` be the tangent to the wire, and `N` be the normal to the skin body. The transition orientation defines how the blend goes from the initial wires: it takes the direction of `iTransition*(T^N)`, where `^` is the cross product.

**Parameters:**

` iBlendLimit`      The limit of the blend whose transition orientation is to be retrieved.

**Legal values** : 1 for the first support, and 2 for the second one

**Returns:**      The retrieved value of transition orientation.

**Legal values** : 1 for direct and -1 for reverse  **Example** :      This example retrieves in `TransOrientation` the transition orientation of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     TransOrientation = ShpBlend.GetTransition(2)

```

### Func **GetTrimSupport**( long  `iBlendLimit`) As long

   Returns whether a support of the blend will be trimmed off.
If the support is set to be trimmed, it will be trimmed using the curve then joined to the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose support is to be trimmed.

**Legal values** : 1 for the first limit, and 2 for the second one

**Returns:**      The trim support mode

**Legal values** :

1     No trim 2     The support will be trimmed  **Example** :      This example retrieves whether the second limit of the `ShpBlend` hybrid shape blended feature should be trimmed off.

```VBScript
     IsTrimmed = ShpBlend.GetTrimSupport(2)

```

### Sub **InsertCoupling**( long  `iPosition`)

   Inserts a coupling into the blend.

**Parameters:**

` iPosition`      The position of the coupling in the list of couplings. Setting `iPosition` to 0 inserts the coupling at the end of the list.  **Example** :      This example inserts a coupling at the end of the coupling list of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.InsertCouplingt 0

```

### Sub **InsertCouplingPoint**( long  `iCouplingIndex`,  long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Inserts a coupling point to a coupling of the blend.

**Parameters:**

` iCouplingIndex`      The index of the coupling in the list of couplings into which the coupling point will be inserted.
` iPosition`      The position of the coupling point in the list of coupling points. Setting `iPosition` to 0 inserts the coupling point at the end of the list.
` iPoint`      The coupling point to be inserted. This point must lay on the section with the same position.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  **Example** :      This example inserts the `Point23` point into the third coupling at the end of the list of coupling points of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.InsertCouplingPoint 3, 0, Point23

```

### Sub **SetBorderMode**( long  `iBlendLimit`,  long  `iBorder`)

   Sets the type of border to a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose type of border is to be set.

**Legal values** : 1 for the first limit, and 2 for the second one
` iBorder`      The type of border

**Legal values** :

1     The border of the blend will be tangent to the border of the support surface, or if the curve ends on the border of a face of the support surface, then the border of the blend will be tangent to the border face. 2     The border of the blend is not constrained. 3     The border of the blend will be tangent to the border of the support surface at the start extremity of the curve, or if the curve ends on the border of a face of the support surface, then the border of the blend will be tangent to the border face at the start extremity of the curve. 4     The border of the blend will be tangent to the border of the support surface at the end extremity of the curve, or if the curve ends on the border of a face of the support surface, then the border of the blend will be tangent to the border face at the end extremity of the curve.  **Example** :      This example sets the type of border of the second limit of the `ShpBlend` hybrid shape blended feature to "no constraint".

```VBScript
     ShpBlend.SetBorderMode 2, 2

```

### Sub **SetClosingPoint**( long  `iBlendLimit`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iClosingPoint`)

   Sets a new closing point to a closed curve of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose curve will be set a new closing point.

**Legal values** : 1 for the first curve, and 2 for the second one
` iClosingPoint`      The closing point to be set. This point must lay on the curve of the blend limit.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  **Example** :      This example sets the `Point10` point as the closing point to the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.SetClosingPoint 2, Point10

```

### Sub **SetContinuity**( long  `iBlendLimit`,  long  `iContinuity`)

   Sets the continuity to a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose continuity is to be set.

**Legal values** : 1 for the first limit, and 2 for the second one
` iContinuity`      The continuity to set

**Legal values** :

0     Point continuity 1     Tangency continuity 2     Curvature continuity  **Example** :      This example sets the continuity of the second limit of the `ShpBlend` hybrid shape blended feature to tangency continuity.

```VBScript
     ShpBlend.SetContinuity 2, 1

```

### Sub **SetCurve**( long  `iBlendLimit`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCurve`)

   Sets a curve to the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend to which the curve will be set.

**Legal values** : 1 for the first curve, and 2 for the second one
` iCurve`      The curve to be set.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  **Example** :      This example sets the `CurveForBlend` curve to the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.SetCurve 2, CurveForBlend

```

### Sub **SetOrientation**( long  `iBlendLimit`,  long  `iOrientation`)

   Sets the orientation of a curve of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose curve orientation is to be set.

**Legal values** : 1 for the first curve, and 2 for the second one
` iOrientation`      The orientation to set to the curve.

**Legal values** : 1 for direct and -1 for reverse  **Example** :      This example sets the orientation of the second limit of the `ShpBlend` hybrid shape blended feature to direct.

```VBScript
     ShpBlend.SetOrientation 2, 1

```

### Sub **SetRuledDevelopableSurfaceConnection**( long  `iBlendLimit`,  long  `iBlendConnection`)

### Sub **SetSmoothAngleThreshold**( double  `iAngle`)

   Sets the angular threshold.

**Parameters:**

` iAngle`      The angular threshold

### Sub **SetSmoothDeviation**( double  `iLength`)

   Sets the deviation value (length) from guide curves allowed during sweeping operation in order to smooth it.

**Parameters:**

` iLength`      The deviation value

### Sub **SetSupport**( long  `iBlendLimit`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Sets a support to the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose support is to be set.

**Legal values** : 1 for the first support, and 2 for the second one
` iSupport`      The support surface to be set. The curve of the blend limit must lay on the surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  **Example** :      This example sets the `SupportSurf` surface as the support of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.SetSupport 2, SupportSurf

```

### Sub **SetTensionInDouble**( long  `iBlendLimit`,  long  `iTensionType`,  double  `iFirstTension`,  double  `iSecondTension`)

   Sets the tension values to a limit of the blend. The values must be expressed as doubles and must be positive.

**Parameters:**

` iBlendLimit`      The limit of the blend to which the tension values are to be set.

**Legal values** : 1 for the first limit, and 2 for the second one
` iTensionType`      The tension type

**Legal values** :

1     Default tension 2     Constant tension 3     Linear tension
` iFirstTension`      The value for the first tension. It must be used with any tension type

**Legal values** : it must be a double and positive.
` iSecondTension`      The value for the second tension. It can be used with linear tension only

**Legal values** : it must be a double and positive.  **Example** :      This example sets the tension values of the tension, supposed to be a linear tension, of the first limit of the `ShpBlend` hybrid shape blended feature to respectively 1.5 and 0.5.

```VBScript
     ShpBlend.SetTensionInDouble 1, 3, 1.5, 0.5

```

### Sub **SetTensionType**( long  `iBlendLimit`,  long  `iTensionType`)

   Sets the tension type of a limit of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend for which the tension type is to be set.

**Legal values** : 1 for the first limit, and 2 for the second one
` iBlendLimit`      The value of tension type

**Legal values** :

1     Default tension 2     Constant tension 3     Linear tension 4     SType tension  **Example** :      This example sets the tension type as Default Tension for the first limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.SetTensionType 1, 1

```

### Sub **SetTransition**( long  `iBlendLimit`,  long  `iTransition`)

   Sets the transition orientation to a limit of the blend.

**Role** : Let `T` be the tangent to the wire, and `N` be the normal to the skin body. The transition orientation defines how the blend goes from the initial wires: it takes the direction of `iTransition*(T^N)`, where `^` is the cross product.

**Parameters:**

` iBlendLimit`      The limit of the blend whose transition orientation is to be set.

**Legal values** : 1 for the first support, and 2 for the second one
` iTransition`      The value of transition orientation.

**Legal values** : 1 for direct and -1 for reverse  **Example** :      This example sets the transition orientation of the second limit of the `ShpBlend` hybrid shape blended feature to reverse.

```VBScript
     ShpBlend.SetTransition 2, -1

```

### Sub **SetTrimSupport**( long  `iBlendLimit`,  long  `iTrimSupport`)

   Sets whether a support of the blend is to be trimmed off.
If the support is set to be trimmed, it will be trimmed using the curve then joined to the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose support is to be trimmed.

**Legal values** : 1 for the first limit, and 2 for the second one
` iTrimSupport`      The trim support mode

**Legal values** :

1     No trim 2     The support will be trimmed  **Example** :      This example sets that the second limit of the `ShpBlend` hybrid shape blended feature should be trimmed off.

```VBScript
     ShpBlend.SetTrimSupport 2, 2

```

### Sub **UnsetClosingPoint**( long  `iBlendLimit`)

   Unsets the closing point of a closed curve of the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose curve closing point is unset.

**Legal values** : 1 for the first curve, and 2 for the second one  **Example** :      This example unsets the closing point of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.UnsetClosingPoint 2

```

### Sub **UnsetSupport**( long  `iBlendLimit`)

   Unsets a support from the blend.

**Parameters:**

` iBlendLimit`      The limit of the blend whose support is to be unset.

**Legal values** : 1 for the first support, and 2 for the second one  **Example** :      This example unsets the support surface of the second limit of the `ShpBlend` hybrid shape blended feature.

```VBScript
     ShpBlend.UnsetSupport 2

```