# HybridShapeCircleCtrPt (Object)

**_Represents the hybrid shape circle object defined using a center and a point on the circle._**

**Role** : To access the data of the hybrid shape circle object.

This data includes:

  * The circle center
  * The point on the circle
  * The surface that supports the circle

Use the CATIAHybridShapeFactory to create a HybridShapeCircleCtrPt object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Center**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle center.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `HybShpCircleCenter` the center of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleCenter As Reference
     HybShpCircleCenter = HybShpCircle.Center

```

### Property **CrossingPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves the passing point of the `HybShpCircle` hybrid shape circle in `HybShpCirclePassingPoint` point.

```VBScript
     Dim HybShpCirclePassingPoint As Reference
     Set HybShpCirclePassingPoint = HybShpCircle.CrossingPoint

```

### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `HybShpCircleSupportSurf` the support surface of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleSupportSurf As Reference
     HybShpCircleSupportSurf = HybShpCircle.Support

```

Methods

### Func **IsGeodesic**( ) As boolean

   Queries whether the circle is geodesic or not.

**Parameters:**

` oGeod`      geodesic type : when TRUE, the circle is geodesic.

### Sub **SetGeometryOnSupport**( )

   Sets GeometryOnSupport of circle.
It puts the circle on the surface.  
### Sub **UnsetGeometryOnSupport**( )

   Inactivates GeometryOnSupport of circle.
Note: The circle becomes euclidean.