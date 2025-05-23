# HybridShapeScaling (Object)

**_Represents the hybrid shape scaling feature object._**

**Role** : To access the data of the hybrid shape feature object. This data includes:

  * The element to be transformed using the scaling
  * The reference element for the scaling which is a point or a plane
  * The ratio and its value

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Center**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the reference element.This element can be a point or a plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) or [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `RefElem` the reference element for the `Scaling` hybrid shape feature.

```VBScript
     Dim RefElem As Reference
     Set RefElem = Scaling.Center

```

### Property **CreationMode**( ) As boolean

   Returns or sets the creation mode(creation or modification).

**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpScaling` hybrid shape scaling to creation

```VBScript
     hybShpScaling.CreationMode = True

```

### Property **ElemToScale**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to scale.

**Example** :      This example retrieves in `Elem` the element to scale for the `Scaling` hybrid shape feature.

```VBScript
     Dim Elem As Reference
     Set Elem = Scaling.ElemToScale

```

### Property **Ratio**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

   Returns the scaling ratio.  
### Property **RatioValue**( ) As double

   Returns or sets the scaling ratio value.

**Example** :      This example retrieves in `Value` the ratio value for the `Scaling` hybrid shape feature.

```VBScript
     Dim Value As double
     Set Value = Scaling.RatioValue

```

### Property **VolumeResult**( ) As boolean

   Returns or sets the volume result.

**Legal values** : **True** if the result of Scaling is required as volume (option is effective only in case of volumes,requires GSO License) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpScaling` hybrid shape scaling is volume.

```VBScript
     hybShpScaling.VolumeResult = True

```