# Shots (Collection)

**_The collection of all shot objects contained in the current sampled._**

## Methods

### Sub **Append**(| [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) | `iShot`)

   Adds a shot to the end of the shots collection.

**Parameters:**

` iShot`      The shot to be added  **Example:**      The following example adds a shot (called `myShot` to the shots collection.

```VBScript
     Shots.Append (myShot)

```

### Func **CreateShot**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Creates a new shot and adds it to the Shots collection.

**Returns:**      The created shot  **Example:**      The following example creates a shot `newShot` in the Shots collection.

```VBScript
     Dim newShot
     Set newShot = Shots.CreateShot

```

### Func **CreateSpecificShot**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Creates a new shot of a specific type and adds it to the Shots collection.

**Parameters:**

` iType`      Specifies the type of the shot to be created. The legal values are FITShotPoints, FITShotDouble, FITShotSimple and FITShotGeneric. These different types correspond to the need of creating different shots for different types of objects.

**Returns:**      The created Shot  **Example:**      The following example creates a shot `shot` in the Shots collection.

```VBScript
     Set newShots = Shots.CreateShot (FITSHOTDouble)

```

### Sub **InsertAfter**( short  `iIndex`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iShot`)

   Adds a shot to a specific location to the shots collection.

**Parameters:**

` iIndex`      The value of the location of an already existing shot. Then when inserting a new shot, it will be placed after it. It is a positive integer, with the range of 1 to the value of the last shot.
` iShot`      The shot to be added  **Example:**      The following example inserts a shot after the second shot.

```VBScript
     Shots.InsertAfter (2, myShot)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns a shot using its index from the colection.

**Parameters:**

` iIndex`      The index of the item to retrieve from the collection of shots. Numerically, the index value corresponds to the rank of the shot in the collection (ie. the first is 1, second is 2, ...).

**Returns:**      The retrieved Shot  **Example:**      The following example retrieves the second shot from the Shots collection.

```VBScript
     Dim myShot
     Set myShot = myShots.Item (2)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a shot from the collection.

**Parameters:**

` iIndex`      The index of the shot to remove from the collection of the shots. Numerically, the index value corresponds to the rank of the shot in the collection (ie. the first is 1, second is 2, ...).  **Example:**      The following example removes the third shot from the Shots collection of the active document.

```VBScript
     Shots.Remove (3)

```