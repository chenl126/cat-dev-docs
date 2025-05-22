# AxisToAxis (Object)

**_Represents the hybrid shape AxisToAxis feature object._**
This solid feature is created from an underlying HybridShapeAxisToAxis aggregated by the AxisToAxis. **Role** : To access the data of the hybrid shape AxisToAxis feature object. This data includes:

  * The element to AxisToAxis
  * Origin for the AxisToAxis
  * Plane for the AxisToAxis
  * Direction for the AxisToAxis
  * XRatio Value for the AxisToAxis
  * YRatio Value for the AxisToAxis
  * ZRatio Value for the AxisToAxis
  * The translation distance and its value

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **HybridShape**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Gets the underlying HybridShapeAxisToAxis.

**Example:**     The following example explains how to retrieve the underlying HybridShape AxisToAxis

```VBScript
 Dim oHybridShape as AnyObject
 Set oHybridShape=oAxisToAxis.HybridShape
 oHybridShape.ElemToAxisToAxis = reference1

```