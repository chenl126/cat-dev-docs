# HybridShapePointCenter (Object)

**_Represents the hybrid shape PointCenter feature object._**

**Role** : To access the data of the hybrid shape PointCenter feature object. It has been created by the CATIAHybridShapeFactory. This data includes:

  * The circle, ellipsa element

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Element**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle, ellipse or sphere.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Edge](../MecModInterfaces/interface_Edge_3456.md).

Example
:      This example retrieves in `Ref_Circle` the center point for the `PointCenter` hybrid shape feature.

```VBScript
     Dim Ref_Circle As Reference
     Set Ref_Circle = PointCenter.Element

```