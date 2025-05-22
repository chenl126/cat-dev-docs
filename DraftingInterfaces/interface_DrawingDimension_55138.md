# DrawingDimension (Object)

**_Represents a drawing dimension in a Drawing view._**

Returns sub parts of dimension: Extension lines, dimension line and dimension value.

## Properties

### Property **CumulateMode**( ) As boolean (Read Only)

Returns cumulate mode or not.

**Example:**      This example retrieves cumulate mode or not `MyDimension` drawing dimension.

```VBScript
oCumulateMode = MyDimension.CumulateMode

```

### Property **DimStatus**( ) As [CatDimAnalyse](../DraftingInterfaces/enum_CatDimAnalyse_35371.md) (Read Only)

Returns or sets status of dimension.

**Example:**      This example retrieves status of dimension `MyDimension` drawing dimension.

```VBScript
oIsStatus = MyDimension.DimStatus

```

### Property **DimType**( ) As [CatDimType](../DraftingInterfaces/enum_CatDimType_21068.md) (Read Only)

Returns dimension type.

**Example:**      This example retrieves the dimension type `MyDimension` drawing dimension.

```VBScript
oTypeDim = MyDimension.DimType

```

### Property **DualValue**( ) As [CatDimDualDisplay](../DraftingInterfaces/enum_CatDimDualDisplay_59976.md)

Returns or sets dual value type of dimension value.

**Example:**      This example retrieves dual value type of dimension value `MyDimension` drawing dimension.

```VBScript
oDualValue = MyDimension.DualValue

```

### Property **Forshortened**( ) As boolean

Returns or sets foreshortened mode or not.

**Example:**      This example retrieves foreshortened mode or not `MyDimension` drawing dimension.

```VBScript
oForsh = MyDimension.Forshortened

```

### Property **HalfDimMode**( ) As boolean

Returns or sets half dimension mode or not.

**Example:**      This example retrieves half dimension mode or not `MyDimension` drawing dimension.

```VBScript
oHalfDimMode = MyDimension.HalfDimMode

```

### Property **IsClipped**( ) As boolean (Read Only)

Returns the clipping status of the dimension. Returns TRUE if the dimension si clipped  **Example:**      This example gets clipping status of `MyDimension` path.

```VBScript
myDimmensionClippingStatus=MyDimension.IsClipped

```

### Property **NbExtLine**( ) As long (Read Only)

Returns numbers of extension line of dimension.

**Example:**      This example retrieves numbers of extension line of dimension `MyDimension` drawing dimension.

```VBScript
oNbExtline = MyDimension.NbExtLine

```

### Property **NbSymb**( ) As long (Read Only)

Returns numbers of symbol of dimension.

**Example:**      This example retrieves numbers of symbol of dimension `MyDimension` drawing dimension.

```VBScript
oNbSymb = MyDimension.NbSymb

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection of parameters of the dimension.
**Warning** : The returned parameters collection does not support adding parameters, it is mainly provided to access dimension value.

**Example:**      This example retrieves in `DimensionParameters` the collection of parameters currently managed by a dimension.

```VBScript
Dim DimensionParameters As Parameters
Set DimensionParameters = MyDimension.Parameters
Dim DimValueParameter As Parameter
Set DimValueParameter = DimensionParameters.Item("Measured length")

```

### Property **SymbolsSide**( ) As long

Returns or sets symbol side of dimension line. **Legal values** : 0 : Automatic positioning (Inside or Outside). 1 : Symbols are inside. 2 : Symbols are outside. 3 : First symbol inside , second symbol outside. 4 : First symbol outsise, second symbol inside.

**Example:**      This example retrieves symbol side of dimension line `MyDimension` drawing dimension.

```VBScript
oSymbSide = MyDimension.SymbolsSide

```

### Property **TrueDimMode**( ) As boolean (Read Only)

Returns or sets true dimension mode or not.

**Example:**      This example retrieves true dimension mode or not `MyDimension` drawing dimension.

```VBScript
oTrueDimMode = MyDimension.TrueDimMode

