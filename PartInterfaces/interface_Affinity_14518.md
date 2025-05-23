# Affinity (Object)

**_Represents the hybrid shape Affinity feature object._**
This solid feature is created from an underlying HybridShapeAffinity aggregated by the Affinity. **Role** : To access the data of the hybrid shape Affinity feature object. This data includes:

  * The element to Affinity
  * Origin for the Affinity
  * Plane for the Affinity
  * Direction for the Affinity
  * XRatio Value for the Affinity
  * YRatio Value for the Affinity
  * ZRatio Value for the Affinity
  * The translation distance and its value

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **HybridShape**(| ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

   Gets the underlying HybridShapeAffinity.

**Example:**     The following example explains how to retrieve the underlying HybridShape Affinity

```VBScript
      Dim oHybridShape as AnyObject
      Set oHybridShape=oAffinity.HybridShape
      oHybridShape.ElemToAffinity = reference1

```