# Files (Collection)

**_A collection of all the file objects in a folder._**
It lists all the files contained in the folder. It allows to retrieve [File](../InfInterfaces/interface_File_3552.md) objects.

## Methods

### Func **Item**(| long | `iNumber`) As [CATIAFile](../InfInterfaces/interface_File_3552.md)

   Returns a file using its index or its name from the file collection.

**Parameters:**

` iIndex`      The index or the name of the file to retrieve from the collection of files. As a numerics, this index is the rank of the file in the collection. The index of the first file in the collection is 1, and the index of the last file is Count. As a string, it is the name you assigned to the file using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved file **Example:**      This example retrieves in `ThisFile` the third file, and it `ThatFile` the file named `MyFile`. in the `TestFiles` file collection.

```VBScript
     Dim ThisFile As File
     Set ThisFile = TestFiles.Item(3)
     Dim ThatFile As File
     Set ThatFile = TestFiles.Item("MyFile")

```