```

### Property **ValueAngle**( ) As double

Returns or sets angle of dimension value.

**Example:**      This example retrieves angle of dimension value `MyDimension` drawing dimension.

```VBScript
oValueAng = MyDimension.ValueAngle

```

### Property **ValueAutoMode**( ) As long

Returns or sets auto mode of dimension value or not.

**Example:**      This example retrieves auto mode of dimension value or not `MyDimension` drawing dimension.

```VBScript
oValueAutoMode = MyDimension.ValueAutoMode

```

### Property **ValueDisplay**( ) As long

Returns or sets display of dimension value state.

**Example:**      This example retrieves display of dimension value state `MyDimension` drawing dimension.

```VBScript
oValueDisplay = MyDimension.ValueDisplay

```

### Property **ValueFrame**( ) As [CatDimFrame](../DraftingInterfaces/enum_CatDimFrame_24655.md)

Returns or sets frame type of dimension value.

**Example:**      This example retrieves frame type of dimension value `MyDimension` drawing dimension.

```VBScript
oValueFrame = MyDimension.ValueFrame

```

### Property **ValueInOut**( ) As long

Returns or sets in/out mode of dimension value or not.

**Example:**      This example retrieves in/out mode of dimension value or not `MyDimension` drawing dimension.

```VBScript
oInOut = MyDimension.ValueInOut

```

### Property **ValueOrientation**( ) As [CatDimOrientation](../DraftingInterfaces/enum_CatDimOrientation_61718.md)

Returns or sets orientation of dimension value.

**Example:**      This example retrieves orientation of dimension value `MyDimension` drawing dimension.

```VBScript
oValueOrient = MyDimension.ValueOrientation

```

### Property **ValueReference**( ) As [CatDimReference](../DraftingInterfaces/enum_CatDimReference_46429.md)

Returns or sets reference of dimension value.

**Example:**      This example retrieves reference of dimension value `MyDimension` drawing dimension.

```VBScript
oValueRef = MyDimension.ValueReference

```

Methods

### Sub **GetBoundaryBox**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oValues`)

Get boundary box coordinates of dimension value.

**Parameters:**

` oValues`      List of boundary box coordinates (X1,Y1,X2,Y2,.....X4,Y4).  **Example:**      This example gets boundary box coordinates of `MyDimension` path.

```VBScript
MyDimension.GetBoundaryBox(oValues)

```

### Sub **GetClip**( double  `X`,  double  `Y`,  long  `oKeptSide`)

Gets informations of the dimension clipping. The value of this parameter can be 1 or 2, and the kept side will be the one corresponding respectively to ptldc1 and ptldc2 from GetGeomInfo method defined in CATIADrawingDimensionLine idl interface. interface. If iKeptSide==0, there is no dimension clipping.

**Parameters:**

` oX`      X coordinate of position.
` oY`      Y coordinate of position.
` oKeptSide`      returns the part of the dimension line will be clipped.  **Example:**

```VBScript
if MyDimension.IsClipped then
  MyDimension.GetClip(X, Y, keptSide)
end if

```

### Func **GetDimExtLine**( ) As [CATIADrawingDimExtLine](../DraftingInterfaces/interface_DrawingDimExtLine_59557.md)

Returns the drawing extension line of the drawing dimension.

**Example:**      This example retrieves in `DimExtLine` extension line of the `MyDimension` drawing dimension.

```VBScript
Dim DimExtLine As DrawingDimExtLine
Set DimExtLine = MyDimension.GetDimExtLine

```

**See also:**      [DrawingDimLine](../DraftingInterfaces/interface_DrawingDimLine_40436.md) 
### Func **GetDimLine**( ) As [CATIADrawingDimLine](../DraftingInterfaces/interface_DrawingDimLine_40436.md)

Returns the drawing dimension line of the drawing dimension.

**Example:**      This example retrieves in `DimDimLine` dimension line of the `MyDimension` drawing dimension.

