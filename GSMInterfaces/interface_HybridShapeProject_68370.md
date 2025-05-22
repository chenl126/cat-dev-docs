# HybridShapeProject (Object)

**_Represents the hybrid shape project feature object._**
**Role** : To access data of the hybrid shape project feature. The data includes:

  * The element to project which is a point or a curve
  * The support element which is a curve or a surface
  * The projection type ( normal or along a direction)
  * The projection direction if needed
  * The option to have either the nearest solution or all solutions

Use the CATIAHybridShapeFactory to create HybridShapeFeatures objects.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the projection direction.

**Example** : This example retrieves in `Dir` the direction for the `Project` hybrid shape feature.

```VBScript
Dim Dir As Reference
Set Dir = Project.Direction

```

### Property **ElemToProject**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the element to project.This element can be a point or a curve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** : This example retrieves in `Elem` the element to project for the `Project` hybrid shape feature.

```VBScript
Dim Elem As Reference
Set Elem = Project.ElemToProject

```

### Property **MaximumDeviationValue**( ) As double

Sets or Gets the maximum deviation allowed for smoothing operation.
Sets in distance unit, it corresponds to the radius of a pipe around the input curve in which the result is allowed to be. This value must be set in SI unit (m).

**Example** : This example retrieves in `DeviationValue` the maximum deviation value for the `Project` hybrid shape feature.

```VBScript
Dim DeviationValue As CATIALength
Set DeviationValue = Project.MaximumDeviationValue

```

### Property **Normal**( ) As boolean

Returns or sets the direction option. **Role** : To define the type of projection. Normal is set to TRUE if the projection is a normal projection.Otherwise, the projection is defined along a specified direction.

**Example** : This example retrieves in `NormalOption` the support for the `Project` hybrid shape feature.

```VBScript
Dim NormalOption As boolean
Set NormalOption = Project.Normal

```

### Property **SmoothingType**( ) As long

Sets or Gets Smoothing Type.
**Role** : Smoothing type
: 0 -> No Smoothing
: 2 -> G1 Smoothing : Enhance current continuity to tangent continuity
: 3 -> G2 Smoothing : Enhance current continuity to curvature continuity

**Example** : This example retrieves in `SType` the smoothing type for the `Project` hybrid shape feature.

```VBScript
Dim SType As long
Set SType = Project.SmoothingType

```

### Property **SolutionType**( ) As long

Returns or sets the solution type. **Role** : All solutions or Nearest solution (only nearest projection is kept when more than one solution is possible).

**Example** : This example retrieves in `SolType` the solution type for the `Project` hybrid shape feature.

```VBScript
Dim SolType As long
Set SolType = Project.SolutionType

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support element.This element can be a plane or a surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** : This example retrieves in `SupportElem` the support for the `Project` hybrid shape feature.

```VBScript
Dim SupportElem As Reference
Set SupportElem = Project.Support

```

### Property **p3DSmoothing**( ) As boolean

Returns or sets the '3D Smoothing' option. **Role** : To activate or not the 3D smoothing option Available only for tangent or curvature smoothing type TRUE : Smoothing performed without specifying support FALSE : Smoothing performed with specific support

**Example** : This example retrieves in `3DSmoothingOption` the support for the `Project` hybrid shape feature.

```VBScript
Dim 3DSmoothingOption As boolean
Set 3DSmoothingOption = Project.p3DSmoothing

```