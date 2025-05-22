# HybridShapeCylinder (Object)

**_Represents the hybrid shape Cylinder feature object._**
**Role** : To access the data of the hybrid shape Cylinder feature object. This data includes:

  * The center of the Cylinder
  * The Radius of the Cylinder
  * Length of Cylinder in the given extrusion direction
  * Length of Cylinder opposite to extrusion direction
  * Direction of extrusion for cylinder.

Use the CATIAHybridShapeFactory to create a HybridShapeCylinder object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Center**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the center of the cylinder object.

**Example** :      This example retrieves in `CylinderCenter` the center of the Cylinder, for the `Cylinder` hybrid shape feature.

```VBScript
Dim CylinderCenter As Reference
Set CylinderCenter = Cylinder.Center

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the direction of the cylinder object.

**Example** :      This example retrieves in `CylinderDirection` the direction of extrusion of the Cylinder, for the `Cylinder` hybrid shape feature.

```VBScript
Dim CylinderDirection As HybridShapeDirection
Set CylinderDirection = Cylinder.Direction

```

### Property **Length1**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns or sets the length of the cylinder object in the given extrusion direction.

**Example** :      This example retrieves in `CylinderLength1` the length of the Cylinder in the given extrusion direction, for the `Cylinder` hybrid shape feature.

```VBScript
Dim CylinderLength1 As Length
Set CylinderLength1 = Cylinder.Length1

```

### Property **Length2**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns or sets the length of the cylinder object in the opposite direction of given extrusion direction.

**Example** :      This example retrieves in `CylinderLength2` the length of the Cylinder in the opposite direction of the given extrusion direction, for the `Cylinder` hybrid shape feature.

```VBScript
Dim CylinderLength2 As Length
Set CylinderLength2 = Cylinder.Length2

```

### Property **Orientation**( boolean  `iOrientation`)

Returns or sets the the inversion of extrusion direction.

**Example** :      This example retrieves in `IsInverted` the inversion status of extrusion direction for the `Cylinder` hybrid shape feature.

```VBScript
Dim IsInverted As boolean
Set IsInverted = Cylinder.Orientation

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns or sets the radius of the cylinder object.

**Example** :      This example retrieves in `CylinderRadius` the radius of the Cylinder, for the `Cylinder` hybrid shape feature.

```VBScript
Dim CylinderRadius As Length
Set CylinderRadius = Cylinder.Radius

```

Methods

### Sub **InvertOrientation**( )

Inverts the Orientation of Cylinder object.

**Example** :      This example inverts the orientation for the `Cylinder` hybrid shape feature.

```VBScript
Cylinder.InvertOrientation

```