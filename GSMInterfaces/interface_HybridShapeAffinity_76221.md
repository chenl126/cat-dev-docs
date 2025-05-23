# HybridShapeAffinity (Object)

**_Represents the hybrid shape affinity feature object._**

**Role** : To access the data of the hybrid shape affinity feature object. This data includes:

  * The element to transform using the affinity
  * The affinity reference coordinate system origin
  * The affinity reference coordinate system reference plane
  * The affinity reference coordinate system first direction
  * The affinity ratio along the x, y and z directions of the reference coordinate system
  * The element to transform using the affinity

The reference coordinate system is always a direct one.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

Use the CATIAHybridShapeFactory to create a HybridShapeAffinity object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **AxisFirstDirection**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first direction of the reference coordinate system.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).

**Example** :      This example retrieves in `FirstDir` the first direction of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim FirstDir As Reference
     Set FirstDir = Affinity.AxisFirstDirection

```

### Property **AxisOrigin**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the origin of the reference coordinate system.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `Origin` the origin of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim Origin As Reference
     Set Origin = Affinity.AxisOrigin

```

### Property **AxisPlane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the reference plane of the reference coordinate system.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

**Example** :      This example retrieves in `RefPlane` the reference plane of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim RefPlane As Reference
     Set RefPlane = Affinity.AxisPlane

```

### Property **CreationMode**( ) As boolean

   Returns or sets the creation mode(creation or modification).

**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpAffinity` hybrid shape affinity to creation

```VBScript
     hybShpAffinity.CreationMode = True

```

### Property **ElemToTransform**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to transform using the affinity.

**Example** :      This example retrieves in `ElementToTransform` the element to transform for the `Affinity` hybrid shape feature.

```VBScript
     Dim ElementToTransform As Reference
     Set ElementToTransform = Affinity.ElemToTransform

```

### Property **VolumeResult**( ) As boolean

   Returns or sets the volume result.

**Legal values** : **True** if the result of affinity is required as volume (option is effective only in case of volumes,requires GSO License) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpAffinity` hybrid shape affinity is volume.

```VBScript
     hybShpAffinity.VolumeResult = True

```

### Property **XRatios**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the affinity ratio along the X Direction of the reference coordinate system.

**Example** :      This example retrieves in `X` the ratio of the affinity along the X Direction of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim X As RealParam
     Set X = Affinity.XRatios

```

### Property **YRatios**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the affinity ratio along the Y Direction of the reference coordinate system.

**Example** :      This example retrieves in `Y` the ratio of the affinity along the Y Direction of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim Y As RealParam
     Set Y = Affinity.YRatios

```

### Property **ZRatios**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the affinity ratio along the Z Direction of the reference coordinate system.

**Example** :      This example retrieves in `Z` the ratio of the affinity along the Z Direction of the reference coordinate system used by the `Affinity` hybrid shape feature.

```VBScript
     Dim Z As RealParam
     Set Z = Affinity.ZRatios

```