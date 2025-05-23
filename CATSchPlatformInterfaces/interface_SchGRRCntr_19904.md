# SchGRRCntr (Object)

**_Manage the graphical representation of a schematic connector._**

## Methods

### Sub **GetSymbol**(| [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `oGRR`,| | [CatSchIDLCntrSymbolType](../CATSchPlatformInterfaces/enum_CatSchIDLCntrSymbolType_107470.md) | `oESymbolType`)

   Get the graphical primitive of a connector.

**Parameters:**

` oGRR`      The graphical primitive (ditto) used to represent a connector.
` oESymbolType`      Connector symbol type such as: point, point/vector, OnOffSheet, LineBoundary.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRCntr
     Dim objArg1 As SchGRR

      ...
     objThisIntf.GetSymbolobjArg1,CatSchIDLCntrSymbolType_Enum

```

### Sub **RemoveSymbol**( )

   Remove the graphical primitive used as the connector's symbol. The default connector's symbol type will be set to point.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRCntr
      ...
     objThisIntf.RemoveSymbol

```

### Sub **SetSymbol**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRRSymbol`,  [CatSchIDLCntrSymbolType](../CATSchPlatformInterfaces/enum_CatSchIDLCntrSymbolType_107470.md)  `iESymbolType`)

   Set the symbol or graphics used to represent a connector.

**Parameters:**

` iGRRSymbol`      The graphical primitive (detail) to be used as the connector's symbol. iGRRSymbol can be NULL if iESymbolType is a point or point/vector.
` iESymbolType`      Connector symbol type such as: point, point/vector, OnOffSheet, LineBoundary.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRCntr
     Dim objArg1 As SchGRR

      ...
     objThisIntf.SetSymbolobjArg1,CatSchIDLCntrSymbolType_Enum

```