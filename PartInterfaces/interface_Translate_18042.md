# Translate (Object)

**_Represents the hybrid shape translate feature object._**
This solid feature is created from an underlying HybridShapeTranslate aggregated by the Translate. **Role** : To access the data of the hybrid shape translate feature object. This data includes:

  * The element to translate
  * The translation direction
  * The translation distance and its value

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **HybridShape**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

Gets the underlying HybridShapeTranslate.

**Example:**     The following example explains how to retrieve the underlying HybridShape Translate

```VBScript
 Dim oHybridShape as AnyObject
 Set oHybridShape=oTranslate.HybridShape
 oHybridShape.ElemToTranslate = reference1

```