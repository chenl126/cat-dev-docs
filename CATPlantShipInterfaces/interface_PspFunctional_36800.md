# PspFunctional (Object)

**_Represents Plant Ship functional object._**
**Role** : To access Plant Ship Functional object information.

## Properties

### Property **CatalogPartName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns catalog part name of physical object that realizes this function.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
 ...
Set strVar1 = objThisIntf.CatalogPartName

```

### Property **FunctionStatus**( ) As [CatPspIDLFunctionStatus](../CATPlantShipInterfaces/enum_CatPspIDLFunctionStatus_109872.md) (Read Only)

Returns function object status.

**Example:**

```VBScript
Dim objThisIntf As PspPhysical
Dim objArg1 As CatPspIDLFunctionStatus
 ...
objArg1 = objThisIntf.FunctionStatus

```

### Property **PartCatalogName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns Part catalog name of physical object that realizes this function.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
 ...
strVar1 = objThisIntf.PartCatalogName

```

### Property **PartNumber**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns part number of physical object that realizes this function.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
 ...
strVar1 = objThisIntf.PartNumber

```

### Property **PartType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the part type of physical object that realizes this function.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
 ...
strVar1 = objThisIntf.PartType

```

### Property **Physicals**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

Returns a list of all associated physical objects.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim objArg1 As PspListOfObjects
 ...
Set objArg1 = objThisIntf.Physicals

```

### Property **Standard**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Return Standard.

**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
 ...
strVar1 = objThisIntf.Standard

```

Methods

### Func **GetCompatiblePartTypes**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Retrieves a list of all physical part types that are compatible with this function.

**Parameters:**

` iuStandard`      Standard name
**Returns:**      List of Compatible Part Types.  **Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
Dim objArg2 As PspListOfBSTRs

 ...
Set objArg1 = objThisIntf.GetCompatiblePartTypes   (strVar1)

```

### Func **IsOKToIntegrate**( ) As boolean

Check it is OK to integrate (realize) this function with a physical part.

**Returns:**      TRUE if ok to be integrated  **Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim objArg1 As boolean
 ...
objArg1 = objThisIntf.IsOKToIntegrate

```

### Func **IsRealized**( ) As boolean

Checks if the Function object is realized or not.

**Returns:**      TRUE if the object is Realized  **Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim objArg1 As boolean
 ...
objArg1 = objThisIntf.IsRealized

```

### Func **IsSpecDriven**( ) As boolean

Checks if the functional object is specification driven or not.

**Returns:**      TRUE if this object is specification driven.  **Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim objArg1 As boolean
 ...
objArg1 = objThisIntf.IsSpecDriven

```

### Sub **ListCompatiblePartNumbers**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuStandard`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuCatalogName`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLPartTypes`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `oLCatalogPartNames`)

Retrieves a list of compatible Part numbers and part types.

**Parameters:**

` iuPartType`      part type
` iuStandard`      Standard name
` iuCatalogName`      catalog name
` oLPartTypes`      a list of part types
` oLCatalogPartNames`      List of catalog part names
**Example:**

```VBScript
Dim objThisIntf As PspFunctional
Dim strVar1 As CATBSTR
Dim strVar2 As CATBSTR
Dim strVar3 As CATBSTR
Dim objArg4 As PspListOfBSTRs
Dim objArg5 As PspListOfBSTRs

..
..
objThisIntf.ListCompatiblePartNumbers strVar1,strVar2,strVar3,objArg4,objArg5

```