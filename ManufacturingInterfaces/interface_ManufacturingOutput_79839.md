# ManufacturingOutput (Object)

**_Object that represents the output machining code._**

## Properties

### Property **Size**( ) As long (Read Only)

Returns the number of bytes written to this data output.

**Parameters:**

` oBytes`      The integer value of the number of bytes
Methods

### Sub **CloseStream**( )

Close the Stream.  
### Sub **DecrementTabulation**( long  `iTab`)

Decrement the tabulation of the current block of text by the specified number of characters.  
### Sub **EndBlock**( )

Specify that the Block is ended.  
### Sub **EndLine**( )

Specify that the line is ended.  
### Sub **Flush**( )

Flush all Data in the Stream.  
### Sub **IncrementTabulation**( long  `iTab`)

Increment the tabulation of the current block of text by the specified number of characters.  
### Sub **NewBlock**( )

Create a New Block in the underlying output stream.  
### Sub **NewLine**( )

Create a New Line in the underlying output stream.  
### Sub **SetBufferLength**( long  `iLines`)

Set the number of lines of the buffer before it will be flushed (default is 200).

**Parameters:**

` iLines`      The integer value of the number of lines

### Sub **write_Chars**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`)

Write the specified string to the underlying output stream.  
### Sub **write_Double**( double  `iVal`)

Write the specified double to the underlying output stream.  
### Sub **write_Long**( long  `iVal`)

Write the specified long to the underlying output stream.