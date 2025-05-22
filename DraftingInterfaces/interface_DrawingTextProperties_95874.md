# DrawingTextProperties (Object)

**_Represents the properties of a drawing text in a drawing view._**

This interface is obtained from CATIADrawingText or CATIADrawingWelding interface. Update method must be called after text properties modification to refresh the visualization.

## Properties

### Property **AnchorPoint**( ) As [CatTextAnchorPosition](../DraftingInterfaces/enum_CatTextAnchorPosition_94223.md)

Returns or sets the anchor point of the drawing text.

**Example:**      This example sets the AnchorPoint of the `MyText` drawing text to the right

```VBScript
MyText.AnchorPoint = catRight

```

### Property **Blanking**( ) As [CatBlankingMode](../DraftingInterfaces/enum_CatBlankingMode_46287.md)

Returns or sets the blanking mode of the drawing text.

**Example:**      This example sets the blanking mode type of `MyText` drawing text to active on geom

```VBScript
MyText.Blanking = catBlankingOnGeom

```

### Property **Bold**( ) As long

Returns or sets the drawing text font bold property.
**True** if the drawing text is bold formatted.

**Example:**      This example get the parameter bold on `MyText` drawing text.

```VBScript
oVal = MyText.Bold

```

### Property **Color**( ) As long

Returns or sets the color of the drawing text.

**Example:**      This example sets the Color type of the `MyText` drawing text to red

```VBScript
redCol  =-16776961 'Encoded RGBA color within long integer (R=255 G=0   B=0   A=255)
MyText.Color = redCol

```

### Property **FontName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the font name of the drawing text.

**Example:**      This example sets the `MyText` drawing text font as `Courrier 10 BT`.

```VBScript
MyText.SetFontName("Courrier 10 BT")

```

### Property **FontSize**( ) As double

Returns or sets the font size of the drawing text.

**Example:**      This example sets the `MyText` drawing text font size to `3.5`.

```VBScript
iFontSize = 3.5
MyText.SetFontSize 0, 0, iFontSize

```

### Property **FrameType**( ) As [CatTextFrameType](../DraftingInterfaces/enum_CatTextFrameType_53822.md)

Returns or sets the frame type of the drawing text.

**Example:**      This example sets the frame type of the `MyText` drawing text to an ellipse

```VBScript
MyText.FrameType = catEllipse

```

### Property **Italic**( ) As long

Returns or sets the drawing text font italic property.
**True** if the drawing text is formatted as italic.

**Example:**      This example set the parameter Italic on `MyText` drawing text.

```VBScript
MyText.Italic = 1

```

### Property **Justification**( ) As [CatJustification](../DraftingInterfaces/enum_CatJustification_55344.md)

Returns or sets the drawing text font justification property.
**True** if the drawing text font is justified.

**Example:**      This example sets the Justification type of the `MyText` drawing text to the right

```VBScript
MyText.Justification = catRight

```

### Property **Kerning**( ) As long

Font kerning property.
**True** if the drawing text font is formatted as kerning

**Example:**      This example set the parameter kerning on `MyText` drawing text.

```VBScript
MyText.Kerning = 1

```

### Property **Mirror**( ) As [CatTextFlipMode](../DraftingInterfaces/enum_CatTextFlipMode_46431.md)

Returns or sets the mirroring of the drawing text.

**Example:**      This example sets the Mirror type of the `MyText` drawing text to no flip

```VBScript
MyText.Mirror = catTextNoFlip

```

### Property **Overline**( ) As long

Returns or sets the drawing text font overline property.
**True** if the drawing text is overlined.

**Example:**      This example get the parameter Overline on `MyText` drawing text.

```VBScript
oval = MyText.Overline()

```

### Property **StrikeThru**( ) As long

Returns or sets the drawing text font strikethrough property.
**True** if the drawing text font is striked through.

**Example:**      This example set the parameter StrikeThru on `MyText` drawing text.

```VBScript
MyText.StrikeThru = 1

```

### Property **Subscript**( ) As long

Returns or sets the drawing text font subscript property.
**True** if the drawing text font is formatted as subscript.

**Example:**      This example set the parameter Subscript on `MyText` drawing text.

```VBScript
MyText.Subscript = 1

```

### Property **Superscript**( ) As long

Returns or sets the drawing text font superscript property.
**True** if the drawing text font is formatted as superscript.

**Example:**      This example set the parameter Superscript on `MyText` drawing text.

```VBScript
MyText.Superscript = 1

```

### Property **Underline**( ) As long

Returns or sets the drawing text font underline property.
**True** if the drawing text is underlined.

**Example:**      This example get the parameter bold on `MyText` drawing text.

```VBScript
oval = MyText.Underline

```

Methods

### Sub **ActivateFrame**( [CatTextFrameType](../DraftingInterfaces/enum_CatTextFrameType_53822.md)  `iType`)

Activates the text frame of the drawing text.

**Parameters:**

` iType`      The text frame type  **Example:**      This example add a rectangle frame to `MyText` drawing text.

```VBScript
CatTextFrameType itype = catRectangle
MyText.ActivateFrame itype

```

**Example:**      This example remove the frame to `MyText` drawing text.

```VBScript
CatTextFrameType itype = catNone
MyText.ActivateFrame itype

```

### Sub **Update**( )

Update the properties of the drawing text.  **Example:**      This example update the properties to `MyText` drawing text.

```VBScript
MyText.Update

```