# VisPropertySet (Object)

**_Represents the graphic properties for the current selection._**
**Role** : We retrieve the graphic properties of the current selection thanks to [Selection.VisProperties](../InfInterfaces/interface_Selection_18040.htm#VisProperties)

**The graphic properties are:**

  * _The Color_

The Color is defined by 3 components (red,green,blue). Each component ranges from 0 to 255
  * _The Opacity_

The opacity is defined from 255 (total opacity) to 0 (total transparency). In Material visualization mode the transparency is real, so the element is truly more or less opaque. But in another visualization mode, the transparency is a simulation, so if the opacity is between 0 and 254 the element is transparent but with the same visual effect and if the opacity is 255 the element is opaque.
  * _The width of a line_

Each index defines a width customizable in Tools/Options.
  * _The type of a line_

Solid, Dashed, ...
  * _The symbol of a point_

Star, Dot, ...
**A partial modification of an object**
A part (for example) contains faces, edges, lines, points. Interactively with the Edit Properties command the end user can change their color, their line type and so one. To go faster there is the Graphic Toolbar which contains a sub-set of properties. So this interface follows the behavior of the graphic toolbar. The color, the line type ... is applicated to the sub-element of the object defined by the application, and that you can retrieve in the graphic toolbar.

**A multiple selection**
When we modify a graphic property using the Setxxx methods, we modify one by one each element of the current selection.
When we read a graphic property using the Getxxx methods, we retrieve an information which is valid for all elements of the current selection.

**Real versus Visible graphic properties**
Elements of the current selection are inside a specification tree:

```VBScript
  Example :

  Product0
       Part1
          Part3
       Part2

```

In this sample, product0 and Part1 are nodes and Part3 and Part2 are leaves.
Each element (node and leaf) of this tree has its own graphic properties: that is the **"Real"** graphic properties.
But there is an inheritance mecanism, so each element has also **"Visible"** graphic properties. An element can be displayed with an another graphic properties that its real graphic properties.

**The inheritance is the following** :
From the root of the tree, the first node with an inheritance flag to 1, gives its property to each element below it. For each graphic property there is an independantly inheritance.

```VBScript
  Example with the color property: ( color inheritance flag, color)

  Product0    (1,red)
       Part1    (0,blue)
          Part3   (1,green)
       Part2    (0,Yellow)

```

In this sample the real colord of the product0 is red, blue for the part1, green for the part3 and yellow for the part2. But the visible color of each element is red, because the product0 gives the red color at all the tree.

**See also:**      [Selection](../InfInterfaces/interface_Selection_18040.md)

## Methods

### Func **GetLayer**( [CatVisLayerType](../InfInterfaces/enum_CatVisLayerType_47681.md)  `oLayerType`,  long  `oLayerValue`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Returns the layer for the current selection.
**Note** : This property is global for the object.

**Parameters:**

` oLayerType`      the type of the layer
When the type is equal to catVisLayerNone, the layer of the current selection is "none".
When the type is equal to catVisLayerBasic, the layer of the currection selection is indicated by the following parameter.

` oLayerValue`      A value between 0 to 1000
This parameter is usefull only when the type of the layer is catVisLayerBasic.
**Example:**      The following sample shows how to retrieve layer of current selection.

```VBScript
Dim layer
layer = CLng(0)
Dim layertype As CatVisLayerType
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetLayer layertype, layer
If (layertype = catVisLayerNone) Then
MsgBox "Layer None"
End If
If (layertype = catVisLayerBasic) Then
MsgBox "layer =" & layer
End If

```

### Func **GetPick**( [CatVisPropertyPick](../InfInterfaces/enum_CatVisPropertyPick_69086.md)  `oPick`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Returns the state pick mode for the current selection.
**Note** : This property is global for the object.

**Example:**      The following sample shows how to retrieve pick mode of current selection.

```VBScript
Dim pickstate As CatVisPropertyPick
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetPick pickstate
MsgBox "pick = " & pickstate

```

### Func **GetRealColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the real color for the current selection.

**Parameters:**

` oRed`      A value between 0 and 255
` oGreen`      A value between 0 and 255
` oBlue`      A value between 0 and 255
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same real color, so oRed, oGreen and oBlue are valid `catVisPropertyUnDefined`     The real color is not the same for all elements of the current selection, so oRed, oGreen and oBlue are not valid
**Example:**      The following sample shows how to retrieve real colors of current selection.

```VBScript
Dim r, g, b
r = CLng(0)
g = CLng(0)
b = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetRealColor r, g, b
MsgBox "r = " & r & " g = " & g & " b = " & b

```

### Func **GetRealInheritance**( [CatVisPropertyType](../InfInterfaces/enum_CatVisPropertyType_70430.md)  `iPropertyType`,  long  `oInheritance`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the real inheritance flag for the current selection.

**Parameters:**

` iPropertyType`      The type of property: Color, Opacity, Line Width, Line Type
` oInheritance`

`0`     No heritance `1`     Heritance
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same real inheritance flag for the iPropertyType , so oInheritance is valid `catVisPropertyUnDefined`     The real inheritance flag for iPropertyType is not the same for all elements of the current selection, so oInheritance is not valid
**Example:**      The following sample shows how to retrieve inheritance of current selection.

```VBScript
Dim inhLineType, inhWidth, inhColor, inhOpacity
inhLineType = CLng(0)
inhWidth = CLng(0)
inhColor = CLng(0)
inhOpacity = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetRealInheritance catVisPropertyLineType, inhLineType
visProperties1.GetRealInheritance catVisPropertyWidth, inhWidth
visProperties1.GetRealInheritance catVisPropertyColor, inhColor
visProperties1.GetRealInheritance catVisPropertyOpacity, inhOpacity
MsgBox "Inheritance : linetype = " & inhLineType & "width =" & inhWidth & "Colour ="  & inhColor & "Opacity =" & inhOpacity

```

### Func **GetRealLineType**( long  `oLineType`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the real line type for the current selection.

**Parameters:**

` oLineType`      The value ranges from 1 to 63. Each indice is a line type customizable in the page Tools/Options/General/Display/Line Type.
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same real line type , so oLineType is valid `catVisPropertyUnDefined`     The real line type is not the same for all elements of the current selection, so oLineType is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oLineType is not valid
**Example:**      The following sample shows how to retrieve real line type of current selection.

```VBScript
Dim linetype
linetype = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetRealLineType linetype
MsgBox "linetype = " & linetype

```

### Func **GetRealOpacity**( long  `oOpacity`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the real opacity for the current selection.

**Parameters:**

` oOpacity`      a value between 0 (total transparency) and 255 (total opacity)
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same real opacity value, so oOpacity is valid `catVisPropertyUnDefined`     The real opacity value is not the same for all elements of the current selection, so oOpacity is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oOpacity is not valid
**Example:**      The following sample shows how to retrieve real opacity of current selection.

```VBScript
Dim op
op = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetRealOpacity op
MsgBox "opacity = " & op

```

### Func **GetRealWidth**( long  `oLineWidth`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the real line width for the current selection.

**Parameters:**

` oLineWidth`      The value ranges from 1 to 63. Each indice is a thickness customizable in the page Tools/Options/General/Display/thickness.
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same real width , so oLineWidth is valid `catVisPropertyUnDefined`     The real width is not the same for all elements of the current selection, so oLineWidth is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oLineWidth is not valid
**Example:**      The following sample shows how to retrieve real line width of current selection.

```VBScript
Dim width
width = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetRealWidth width
MsgBox "width = " & width

```

### Func **GetShow**( [CatVisPropertyShow](../InfInterfaces/enum_CatVisPropertyShow_70452.md)  `oShow`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Returns the state show mode for the current selection.
**Note** : This property is global for the object.

**Example:**      The following sample shows how to retrieve show mode of current selection.

```VBScript
Dim showstate As CatVisPropertyShow
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetShow showstate
MsgBox "show = " & showstate

```

### Func **GetSymbolType**( long  `oSymbolType`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the symbol type for the current selection.

**Parameters:**

` oSymbolType`      The symbol type. See
SetSymbolType to have values. ` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same symbol type , so oLineType is valid `catVisPropertiesUnDefined`     The symbol type is not the same for all elements of the current selection, so oLineType is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oSymbolType is not valid
**Example:**      The following sample shows how to retrieve symbol line type of current selection.

```VBScript
Dim symbol
symbol = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetSymbolType symbol
MsgBox "Symbol = " & symbol

```

### Func **GetVisibleColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the displayed (visible) color for the current selection.

**Parameters:**

` oRed`      a value between 0 and 255
` oGreen`      a value between 0 and 255
` oBlue`      a value between 0 and 255
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same visible color, so oRed, oGreen and oBlue are valid `catVisPropertyUnDefined`     The visible color is not the same for all elements of the current selection, so oRed, oGreen and oBlue are not valid
**Example:**      The following sample shows how to retrieve displayed colors of current selection.

```VBScript
Dim r, g, b
r = CLng(0)
g = CLng(0)
b = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetVisibleColor r, g, b
MsgBox "r = " & r & " g = " & g & " b = " & b

```

### Func **GetVisibleInheritance**( [CatVisPropertyType](../InfInterfaces/enum_CatVisPropertyType_70430.md)  `iPropertyType`,  long  `oInheritance`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Checks if the real property is hidden.

**Parameters:**

` iPropertyType`      The type of property : Color, Opacity, Line Width, Line Type
` oInheritance`

`0`     No heritance: All parents of each element of the current selection have an inheritance flag to 0. `1`     Heritance: one parent of each element, perhaps the element itself, as a inheritance flag to 1.
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same inheritance flag for the iPropertyType , so oInheritance is valid `catVisPropertyUnDefined`     The inheritance flag for iPropertyType is not the same for all elements of the current selection, so oInheritance is not valid

### Func **GetVisibleLineType**( long  `oLineType`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the displayed (visible) line type for the current selection.

**Parameters:**

` oLineType`      A value ranges from 1 to 63.
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same visible line type , so oLineType is valid `catVisPropertyUnDefined`     The visible line type is not the same for all elements of the current selection, so oLineType is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oLineType is not valid
**Example:**      The following sample shows how to retrieve displayed line type of current selection.

```VBScript
Dim linetype
linetype = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetVisibleLineType linetype
MsgBox "linetype = " & linetype

```

### Func **GetVisibleOpacity**( long  `oOpacity`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the displayed (visible) opacity for the current selection.

**Parameters:**

` oOpacity`      a value between 0 (total transparency) and 255 (total opacity)
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same visible opacity value, so oOpacity is valid `catVisPropertyUnDefined`     The visible opacity value is not the same for all elements of the current selection, so oOpacity is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oOpacity is not valid
**Example:**      The following sample shows how to retrieve displayed opacity of current selection.

```VBScript
Dim op
op = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetVisibleOpacity op
MsgBox "opacity = " & op

```

### Func **GetVisibleWidth**( long  `oLineWidth`) As [CatVisPropertyStatus](../InfInterfaces/enum_CatVisPropertyStatus_87582.md)

Retrieves the displayed (visible) line width for the current selection.

**Parameters:**

` oLineWidth`      A value ranges from 1 to 63.
` oStatus`      **Legal value:**

`catVisPropertyDefined`     All elements in the current selection have the same visible width , so oLineWidth is valid `catVisPropertyUnDefined`     The visible width is not the same for all elements of the current selection, so oLineWidth is not valid `catVisProperty?`     At least one element of the current selection is not concerned by this property, so oLineWidth is not valid
**Example:**      The following sample shows how to retrieve displayed line width of current selection.

```VBScript
Dim width
width = CLng(0)
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.GetVisibleWidth width
MsgBox "width = " & width

```

### Sub **SetLayer**( [CatVisLayerType](../InfInterfaces/enum_CatVisLayerType_47681.md)  `iLayerType`,  long  `iLayerValue`)

Sets the layer for the current selection.
**Note** : This property is global for the object.

**Parameters:**

` iLayerType`      the type of the layer
` iLayerValue`      A value between 0 to 1000
This parameter is used only when the type of the layer is catVisLayerBasic.
**Example:**      The following sample shows how to change layer of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetLayer catVisLayerBasic, 100

```

### Sub **SetPick**( [CatVisPropertyPick](../InfInterfaces/enum_CatVisPropertyPick_69086.md)  `iPick`)

Sets the state pick mode for the current selection.
**Note** : This property is global for the object.

**Example:**      The following sample shows how to change pick mode of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetPick catVisPropertyNoPickAttr

```

### Sub **SetRealColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`,  long  `iInheritance`)

