# Folder (Object)

**_Represents the folder object._**
It allows you to manipulate folders and gives access to information about them.

## Properties

### Property **Files**(| ) As [CATIAFiles](../InfInterfaces/interface_Files_5661.md) (Read Only)

   Returns the file collection of the folder.

**Example:**      This example retrieves in `TestFiles` the file collection of the folder `TestFolder`.

```VBScript
     Dim TestFiles As Files
     Set TestFiles = TestFolder.Files

```

### Property **SubFolders**( ) As [CATIAFolders](../InfInterfaces/interface_Folders_11053.md) (Read Only)

   Returns the folder collection of the folder.

**Example:**      This example retrieves in `TestSubFolders` the folder colection of the folder `TestFolder`.

```VBScript
     Dim TestSubFolders As CATIAFolders
     Set TestSubFolders = TestFolder.SubFolders

```