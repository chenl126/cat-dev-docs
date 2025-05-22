# HybridShapeCircle3Points (Object)

**_Represents the hybrid shape circle object defined using three points._**
**Role** : To access the data of the hybrid shape circle object.

This data includes the circle three passing points.

Use the CATIAHybridShapeFactory to create a HybridShapeCircle2PointsRad object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Element1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the circle first passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves the first passing point of the `HybShpCircle3Pt` hybrid shape circle in `HybShpCircle3PtFirstPassingPoint` point.

```VBScript
Dim HybShpCircle3PtFirstPassingPoint As Reference
Set HybShpCircle3PtFirstPassingPoint= HybShpCircle3Pt.Element1

```

### Property **Element2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the circle second passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example sets the second passing point of the `HybShpCircle3Pt` hybrid shape circle as the `Point2` point.

```VBScript
HybShpCircle3Pt.Element2 Point2

```

### Property **Element3**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the circle third passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves the third passing point of the `HybShpCircle3Pt` hybrid shape circle in `HybShpCircle3PtThirdPassingPoint` point.

```VBScript
Dim HybShpCircle3PtThirdPassingPoint As Reference
Set HybShpCircle3PtThirdPassingPoint= HybShpCircle3Pt.Element3

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

### Sub **RemoveSupport**( )

Removes the support surface.