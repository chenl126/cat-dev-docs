# DrawingDimLine (Object)

**_Manages dimension line of a dimension in drawing view._**

This interface is obtained from [DrawingDimension.GetDimLine](../DraftingInterfaces/interface_DrawingDimension_55138.htm#GetDimLine) method.

## Properties

### Property **Color**( ) As long

Returns or sets color of dimension line.

**Example:**      This example retrieves color of dimension line `MyDimLine` drawing dimension.

```VBScript
oColorDimLine = MyDimLine.Color

```

### Property **DimLineGraphRep**( ) As [CatDimLineGraphRep](../DraftingInterfaces/enum_CatDimLineGraphRep_65476.md)

Returns or graphic representation of dimension line.

**Example:**      This example retrieves graphic representation of dimension line `MyDimLine` drawing dimension.

```VBScript
odimLineGraphRep = MyDimLine.DimLineGraphRep

```

### Property **DimLineOrientation**( ) As [CatDimOrientation](../DraftingInterfaces/enum_CatDimOrientation_61718.md)

Returns or orientation of dimension line.

**Example:**      This example retrieves orientation of dimension line `MyDimLine` drawing dimension.

```VBScript
odimLineOrient = MyDimLine.DimLineOrientation

```

### Property **DimLineReference**( ) As [CatDimReference](../DraftingInterfaces/enum_CatDimReference_46429.md)

Returns or reference of dimension line.

**Example:**      This example retrieves reference of dimension line `MyDimLine` drawing dimension.

```VBScript
odimLineRef = MyDimLine.DimLineReference

```

### Property **DimLineRep**( ) As [CatDimLineRep](../DraftingInterfaces/enum_CatDimLineRep_34241.md) (Read Only)

Returns or representation of dimension line.

**Example:**      This example retrieves representation of dimension line `MyDimLine` drawing dimension.

```VBScript
odimLineRep = MyDimLine.DimLineRep

```

### Property **DimLineType**( ) As long (Read Only)

Returns type of dimension line.

**Example:**      This example retrieves type of dimension line `MyDimLine` drawing dimension.

```VBScript
odimLineType = MyDimLine.DimLineType

```

### Property **Thickness**( ) As double

Returns or sets thickness of dimension line.

**Example:**      This example retrieves thickness of dimension line `MyDimLine` drawing dimension.

```VBScript
oThickDimLine = MyDimLine.Thickness

```

Methods

### Sub **GetDimLineDir**( double  `oDirX`,  double  `oDirY`)

Returns direction of a dimension line in case of a DrwDimUserDefined representation mode.

**Parameters:**

` oDirX,oDirY`      The components of the direction vector  **Example:**      This example retrieves the direction vector of a dimension line `MyDimLine` drawing dimension.

```VBScript
MyDimLine.GetDimLineDir oDirX, oDirY

```

### Sub **GetGeomInfo**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oGeomInfos`)

Get geometrical infomation of dimension line.

**Parameters:**

` oGeomInfos`      geometrical information.  **Example:**      This example gets geometrical infomation of `MyDimLine` path.

```VBScript
MyDimLine.GetGeomInfo(oGeomInfos)

```

### Func **GetSymbColor**( long  `Index`) As long

Get symbol color of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` oColorSymb`      symbol color.  **Example:**      This example gets symbol color of `MyDimLine` path.

```VBScript
ColorSymb = MyDimLine.GetSymbColor(Index)

```

### Func **GetSymbThickness**( long  `Index`) As double

Get symbol thickness of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` oThickSymb`      symbol thickness.  **Example:**      This example gets symbol thickness of `MyDimLine` path.

```VBScript
ThickSymb = MyDimLine.GetSymbThickness(Index)

```

### Func **GetSymbType**( long  `Index`) As [CatDimSymbols](../DraftingInterfaces/enum_CatDimSymbols_36155.md)

Get symbol type of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` oTypeSymb`      symbol type.  **Example:**      This example gets symbol type of `MyDimLine` path.

```VBScript
typeSymb = MyDimLine.GetSymbType(Index)

```

### Sub **SetSymbColor**( long  `Index`,  long  `iColorSymb`)

Set symbol color of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` oColorSymb`      symbol color.  **Example:**      This example sets symbol color of `MyDimLine` path.

```VBScript
MyDimLine.SetSymbColor(Index, iColorSymb)

```

### Sub **SetSymbThickness**( long  `Index`,  double  `iThickSymb`)

Set symbol thickness of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` oThickSymb`      symbol thickness.  **Example:**      This example sets symbol thickness of `MyDimLine` path.

```VBScript
MyDimLine.GetSymbThickness(Index, iThickSymb)

```

### Sub **SetSymbType**( long  `Index`,  [CatDimSymbols](../DraftingInterfaces/enum_CatDimSymbols_36155.md)  `iSymbType`)

Set symbol type of dimension line.

**Parameters:**

` Index`      1:first symbol 2:second symbol 3:leader symbol
` iSymbType`      symbol type.  **Example:**      This example sets symbol type of `MyDimLine` path.

```VBScript
MyDimLine.SetSymbType(Index, iSymbType)

```