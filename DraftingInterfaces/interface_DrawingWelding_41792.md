# DrawingWelding (Object)

**_Represents a drawing welding in a drawing view._**

## Properties

### Property **Angle**( ) As double

Returns or sets the angle of the drawing text. The angle is measured between the axis system of the drawing view and the local axis system of the drawing text. The angle is measured in radians and is counted counterclockwise.

**Example:**      This example sets the angle of the `MyText` drawing Text to 90 degrees clockwise. You first need to compute the angle in degrees and set the minus sign to indicate the rotation is clockwise.

```VBScript
Angle90Clockwise = -90
MyText.Angle = Angle90Clockwise

```

### Property **IdentificationLineSide**( ) As [CatWeldingSide](../DraftingInterfaces/enum_CatWeldingSide_40476.md)

Returns or sets the welding identification line Side of the drawing welding symbol.
**Precondition** : This property is only available for ISO standard.

**Example:**      This example sets welding identification line Side to Up .

```VBScript
MyWeld.IdentificationLineSide = catWeldingUp

```

### Property **Leaders**( ) As [CATIADrawingLeaders](../DraftingInterfaces/interface_DrawingLeaders_41600.md) (Read Only)

Returns the drawing leader collection of the drawing welding.

**Example:**      This example retrieves in `LeaderCollection` the collection of leaders of the `MyWelding` drawing welding.

```VBScript
Dim LeaderCollection As DrawingLeaders
Set LeaderCollection = MyWelding.Leaders

```

### Property **TextProperties**( ) As [CATIADrawingTextProperties](../DraftingInterfaces/interface_DrawingTextProperties_95874.md) (Read Only)

Returns the text properties of the drawing welding.

**Example:**      This example retrieves in `TextProperties` the text properties of the `MyWelding` drawing welding..

```VBScript
Dim TextProperties As DrawingTextProperties
Set TextProperties = MyWelding.TextProperties

```

### Property **WeldingSide**( ) As [CatWeldingSide](../DraftingInterfaces/enum_CatWeldingSide_40476.md)

Returns or sets the welding side of the drawing welding symbol.

**Example:**      This example sets welding side to Up .

```VBScript
MyWeld.WeldingSide = catWeldingUp

```

### Property **WeldingTail**( ) As [CatDftWeldingTail](../DraftingInterfaces/enum_CatDftWeldingTail_59332.md)

Returns or sets the welding tail of the drawing welding symbol.

**Example:**      This example displays the welding symbol tail.

```VBScript
MyWeld.WeldingTail = catDftWeldingTailYES

```

### Property **x**( ) As double

Returns or sets the x coordinate of the drawing welding. It is expressed with respect to the current view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example retrieves in `X` the x coordinate of the `MyWelding` drawing welding.

```VBScript
X = MyWelding.x

```

### Property **y**( ) As double

Returns or sets the y coordinate of the drawing welding. It is expressed with respect to the current view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the y coordinate of the `MyWelding` drawing welding to 5 inches. You need first to convert the 5 inches into millmeters.

```VBScript
NewYCoordinate = 5*25.4/1000
MyWelding.y = NewYCoordinate

```

Methods

### Func **GetAdditionalSymbol**( [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iWeld`) As [CatWeldAdditionalSymbol](../DraftingInterfaces/enum_CatWeldAdditionalSymbol_110811.md)

Returns the additional symbol of the drawing welding.

**Parameters:**

` iWeld`      The xxx

**Example:**      This example sets an concave additinal symbol on the `MyWelding` drawing welding

```VBScript
MyWelding.Symbol = DftConcaveSymbol

```

### Func **GetFinishSymbol**( [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iWeld`) As [CatDftWeldFinishSymbol](../DraftingInterfaces/enum_CatDftWeldFinishSymbol_100666.md)

Returns the finish symbol of the drawing welding.

**Parameters:**

` iWeld`      The field on which finish symbol is applied.

**Example:**      This example returns the finish symbol on the first symbol of the `MyWelding` drawing welding

```VBScript
MyWelding.GetFinishSymbol(catWeldingFieldOne,oFinishSymbol)

```

### Func **GetSymbol**( [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iWeld`) As [CatWeldingSymbol](../DraftingInterfaces/enum_CatWeldingSymbol_54418.md)

Returns the symbol of the drawing welding.

**Parameters:**

` iWeld`      The field on which the symbol is applied
` oSymbol`      The welding symbol

**Example:**      This example gets the symbol on the first field of the `MyWelding` drawing welding

```VBScript
MyWelding.GetSymbol(catWeldingFieldOne,oSymbol)

```

### Func **GetTextRange**( [CatWeldingField](../DraftingInterfaces/enum_CatWeldingField_46220.md)  `iField`) As [CATIADrawingTextRange](../DraftingInterfaces/interface_DrawingTextRange_54024.md)

Returns the field of the drawing welding in a drawing text range.

**Parameters:**

` iField`      The drawing welding field
**Returns:**      The drawing text range that corresponds to the drawing welding field  **Example:**      This example retrieves the xxx.

```VBScript
Dim textRange As DrawingTextRange
Set textRange = MyWelding.GetTextRange (catWeldingUp)

```

### Sub **SetAdditionalSymbol**( [CatWeldAdditionalSymbol](../DraftingInterfaces/enum_CatWeldAdditionalSymbol_110811.md)  `iSymbol`,  [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iweld`)

Sets the additional symbol of the drawing welding.

**Parameters:**

` iSymbol`      The welding additional symbol
` iWeld`      The xxx

**Example:**      This example sets an concave additinal symbol on the `MyWelding` drawing welding

```VBScript
MyWelding.Symbol = DftConcaveSymbol

```

### Sub **SetFinishSymbol**( [CatDftWeldFinishSymbol](../DraftingInterfaces/enum_CatDftWeldFinishSymbol_100666.md)  `iFinishSymbol`,  [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iWeld`)

Sets the finish symbol of the drawing welding.

**Parameters:**

` iFinishSymbol`      The finish welding symbol
` iWeld`      The field on which finish symbol will be applied.

**Example:**      This example sets the finish symbol on the first symbol of the `MyWelding` drawing welding

```VBScript
MyWelding.GetFinishSymbol(catWeldingFieldOne,catDftLetterCWelding)

```

### Sub **SetSymbol**( [CatWeldingSymbol](../DraftingInterfaces/enum_CatWeldingSymbol_54418.md)  `iSymbol`,  [CatWelding](../DraftingInterfaces/enum_CatWelding_21280.md)  `iweld`)

Sets the symbol of the drawing welding.

**Parameters:**

` iSymbol`      The welding symbol
` iWeld`      The field on which the symbol is applied

**Example:**      This example sets a symbol on the first field of the `MyWelding` drawing welding

```VBScript
MyWelding.SetSymbol(catSquareWelding,catWeldingFieldOne)

```