# HybridShapeReflectLine (Object)

**_Represents the hybrid shape reflect line feature object._**

**Role** : To access the data of the hybrid shape reflect line feature object. This data includes:

  * The surface used to create the reflect line
  * The direction (cylindrical)
  * The origin (conical)
  * The angle value

Use the CATIAHybridShapeFactory to create a HybridShapeReflectLine object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Angle**(| ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

   Returns or sets the angle used to create the reflectline.

**Example** :      This example retrieves in `Ang` the angle for the `RelectLine` hybrid shape feature.

```VBScript
     Dim Ang As CATIAAngle
     Set Ang = ReflectLine.Angle

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the direction used to create the cylindrical reflectline.

**Example** :      This example retrieves in `Dir` the direction for the cylindrical `RelectLine` hybrid shape feature.

```VBScript
     Dim Dir As CATIAHybridShapeDirection
     Set Dir = ReflectLine.Direction

```

### Property **OrientationDirection**( ) As long

   Returns or sets the direction orientation used to compute the reflect line.

**Role** : The orientation is used to define the angle between the direction and the normal to the support of the points on the result curve. The orientation is the same than or the inverse of the result of the cross product: Normal(support) ^ Tangent(FirstReferenceCurve).

**Legal values** : 1 for same orientation, and -1 for inverse  
### Property **OrientationSupport**( ) As long

   Returns or sets the support orientation used to compute the reflect line.

**Role** : The orientation is used to define the angle between the direction and the normal to the support of the points on the result curve. The orientation is the same than or the inverse of the result of the cross product: Normal(support) ^ Tangent(FirstReferenceCurve).

**Legal values** : 1 for same orientation, and -1 for inverse  
### Property **Origin**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the origin point used to create the conical reflectline.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `Point` the origin point for the conical `ReflectLine` hybrid shape feature.

```VBScript
     Dim Point As Reference
     Set Point = ReflectLine.Origin

```

### Property **SourceType**( ) As long

   Returns or sets whether the reflectline curve is or should be created with infinite light source (cylindrical) or with finite point light source (conical).

**Role** : The SourceType indicates whether the created reflectline curve is compute with infinite light source for cylindrical type or with finite point light source for conical type.

**Legal values** : 0 for cylindrical and 1 for conical.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support surface used to create the reflectline.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `Surface` the support surface for the `RelectLine` hybrid shape feature.

```VBScript
     Dim Surface As Reference
     Set Surface = ReflectLine.Support

```

### Property **TypeSolution**( ) As long

   Returns or sets whether the reflectline curve is or should be created with the normal to the support or the tangent plane to the support.

**Role** : The TypeSolution indicates whether the created reflectline curve is compute with the angle between the normale to the support and the direction or with the angle between the tangent plane to the support and the direction.

**Legal values** : 0 for the normal and 1 for the tangent plane.  Methods

### Sub **InvertOrientationDirection**( )

   Inverts the orientation of direction. This example inverts the direction orientation of `hybRefLine` hybrid shape reflect line object.

```VBScript
     hybRefLine.InvertOrientationDirection

```

### Sub **InvertOrientationSupport**( )

   Inverts the orientation of support. This example inverts the support orientation of `hybRefLine` hybrid shape reflect line object.

```VBScript
     hybRefLine.InvertOrientationSupport

```