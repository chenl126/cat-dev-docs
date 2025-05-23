# Marker2D (Object)

**_Represents a marker 2D in a specified annotated view._**

## Properties

### Property **Fill**(| ) As long

   Returns or sets the Marker2D's filling status (1 the figure is filled, 0 the figure is not filled).

**Example:**      This example retrieves the filling status of the `NewMarker2D` Marker2D.

```VBScript
        Dim status As Integer
        status = NewMarker2D.Fill

```

### Property **Frame**( ) As long

   Returns or sets the Marker2D's framing status (1 the figure is framed, 0 the figure is not framed).

**Example:**      This example retrieves the framing status of the `NewMarker2D` Marker2D.

```VBScript
        Dim status As Integer
        status = NewMarker2D.Frame

```

### Property **Picture**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path to a picture file for a picture Marker2D.

**Example:**      This example retrieves the path to a picture file of the `NewMarker2D` Marker2D.

```VBScript
        Dim path As String
        path = NewMarker2D.Picture

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text for a text Marker2D.

**Example:**      This example retrieves the text of the `NewMarker2D` Marker2D.

```VBScript
        Dim text As String
        text = NewMarker2D.Text

```

### Property **TextAngle**( ) As double

   Returns or sets the text's angle for a text Marker2D.

**Example:**      This example retrieves the text's angle of the `NewMarker2D` Marker2D.

```VBScript
        Dim angle As Double
        size = NewMarker2D.TextAngle

```

### Property **TextFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text's font for a text Marker2D.

**Example:**      This example retrieves the text's font of the `NewMarker2D` Marker2D.

```VBScript
        Dim font As String
        font = NewMarker2D.TextFont

```

### Property **TextOrientation**( ) As [CatMarkerTextOrientation](../NavigatorInterfaces/enum_CatMarkerTextOrientation_123088.md)

   Return or set the orientation of text.

**Example:**      This example retrieves the orientation of the `NewMarker2D` Marker2D.

```VBScript
        Dim orientation As CatMarkerTextOrientation
        orientation = NewMarker2D.TextOrientation

```

### Property **TextSize**( ) As double

   Returns or sets the text's size for a text Marker2D.

**Example:**      This example retrieves the text's size of the `NewMarker2D` Marker2D.

```VBScript
        Dim size As Double
        size = NewMarker2D.TextSize

```

### Property **Type**( ) As [CatMarker2DType](../NavigatorInterfaces/enum_CatMarker2DType_44552.md) (Read Only)

   Returns the type of the marker 2D.

**Example:**      This example retrieves the type of the `NewMarker2D` Marker2D.

```VBScript
        Dim type As CatMarker2DType
        type = NewMarker2D.Type

```

Methods

### Sub **GetPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the positions of the Marker2D.  These positions depend on the type of the Marker2D :

  * Line: 2 positions.
  * Arrow: 2 positions, the first being the head and the second being the tail.
  * Rectangle: 2 positions, the first being the bottom-left corner and the second being the top-right corner.
  * Circle: 2 positions, the first being the center and the second being a point on the circle.
  * FreeHand: as many positions as points.
  * Text: 1 position, the bottom-left corner.
  * Picture: 2 positions, the first being the bottom-left corner and the second being the top-right corner.

**Parameters:**

` oCoordinates`      The coordinates of the positions expressed as an array of variants are:

  * oCoordinates(0) is the X coordinate of the first point
  * oCoordinates(1) is the Y coordinate of the first point
  * oCoordinates(2) is the X coordinate of the second point
  * oCoordinates(3) is the Y coordinate of the second point
  * oCoordinates(n*2-2) is the X coordinate of the n-th point
  * oCoordinates(n*2-1) is the Y coordinate of the n-th point

**Example:**      This example retrieves the coordinates of the positions of the `NewMarker2D` Marker2D.

```VBScript
        Dim Coordinates (3)
        NewMarker2D.GetPositions Coordinates

```

### Sub **SetPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the positions of the Marker2D.  These positions depend on the type of the Marker2D :

  * Line: 2 positions.
  * Arrow: 2 positions, the first being the head and the second being the tail.
  * Rectangle: 2 positions, the first being the bottom-left corner and the second being the top-right corner.
  * Circle: 2 positions, the first being the center and the second being a point on the circle.
  * FreeHand: as many positions as points.
  * Text: 1 position, the bottom-left corner.
  * Picture: 2 positions, the first being the bottom-left corner and the second being the top-right corner.

**Parameters:**

` iCoordinates`      The coordinates of the positions expressed as an array of variants are:

  * iCoordinates(0) is the X coordinate of the first point
  * iCoordinates(1) is the Y coordinate of the first point
  * iCoordinates(2) is the X coordinate of the second point
  * iCoordinates(3) is the Y coordinate of the second point
  * oCoordinates(n*2-2) is the X coordinate of the n-th point
  * oCoordinates(n*2-1) is the Y coordinate of the n-th point

**Example:**      This example sets the coordinates of the positions of the `NewMarker2D` Marker2D.

```VBScript
        Dim Coordinates (3) 'To be valuated
        NewMarker2D.SetPositions Coordinates

```