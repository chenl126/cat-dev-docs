# HybridShapeExtrude (Object)

**_The Extrude feature : an Extrude is made up of a face to process and one Extrude parameter._**
**Role** : To access the data of the hybrid shape extrude feature object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

## Properties

### Property **BeginOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

**Role** : To get_BeginOffset on the object. For surface extrude, if limit type is upto, this offset value is not used. In case of Volume Extrude, if the up-to element is specified, this will act as offset value from the upto element.

**Parameters:**

` oExtrude`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Context**( ) As long

Returns or sets the context on Extrude feature.
**Legal values** :

  * **0** This option creates surface of extrusion.
  * **1** This option creates volume of extrusion.

Note: Setting volume result requires GSO License.

**Example** :      This example retrieves in `oContext` the context for the `Extrude1` hybrid shape feature.

```VBScript
Dim oContext
Set oContext = Extrude1.Context

```

### Property **Direction**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

**Role** : To get_Direction on the object.

**Parameters:**

` oDir`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **EndOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

**Role** : To get_EndOffset on the object. For surface extrude, if limit type is upto, this offset value is not used. In case of Volume Extrude, if the up-to element is specified, this will act as offset value from the upto element.

**Parameters:**

` oExtrude`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **ExtrudedObject**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : To get_ExtrudedObject on the object.

**Parameters:**

` oFaceToExtrude`      return value for CATScript applications, with (IDLRETVAL) function type
**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **FirstLimitType**( ) As long

Returns or sets the First limit type.
**Legal values** :

0
    Unknown Limit type.
1
    Limit type is Dimension. It implies that limit is defined by length
2
    Limit type is UptoElement. It implies that limit is defined by a geometrical element
**Example** :      This example retrieves in `oLim1Type` the first limit type for the `Extrude` hybrid shape feature.

```VBScript
Dim oLim1Type
Set oLim1Type = Extrude.FirstLimitType

```

### Property **FirstUptoElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the First up-to element used to limit extrusion.

**Example** :      This example retrieves in `Lim1Elem` the First up-to element for the `Extrude` hybrid shape feature.

```VBScript
Dim Lim1Elem As Reference
Set Lim1Elem = Extrude.FirstUptoElement

```

### Property **Orientation**( boolean  `iOrientation`)

Gets or sets orientation of the extrude. Orientation = TRUE : The natural orientation is taken. = FALSE : The opposite orientation is taken This example retrieves in `IsInverted` orientation of the extrude for the `Extrude` hybrid shape feature.

```VBScript
Dim IsInverted As boolean
IsInverted = Extrude.Orientation

```

### Property **SecondLimitType**( ) As long

Returns or sets the Second limit type.
**Legal values** :

0
    Unknown Limit type.
1
    Limit type is Dimension. It implies that limit is defined by length
2
    Limit type is UptoElement. It implies that limit is defined by a geometrical element
**Example** :      This example retrieves in `oLim2Type` the second limit type for the `Extrude` hybrid shape feature.

```VBScript
Dim oLim2Type
Set oLim2Type = Extrude.SecondLimitType

```

### Property **SecondUptoElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the Second up-to element used to limit extrusion.

**Example** :      This example retrieves in `Lim2Elem` the Second up-to element for the `Extrude` hybrid shape feature.

```VBScript
Dim Lim2Elem As Reference
Set Lim2Elem = Extrude.SecondUptoElement

```