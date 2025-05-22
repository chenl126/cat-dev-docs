# DrawingDimValue (Object)

**_Manages dimension value of a dimension in drawing view._**

This interface is obtained from [DrawingDimension.GetValue](../DraftingInterfaces/interface_DrawingDimension_55138.htm#GetValue) method.

## Properties

### Property **FakeDimType**( ) As [CatDimFake](../DraftingInterfaces/enum_CatDimFake_19968.md)

Returns or sets fake dimension type of value.

**Example:**      This example retrieves fake dimension type of value `MyDimValue` drawing dimension.

```VBScript
oFakeType = MyDimValue.FakeDimType

```

### Property **ScoringMode**( ) As [CatDimScore](../DraftingInterfaces/enum_CatDimScore_25136.md)

Get dimension scoring mode.  **Example:**      This example gets dimension scoring mode of `MyValue` path.

```VBScript
ValueScoreType = MyValue.ScoringMode

```

### Property **Value**( ) As double (Read Only)

Returns value of dimension.

**Example:**      This example retrieves value of dimension `MyDimValue` drawing dimension.

```VBScript
oValue = MyDimValue.Value

```

### Property **ValueFramedElement**( ) As [CatDimFramedElement](../DraftingInterfaces/enum_CatDimFramedElement_74083.md)

Get dimension framed element.  **Example:**      This example gets dimension framed element of `MyValue` path.

```VBScript
ValueFramedElement = MyValue.ValueFramedElement

```

### Property **ValueFramedGroup**( ) As [CatDimFramedGroup](../DraftingInterfaces/enum_CatDimFramedGroup_59918.md)

Returns or sets dimension framed group.

**Example:**      This example retrieves dimension framed group `MyDimValue` drawing dimension.

```VBScript
oValueFramedGroup = MyDimValue.FakeDimType

```

Methods

### Sub **GetBaultText**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oBefore`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oAfter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oUpper`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLower`)

Get bault text of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oBefore`      before text.
` oAfter`      after text
` oUpper`      upper text
` oLower`      lower text  **Example:**      This example gets bault text of `MyValue` path.

```VBScript
MyValue.GetBaultText(iIndex, oBefore, oAfter, oUpper, oLower)

```

### Func **GetDisplayUnit**( long  `iIndex`) As long

Get display unit of dimension value.

**Parameters:**

` Index`      1: main value 2: dual value
` oDisplUnit`      before text.  **Example:**      This example gets format unit of `MyValue` path.

```VBScript
FrmUnit = MyValue.GetDisplayUnit(iIndex)

```

### Func **GetFakeDimValue**( long  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Get fake value of dimension.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oFakeDimValue`      before text.  **Example:**      This example gets fake value of `MyValue` path.

```VBScript
FakeDimValue = MyValue.GetFakeDimValue(iIndex)

```

### Func **GetFormatDisplayFactor**( long  `iIndex`) As long

Get format display factor of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oFrmDspFact`      before text.  **Example:**      This example gets format display factor of `MyValue` path.

```VBScript
FrmDspFact = MyValue.GetFormatDisplayFactor(iIndex)

```

### Func **GetFormatName**( long  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Get format name of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oFmName`      before text.  **Example:**      This example gets format name of `MyValue` path.

```VBScript
FmName = MyValue.GetFormatName(iIndex)

```

### Func **GetFormatPrecision**( long  `Index`) As double

Get format precision of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oFrmPrecision`      before text.  **Example:**      This example gets format precision of `MyValue` path.

```VBScript
FrmPrecision = MyValue.GetFormatPrecision(iIndex)

```

### Func **GetFormatType**( long  `iIndex`) As long

Get format type of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oFrmType`      before text.  **Example:**      This example gets format type of `MyValue` path.

```VBScript
FrmType = MyValue.GetFormatType(iIndex)

```

### Func **GetFormatUnit**( long  `iIndex`) As long

Get format unit of dimension value.

**Parameters:**

` Index`      1: main value 2: dual value
` oFrmUnit`      before text.  **Example:**      This example gets format unit of `MyValue` path.

```VBScript
FrmUnit = MyValue.GetFormatUnit(iIndex)

```

### Sub **GetPSText**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oSuffix`)

Get PS text to dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oPrefix`      prefix text.
` oSuffix`      suffix text  **Example:**      This example gets PS text of `MyValue` path.

```VBScript
MyValue.GetBaultText(iIndex, oPrefix, oSuffix)

```

### Func **GetScoredElement**( long  `iIndex`) As boolean

Get dimension scored element.

**Parameters:**

` iIndex`      1: main value 2: dual value
` oScoredElement`      TRUE: Scoring is applied to the all bloc text. FALSE: Scoring is only applied to the value.  **Example:**      This example gets dimension scored element of `MyValue` path.

```VBScript
ScoredElement = MyValue.GetScoredElement(iIndex)

```

### Sub **SetBaultText**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iBefore`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAfter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iUpper`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLower`)

Set bault text to dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iBefore`      before text.
` iAfter`      after text
` iUpper`      upper text
` iLower`      lower text  **Example:**      This example sets bault text of `MyValue` path.

```VBScript
MyValue.SetBaultText(iIndex, iBefore, iAfter, iUpper, iLower)

```

### Sub **SetFakeDimValue**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFakeDimValue`)

Set fake value of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFakeDimValue`      before text.  **Example:**      This example gets fake value of `MyValue` path.

```VBScript
MyValue.SetFakeDimValue(iIndex, iFakeDimValue)

```

### Sub **SetFormatDisplayFactor**( long  `iIndex`,  long  `iFrmDspFact`)

Set format display factor of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFrmDspFact`      before text.  **Example:**      This example gets format display factor of `MyValue` path.

```VBScript
MyValue.SetFormatDisplayFactor(iIndex, iFrmDspFact)

```

### Sub **SetFormatName**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFrmName`)

Set format name of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFrmName`      before text.  **Example:**      This example gets format name of `MyValue` path.

```VBScript
MyValue.SetFormatName(iIndex, iFrmName)

```

### Sub **SetFormatPrecision**( long  `iIndex`,  double  `iFrmPrecision`)

Set format precision of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFrmPrecision`      before text.  **Example:**      This example gets format precision of `MyValue` path.

```VBScript
MyValue.SetFormatPrecision(iIndex, iFrmPrecision)

```

### Sub **SetFormatType**( long  `iIndex`,  long  `iFrmType`)

Set format type of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFrmType`      before text.  **Example:**      This example gets format type of `MyValue` path.

```VBScript
MyValue.SetFormatType(iIndex, iFrmType)

```

### Sub **SetFormatUnit**( long  `iIndex`,  long  `iFrmUnit`)

Set format unit of dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iFrmUnit`      before text.  **Example:**      This example gets format unit of `MyValue` path.

```VBScript
MyValue.SetFormatUnit(iIndex, iFrmUnit)

```

### Sub **SetPSText**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSuffix`)

Set PS text to dimension value.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iPrefix`      prefix text.
` iSuffix`      suffix text  **Example:**      This example sets PS text of `MyValue` path.

```VBScript
MyValue.SetBaultText(iIndex, iPrefix, iSuffix)

```

### Sub **SetScoredElement**( long  `iIndex`,  boolean  `iScoredElement`)

Set dimension scored element.

**Parameters:**

` iIndex`      1: main value 2: dual value
` iScoredElement`      TRUE: Scoring is applied to the all bloc text. FALSE: Scoring is only applied to the value.  **Example:**      This example gets dimension scored element of `MyValue` path.

```VBScript
MyValue.SetScoredElement(iIndex, iScoredElement)

```