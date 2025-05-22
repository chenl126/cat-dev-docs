# DrawingText (Object)

**_Represents a drawing text in a drawing view._**

## Properties

### Property **AnchorPosition**( ) As [CatTextAnchorPosition](../DraftingInterfaces/enum_CatTextAnchorPosition_94223.md)

Returns or sets the anchor position of the drawing text.

**Example:**      This example sets the anchor position of the `MyText` drawing text to top left position.

```VBScript
MyText.AnchorPosition = TopLeft

```

### Property **Angle**( ) As double

Returns or sets the angle of the drawing text. The angle is measured between the axis system of the drawing view and the local axis system of the drawing text. The angle is measured in radians and is counted counterclockwise.

**Example:**      This example sets the angle of the `MyText` drawing Text to 90 degrees clockwise. You first need to compute the angle in degrees and set the minus sign to indicate the rotation is clockwise.

```VBScript
Angle90Clockwise = -90
MyText.Angle = Angle90Clockwise

```

### Property **AssociativeElement**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns or sets the associative object of the drawing text.

**Example:**      This example sets an associative line of the `MyText` drawing text to top left position.

```VBScript
MyText.AssociativeElement = line

```

### Property **FrameType**( ) As [CatTextFrameType](../DraftingInterfaces/enum_CatTextFrameType_53822.md)

Returns or sets the frame type of the drawing text.

**Example:**      This example sets the frame type of the `MyText` drawing text to an ellipse.

```VBScript
MyText.FrameType = catEllipse

```

### Property **Leaders**( ) As [CATIADrawingLeaders](../DraftingInterfaces/interface_DrawingLeaders_41600.md) (Read Only)

Returns the drawing leader collection of the drawing text.

**Example:**      This example retrieves in `LeaderCollection` the collection of leaders of the `MyText` drawing text.

```VBScript
Dim LeaderCollection As DrawingLeaders
Set LeaderCollection = MyText.Leaders

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets character string that makes up the text.

**Example:**      This example retrieves in `CharString` the character string of the `MyText` drawing text.

```VBScript
CharString = MyText.Text

```

### Property **TextProperties**( ) As [CATIADrawingTextProperties](../DraftingInterfaces/interface_DrawingTextProperties_95874.md) (Read Only)

Returns the text properties of the drawing text. Allows to modify the whole text properties. To manage a sub part of the text use GetParameterOnSubString

**Example:**      This example retrieves in `TextProperties` the text properties of the `MyText` drawing text.

```VBScript
Dim TextProperties As DrawingTextProperties
Set TextProperties = MyText.TextProperties

```

### Property **WrappingWidth**( ) As double

Returns or sets the wrapping width of the drawing text.

**Example:**      This example sets the wrapping width of the `MyText` drawing text to 50.

```VBScript
MyText.WrappingWidth = 50.

```

### Property **x**( ) As double

Returns or sets the x coordinate of the text. It is expressed with respect to the current view coordinate system. This coordinate, like any length, is measured in meters.

**Example:**      This example retrieves the x coordinate of the text `MyText` drawing text.

```VBScript
X = MyText.x

```

### Property **y**( ) As double

Returns or sets the y coordinate of the text. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in meters.

**Example:**      This example sets the y coordinate of the text `MyText` drawing text to 5 inches. You need first to convert the 5 inches into meters.

```VBScript
NewYCoordinate = 5*25.4/1000
MyText.y =  NewYCoordinate

```

Methods

### Sub **ActivateFrame**( [CatTextFrameType](../DraftingInterfaces/enum_CatTextFrameType_53822.md)  `itype`)

Activates the text frame of the drawing text.

**Example:**      This example adds a rectangle frame to `MyText` drawing text.

```VBScript
CatTextFrameType ityp = catRectangle
MyText.ActivateFrame(itype)

```

This example removes the frame to `MyText` drawing text.

```VBScript
CatTextFrameType ityp = catNone
MyText.ActivateFrame(itype)

```

### Func **GetFontName**( long  `iFirst`,  long  `inbCharacter`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns the font name on a substring of the drawing text.

**Parameters:**

` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
**Returns:**      oFontName The name of the font  **Example:**      This example gets the `MyText` drawing text font.

