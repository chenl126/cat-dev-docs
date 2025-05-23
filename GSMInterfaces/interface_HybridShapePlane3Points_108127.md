# HybridShapePlane3Points (Object)

**_Represents the hybrid shape plane through three points feature object._**

**Role** : Allows to access data of the plane feature passing though three points. This data includes:

  * The first point
  * The second point
  * The third point

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **First**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** : This example retrieves in `FirstPoint` the first point for the `Plane` passing through three points hybrid shape feature.

```VBScript
     Dim FirstPoint As Reference
     Set FirstPoint = Plane3Points.First

```

### Property **Second**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** : This example retrieves in `SecondPoint` the second point for the `Plane` passing through three points hybrid shape feature.

```VBScript
     Dim SecondPoint As Reference
     Set SecondPoint = Plane3Points.Second

```

### Property **Third**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the third point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** : This example retrieves in `ThirdPoint` the third point for the `Plane` passing through three points hybrid shape feature.

```VBScript
     Dim ThridPoint As Reference
     Set ThirdPoint = Plane3Points.Third

```