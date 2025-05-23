# HybridShapeCircleCtrRad (Object)

**_Represents the hybrid shape circle object defined using a center and a radius._**

**Role** : To access the data of the hybrid shape circle object.

This data includes:

  * The circle center
  * The circle radius
  * The surface that supports the circle

Use the CATIAHybridShapeFactory to create a HybridShapeCircleCtrRad object.

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

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle diameter.
It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to True.  **Example** :      This example retrieves in `HybShpCircleDiameter` the diameter of the `HybShpCircle` hybrid shape circle feature

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

### Property **FirstDirection**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the first direction used to set the angles reference.  **Example** :      This example retrieves in `myHybridShapeDirection` the first direction of the `HybShpCircle` hybrid shape circle feature

```VBScript
     Dim myHybridShapeDirection As CATIAHybridShapeDirection
     myHybridShapeDirection = HybShpCircle.FirstDirection

```

**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) 
### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the circle radius. It is expressed as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) literal. Succeeds only if DiameterMode is set to False.  **Example** :      This example retrieves in `HybShpCircleRadius` the radius of the `HybShpCircle` hybrid shape circle.

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

### Sub **GetSecondDirection**( double  `oDirX`,  double  `oDirY`,  double  `oDirZ`)

   Gets the second direction on the plane to compute the point (for stability).
This direction has to be kept perpendicular to the first direction

**Parameters:**

` oDirX,`      oDirY, oDirZ. second direction

**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) 
### Func **IsGeodesic**( ) As boolean

   Queries whether the circle is geodesic or not.

**Parameters:**

` oGeod`      geodesic type : when TRUE, the circle is geodesic.

### Sub **SetGeometryOnSupport**( )

   Sets GeometryOnSupport of circle.
It puts the circle on the surface.  
### Sub **SetSecondDirection**( double  `iDirX`,  double  `iDirY`,  double  `iDirZ`)

   Sets the second direction on the plane to compute the point (for stability).
This direction has to be kept perpendicular to the first direction

**Parameters:**

` iDirX,`      iDirY, iDirZ. second direction

**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) 
### Sub **UnsetGeometryOnSupport**( )

   Inactivates GeometryOnSupport of circle.
Note: The circle becomes euclidean.