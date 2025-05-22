# Documents (Collection)

**_A collection of all the Document objects currently managed by the application._**
These documents belong to one of the following types: PartDocument, ProductDocument, and Drawing.

**See also:**      [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md), [ProductDocument](../ProductStructureInterfaces/interface_ProductDocument_49026.md), [DrawingDocument](../DraftingInterfaces/interface_DrawingDocument_48585.md)

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `docType`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Creates a Document object and adds it to the documents collection. This document becomes the active one, and a window is created to accomodate it which becomes the active window.

**Parameters:**

` docType`      The type of the document to create, chosen among:

Part     For PartDocument Product     For ProductDocument Drawing     For Drawing
**Returns:**      The created document  **Example:**      The following example creates a PartDocument document in the collection retrieved in `PartDoc`.

```VBScript
Dim PartDoc As Document
Set PartDoc = Documents.Add("Part")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Returns a document using its index or its name from the documents collection.

**Parameters:**

` iIndex`      The index or the name of the document to retrieve frm the collection of documents. As a numerics, this index is the rank of the document in the collection. The index of the first document in the collection is 1, and the index of the last document is Count. As a string, it is the name you assigned to the document using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved document **Example:**      This example retrieves in `ThisDoc` the fifth document in the collection and in `ThatDoc` the document named `MyDoc`.

```VBScript
Dim ThisDoc As Document
Set ThisDoc = Documents.Item(5)
Dim ThatDoc As Document
Set ThatDoc = Documents.Item("MyDoc")

```

### Func **NewFrom**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Creates a new document from a document stored in a file. **Role** : Reads a document stored in a file and creates a new document containing the resulting data, adds the new document to the document collection, displays it in a new window, adds the window to the window collection and activates both the document and the window.

**Parameters:**

` The`      name of the file containing the document.
**Returns:**      The created document. **Example:**      The following example creates a new `Doc` document from the contents of the `FileToRead` file.

```VBScript
FileToRead = "e:\users\psr\Parts\ThisIsANicePart.CATPart"
Dim Doc As Document
Set Doc = Documents.NewFrom(FileToRead)

```

### Func **Open**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Opens a document stored in a file. Reads a document stored in a file, displays it in a new window, adds the document to the documents collection and the window to the windows collection, and makes both the document and the window the active ones.

**Parameters:**

` iFileName`      The name of the file containing the document
**Returns:**      The retrieved document **Example:**      The following example opens the `Doc` document contained in the `FileToOpen` file.

```VBScript
FileToOpen = "e:\users\psr\Parts\ThisIsANicePart.CATPart"
Dim Doc As Document
Set Doc = Documents.Open(FileToOpen)

```

### Func **Read**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Reads a document stored in a file. This method has to be used only for Browse purpose, for instance to retrieve Product properties. Be careful, it doesn't open any editor (no visualization, no undo/redo capabilities...) As soon as you want to modify the V5 document, you have to use the VB Open method collection. If this solution is not satisfactory because it opens an editor for every document, you have to move to C++ and use the CAA methods CATDocumentServices::Open and CATDocumentServices::SaveAs with the same file name as the initial one.

**Parameters:**

` iFileName`      The name of the file containing the document
**Returns:**      The retrieved document **Example:**      The following example reads the `Doc` document contained in the `FileToOpen` file.

```VBScript
FileToOpen = "e:\users\psr\Parts\ThisIsANicePart.CATPart"
Dim Doc As Document
Set Doc = Documents.Read(FileToOpen)

```