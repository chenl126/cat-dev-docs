# SchAppMultiImage (Object)

**_Interface to manage the image object in the Multi-Image-Object concept._**

## Methods

### Sub **AppGetMasterDocument**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `oDocument`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oDocumentName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oSymbolicLinkName`)

Get the document where the master of this image object resides.

**Parameters:**

` oDocument`      Pointer to the document.
` oDocumentName`      Name of the document containing the master.
` oSymbolicLinkName`      Name of the symbolic link.
**Example:**

```VBScript
Dim objThisIntf As SchAppMultiImage
Dim objDoc As Document
Dim strDocName As String
Dim strLinkName As String
 ...
objThisIntf.AppGetMasterDocument objDoc,strDocName,strLinkName

```

### Func **AppGetMasterObject**( ) As [CATIASchAppMultiImageMaster](../CATSchPlatformInterfaces/interface_SchAppMultiImageMaster_100118.md)

Get the master object of this image.

**Parameters:**

` oMasterImage`      Pointer to the master object.
**Example:**

```VBScript
Dim objThisIntf As SchAppMultiImage
Dim objMaster As SchMultiImageMaster
 ...
Set objMaster = objThisIntf.AppGetMasterObject

```

### Sub **AppIsUpToDate**( [CatSchIDLMultiImageStatus](../CATSchPlatformInterfaces/enum_CatSchIDLMultiImageStatus_126769.md)  `oStatus`)

Check if the image object is up-to-date.

**Parameters:**

` oStatus`      Status of the image object.
**Example:**

```VBScript
Dim objThisIntf As SchAppMultiImage
 ...
objThisIntf.AppIsUpToDate CatSchIDLMultiImageStatus_Enum

```

### Sub **AppUpdate**( [CATIASchAppMultiImageMaster](../CATSchPlatformInterfaces/interface_SchAppMultiImageMaster_100118.md)  `iMasterImage`,  [CATIASchAppMultiImage](../CATSchPlatformInterfaces/interface_SchAppMultiImage_52614.md)  `oImage`)

Update the image object.

**Parameters:**

` iMasterImage`      This is an optional input. Not NULL - the application has a handle on the master to update this image (for example in DSA application, the application will make sure the ID of this image is the same as the input master). NULL - the application will find the master based on the specific way it models the MIO concept. Sample case: the application will make sure the ID of this image is the same as the input master.
` oImage`      Pointer to a new image object created if existing image object has to be replaced during the update process. This pointer is NULL if the image object is not replaced.
**Example:**

```VBScript
Dim objThisIntf As SchAppMultiImage
Dim objMaster As SchAppMultiImageMaster
Dim objNewImage As SchAppMultiImage
 ...
objThisIntf.AppUpdate objMaster,objNewImage

```