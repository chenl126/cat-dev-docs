# HybridShapeRotate (Object)

**_Represents the hybrid shape rotate feature object._**

**Role** : To access the data of the hybrid shape rotate feature object. This data includes:

  * The element to be rotated
  * The rotation axis
  * The angle and its value

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect
Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Angle**(| ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the rotation angle.  
### Property **AngleValue**( ) As double

   Returns or sets the rotation angle value.

**Example** : This example retrieves in `AngleValue` the angle value for the `Rotate` hybrid shape feature.

```VBScript
     Dim AngleValue As double
     Set AngleValue = Rotate.AngleValue

```

### Property **Axis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the rotation axis.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Edge](../MecModInterfaces/interface_Edge_3456.md).

**Example** : This example retrieves in `RotationAxis` the rotation axis for the `Rotate` hybrid shape feature.

```VBScript
     Dim RotationAxis As Reference
     Set RotationAxis = Rotate.Axis

```

### Property **ElemToRotate**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retuns or sets the element to be rotated.

**Example** : This example retrieves in `Elem` the element to be rotated for the `Rotate` hybrid shape feature.

```VBScript
     Dim Elem As Reference
     Set Elem = Rotate.ElemToRotate

```

### Property **FirstElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first element defining the rotation angle.  
### Property **FirstPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first point defining the rotation.  
### Property **OrientationOfFirstElement**( ) As boolean

   Returns or sets the orientation of the first element defining the rotation angle.
This applies in case of line or plane element.  
### Property **OrientationOfSecondElement**( ) As boolean

   Returns or sets the orientation of the second element defining the rotation angle.
This applies in case of line or plane element.  
### Property **RotationType**( ) As long

   Returns or sets the type of the rotation definition.

  * 0= Axis + angle
  * 1= Axis + two elements
  * 2= Three Points
  * 3= Unknown type

### Property **SecondElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second element defining the rotation angle.  
### Property **SecondPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second point defining the rotation.  
### Property **ThirdPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the third point defining the rotation.  
### Property **VolumeResult**( ) As boolean

   Returns or sets the volume result.

**Legal values** : **True** if the result of Rotate is required as volume (option is effective only in case of volumes,requires GSO License) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpRotate` hybrid shape rotate is volume.

```VBScript
     hybShpRotate.VolumeResult = True

```

Methods

### Func **GetCreationMode**( ) As long

   Gets the creation mode.

**Legal values** :

0
    CATGSMTransfoModeUnset. Default behavior: creation mode by default for all features, modification mode for axis system
1
    CATGSMTransfoModeCreation. Creation mode.
2
    CATGSMTransfoModeModification. Modification mode.

**Example** :      This example retrieves in `oCreation` the creation mode for the `hybShpRotate` hybrid shape feature.

```VBScript
     oCreation = hybShpRotate.GetCreationMode

```

### Sub **SetCreationMode**( boolean  `iCreation`)

   Sets the creation mode(creation or modification).

**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpRotate` hybrid shape rotate to creation

```VBScript
     hybShpRotate.SetCreationMode True

```