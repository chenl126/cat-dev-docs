# File (Object)

**_Represents the file object._**
**Role** : The file object allows to manipulate files with UNIX and Windows. Use it instead of the one of Visual Basic to make portable macros. Its gives access to information about the file and can open a file as a [TextStream](../InfInterfaces/interface_TextStream_21990.md) object.

## Properties

### Property **Size**( ) As long (Read Only)

Returns the size of the file.

**Example:**      This example retrieves in `FileSize` the size of the File `TestFile`.

```VBScript
Dim FileSize As Long
FileSize = TestFile.Size

```

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the type of the file. For instance, if the file has a .txt or .doc extension, its type will be "Text Document".

**Example:**      This example retrieves in `FileType` the type of the File `TestFile`.

```VBScript
Dim FileType As String
FileSize = TestFile.Size

```

Methods

### Func **OpenAsTextStream**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMode`) As [CATIATextStream](../InfInterfaces/interface_TextStream_21990.md)

Opens the file and retrieves it as a TextSteam object. Paramater **iMode** can have the value "ForReading", "ForWriting" or "ForAppending".

**Example:**      This example opens the file `TestFile` for reading and retrieves in the text stream `TextStr`.

```VBScript
Dim TextStr As CATIATextSteam
Set TextStr = TestFile.OpenAsTextStream("ForReading")

```