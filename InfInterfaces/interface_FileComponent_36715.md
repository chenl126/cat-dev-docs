# FileComponent (Object)

**_Represents the file object._**
**Role** : The file object allows to manipulate files with UNIX and Windows. Use it instead of the one of Visual Basic to make portable macros. Its gives access to information about the file and can open a file as a [TextStream](../InfInterfaces/interface_TextStream_21990.md) object.

## Properties

### Property **ParentFolder**( ) As [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)

Returns or sets the parent folder of the file.

**Example:**      This example sets the folder `ParentFold` as parent of the file `TestFile`. This moves the file into `ParentFold`.

```VBScript
TestFile.ParentFolder=ParentFold

```

### Property **Path**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the full path of the file.

**Example:**      This example retrieves in `FilePath` the path of the File `TestFile`.

```VBScript
Dim FilePath As String
FilePath = TestFile.Path

```