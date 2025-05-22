# Marker2Ds (Collection)

**_A collection of Marker2Ds objects._**

## Methods

### Func **Add2DArrow**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates an arrow marker 2D and adds it to the marker 2D collection. The arrow is defined using the coordinates of its head and tail points.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the head point
  * iCoordinates(1) is the Y coordinate of the head point
  * iCoordinates(2) is the X coordinate of the tail point
  * iCoordinates(3) is the Y coordinate of the tail point

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DArrow As Marker2D
   Set NewMarker2DArrow = TheMarker2Ds.Add2DArrow(Positions)

```

### Func **Add2DCircle**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  long  `iFillStatus`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a circle marker 2D and adds it to the marker 2D collection. The circle is defined using the coordinates of its center and a point through which it passes.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the center
  * iCoordinates(1) is the Y coordinate of the center
  * iCoordinates(2) is the X coordinate of the a point on the circle
  * iCoordinates(3) is the Y coordinate of the a point on the circle

` iFillStatus`      The filling status (1 the figure is filled, 0 the figure is not filled).
**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DCircle As Marker2D
   Set NewMarker2DCircle = TheMarker2Ds.Add2DCircle(Positions, 0)

```

### Func **Add2DFreeHand**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a free hand drawing marker 2D and adds it to the marker 2D collection. The free hand drawing is defined using the coordinates of a series of points.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the first point
  * iCoordinates(1) is the Y coordinate of the first point
  * iCoordinates(2) is the X coordinate of the second point
  * iCoordinates(3) is the Y coordinate of the second point
  * iCoordinates(n*2-2) is the X coordinate of the n-th point
  * iCoordinates(n*2-1) is the Y coordinate of the n-th point

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DFreeHand As Marker2D
   Set NewMarker2DFreeHand = TheMarker2Ds.Add2DFreeHand(Positions)

```

### Func **Add2DLine**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a line marker 2D and adds it to the marker 2D collection. The line segment is defined using the coordinates of its two endpoints.

**Parameters:**

` iCoordinates`      The coordinates of the endpoints

  * iCoordinates(0) is the X coordinate of the first endpoint
  * iCoordinates(1) is the Y coordinate of the first endpoint
  * iCoordinates(2) is the X coordinate of the second endpoint
  * iCoordinates(3) is the Y coordinate of the second endpoint

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DLine As Marker2D
   Set NewMarker2DLine = TheMarker2Ds.Add2DLine(Positions)

```

### Func **Add2DPicture**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a picture marker 2D and adds it to the marker 2D collection. The picture is defined as a rectangle whose bottom-left and top-right corners are given.

**Parameters:**

` iCoordinates`      The coordinates of the corners

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point
  * iCoordinates(2) is the X coordinate of the top-right point
  * iCoordinates(3) is the Y coordinate of the top-right point

` iPath`      The path to the picture file
**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DPicture As Marker2D
   Set NewMarker2DPicture = TheMarker2Ds.Add2DPicture(Positions, "e:\picture.bmp")

```

### Func **Add2DRectangle**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  long  `iFillStatus`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a rectangle marker 2D and adds it to the marker 2D collection. The rectangle is defined using the coordinates of its bottom-left and top-right corners.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point
  * iCoordinates(2) is the X coordinate of the top-right point
  * iCoordinates(3) is the Y coordinate of the top-right point

` iFillStatus`      The filling status (1 the figure is filled, 0 the figure is not filled).
**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DRectangle As Marker2D
   Set NewMarker2DRectangle = TheMarker2Ds.Add2DRectangle(Positions, 0)

```

### Func **Add2DText**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Creates a text marker 2D and adds it to the marker 2D collection. The text is anchored using the coordinates of its bottom-left point.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point

` iText`      The text
**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
   Dim NewMarker2DText As Marker2D
   Set NewMarker2DText = TheMarker2Ds.Add2DText(Positions, "example")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

Returns a marker 2D using its index from the Marker2Ds collection.

**Parameters:**

` iIndex`      The index of the marker 2D to retrieve from the collection of Marker2Ds. As a numerics, this index is the rank of the marker 2D in the collection. The index of the first marker 2D in the collection is 1, and the index of the last marker 2D is Count.
**Returns:**      The retrieved marker 2D  **Example:**      This example retrieves in `ThisMarker2D` the ninth marker 2D from the `TheMarker2Ds` collection.

```VBScript
   Dim ThisMarker2D As Marker2D
   Set ThisMarker2D = TheMarker2Ds.Item(9)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a marker 2D from the Marker2Ds collection.

**Parameters:**

` iIndex`      The index of the marker 2D to retrieve from he collection of Marker2Ds. As a numerics, this index is the rank of the marker 2D in the collection. The index of the first marker 2D in the collection is 1, and the index of the last marker 2D is Count.
**Example:**      The following example removes the tenth marker 2D from the `TheMarker2Ds` collection.

```VBScript
   TheMarker2Ds.Remove(10)

```