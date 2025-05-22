# HybridShapeFilletBiTangent (Object)

**_Fillet Bi-Tangent feature._**
**Role** : Manipulation of Fillet Bi-Tangent feature Allows to access data of the Fillet Bi-Tangent feature created by using two support surfaces, their orientation, a radius, and options (supports trimming and fillet extremities type)

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **ConicalSectionParameter**( ) As double

Returns or Sets parameter for conical section.  
### Property **FirstElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the first support surface feature.  
### Property **FirstLawRelimiter**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets or sets Law first relimiter for variable shape fillet with law management.
Relimiters must be point on spine.
The input law will be mapped between first and second relimiters. This example retrieves in `HybLaw` the first law relimiter for the `Fillet` hybrid shape feature.

```VBScript
Dim HybLaw As Reference
HybLaw = Fillet.FirstLawRelimiter

```

### Property **FirstOrientation**( ) As long

Returns or Setsthe first orientation used to specify fillet center position.
Orientation is same or inverse than the normal to the first surface support  
### Property **HoldCurve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the Hold Curve feature.  
### Property **IntegratedLaw**( ) As [CATIAHybridShapeIntegratedLaw](../GSMInterfaces/interface_HybridShapeIntegratedLaw_119452.md)

Gets or sets Integrated Law to manage Variable Shape Fillet with law.

**Parameters:**

` oILaw`      Integrated law This example retrieves in `HybridIntegratedLaw` the IntegratedLaw for the `Fillet` hybrid shape feature.

```VBScript
Dim HybridIntegratedLaw
Set HybridIntegratedLaw = Fillet.IntegratedLaw

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns fillet radius in a CATIALength.  
### Property **RadiusType**( ) As long

Returns or Sets fillet radius type.
Fillet radius type :
\- CATGSMRadiusDefault (0)
\- CATGSMRadiusChordLength(1)  
### Property **RadiusValue**( ) As double

Returns or Sets fillet radius value.  
### Property **RibbonRelimitationMode**( ) As long

Returns or Sets fillet ribbon relimitation mode (or fillet extremities mode).
Fillet extremities mode :
\- CATGSMSmooth (0)
\- CATGSMStraight(1)
\- CATGSMMaximum (2)
\- CATGSMMinimum (3)  
### Property **SecondElem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the Second support surface feature.  
### Property **SecondLawRelimiter**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets or sets Law second relimiter for variable shape fillet with law management.
Relimiters must be point on spine.
The input law will be mapped between first and second relimiters. This example retrieves in `HybLaw` the second law relimiter for the `Fillet` hybrid shape feature.

```VBScript
Dim HybLaw As Reference
HybLaw = Fillet.SecondLawRelimiter

```

### Property **SecondOrientation**( ) As long

Returns or Sets the Second orientation used to specify fillet center position.
Orientation is same or inverse than the normal to the Second surface support

### Property **SectionType**( ) As long

Returns or Sets fillet section type.
Fillet radius type :
\- CATGSMCircularSection(0)
\- CATGSMConicalSection (1)  
### Property **Spine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the spine feature.  
### Property **SupportsTrimMode**( ) As long

Returns or Sets whether support surfaces are trimmed or not. Possible values of SupportsTrimMode = 0 : No trim of fillet supports. = 1 : Trim of both fillet supports. = 2 : Trim of fillet support 1. = 3 : Trim of fillet support 2.  Methods

### Sub **AppendNewFaceToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

Append a new face to keep.

**Parameters:**

` iFace`

### Func **GetFaceToKeep**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets the face to keep for fillet operation.

**Parameters:**

` oFace`      The face to keep for fillet operation.
` iPos`      Position of the face to be retrieved.

### Sub **InvertFirstOrientation**( )

Inverts first orientation used to specify fillet center position.  
### Sub **InvertSecondOrientation**( )

Inverts second orientation used to specify fillet center position.  
### Sub **RemoveAllFacesToKeep**( )

Remove all the faces to keep.  
### Sub **RemoveFaceToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

Remove a face to keep.

**Parameters:**

` iFace`