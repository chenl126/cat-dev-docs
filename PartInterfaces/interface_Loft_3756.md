# Loft (Object)

**_Loft feature._**
Manipulation of solid Loft feature. Allows to access data of the Loft feature created by the CATIAShapeFactory. This solid feature is created from an underlying HybridShapeLoft aggregated by the Loft.

**See also:**      [ShapeFactory](../PartInterfaces/interface_ShapeFactory_31272.md)

## Properties

### Property **HybridShape**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Gets the underlying HybridShapeLoft.

**Example:**     The following example explains how to retrieve the underlying HybridShape Loft

```VBScript
 Dim oHybridShape as AnyObject
 Set oHybridShape=oLoft.HybridShape
 oHybridShape.SectionCoupling = 2

```