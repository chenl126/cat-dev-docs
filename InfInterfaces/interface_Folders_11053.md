# Folders (Collection)

**_The folders object belongs to a folder._**
It lists all the folders contained in the folder. It allows to retrieve [Folder](../InfInterfaces/interface_Folder_8034.md) objects.

## Methods

### Func **Item**(| long | `iNumber`) As [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)

   Returns a folder using its index or its name from the folder collection.

**Parameters:**

` iIndex`      The index or the name of the folder to retrieve from the collection of folders. As a numerics, this index is the rank of the folder in the collection. The index of the first folder in the collection is 1, and the index of the last folder is Count. As a string, it is the name you assigned to the folder using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved folder **Example:**      This example retrieves in `ThisFolder` the third folder, and it `ThatFolder` the folder named `MyFolder`. in the `TestFolders` folder collection.

```VBScript
     Dim ThisFolder As Folder
     Set ThisFolder = TestFolders.Item(3)
     Dim ThatFolder As Folder
     Set ThatFolder = TestFolders.Item("MyFolder")

```