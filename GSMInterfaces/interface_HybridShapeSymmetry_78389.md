# HybridShapeSymmetry (Object)

**_Represents the hybrid shape symmetry feature object._**
**Role** : To access the data of the symmetry shape feature object. The data includes:

  * The element to be transformed
  * The reference element which can be a point, a line or a plane

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **CreationMode**( ) As boolean

Returns or sets the creation mode(creation or modification).
**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpSymmetry` hybrid shape symmetry to creation

```VBScript
hybShpSymmetry.CreationMode = True

```

### Property **ElemToSymmetry**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the element to transform.

**Example** :      This example retrieves in `Elem` the element to transform for the `Symmetry` hybrid shape feature.

```VBScript
Dim Elem As Reference
Set Elem = Symmetry.ElemToSymmetry

```

### Property **Reference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference element.This element can be a point, a line or a plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [Edge](../MecModInterfaces/interface_Edge_3456.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `Ref` the reference element for the `Symmetry` hybrid shape feature.

```VBScript
Dim Ref As Reference
Set Ref = Symmetry.Reference

```

### Property **VolumeResult**( ) As boolean

Returns or sets the volume result.
**Legal values** : **True** if the result of symmetry is required as volume (option is effective only in case of volumes, requires GSO License) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpSymmetry` hybrid shape symmetry is volume.

```VBScript
hybShpSymmetry.VolumeResult = True

```