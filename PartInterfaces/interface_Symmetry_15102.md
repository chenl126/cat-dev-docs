# Symmetry (Object)

**_Represents the shape symmetry feature object._**
This solid feature is created from an underlying HybridShapeSymmetry aggregated by the Symmetry. **Role** : To access the data of the symmetry shape feature object. The data includes:

  * The element to be transformed
  * The reference element which can be a point, a line or a plane

Use the CATIAShapeFactory to create ShapeFeature object.

**See also:**      [ShapeFactory](../PartInterfaces/interface_ShapeFactory_31272.md)

## Properties

### Property **HybridShape**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Gets the underlying HybridShapeSymmetry.

**Example:**     The following example explains how to retrieve the underlying HybridShape Symmetry

```VBScript
 Dim oHybridShape as AnyObject
 Set oHybridShape=oSymmetry.HybridShape
 oHybridShape.SectionCoupling = 2

```