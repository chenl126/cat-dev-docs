# ClashResults (Collection)

**_A collection of all ClashResult objects currently managed by the application._**

The results linked to a specification are not managed thru this collection (see [Clashes](../SpaceAnalysisInterfaces/interface_Clashes_10879.md) ).

The method `GetTechnologicalObject("ClashResults")` on the root product, allows you to retrieve this collection.

## Methods

### Func **AddFromXML**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`,  [CatClashImportType](../SpaceAnalysisInterfaces/enum_CatClashImportType_68774.md)  `iType`) As [CATIAClashResult](../SpaceAnalysisInterfaces/interface_ClashResult_26594.md)

Creates a ClashResult object from a XML file and adds it to the ClashResults collection.

**Parameters:**

` iPath`      The path of the XML file.
` iType`      The type of import.
**Returns:**      The created ClashResult  **Example:**      This example creates a new ClashResult in the `TheClashResults` collection.

```VBScript
   Dim NewClashResult As ClashResult
   Set NewClashResult = TheClashResults.AddFromXML("c:\tmp\sample.xml", CatClashImportTypeClashOnly)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAClashResult](../SpaceAnalysisInterfaces/interface_ClashResult_26594.md)

Returns a ClashResult object using its index or its name from the ClashResults collection.

**Parameters:**

` iIndex`      The index or the name of the ClashResult to retrieve from the collection of ClashResults. As a numerics, this index is the rank of the ClashResult in the collection. The index of the first ClashResult in the collection is 1, and the index of the last ClashResult is Count. As a string, it is the name you assigned to the ClashResult.
**Example:**      This example retrieves in `ThisClashResult` the ninth ClashResult, and in `ThatClashResult` the ClashResult named `ClashResult Of MyProduct` from the `TheClashResults` collection.

```VBScript
   Dim ThisClashResult As ClashResult
   Set ThisClashResult = TheClashResults.Item(9)
   Dim ThatClashResult As ClashResult
   Set ThatClashResult = TheClashResults.Item("ClashResult Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a ClashResult object from the ClashResults collection.

**Parameters:**

` iIndex`      The index or the name of the ClashResult to remove from the collection of ClashResults. As a numerics, this index is the rank of the ClashResult in the collection. The index of the first ClashResult in the collection is 1, and the index of the last ClashResult is Count. As a string, it is the name you assigned to the ClashResult.
**Example:**      The following example removes the tenth ClashResult and the ClashResult named `ClashResult Of MyProduct` from the `TheClashResults` collection.

```VBScript
   TheClashResults.Remove(10)
   TheClashResults.Remove("ClashResult Of MyProduct")

```