# HybridShapeIntersection (Object)

**_Represents the hybrid shape intersection feature object._**
**Role** : To access the data of the hybrid shape intersection object. This data includes:

  * The first element to intersect
  * The second element to intersect

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Element1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first element to intersect.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `FirstElem` the first element to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim FirstElem As Reference
Set FirstElem = Intersection.Element1

```

### Property **Element2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the second element to intersect.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md), [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `SecondElem` the second element to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim SecondElem As Reference
Set SecondElem = Intersection.Element2

```

### Property **ExtendMode**( ) As long

Returns or sets the ExtendMode flag for intersect.

**Example** :      This example retrieves in `ExtendMode` the ExtendMode to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim ExtendMode As Reference
Set ExtendMode = Intersection.ExtendMode
ExtendMode is 0 when both "Extend Linear Supposr for intersection" are unchecked
ExtendMode is 1 when "Extend Linear Supposr for intersection" for First Element is checked and for Second Element is unchecked
ExtendMode is 2 when "Extend Linear Supposr for intersection" for First Element is unchecked and for Second Element is checked
ExtendMode is 3 when both "Extend Linear Supposr for intersection" are checked

```

### Property **ExtrapolateMode**( ) As boolean

Returns or sets the ExtrapolateMode flag for intersect.

**Example** :      This example retrieves in `ExtrapolateMode` the ExtrapolateMode to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim ExtrapolateMode As Reference
Set ExtrapolateMode = Intersection.ExtrapolateMode

```

### Property **IntersectMode**( ) As boolean

Returns or sets the IntersectMode flag for intersect.

**Example** :      This example retrieves in `IntersectMode` the IntersectMode to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim IntersectMode As Reference
Set IntersectMode = Intersection.IntersectMode

```

### Property **PointType**( ) As long

Returns or sets the PointType flag for intersect.

**Example** :      This example retrieves in `PointType` the PointType to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim PointType As Reference
Set PointType = Intersection.PointType

```

### Property **SolidMode**( ) As boolean

Returns or sets the SolidMode flag for intersect.

**Example** :      This example retrieves in `SolidMode` the SolidMode to intersect for the `Intersection` hybrid shape feature.

```VBScript
Dim SolidMode As Reference
Set SolidMode = Intersection.SolidMode

```