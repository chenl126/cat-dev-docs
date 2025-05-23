# Scaling2 (Object)

**_Represents the Scaling2 feature object._**
This solid feature is created from an underlying HybridShapeScaling aggregated by the Scaling. **Role** : To access the data of the feature object. This data includes:

  * The element to be transformed using the Scaling2
  * The reference element for the Scaling2 which is a point or a plane
  * The ratio and its value

Use the CATIAShapeFactory to create Part object.

**See also:**      [ShapeFactory](../PartInterfaces/interface_ShapeFactory_31272.md)

## Properties

### Property **Center**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the reference element.This element can be a point or a plane.
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `RefElem` the reference element for the `Scaling2` hybrid shape feature.

```VBScript
     Dim RefElem As Reference
     Set RefElem = Scaling2.Center

```

### Property **Ratio**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the scaling ratio.  
### Property **RatioValue**( ) As double

   Returns or sets the scaling ratio value.

**Example** :      This example retrieves in `Value` the ratio value for the `Scaling` hybrid shape feature.

```VBScript
     Dim Value As double
     Set Value = Scaling2.RatioValue

```