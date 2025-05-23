# HybridShapeWrapCurve (Object)

**_Represents the hybrid shape wrap curve surface object._**

**Role** : To access the data of the hybrid shape wrap curve surface object.

This data includes:

  * Two support surfaces, one at each limit of the wrap curve surface
  * Two curves, one for each support surface
  * The curve closing points

Use the CATIAHybridShapeFactory to create a HybridShapeWrapCurve object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FirstCurvesConstraint**(| ) As long

   Returns or sets constraint at first curves of the WrapCurve.

**Legal values** : 1 = no constraint, 2 = Deformed surface will have the same tangency and the same curvature as the original surface at first curves.

**Example** :      This example retrieves in `FirstCurvesConstraint` the constraint at first curves of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     Dim FirstCurvesConstraint As long
     Set FirstCurvesConstraint = ShpWrapCurve.FirstCurvesConstraint

```

### Property **LastCurvesConstraint**( ) As long

   Returns or sets constraint at last curves of the WrapCurve.

**Legal values** : 1 = no constraint, 2 = Deformed surface will have the same tangency and the the same curvatureas the original surface at last curves.

**Example** :      This example retrieves in `LastCurvesConstraint` the constraint at last curves of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     Dim LastCurvesConstraint As long
     Set LastCurvesConstraint = ShpWrapCurve.LastCurvesConstraint

```

### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the surface to deform of the WrapCurve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `SurfaceToDeform` the surface to deform of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     SurfaceToDeform = ShpWrapCurve.Surface

```

Methods

### Sub **GetCurves**( long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oReferenceCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oTargetCurve`)

   Returns a curve from the WrapCurve.

**Parameters:**

` iPosition`      The position of the curves in the list of curves.
` oReferenceCurve`      the reference curve.
` oTargetCurve`      the target curve.

**Legal values** : can be egal to Nothing. In this case, the associated ref curve will be fixed.

**Example** :      This example retrieves in `WrapCurveRefCurve` the first reference curve of the `ShpWrapCurve` hybrid shape WrapCurve feature and retrieves in `WrapCurveTargCurve` the first target curve of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     Dim WrapCurveRefCurve As Reference
     Dim WrapCurveTargCurve As Reference
     ShpWrapCurve.GetCurve(2)

```

### Func **GetNumberOfCurves**( ) As long

   Returns the number of couples of curves of the WrapCurve.

**Returns:**      The number of couples of curves

**Legal values** : positive or null.  **Example** :      This example retrieves in `NumberOfCurves` the number of couples of curves of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     NumberOfCurves = ShpWrapCurve.GetNumberOfCurves(2)

```

### Sub **GetReferenceDirection**( long  `oDirectionType`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `oDirection`)

   Gets the reference direction projection of the wrap curve feature.

**Parameters:**

` oDirectionType`      type of direction.

**Legal values** : 1 = reference direction is computed, and 2 = user direction.
` oDirection`      curve to be added as a direction, if oDirectionType = 2. **Example** :      This example retrieves in `RefDirection` the reference direction of the `ShpWrapCurve` hybrid shape WrapCurve feature and in `RefDirectionType` the reference direction of the `ShpWrapCurve` hybrid shape WrapCurve

```VBScript
     Dim RefDirectionType As long
     Dim RefDirection As CATIAHybridShapeDirection
     ShpWrapCurve.SetReferenceDirection (RefDirectionType, RefDirection)

```

### Sub **GetReferenceSpine**( long  `oSpineType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oSpine`)

   Returns the reference spine of the wrap curve feature.

**Parameters:**

` oSpineType`      type of spine.

**Legal values** : 1 = Reference Spine is equal to the first reference curve, and 2 = user spine.
` oSpine`      curve to be added as a spine, if iSpineType = 2.  **Example** :      This example retrieves in `RefSpine` the reference spine of the `ShpWrapCurve` hybrid shape WrapCurve feature and in `RefSpineType` the reference spine type.

```VBScript
     Dim RefSpineType As long
     Dim RefSpine As Reference
     ShpWrapCurve.GetReferenceSpine (RefSpineType, RefSpine)

```

### Sub **InsertCurves**( long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferenceCurve`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTargetCurve`)

   Inserts a couple of reference curve and target curve to the wrap curve.

**Parameters:**

` iPosition`      The position of the curves in the list of curves.

**Legal values** : 0 for the end of the list, or positive and not null.
` iReferenceCurve`      the reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iTargetCurve`      the target curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  **Example** :      This example sets the `RefCurveForWrapCurve` curve and the `TargCurveForWrapCurve` curve at the end of the list to the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     ShpWrapCurve.InsertCurves (0, RefCurveForWrapCurve, TargCurveForWrapCurve)

```

### Sub **InsertReferenceCurve**( long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReferenceCurve`)

   Inserts a of reference curve to the wrap curve.

**Parameters:**

` iPosition`      The position of the curves in the list of curves.

**Legal values** : 0 for the end of the list, or positive and not null.
` iReferenceCurve`      the reference curve.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). **Example** :      This example sets the `RefCurveForWrapCurve` curve at the end of the list to the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     ShpWrapCurve.InsertCurves (0, RefCurveForWrapCurve)

```

### Sub **RemoveCurves**( long  `iPosition`)

   Removes a couple of reference curve and target curve from the WrapCurve.

**Parameters:**

` iPosition`      The position of the curves in the list of curves.

**Legal values** : positive, not null and lower to numberOfCurves  **Example** :      This example removes the first couple of reference curve and target curve of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     ShpWrapCurve.RemoveCurves (1)

```

### Sub **SetReferenceDirection**( [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iDirection`)

   Sets the reference direction projection to the wrap curve feature.

**Parameters:**

` iDirection`      curve to be added as a direction, if iDirectionType = 2. **Example** :      This example sets the `RefDirection` curve as the reference direction of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     ShpWrapCurve.SetReferenceDirection RefDirection

```

### Sub **SetReferenceSpine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSpine`)

   Sets the reference spine to the wrap curve feature.

**Parameters:**

` iSpine`      curve to be added as a spine.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  **Example** :      This example sets the `Curve10` curve as the reference Spine of the `ShpWrapCurve` hybrid shape WrapCurve feature.

```VBScript
     ShpWrapCurve.SetReferenceSpine Curve10

```