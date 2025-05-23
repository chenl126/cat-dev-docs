# SchCntrLocation (Object)

**_Manage the location of a schematic connector._**

## Methods

### Sub **GetAlignVector**(| [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `iGRR`,| | [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md) | `oDb2AlignVector`)

   Get the current alignment vector of the connector.

**Parameters:**

` iGRR`      Pointer to the graphical primitive or the graphical image or the graphical primitives of the owner of the connector.
` oDb2AlignVector`      X-Y component of the current alignment vector of the connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim objArg1 As SchGRR
     Dim objArg2 As SchListOfDoubles
      ...
     objThisIntf.GetAlignVectorobjArg1,objArg2

```

### Sub **GetPosition**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRR`,  [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2Position`)

   Get the current position of the connector in **absolute** coordinates.

**Parameters:**

` iGRR`      Pointer to the graphical primitive or the graphical image or the graphical primitives of the owner of the connector.
` oDb2Position`      Absolute X-Y coordinates of the current position of the connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim objArg1 As SchGRR
     Dim objArg2 As SchListOfDoubles
      ...
     objThisIntf.GetPositionobjArg1,objArg2

```

### Sub **GetRelativePosition**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2RelativePosition`)

   Get the current position of the connector in **relative** coordinates.

**Parameters:**

` oDb2RelativePosition`      relative X-Y coordinates of the current position of the connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetRelativePositionobjArg1

```

### Sub **SetAlignVector**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2AlignVector`)

   Set the current alignment vector of the connector.

**Parameters:**

` iGRR`      Pointer to the graphical primitive or the graphical image or the graphical primitives of the owner of the connector.
` iDb2AlignVector`      X-Y component of the current alignment vector of the connector to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim objArg1 As SchGRR
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetAlignVectorobjArg1,dbVar2

```

### Sub **SetPosition**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Position`)

   Set the current position of the connector in **absolute** coordinates. All connectors on multi-images are affected because the relative position on connect will be changed accordingly.

**Parameters:**

` iGRR`      Pointer to the graphical primitive or the graphical image or the graphical primitives of the owner of the connector..
` iDb2Position`      absolute X-Y coordinates of the current position of the connector to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim objArg1 As SchGRR
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetPositionobjArg1,dbVar2

```

### Sub **SetRelativePosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2RelativePosition`)

   Set the current position of the connector in absolute coordinates.

**Parameters:**

` iDb2RelativePosition`      relative X-Y coordinates of the current position of the connector to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrLocation
     Dim dbVar1(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetRelativePositiondbVar1

```