```VBScript
Dim DimDimLine As DrawingDimLine
Set DimDimLine = MyDimension.GetDimLine

```

**See also:**      [DrawingDimLine](../DraftingInterfaces/interface_DrawingDimLine_40436.md) 
### Sub **GetTolerances**( long  `oTolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oTolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oUpTol`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oLowTol`,  double  `odUpTol`,  double  `odLowTol`,  long  `oDisplayMode`)

Get tolerance infomation of dimension value.

**Parameters:**

` oTolType`      Tolerance type
` oTolName`      Tolerance name
` oUpTol`      Upper tolerance value (alpha numerical type)
` oLowTol`      Lower tolerance value (alpha numerical type)
` odUpTol`      Upper tolerance value (numerical type)
` odLowTol`      Lower tolerance value (numerical type)
` oDisplayMode`      Tolerance display mode  **Example:**      This example gets tolerance infomation of `MyDimension` path.

```VBScript
MyDimension.GetTolerances(oTolType, oTolName, oUpTol, oLowTol, odUpTol, odLowTol, oDisplayMode)

```

### Func **GetValue**( ) As [CATIADrawingDimValue](../DraftingInterfaces/interface_DrawingDimValue_47035.md)

Returns the drawing value of the drawing dimension.

**Example:**      This example retrieves in `DimDimValue` value of the `MyDimension` drawing dimension.

```VBScript
Dim DimDimValue As DrawingDimValue
Set DimDimValue = MyDimension.GetValue

```

**See also:**      [DrawingDimValue](../DraftingInterfaces/interface_DrawingDimValue_47035.md) 
### Sub **MoveValue**( double  `X`,  double  `Y`,  long  `SubPart`,  long  `DimAngleBehavior`)

Move dimension value.

**Parameters:**

` X`      X coordinate of position.
` Y`      Y coordinate of position.
` SubPart`      Defines which part of the dimension should be moved.
` DimAngleBehavior`      Defines angle dimension line behavior.  **Example:**      This example move dimension value `MyDimension` path.

```VBScript
MyDimension.MoveValue(X, Y, SubPart, DimAngleBehavior)

```

### Sub **RestoreValuePosition**( )

Restore dimension value position.  **Example:**      This example gets Restore dimension value position of `MyDimension` path.

```VBScript
MyDimension.RestoreValuePosition()

```

### Sub **SetClip**( double  `X`,  double  `Y`,  long  `iKeptSide`)

Creates a clip on the dimension at the given point, with respect to the side given by iKeptSide. The value of this parameter can be 1 or 2, and the kept side will be the one corresponding respectively to ptldc1 and ptldc2 from GetGeomInfo method defined in CATIADrawingDimensionLine idl interface. interface.

**Parameters:**

` iX`      X coordinate of position.
` iY`      Y coordinate of position.
` iKeptSide`      Defines which part of the dimension should be kept.  **Example:**      This example clips dimension `MyDimension` path.

```VBScript
MyDimension.SetClip(X, Y, 1)

```

### Sub **SetTolerances**( long  `iTolType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `itolName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iUpTol`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLowTol`,  double  `idUpTol`,  double  `idLowTol`,  long  `DisplayMode`)

Set tolerance infomation of dimension value.

**Parameters:**

` iTolType`      Tolerance type
` itolName`      Tolerance name
` iUpTol`      Upper tolerance value (alpha numerical type)
` iLowTol`      Lower tolerance value (alpha numerical type)
` idUpTol`      Upper tolerance value (numerical type)
` idLowTol`      Lower tolerance value (numerical type)
` DisplayMode`      Tolerance display mode  **Example:**      This example sets tolerance infomation of `MyDimension` path.

```VBScript
MyDimension.SetTolerances(iTolType, itolName, iUpTol, iLowTol, idUpTol, idLowTol, DisplayMode)

```

### Sub **Unclip**( )

Unclip the dimension if it is clipped.  **Example:**      This example unclip `MyDimension` path.

```VBScript
if MyDimension.IsClipped then
  MyDimension.Unclip

```