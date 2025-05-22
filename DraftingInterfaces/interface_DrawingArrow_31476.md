# DrawingArrow (Object)

**_Represents a drawing arrow in a drawing view._**

## Properties

### Property **HeadSymbol**( ) As [CatSymbolType](../DraftingInterfaces/enum_CatSymbolType_36412.md)

Returns or sets symbol type of head side.

**Example:**      This example retrieves the symbol type of head side on `MyArrow` drawing arrow.

```VBScript
oSymbol = MyArrow.HeadSymbol

```

### Property **HeadTarget**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns or sets target element of head side.

**Example:**      This example retrieves the target element of head side on `MyArrow` drawing arrow.

```VBScript
oTarget = MyArrow.HeadTarget

```

### Property **NbInterruption**( ) As long (Read Only)

Returns the number of interruptions of arrow path.

**Example:**      This example retrieves the number of interruptions on `MyArrow` drawing arrow.

```VBScript
oNbInterruption = MyArrow.NbInterruption

```

### Property **NbPoint**( ) As long (Read Only)

Returns the number of points of arrow path.

**Example:**      This example retrieves the number of points on `MyArrow` drawing arrow.

```VBScript
oNbPoint = MyArrow.NbPoint

```

### Property **TailSymbol**( ) As [CatSymbolType](../DraftingInterfaces/enum_CatSymbolType_36412.md)

Returns or sets symbol type of tail side.

**Example:**      This example retrieves the symbol type of tail side on `MyArrow` drawing arrow.

```VBScript
oSymbol = MyArrow.TailSymbol

```

### Property **TailTarget**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns or sets target element of tail side.

**Example:**      This example retrieves the target element of tail side on `MyArrow` drawing arrow.

```VBScript
oTarget = MyArrow.TailTarget

```

Methods

### Sub **AddInterruption**( double  `iFirstPointX`,  double  `iFirstPointY`,  double  `iSecondPointX`,  double  `iSecondPointY`)

Add an interruption to an arrow.

**Parameters:**

` iFirstPointX`      X coordinates of first point.
` iFirstPointY`      Y coordinates of first point.
` iSecondPointX`      X coordinates of second point.
` iSecondPointY`      Y coordinates of second point.  **Example:**      This example adds an interruption to `MyArrow`.

```VBScript
iFirstPointX = 10.
iFirstPointY = 20.
iSecondPointX = 20.
iSecondPointY = 20.
MyArrow.AddInterruption iFirstPointX, iFirstPointY, iSecondPointX, iSecondPointY

```

### Sub **AddPoint**( long  `iNum`,  double  `iX`,  double  `iY`)

Add a point to an arrow.

**Parameters:**

` iNum`      Point number. Point will be inserted at iNum+1 position.
` iX`      X coordinates of point to add.
` iY`      Y coordinates of point to add.  **Example:**      This example adds a point to `MyArrow`.

```VBScript
iNum = 1
iX = 10.
iY = 20.
MyArrow.AddPoint iNum, iX, iY

```

### Func **GetInterruptions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInterruptions`) As long

Get arrow path.

**Parameters:**

` oInterruptions`      List of interruptions coordinates (X1,Y1,X2,Y2,.....Xn,Yn).
**Returns:**      oNbInterruptions Number of interruptions.  **Example:**      This example gets interruptions of `MyArrow` path.

```VBScript
oNbInterruptions = MyArrow.GetInterruptions(oInterruptions)

```

### Sub **GetPoint**( long  `iNum`,  double  `oX`,  double  `oY`)

Get arrow point coordinates.

**Parameters:**

` iNum`      Point number.
` oX`      X coordinates of point.
` oY`      Y coordinates of point.  **Example:**      This example gets a point to `MyArrow`.

```VBScript
iNum = 1
MyArrow.GetPoint(iNum, oX, oY)

```

### Func **GetPoints**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPoints`) As long

Get arrow path.

**Parameters:**

` oPoints`      List of points coordinates (X1,Y1,X2,Y2,.....Xn,Yn).
**Returns:**      oNbPoints Number of points.  **Example:**      This example gets points of `MyArrow` path.

```VBScript
oNbPoints = MyArrow.GetPoints(oPoints)

```

### Sub **ModifyPoint**( long  `iNum`,  double  `iX`,  double  `iY`)

Modify a point of an Arrow.

**Parameters:**

` iNum`      Point number to modify.
` iX`      X coordinates of new point.
` iY`      Y coordinates of new point.  **Example:**      This example modifys a point to `MyArrow`.

```VBScript
iNum = 1
iX = -10.
iY = -20.
MyArrow.ModifyPoint iNum, iX, iY

```

### Sub **RemoveInterruption**( long  `iNum`)

Remove an interruption to an arrow.

**Parameters:**

` iNum`      Interruption number to delete.       \- If iNum equals to 0, all interruptions will be removed.  **Example:**      This example removes an interruption from `MyArrow`.

```VBScript
iNum = 2
MyArrow.RemoveInterruption iNum

```

### Sub **RemovePoint**( long  `iNum`)

Remove a point from an arrow.

**Parameters:**

` iNum`      Point number to delete.  **Example:**      This example removes a point from `MyArrow`.

```VBScript
iNum = 2
MyArrow.RemovePoint iNum

```