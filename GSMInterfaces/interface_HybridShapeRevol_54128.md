# HybridShapeRevol (Object)

**_The Revol feature : an Revol is made up of a face to process and one Revol parameter._**

**Role** : To access the data of the hybrid shape revol feature object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

## Properties

### Property **Axis**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : To get_Axis on the object.

**Parameters:**

` oDir`      return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **BeginAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   **Role** : To get_BeginAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Context**( ) As long

   Returns or sets the context on Revolve feature.

**Legal values** :

  * **0** This option creates surface of revolution.
  * **1** This option creates volume of revolution.

Note: Setting volume result requires GSO License.

**Example** :      This example retrieves in `oContext` the context for the `Revol` hybrid shape feature.

```VBScript
     Dim oContext
     Set oContext = Revol.Context

```

### Property **EndAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   **Role** : To get_EndAngle on the object.

**Parameters:**

` oAngle`      return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) 
### Property **Orientation**( boolean  `iOrientation`)

   Gets or sets orientation of the revolution. Orientation = TRUE : The natural orientation of the axis is taken. = FALSE : The opposite orientation is taken This example retrieves in `IsInverted` orientation of the revolution for the `Revol` hybrid shape feature.

```VBScript
     Dim IsInverted As boolean
     IsInverted = Revol.Orientation

```

### Property **Profil**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   **Role** : To get_Profil on the object.

**Parameters:**

` oProfil`      return value for CATScript applications, with (IDLRETVAL) function type

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **Returns:**      HRESULT S_OK if Ok E_FAIL else return error code for C++ Implementations  **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)