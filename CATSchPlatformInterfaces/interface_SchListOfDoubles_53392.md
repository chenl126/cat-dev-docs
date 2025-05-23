# SchListOfDoubles (Object)

**_Represents a list of DOUBLEs to be used with Schematic IDLs._**

## Properties

### Property **Count**(| ) As long (Read Only)

   Returns the number of doubles in the list.

**Example:**      This example retrieves in `NumberOfdoubles` the number of doubles currently gathered in `MyList`.

```VBScript
     NumberOfdoubles = MyList.Count

```

Methods

### Sub **Append**( double  `iDouble`)

   Adds a double to the end of the list.

**Parameters:**

` iDouble`      The double to be added to the list.

**Example:**      The following example appends an object to the list.

```VBScript
     Dim MyDouble As Double
     MyDouble = 0.6789
     Dim MyList As SchListOfDoubles
     MyList.Append(MyDouble)

```

### Func **Item**( long  `iIndex`) As double

   Returns a double from its index in the list.

**Parameters:**

` iIndex`      The index of the first double in the collection is 1, and the index of the last double is Count.

**Returns:**      the retrieved double.  **Example:**      The following example returns in the third double in the list.

```VBScript
     Dim MyDouble As double
     Dim MyList As SchListOfDoubles
     Set MyDouble = SchListOfDoubles.Item(2)

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Remove a double from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the double to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As SchListOfDoubles
     MyList.Remove(1)

```