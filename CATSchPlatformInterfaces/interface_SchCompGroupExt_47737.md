# SchCompGroupExt (Object)

**_Manage the graphical representation of a temporary group of schematic objects._**

## Methods

### Sub **GetPlacementAxis**(| [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md) | `oDb6PlaceMatrix`)

   Get the placement axis for the component group.

**Parameters:**

` oDb6PlaceMatrix`      Placement matrix of the component group (an array of 6 doubles) See
[SchGRRComp.GetTransformation2D](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.htm#GetTransformation2D) for explanation of this argument.  **Example:**

```VBScript
     Dim objThisIntf As SchCompGroupExt
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetPlacementAxisobjArg1

```

### Sub **SetPlacementAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDb6PlaceMatrix`)

   Set the placement axis for the component group.

**Parameters:**

` iDb6PlaceMatrix`      Placement matrix of the component group (an array of 6 doubles) See
[SchGRRComp.GetTransformation2D](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.htm#GetTransformation2D) for explanation of this argument.  **Example:**

```VBScript
     Dim objThisIntf As SchCompGroupExt
     Dim dbVar1(x) As CATSafeArrayVariant
      ...
     objThisIntf.SetPlacementAxisdbVar1

```