```VBScript
oFontName = MyText.GetFontName(0, 0)

```

### Func **GetFontSize**( long  `iFirst`,  long  `inbCharacter`) As double

Returns the font size on a substring of the drawing text.

**Parameters:**

` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
**Returns:**      oFontSize The size of the font  **Example:**      This example gets the `MyText` font size.

```VBScript
oFontSize = MyText.GetFontSize(0, 0)

```

### Func **GetModifiableIn2DComponentInstances**( ) As boolean

Returns if the text is modifiable or not in 2D component instances. The text must own to a 2D component (NOT to a view)

**Example:**      This example retrieves if `MyText` drawing text is modifiable or not

```VBScript
IsModifiable = MyText.GetModifiableIn2DComponentInstances

```

### Func **GetParameterOnSubString**( [CatTextProperty](../DraftingInterfaces/enum_CatTextProperty_49796.md)  `iParam`,  long  `iFirst`,  long  `inbCharacter`) As long

Returns a property on a substring of the drawing text.

**Parameters:**

` iParam`      The drawing text property
` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
**Returns:**      oval The value corresponding to the property  **Example:**      This example gets the parameter Italic on `MyText` drawing text.

```VBScript
CatTextProperty iParam = catItalic
iFirst = 0
inbCharacter = 0
oval = MyText.GetParameterOnsubString(iParam, iFirst, inbCharacter)

```

### Sub **InsertVariable**( long  `iFirst`,  long  `inbCharacter`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `ibase`)

Sets a Parameter in a string of the drawing text.

**Parameters:**

` iFirst`      The first character from which the parameter is inserted
` inbCharacter`      The number of characters the parameter will replace
` iParameter`      The parameter to be inserted  **Example:**      This example sets a parameter right at the end of `MyText` drawing text.

```VBScript
Dim DrwDocument As DrawingDocument
Set DrwDocument = CATIA.ActiveDocument

Dim iParameter As Parameter
Set iParameter = DrwDocument.Parameters.Item("Drawing\Sheet.1\ViewMakeUp.1\Scale")

MyText.InsertVariable 0, 0, iParameter

```

### Sub **SetFontName**( long  `iFirst`,  long  `inbCharacter`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFontName`)

Sets the font size on a substring of the drawing text.

**Parameters:**

` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
` iFontName`      The name of the font

**Example:**      This example sets the `MyText` drawing text font as `Courrier 10 BT`.

```VBScript
MyText.SetFontName 0,  0, "Courrier 10 BT"

```

### Sub **SetFontSize**( long  `iFirst`,  long  `inbCharacter`,  double  `iFontSize`)

Sets the font size on a substring of the drawing text.

**Parameters:**

` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
` iFontSize`      The size of the font  **Example:**      This example sets the `MyText` font size to `3.5`.

```VBScript
iFontSize = 3.5
MyText.SetFontSize 0,  0, iFontSize

```

### Sub **SetModifiableIn2DComponentInstances**( )

Sets the text as modifiable in 2D component instances.The text must own to a 2D component (NOT to a view).then ,its content will be modifiable inside instances of this 2D component.

**Example:**      This example sets the `MyText` drawing text as modifiable.

```VBScript
MyText.SetModifiableIn2DComponentInstances

```

### Sub **SetParameterOnSubString**( [CatTextProperty](../DraftingInterfaces/enum_CatTextProperty_49796.md)  `iParam`,  long  `iFirst`,  long  `inbCharacter`,  long  `iVal`)

Sets a property on a substring of the drawing text.

**Parameters:**

` iParam`      The drawing text property
` iFirst`      The first character to which the property should apply
` inbCharacter`      The number of characters to which the property should apply
` iVal`      The value to be applied according to the property  **Example:**      This example sets all `MyText` drawing text in bold character.

```VBScript
CatTextProperty iParam = catBold
iFirst = 0
inbCharacter = 0
ival = 1
MyText.SetParameterOnsubString iParam, iFirst, inbCharacter, ival

```