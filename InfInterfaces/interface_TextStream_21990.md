# TextStream (Object)

**_The textstream object allows to manage input and output for a text stream._**

## Properties

### Property **AtEndOfLine**(| ) As boolean (Read Only)

   Returns a boolean value which specifies if the index position in the stream is at a end of line.

**Example:**      This example retrieves in `EndLine` the end of line value for the TextStream `TestStream`.

```VBScript
     Dim EndLine As Boolean
     EndLine = TestStream.AtEndOfLine

```

### Property **AtEndOfStream**( ) As boolean (Read Only)

   Returns a boolean value which specifies if the index position in the stream is at a end of stream.

**Example:**      This example retrieves in `EndStream` the end of stream value for the TextStream `TestStream`.

```VBScript
     Dim EndStream As Boolean
     EndStream = TestStream.AtEndOfStream

```

Methods

### Sub **Close**( )

   Closes a text stream.

**Example:**      This example closes the TextStream `TestStream`

```VBScript
     TestStream.Close

```

### Func **Read**( long  `iNumOfChar`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns a string which contains a given number of characters from the current position in the stream.

**Parameters:**

` iNumOfChar`      The number of characters to read.

**Returns:**      oReadString The retrieved string.

**Example:**      This example retrieves the next fifty characters of the TextStream `TestStream` in the stream `ReadString`.

```VBScript
     Dim ReadString As String
     Set ReadString = TestStream.Read(50)

```

### Func **ReadLine**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns a string which contains a line of charaters from the current position in the stream.

**Returns:**      oReadLine The retrieved read line.

**Example:**      This example retrieves the next line of the TextStream `TestStream` in the stream `ReadString`.

```VBScript
     Dim ReadString As String
     Set ReadString = TestStream.ReadLine

```

### Sub **Write**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iWrittenString`)

   Writes a string in the text stream.

**Parameters:**

` iWrittenString`      The string to write in the stream.

**Example:**      This example write a string in the the TextStream `TestStream`.

```VBScript
     TestStream.Write("This is a test")

```