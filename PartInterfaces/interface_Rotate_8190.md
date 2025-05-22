# Rotate (Object)

**_Represents the shape rotate feature object._**
This solid feature is created from an underlying HybridShapeRotate aggregated by the Rotate. **Role** : To access the data of the hybrid shape rotate feature object. This data includes:

  * The element to be rotated
  * The rotation axis
  * The angle and its value

Use the CATIAShapeFactory to create ShapeFeature object.

**See also:**      [ShapeFactory](../PartInterfaces/interface_ShapeFactory_31272.md)

## Properties

### Property **Angle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the rotation angle.  
### Property **AngleValue**( ) As double

Returns or sets the rotation angle value.

**Example** : This example retrieves in `AngleValue` the angle value for the `Rotate` hybrid shape feature.

```VBScript
Dim AngleValue As double
Set AngleValue = Rotate.AngleValue

```

### Property **Axis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the rotation axis.
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).

**Example** : This example retrieves in `RotationAxis` the rotation axis for the `Rotate` hybrid shape feature.

```VBScript
Dim RotationAxis As Reference
Set RotationAxis = Rotate.Axis

```

### Property **HybridShape**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Gets the underlying HybridShapeRotate.

**Example:**     The following example explains how to retrieve the underlying HybridShape Rotate

```VBScript
 Dim oHybridShape as AnyObject
 Set oHybridShape=oRotate.HybridShape
 oHybridShape.SectionCoupling = 2

```