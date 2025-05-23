# HybridShapeTranslate (Object)

**_Represents the hybrid shape translate feature object._**

**Role** : To access the data of the hybrid shape translate feature object. This data includes:

  * The element to translate
  * The translation direction
  * The translation distance and its value

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

Use the CATIAHybridShapeFactory to create HybridShapeFeature object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **CoordXValue**(| ) As double

   Returns or sets the translate X coordinate value.  
### Property **CoordYValue**( ) As double

   Returns or sets the translate Y coordinate value.  
### Property **CoordZValue**( ) As double

   Returns or sets the translate Z coordinate value.  
### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

   Returns or sets the translate direction.

**Example**      This example retrieves in `Dir` the translation direction for the `Translate` hybrid shape feature.

```VBScript
     Dim Dir As CATIAHybridShapeDirection
     Set Dir=Translate.Direction

```

### Property **Distance**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the translate distance.  
### Property **DistanceValue**( ) As double

   Returns or sets the translate distance value.

**Example**      This example retrieves in `DistVal` the translation distance value for the `Translate` hybrid shape feature.

```VBScript
     Dim DistVal As double
     Set DistVal =Translate.DistanceValue

```

### Property **ElemToTranslate**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the element to translate.

**Example**      This example retrieves in `Element` the element to be translated for the `Translate` hybrid shape feature.

```VBScript
     Dim Element As Reference
     Set Element=Translate.ElemToTranslate

```

### Property **FirstPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first point defining the translation.  
### Property **RefAxisSystem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the reference Axis System for Translate feature.
This data is not mandatory, if element is null, the absolute axis system is taken.
When an element is given, X, Y and Z are considered in this Axis system. Example
:      This example retrieves in `oRefAxis` the reference Axis System for `Translate` feature.

```VBScript
     Dim oRefAxis As CATIAReference
     Set oRefAxis  = Translate.RefAxisSystem

```

### Property **SecondPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the second point defining the translation.  
### Property **VectorType**( ) As long

   Returns or sets the way the translation vector is defined.

  * 0= Direction + distance
  * 1= point + points
  * 2= coordinates
  * 3= Unknown type

### Property **VolumeResult**( ) As boolean

   Returns or sets the volume result.

**Legal values** : **True** if the result of translation is required as volume (option is effective only in case of volumes,requires GSO License) and **False** if it is needed as surface .

**Example:**      This example sets that the result of the `hybShpTranslate` hybrid shape translate is volume.

```VBScript
     hybShpTranslate.VolumeResult = True

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

**Example** :      This example retrieves in `oCreation` the creation mode for the `hybShpTranslate` hybrid shape feature.

```VBScript
     oCreation = hybShpTranslate.GetCreationMode

```

### Sub **SetCreationMode**( boolean  `iCreation`)

   Sets the creation mode(creation or modification).

**Legal values** : **True** if the result is a creation feature and **False** if the result is a modification feature.

**Example:**      This example sets that the mode of the `hybShpTranslate` hybrid shape translate to creation

```VBScript
     hybShpTranslate.SetCreationMode True

```