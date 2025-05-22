# ManufacturingGeneratorData (Object)

**_Represents the manufacturing output stream object._**
This object contains the output stream generated for the output files (APT, etc.).

## Methods

### Sub **AddObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Adds an object to the output stream.

  * With buffer: V5R13 and next <=> AddObjectToGenerate
  * Without buffer: V5R12 and previous <=> AddObjectToGenerate
  * From buffer: Debug only

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateFromBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Adds an object to the output stream from the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateWithBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Adds an object to the output stream within the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToGenerateWithOutBuffer**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Adds an object to the output stream without the buffer.

**Parameters:**

` iObject`      The object to add

### Sub **AddObjectToModalValues**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Adds an object to the modal values manager only.

**Parameters:**

` iObject`      The object to add

### Sub **GetFT06Stream**( [CATIAManufacturingOutput](../ManufacturingInterfaces/interface_ManufacturingOutput_79839.md)  `oStream`)

Retrieves the FT06 stream.

**Parameters:**

` oStream`      The retrieved stream

### Sub **GetLastObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `oObject`)

Retrieves the last object to generate.

**Parameters:**

` oObject`      The retrieved object

### Sub **GetOutputStream**( [CATIAManufacturingOutput](../ManufacturingInterfaces/interface_ManufacturingOutput_79839.md)  `oStream`)

Retrieves the output stream.

**Parameters:**

` oStream`      The retrieved stream

### Sub **ResetAllModalValues**( )

Resets all modal values.  
### Sub **SetLastObjectToGenerate**( [CATBaseUnknown](../System/interface_CATBaseUnknown_40786.md)  `iObject`)

Sets the last Activity to generate.

**Parameters:**

` iObject`      The activity to generate