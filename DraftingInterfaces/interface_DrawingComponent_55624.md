# DrawingComponent (Object)

**_Represents a drawing component instance (ditto) in a drawing view._**

## Properties

### Property **Angle**(| ) As double

   Returns or sets the angle of the drawing component instance. The angle is given in the axis system of the drawing view The angle is measured in radians and is counted counterclockwise.

**Example:**      This example sets the angle of the `MyComponent` drawing component instance to 90 degrees clockwise. You first need to compute the angle in radians and set the minus sign to indicate the rotation is clockwise.

```VBScript
     PI = 3.1415926535
     Angle90Clockwise = -PI/2
     MyComponent.Angle = Angle90Clockwise

```

### Property **CompRef**( ) As [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md) (Read Only)

   Returns the component reference of this drawing component instance. this is a CATIADrawingView

**Example:**      This example gets the drawing component reference of the `MyComponent` drawing component instance.

```VBScript
     Dim ComponentRef As DrawingView
     Set ComponentRef = MyComponent.CompRef

```

### Property **Scale2**( ) As double

   Returns or sets the scale of the drawing component instance (Workaround for VBA keyword).

**Example:**      This example sets the scale of the `MyComponent` drawing component instance to 0.5.

```VBScript
     MyComponent.Scale2 = 0.5

```

### Property **x**( ) As double

   Returns or sets the x coordinate of the drawing component instance position. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the x coordinate of the position of the `MyComponent` drawing component instance to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewXCoordinate = 5*25.4
     MyComponent.x =  NewXCoordinate

```

### Property **y**( ) As double

   Returns or sets the y coordinate of the drawing component instance position. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the y coordinate of the position of the `MyComponent` drawing component instance to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewYCoordinate = 5*25.4
     MyComponent.y =  NewYCoordinate

```

Methods

### Sub **Explode**( )

   Explodes the drawing component instance (every sub elements of the drawing component are created). Note: The drawing component is not removed by Explode method

**Example:**      This example Explodes the `MyComponent` drawing component instance and removes it.

```VBScript
     MyComponent.Explode
     Set MySelection = CATIA.ActiveDocument.Selection
     MySelection.clear
     MySelection.add MyComponent
     MySelection.delete

```

### Sub **ExplodeAndSelect**( )

   Explodes the drawing component instance (every sub elements of the drawing component are created) and put created sub elements in selection set.

**Example:**      This example Explodes the `MyComponent` drawing component instance.

```VBScript
     MyComponent.ExplodeAndSelect

```

### Sub **ExposeCompRef**( )

   Exposes the component reference of this drawing component instance in a new detail sheet.

**Example:**      This example exposes the component reference of the `MyComponent` drawing component instance in a new detail sheet.

```VBScript
     MyComponent.ExposeCompRef

```

### Sub **ExposeCompRefInSheet**( [CATIADrawingSheet](../DraftingInterfaces/interface_DrawingSheet_30816.md)  `iSheet`)

   Exposes the component reference of this drawing component instance in a specific detail sheet.

**Parameters:**

` iSheet`      The drawing sheet where the reference component has to be exposed. This sheet has to be a detail sheet, if not the component reference will be placed in a new detail sheet.

**Example:**      This example exposes the component reference of the `MyComponent` drawing component instance in the `MyDetailSheet` drawing sheet.

```VBScript
     MyComponent.ExposeCompRefInSheet MyDetailSheet

```

### Sub **Flip**( )

   Flips the drawing component instance around X axis To flip around Y axis you have to flip the component around X and to add a rotation of 180 degrees.

**Example:**      This example Flips the `MyComponent` drawing component instance.

```VBScript
     MyComponent.Flip

```

### Func **GetFlip**( ) As boolean

   Returns the flip state of a drawing component instance around X axis.

**Example:**      This example Get the flip info of the `MyComponent` drawing component instance.

```VBScript
     IsFlipped = MyComponent.GetFlip

```

### Sub **GetMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioMatrix`)

   Gets the matrix of the drawing component instance. This matrix enables you to define the position (index 4 and 5 of the matrix) and the scale, the angle and the flip (index 0,1,2 and 3) of the drawing component instance at the same time.

**Parameters:**

` ioMatrix[0]`      The 1st coordinate of the first vector
` ioMatrix[1]`      The 2nd coordinate of the first vector
` ioMatrix[2]`      The 1st coordinate of the second vector
` ioMatrix[3]`      The 2nd coordinate of the second vector
` ioMatrix[4]`      The x value of the translation vector
` ioMatrix[5]`      The y value of the translation vector

### Func **GetModifiableObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a modifiable object by index or name in this drawing component instance.

**Example:**      This example Gets the first modifiable object in the `MyComponent` drawing component instance.

```VBScript
     Object = MyComponent.GetModifiableObject(1)

```

### Func **GetModifiableObjectsCount**( ) As long

   Gets the number of modifiable objects in this drawing component instance.

**Example:**      This example Gets the number of modifiable objects in `MyComponent` drawing component instance.

```VBScript
     Count = MyComponent.GetModifiableObjectsCount

```

### Sub **SetMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iMatrix`)

   Sets the matrix of the drawing component instance. This matrix enables you to define the position (index 4 and 5 of the matrix) and the scale, the angle and the flip (index 0,1,2 and 3) of the drawing component instance at the same time.

**Parameters:**

` ioMatrix[0]`      The 1st coordinate of the first vector
` ioMatrix[1]`      The 2nd coordinate of the first vector
` ioMatrix[2]`      The 1st coordinate of the second vector
` ioMatrix[3]`      The 2nd coordinate of the second vector
` ioMatrix[4]`      The x value of the translation vector
` ioMatrix[5]`      The y value of the translation vector