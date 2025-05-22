# PspListOfBSTRs (Object)

**_Represents a collection of CATBSTR type of strings._**
**Role** : Collection of CATBSTR type of strings.

## Properties

### Property **Count**( ) As long (Read Only)

Returns the number of character strings in the list.

**Example:**      This example retrieves in `NumberOfStrings` the number of character strings currently gathered in `MyList`.

```VBScript
Dim NumberOfStrings As long
NumberOfStrings = MyList.Count

```

Methods

### Sub **Append**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iBSTR`)

Adds a character string to the end of the list.

**Parameters:**

` iBSTR`      The character string to be added to the list.
**Example:**      The following example appends a string to the list.

```VBScript
Dim MyList As PspListOfBSTRs
MyList.Append("MyString")

```

### Func **Item**( long  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns a character string from its index in the list.

**Parameters:**

` iIndex`      The index of the first character string in the collection is 1, and the index of the last character string is Count.
**Returns:**      the retrieved string.  **Example:**      The following example returns the third character string in the list.

```VBScript
Dim MyStr As String
Dim MyList As PspListOfBSTRs
MyStr = PspListOfBSTRs.Item(3)

```

### Sub **RemoveByIndex**( long  `iIndex`)

Remove a character string from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the character string to be removed in the list.
**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
Dim MyList As PspListOfBSTRs
MyList.Remove(2)

```