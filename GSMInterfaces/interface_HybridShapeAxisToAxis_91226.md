# HybridShapeAxisToAxis (Object)

**_Represents the hybrid shape axis to axis tranformation feature object._**
**Role** : To access the data of the axis to axis tranformation shape feature object. The data includes:

  * The element to be transformed
  * The reference axis system
  * The target axis system

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect
Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **CreationMode**( ) As boolean

Returns or sets the creation mode(creation or modification).
**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpAxisToAxis` hybrid shape axis to axis to creation

```VBScript
hybShpAxisToAxis.CreationMode = True

```

### Property **ElemToTransform**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the element to transform.

**Example** :      This example retrieves in `Elem` the element to transform for the `AxisToAxis` hybrid shape feature.

```VBScript
Dim Elem As Reference
Set Elem = AxisToAxis.ElemToTransform

```

### Property **ReferenceAxis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference axis.

**Example** :      This example retrieves in `Ref` the reference axis for the `AxisToAxis` hybrid shape feature.

```VBScript
Dim Ref As Reference
Set Ref = AxisToAxis.ReferenceAxis

```

### Property **TargetAxis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the target axis.

**Example** :      This example retrieves in `Ref` the target axis for the `AxisToAxis` hybrid shape feature.

```VBScript
Dim Ref As Reference
Set Ref = AxisToAxis.ReferenceAxis

```

### Property **VolumeResult**( ) As boolean

Returns or sets the volume result.
**Legal values** : **True** if the result of axis to axis transformation is required as volume (option is effective only in case of volumes,requires GSO License)) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpAxisToAxis` hybrid shape AxisToAxis is volume.

```VBScript
hybShpAxisToAxis.VolumeResult = True

```