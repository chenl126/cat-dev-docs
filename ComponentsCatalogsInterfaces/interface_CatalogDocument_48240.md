# CatalogDocument (Object)

**_Represents the Document object for catalog._**
**Role** : A catalog document references data (documents: CATPart..., features, etc) organized as a tree: the nodes are called chapters and the leaves are called descriptions. Each description may reference a document (CATPart...) and couples of keyword + value. The keywords are defined at the parent chapter level.
A catalog may reference parametric Parts. In that case, the Part is associated with a Design Table. A Design Table is a file (text file, Excel document) that contains named columns and rows. Each row corresponds to a description, and each column may correspond to a keyword.
Refer to CATIA V5 Documentation, Component Catalog Editor and to CAA V5 Encyclopedia, Document, Catalog.

## Methods

### Sub **CreateCatalogFromLibrary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLibraryPath`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProjectPath`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCatalogPath`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTablePath`,  short  `iConvFormat`,  short  `iBatchMode`)

Creates a catalog from a V4 library.

**Parameters:**

` iLibraryPath`      The V4 library path.
` iProjectPath`      The V4 project path.
` iCatalogPath`      The new catalog path.
` iTablePath`      The mapping table path.
` iConvFormat`      `0`: As Specification
`1`: As Result
` iBatchMode`      `0`: As Specification
`1`: As Result
` iBatchMode`      `0`: Create the V5 documents
`1`: Simulate: the V5 documents are not created
`2`: If the previous migration has failed, continue since this point.

### Sub **CreateCatalogFromcsv**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInitData`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNewCatalog`)

Creates a catalog from a csv file.
Refer to CATIA V5 Documentation, Component Catalog Editor, Creating a Catalog in Batch Mode.

**Parameters:**

` iInitData`      The csv (Comma Separated Values) file path.
` iNewCatalog`      The new catalog path.

**Example:**      This example creates a catalog from a csv file.

```VBScript
  InputFile ="E:\users\Catalogs\BatchCatalog.csv"
  OutputFile ="E:\users\Catalogs\Catalog_Result.catalog"
  Dim Catalog As Document
  Set Catalog=CATIA.Documents.Add("CatalogDocument")
  Catalog.CreateCatalogFromcsv InputFile, OutputFile

```

### Sub **CreateChapterFromDesignTable**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iChapterName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentContainingDT`)

Creates a chapter in the current catalog document where keywords correspond to parameters of the Design Table and add the descriptions corresponding to whole configurations of the Design Table.
Refer to CATIA V5 Documentation, Component Catalog Editor, Creating a Catalog in Batch Mode.

**Parameters:**

` iChapterName`      The name of the new chapter.
` iDocumentContainingDT`      The path of the Design Table.

**Example:**      This example creates a catalog and a chapter is added from a Design Table.

```VBScript
  Chapter = "NewChapter"
  DTFile ="E:\users\Catalogs\DesignTable.xls"
  Dim Catalog As Document
  Set Catalog=CATIA.Documents.Add("CatalogDocument")
  Catalog.CreateChapterFromDesignTable Chapter, DTFile

```