# DrawingPicture (Object)

**_Represents a drawing picture in a drawing view._**

## Properties

### Property **cropBottom**(| ) As double

   Returns or sets the cropBottom of the drawing picture. The cropBottom is the size of the margin on the bottom of the picture. The cropBottom, like any length, is measured in millimeters.

**Example:**      This example sets the cropBottom of the `MyPicture` drawing picture to 10 mm

```VBScript
     MyPicture.cropBottom = 10.

```

### Property **cropLeft**( ) As double

   Returns or sets the cropLeft of the drawing picture. The cropLeft is the size of the margin on the left of the picture. The cropLeft, like any length, is measured in millimeters.

**Example:**      This example sets the cropLeft of the `MyPicture` drawing picture to 10 mm

```VBScript
     MyPicture.cropLeft = 10.

```

### Property **cropRight**( ) As double

   Returns or sets the cropRight of the drawing picture. The cropRight is the size of the margin on the right of the picture. The cropRight, like any length, is measured in millimeters.

**Example:**      This example sets the cropRight of the `MyPicture` drawing picture to 10 mm

```VBScript
     MyPicture.cropRight = 10.

```

### Property **cropTop**( ) As double

   Returns or sets the cropTop of the drawing picture. The cropTop is the size of the margin on the top of the picture. The cropTop, like any length, is measured in millimeters.

**Example:**      This example sets the cropTop of the `MyPicture` drawing picture to 10 mm

```VBScript
     MyPicture.cropTop = 10.

```

### Property **format**( ) As [CatPictureFormat](../DraftingInterfaces/enum_CatPictureFormat_54570.md)

   Sets the picture format.

**Parameters:**

` iPictureFormat`      Compression format.

**Returns:**

**Legal values** :

S_OK     Method correctly executed. E_FAIL     Method execution failed.     Reasons of the failure are not given. E_IMPL     No implementation available for this method.  **See also:**      [CatPictureFormat](../DraftingInterfaces/enum_CatPictureFormat_54570.md) 
### Property **height**( ) As double

   Returns or sets the height of the drawing picture. The height, like any length, is measured in millimeters.

**Example:**      This example gets the height of the `MyPicture` drawing picture

```VBScript
     Height = MyPicture.height

```

### Property **ratioLock**( ) As boolean

   Returns or sets the ratioLock of the drawing picture. The ratioLock is a boolean value If ratioLock is True it means that the size must not be changed by command in a interactive session.But it does not avoid size modifications thru VBscript exec (height and width still available for modification).

**Example:**      This example sets the ratioLock of the `MyPicture` drawing picture to True

```VBScript
     MyPicture.ratioLock = True

```

### Property **width**( ) As double

   Returns or sets the width of the drawing picture. The width, like any length, is measured in millimeters.

**Example:**      This example gets the width of the `MyPicture` drawing picture

```VBScript
     Width = MyPicture.width

```

### Property **x**( ) As double

   Returns or sets the x coordinate of the drawing picture position. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the x coordinate of the position of the `MyPicture` drawing picture to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewXCoordinate = 5*25.4
     MyPicture.x =  NewXCoordinate

```

### Property **y**( ) As double

   Returns or sets the y coordinate of the drawing picture position. It is expressed with respect to the view coordinate system. This coordinate, like any length, is measured in millimeters.

**Example:**      This example sets the y coordinate of the position of the `MyPicture` drawing picture to 5 inches. You need first to convert the 5 inches into millimeters.

```VBScript
     NewYCoordinate = 5*25.4
     MyPicture.y =  NewYCoordinate

```

Methods

### Func **GetOriginalHeight**( ) As double

   Gets the original height of the drawing picture. The height, like any length, is measured in millimeters.

**Example:**      This example gets the original height of the `MyPicture` drawing picture

```VBScript
     Height = MyPicture.GetOriginalHeight()

```

### Func **GetOriginalWidth**( ) As double

   Gets the original width of the drawing picture. The width, like any length, is measured in millimeters.

**Example:**      This example gets the original width of the `MyPicture` drawing picture

```VBScript
     Width = MyPicture.GetOriginalWidth()

```