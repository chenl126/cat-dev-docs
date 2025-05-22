# SchListOfLongs (Object)

**_Represent a non-persistant list of LONGs to be used with schematic IDLs._**

## Properties

### Property **Count**( ) As long (Read Only)

Returns the number of long integers in the list.

**Example:**      This example retrieves in `NumberOfLongs` the number of long integers currently gathered in `MyList`.

```VBScript
NumberOfLongs = MyList.Count

```

Methods

### Sub **Append**( long  `iLong`)

Adds an long integer to the end of the list.

**Parameters:**

` iLong`      The long integer to be added to the list.
**Example:**      The following example appends a long integer to the list.

```VBScript
Dim MInteger As Long
MInteger = 4
Dim MyList As SchListOfLongs
MyList.Append(MInteger)

```

### Func **Item**( long  `iIndex`) As long

Returns a long integer from its index in the list.

**Parameters:**

` iIndex`      The index of the first long integer in the collection is 1, and the index of the last long integer is Count.
**Returns:**      the retrieved long integer.  **Example:**      The following example returns in the third long integer in the list.

```VBScript
Dim MyLong As Integer
Dim MyList As SchListOfLongs
Set MyLong = SchListOfLongs.Item(2)

```

### Sub **RemoveByIndex**( long  `iIndex`)

Remove a long integer from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the long integer to be removed in the list.
**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
Dim MyList As SchListOfLongs
MyList.Remove(1)

```