# DrawingLeader (Object)

**_Represents a drawing leader in a drawing view._**

## Properties

### Property **AllAround**(| ) As boolean

   Returns or sets the status of all around.

**Example:**      This example retrieves the status of all around on `MyLeader` drawing leader.

```VBScript
     oSymbol = MyLeader.AllAround

```

### Property **AnchorPoint**( ) As long

   Returns or sets anchor point.

**Example:**      This example retrieves the anchor point on `MyLeader` drawing leader.

```VBScript
     oAnchorPoint = MyLeader.AnchorPoint

```

### Property **HeadSymbol**( ) As [CatSymbolType](../DraftingInterfaces/enum_CatSymbolType_36412.md)

   Returns or sets symbol type of head side.

**Example:**      This example retrieves the symbol type of head side on `MyLeader` drawing leader.

```VBScript
     oSymbol = MyLeader.HeadSymbol

```

### Property **HeadTarget**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns or sets target element of head side.

**Example:**      This example retrieves the target element of head side on `MyLeader` drawing leader.

```VBScript
     oTarget = MyLeader.HeadTarget

```

### Property **NbInterruption**( ) As long (Read Only)

   Returns the number of interruptions of leader path.

**Example:**      This example retrieves the number of interruptions on `MyLeader` drawing leader.

```VBScript
     oNbInterruption = MyLeader.NbInterruption

```

### Property **NbPoint**( ) As long (Read Only)

   Returns the number of points of leader path.

**Example:**      This example retrieves the number of points on `MyLeader` drawing leader.

```VBScript
     oNbPoint = MyLeader.NbPoint

```

Methods

### Sub **AddInterruption**( double  `iFirstPointX`,  double  `iFirstPointY`,  double  `iSecondPointX`,  double  `iSecondPointY`)

   Add an interruption to an leader.

**Parameters:**

` iFirstPointX`      X coordinates of first point.
` iFirstPointY`      Y coordinates of first point.
` iSecondPointX`      X coordinates of second point.
` iSecondPointY`      Y coordinates of second point.  **Example:**      This example adds an interruption to `MyLeader`.

```VBScript
     iFirstPointX = 10.
     iFirstPointY = 20.
     iSecondPointX = 20.
     iSecondPointY = 20.
     MyLeader.AddInterruption iFirstPointX, iFirstPointY, iSecondPointX, iSecondPointY

```

### Sub **AddPoint**( long  `iNum`,  double  `iX`,  double  `iY`)

   Add a point to an leader.

**Parameters:**

` iNum`      Point number. Point will be inserted at iNum+1 position.
` iX`      X coordinates of point to add.
` iY`      Y coordinates of point to add.  **Example:**      This example adds a point to `MyLeader`.

```VBScript
     iNum = 1
     iX = 10.
     iY = 20.
     MyLeader.AddPoint iNum, iX, iY

```

### Func **GetInterruptions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oInterruptions`) As long

   Get leader path.

**Parameters:**

` oInterruptions`      List of interruptions coordinates (X1,Y1,X2,Y2,.....Xn,Yn).

**Returns:**      oNbInterruptions Number of interruptions.  **Example:**      This example gets interruptions of `MyLeader` path.

```VBScript
     oNbInterruptions = MyLeader.GetInterruptions(oInterruptions)

```

### Sub **GetPoint**( long  `iNum`,  double  `oX`,  double  `oY`)

   Get leader point coordinates.

**Parameters:**

` iNum`      Point number.
` oX`      X coordinates of point.
` oY`      Y coordinates of point.  **Example:**      This example gets a point to `MyLeader`.

```VBScript
     iNum = 1
     MyLeader.GetPoint(iNum, oX, oY)

```

### Func **GetPoints**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oPoints`) As long

   Get leader path.

**Parameters:**

` oPoints`      List of points coordinates (X1,Y1,X2,Y2,.....Xn,Yn).

**Returns:**      oNbPoints Number of points.  **Example:**      This example gets points of `MyLeader` path.

```VBScript
     oNbPoints = MyLeader.GetPoints(oPoints)

```

### Sub **ModifyPoint**( long  `iNum`,  double  `iX`,  double  `iY`)

   Modify a point of an leader.

**Parameters:**

` iNum`      Point number to modify.
` iX`      X coordinates of new point.
` iY`      Y coordinates of new point.  **Example:**      This example modifys a point to `MyLeader`.

```VBScript
     iNum = 1
     iX = -10.
     iY = -20.
     MyLeader.ModifyPoint iNum, iX, iY

```

### Sub **RemoveInterruption**( long  `iNum`)

   Remove an interruption to an leader.

**Parameters:**

` iNum`      Interruption number to delete.       \- If iNum equals to 0, all interruptions will be removed.  **Example:**      This example removes an interruption from `MyLeader`.

```VBScript
     iNum = 2
     MyLeader.RemoveInterruption iNum

```

### Sub **RemovePoint**( long  `iNum`)

   Remove a point from an leader.

**Parameters:**

` iNum`      Point number to delete.  **Example:**      This example removes a point from `MyLeader`.

```VBScript
     iNum = 2
     MyLeader.RemovePoint iNum

```