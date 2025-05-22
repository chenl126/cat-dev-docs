# HybridShapeThickness (Object)

**_Represents the hybrid shape Thickness feature object._**
**Role** : To access the data of the thickness on an hybrid shape feature object. This data includes:

  * The thickness orientation
  * The thickness1 value
  * The thickness2 value

## Properties

### Property **Orientation**( ) As long

Returns or sets the orientation.
**Role** :
Orientation = 1 means that the first thickness is measured with the normal of the support Orientation = -1 means that the first thickness is measured with the inverted normal of the support

**Example** :      This example retrieves in `Orient` the orientation for the `Thickness1` hybrid shape feature.

```VBScript
Dim Orient As long
Set Orient = Thickness1.Orientation

```

### Property **Thickness1**( ) As double

Returns or sets the first thickness value in mm.

**Example** : This example retrieves in `ThickVal1` the first thickness value for the `Thick` hybrid shape feature.

```VBScript
Dim ThickVal1 As double
Set ThickVal1 = Thick.Thickness1

```

### Property **Thickness1Value**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the first thickness value.

**Example** :      This example retrieves in `ThickVal1` the first thickness value for the `Thick` hybrid shape feature.

```VBScript
Dim ThickVal1 As Length
Set ThickVal1 = Thick.Thickness1Value

```

### Property **Thickness2**( ) As double

Returns or sets the second thickness value in mm.

**Example** : This example retrieves in `ThickVal2` the second thickness value for the `Thick` hybrid shape feature.

```VBScript
Dim ThickVal2 As double
Set ThickVal2 = Thick.Thickness2

```

### Property **Thickness2Value**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the second thickness value.

**Example** :      This example retrieves in `ThickVal2` the second thickness value for the `Thick` hybrid shape feature.

```VBScript
Dim ThickVal2 As Length
Set ThickVal2 = Thick.Thickness2Value

```