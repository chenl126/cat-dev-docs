# DrawingTextRange (Object)

**_Represents a drawing text range, or contiguous area, in a drawing text._**

A range is a contiguous area in a drawing text defined by the position of a starting and ending character, or by the position of a starting character and a length expressed in number of characters.

## Properties

### Property **Length**( ) As long (Read Only)

Returns the number of characters of the drawing text range.

**Example:**      This example retrieves in `NbChar` the number of characters of the `MyTextRange` drawing text range.

```VBScript
NbChar = MyTextRange.Length

```

### Property **Start**( ) As long (Read Only)

Returns the starting character position of the drawing text range.

**Example:**      This example retrieves in `StartCharPos`the starting character position of the `MyTextRange` drawing text range.

```VBScript
StartCharPos = MyTextRange.Start

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the character string making up the drawing text range.

**Example:**      This example sets in `text` the character string that makes up the `MyTextRange` drawing text range.

```VBScript
MyTextRange.Text = text
Set MyTextProperties = MyTextRange.TextProperties
MyTextProperties.Update

```

**See also:**      [DrawingTextProperties.Update](../DraftingInterfaces/interface_DrawingTextProperties_95874.htm#Update) 
### Property **TextProperties**( ) As [CATIADrawingTextProperties](../DraftingInterfaces/interface_DrawingTextProperties_95874.md) (Read Only)

**Deprecated:**      V5R18 use [DrawingWelding.TextProperties](../DraftingInterfaces/interface_DrawingWelding_41792.htm#TextProperties) This method has not to be used to manage the text range properties. Text properties is only applied on the whole text, not on a sub text identified by a text range. Returns the drawing text range properties.

**Example:**      This example returns in `Prop` the text properties of the `MyTextRange` drawing text range.

```VBScript
Dim Prop As CATIADrawingTextProperties
Set Prop = MyTextRange.TextProperties(String)

```

Methods

### Func **GetTextRange**( long  `iStart`,  long  `iEnd`) As [CATIADrawingTextRange](../DraftingInterfaces/interface_DrawingTextRange_54024.md)

Returns a drawing text range within another drawing text range. The text range is retrieved using its starting and ending character positions.

**Parameters:**

` iStart`      The position of the drawing text range starting character
` iEnd`      The position of the drawing text range ending character  **Example:**      This example retrieves in `extractedTextRange` the drawing text range that begins at the eighth character and end at the fifteenth character of the `MyTextRange` drawing text range.

```VBScript
Dim extractedTextRange As DrawingTextRange
start = 8
end = 15
extractedTextRange = MyTextRange.GetTextRange(start, end)

```

### Sub **InsertAfter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iString`)

Inserts a character string at the end of the drawing text range.

**Parameters:**

` iString`      The character string to be added  **Example:**      This example inserts the `String` character string at the end of the `MyTextRange` drawing text range.

```VBScript
String = "String to insert after"
MyTextRange.InsertAfter(String)
Set MyTextProperties = MyTextRange.TextProperties
MyTextProperties.Update

```

**See also:**      [DrawingTextProperties.Update](../DraftingInterfaces/interface_DrawingTextProperties_95874.htm#Update) 
### Sub **InsertBefore**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iString`)

Inserts a character string at the beginning of the drawing text range.

**Parameters:**

` iString`      The character string to be added  **Example:**      This example inserts the `String` character string at the beginning of the `MyTextRange` drawing text range.

```VBScript
String = "String to insert before"
MyTextRange.InsertBefore(String)
Set MyTextProperties = MyTextRange.TextProperties
MyTextProperties.Update

```

**See also:**      [DrawingTextProperties.Update](../DraftingInterfaces/interface_DrawingTextProperties_95874.htm#Update)