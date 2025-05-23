# HybridShapePointBetween (Object)

**_Represents the hybrid shape PointBetween feature object._**

**Role** : To access the data of the hybrid shape PointBetween feature object.
This data includes:

  * The first reference point
  * The second reference point

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FirstPoint**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first reference point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `RefPoint1` the first reference point for the `PointBetween` hybrid shape feature.

```VBScript
     Dim RefPoint1 As Reference
     Set RefPoint1 = PointBetween.FirstPoint

```

### Property **Orientation**( ) As long

   Returns or sets the orientation. **Role** :
Orientation = 1 means that distance is measured from the second point

**Example** :      This example retrieves in `Orient` the orientation for the `PointBetween` hybrid shape feature.

```VBScript
     Dim Orient As long
     Set Orient = PointBetween.Orientation

```

### Property **Ratio**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Get the ratio. **Role** :
if d1 is the distance between the first point and the created point, and d2 is the distance between the first point and the second point, then ratio = d1/d2.

**Example** :      This example retrieves in `ratio` the orientation for the `PointBetween` hybrid shape feature.

```VBScript
     Dim ratio  As CATIARealParam
     Get ratio = PointBetween.Ratio

```

### Property **SecondPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second reference point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `RefPoint2` the second reference point for the `PointBetween` hybrid shape feature.

```VBScript
     Dim RefPoint2 As Reference
     Set RefPoint2 = PointBetween.SecondPoint

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the support.
Note: the support can be surface or curve. It is not mandatory.

Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md) and [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example** :      This example retrieves in `oSupport` the support(if it exist) for the `PointBetween` hybrid shape feature.

```VBScript
     Dim oSupport As Reference
     Set oSupport = PointBetween.Support

```