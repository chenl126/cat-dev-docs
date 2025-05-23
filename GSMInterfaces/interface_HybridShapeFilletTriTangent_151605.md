# HybridShapeFilletTriTangent (Object)

**_Fillet Tri-Tangent feature._**

**Role** : Manipulation of Fillet Tri-Tangent feature Allows to access data of the Fillet Tri-Tangent feature created by using three support surfaces, their orientation, and options (supports trimming and fillet extremities type)

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **FirstElem**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the first support surface feature.

**Example** :      This example retrieves in `FirstElem` the first support element used by the `HybShpFilletTriTangent` hybrid shape feature.

```VBScript
     Dim FirstElem As Reference
     Set FirstElem = HybShpFilletTriTangent.FirstElem

```

### Property **FirstOrientation**( ) As long

   Returns or sets the first orientation used to specify fillet center position.
Note; Orientation is same or inverse than the normal to the first surface support  
### Property **RemoveElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the support surface to remove feature.  
### Property **RemoveOrientation**( ) As long

   Returns or sets the third orientation used to specify fillet center position.
note: Orientation is same or inverse than the normal to the surface support to remove

### Property **RibbonRelimitationMode**( ) As long

   Returns or sets fillet ribbon relimitation mode (or fillet extremities mode).
note: Smooth(0) or Straight(1) or Maximum(2) or Minimum(3)  
### Property **SecondElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the Second support surface feature.

**Example** :      This example retrieves in `SecondElem` the Second support element used by the `HybShpFilletTriTangent` hybrid shape feature.

```VBScript
     Dim SecondElem As Reference
     Set SecondElem = HybShpFilletTriTangent.SecondElem

```

**Parameters:**

` oElem`      Second support surface feature.

### Property **SecondOrientation**( ) As long

   Returns or sets the Second orientation used to specify fillet center position.
note: Orientation is same or inverse than the normal to the Second surface support  
### Property **SupportsTrimMode**( ) As long

   Returns or sets whether support surfaces are trimmed or not.
Trim (1) or NoTrim(0)
note: if "Trim" the 2 supports are trimmed and assembled with the fillet ribbon.  Methods

### Sub **InvertFirstOrientation**( )

   Inverts first orientation used to specify fillet center position.  
### Sub **InvertRemoveOrientation**( )

   Inverts third orientation used to specify fillet center position.  
### Sub **InvertSecondOrientation**( )

   Inverts second orientation used to specify fillet center position.