Sets the real color and the color inheritance flag for the current selection.

**Parameters:**

` iRed`      A value between 0 and 255
` iGreen`      A value between 0 and 255
` iBlue`      A value between 0 and 255
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance
**Example:**      The following sample shows how to change colour of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetRealColor 255,0,0,1

```

### Sub **SetRealLineType**( long  `iLineType`,  long  `iInheritance`)

Sets the real line type and the line type inheritance flag for the current selection.

**Parameters:**

` iLineType`      The value ranges from 1 to 63. Each indice is a line type customizable in the page Tools/Options/General/Display/Line Type.
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance
**Example:**      The following sample shows how to change line type of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetRealLineType 4,1

```

### Sub **SetRealOpacity**( long  `iOpacity`,  long  `iInheritance`)

Sets the opacity and the opacity inheritance flag for the current selection.

**Parameters:**

` iOpacity`      A value between 0 (total transparency) and 255 (total opacity).
` iInheritance`      **Legal value:**

`0`     No heritance
**Example:**      The following sample shows how to change opacity of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetRealOpacity 128,1

```

### Sub **SetRealWidth**( long  `iLineWidth`,  long  `iInheritance`)

Sets the real line width and the line width inheritance flag for the current selection.

**Parameters:**

` iLineWidth`      The value ranges from 1 to 63. Each indice is a thickness customizable in the page Tools/Options/General/Display/thickness.
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance
**Example:**      The following sample shows how to change line width of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetRealWidth 4,1

```

