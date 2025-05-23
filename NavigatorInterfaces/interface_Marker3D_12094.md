# Marker3D (Object)

**_Represents a marker 3D._**

## Properties

### Property **Fill**(| ) As long

   Returns or sets the marker 3D's filling status (1 the figure is filled, 0 the figure is not filled).

**Example:**      This example retrieves the filling status of `NewMarker3D` marker 3D.

```VBScript
        Dim status As Integer
        status = NewMarker3D.Fill

```

### Property **Frame**( ) As long

   Returns or sets the marker 3D's framing status (1 the figure is framed, 0 the figure is not framed).

**Example:**      This example retrieves the framing status of `NewMarker3D` marker 3D.

```VBScript
        Dim status As Integer
        status = NewMarker3D.Frame

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text for a text marker 3D.

**Example:**      This example reads the text of `NewMarker3D` marker 3D.

```VBScript
        Dim text As String
        text = NewMarker3D.Text

```

### Property **TextFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text's font for a marker 3D.

**Example:**      This example retrieves the text's font of `NewMarker3D` marker 3D.

```VBScript
        Dim font As String
        font = NewMarker3D.TextFont

```

### Property **TextOrientation**( ) As [CatMarkerTextOrientation](../NavigatorInterfaces/enum_CatMarkerTextOrientation_123088.md)

   Returns or sets the orientation of text.

**Example:**      This example retrieves the orientation of `NewMarker3D` marker 3D.

```VBScript
        Dim orientation As CatMarkerTextOrientation
        orientation = NewMarker3D.TextOrientation

```

### Property **TextSize**( ) As double

   Returns or sets the text's size for a marker 3D.

**Example:**      This example retrieves the text's size of `NewMarker3D` marker 3D.

```VBScript
        Dim size As Double
        size = NewMarker3D.TextSize

```

### Property **Type**( ) As [CatMarker3DType](../NavigatorInterfaces/enum_CatMarker3DType_44587.md) (Read Only)

   Returns the type of the marker 3D.

**Example:**      This example reads the type of `NewMarker3D` marker 3D.

```VBScript
        Dim type As CatMarker3DType
        type = NewMarker3D.Type

```

Methods

### Sub **AddObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Adds a link to an object.

**Parameters:**

` iObject`      The object to be linked.

**Example:**      This example links `ThisProduct` to the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.AddObject(ThisProduct)

```

### Func **CountObject**( ) As long

   Returns the number of objects which are linked to the marker 3D.

**Example:**      This example reads the number of objects in the marker3D `NewMarker3D`.

```VBScript
        Dim number As Integer
        number = NewMarker3D.CountObject

```

### Sub **GetObjectPositions**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the anchor point of the marker on the object.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.
` oCoordinates`      The coordinates of the anchor point

  * oCoordinates(0) is the X coordinate of the anchor point
  * oCoordinates(1) is the Y coordinate of the anchor point
  * oCoordinates(2) is the Z coordinate of the anchor point

**Example:**      This example retrieves the coordinates of the anchor in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (3)
        NewMarker3D.GetObjectPositions Coordinates

```

### Sub **GetTextPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the positions of a text marker 3D. The bottom-left corner of the text is anchored to a given point.

**Returns:**      The coordinates of the text anchor point

  * oCoordinates(0) is the X coordinate of the text anchor point
  * oCoordinates(1) is the Y coordinate of the text anchor point
  * oCoordinates(2) is the Z coordinate of the text anchor point

**Example:**      This example retrieves the coordinates of the text in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (2)
        NewMarker3D.GetTextPositions Coordinates

```

### Func **ItemObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns an object which is linked to the marker 3D using its index.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.

**Returns:**      The retrieved object  **Example:**      This example retrieves in `ThisObject` the ninth object from the `NewMarker3D` marker 3D.

```VBScript
        Dim ThisObject As Marker3D
        Set ThisObject = NewMarker3D.ItemObject(9)

```

### Sub **RemoveObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an object which is linked to the marker 3D using its index.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.

**Example:**      This example removes the ninth object from the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.RemoveObject(9)

```

### Sub **SetObjectPositions**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the anchor point of the marker on the object.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.
` iCoordinates`      The coordinates of the anchor point

  * oCoordinates(0) is the X coordinate of the anchor point
  * oCoordinates(1) is the Y coordinate of the anchor point
  * oCoordinates(2) is the Z coordinate of the anchor point

**Example:**      This example sets the coordinates of the anchor in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (3)
        NewMarker3D.SetObjectPositions Coordinates

```

### Sub **SetTextPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the positions of a text marker 3D.

**Parameters:**

` iCoordinates`      The coordinates of the text anchor point

  * oCoordinates(0) is the X coordinate of the text anchor point
  * oCoordinates(1) is the Y coordinate of the text anchor point
  * oCoordinates(2) is the Z coordinate of the text anchor point

**Example:**      This example sets the coordinates of the text in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (2)
        NewMarker3D.SetTextPositions Coordinates

```

### Sub **Update**( )

   Updates the the marker 3D: that is to take into account all modifications which occur since last update.

**Example:**      This example updates the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.Update

```