# HybridShapeCircle2PointsRad (Object)

**_Represents the hybrid shape circle object defined using two points and a radius._**

**Role** : To access the data of the hybrid shape circle object.

This data includes:

  * The circle two passing points
  * The circle radius
  * The surface that supports the circle
  * The circle orientation

Use the CATIAHybridShapeFactory to create a HybridShapeCircle2PointsRad object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Diameter**(| ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle diameter. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to True.  **Example** :      This example retrieves in `HybShpCircleDiameter` the diameter of the `HybShpCircle` hybrid shape circle feature

```VBScript
     Dim HybShpCircleDiameter As Length
     HybShpCircleDiameter = HybShpCircle.Diameter

```

### Property **DiameterMode**( ) As boolean

   Returns or sets the DiameterMode.

**Legal values** : **True** implies diameter **False** implies radius (default). When DiameterMode is changed, Radius/Diameter value, which is stored will not be modified.

**Example:**      This example sets that the DiameterMode of the `HybShpCircle` hybrid shape circle feature

```VBScript
      HybShpCircle.DiameterMode = True

```

### Property **Orientation**( ) As long

   Returns or sets the circle orientation.

**Role** : The circle orientation indicates which side of the line made up using the two passing points is used to create the major part of the circle. It is determined using the cross product of the normal to the suppport and the vector made up using the two passing points (Pt1-Pt2).

**Legal values** : 1 to state that the major part of the circle is or should be created on the side of the line shown by the vector resulting from this cross product, and -1 otherwise.

**Example** :      This example retrieves in `HybShpCircleOrientation` the orientation of the `HybShpCircle` hybrid shape circle.

```VBScript
     HybShpCircleOrientation = HybShpCircle.Orientation

```

### Property **Pt1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle first passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves the first passing point of the `HybShpCircle` hybrid shape circle in `HybShpCircleFirstPassingPoint` point.

```VBScript
     Dim HybShpCircleFirstPassingPoint As Reference
     Set HybShpCircleFirstPassingPoint = HybShpCircle.Pt1

```

### Property **Pt2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the circle second passing point.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example sets the second passing point of the `HybShpCircle` hybrid shape circle as the `Point12` point.

```VBScript
     HybShpCircle.Pt2 Point12

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle radius.

**Parameters:**

` Radius`      The circle radius, expressed as a
[Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to False.  **Example** :      This example retrieves in `HybShpCircleRadius` the radius of the `HybShpCircle` hybrid shape circle.

```VBScript
     Dim HybShpCircleRadius As Length
     HybShpCircleRadius = HybShpCircle.Radius

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
It puts the circle on the surface. S_OK if OK, E_FAIL if fail  
### Sub **UnsetGeometryOnSupport**( )

   Inactivates GeometryOnSupport of circle.
Note: The circle becomes euclidean.