### Sub **SetShow**( [CatVisPropertyShow](../InfInterfaces/enum_CatVisPropertyShow_70452.md)  `iShow`)

Sets the state show mode for the current selection.
**Note** : This property is global for the object.

**Example:**      The following sample shows how to change show mode of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetShow catVisPropertyNoShowAttr

```

### Sub **SetSymbolType**( long  `iSymbolType`)

Sets the symbol type.
**Note:** There is no heritage for symbols. That is why there is only one function "SetSymbolType" and no function "SetRealSymbolType" or "SetVisibleSymbolType"

**Parameters:**

` iSymbolType`      The symbol type
**legal values** :

  * 1 : a cross which looks like a "X".
  * 2 : a cross which looks like a "+"
  * 3 : an unfilled circle
  * 4 : two unfilled concentric circles
  * 5 : a filled circle
  * 6 : a filled square
  * 7 : a star which is the union of a 2D marker CROSS ,a 2D marker PLUS and a 2D marker DOT
  * 8 : a dot
  * 9 : a smalldot (one pixel)
  * 10 : a kind of arrow which points to the bottom-left

```VBScript
   	|  /
   	|/__

```

  * 11 : a kind of arrow which points to the top-rigth

```VBScript
   	      /|
   	    /  |
   	  /

```

  * FULLCIRCLE2 : a big 12
  * FULLSQUARE2 : a big 13

**Example:**      The following sample shows how to change symbol type of current selection.

```VBScript
Set visProperties1 = CATIA.ActiveDocument.Selection.VisProperties
visProperties1.SetSymbolType 4

```