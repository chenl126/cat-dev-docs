# SchAppMultiImageMaster (Object)

**_Interface to manage the master object in the Multi-Image-Object concept._**

## Methods

### Sub **AppAddImage**(| [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md) | `iImage`)

   Add an image for this master object.

**Parameters:**

` iImage`      Pointer to the image to link this master to.

**Example:**

```VBScript
     Dim objThisIntf As SchAppMultiImageMaster
     Dim objImage As SchAppConnectable
      ...
     objThisIntf.AppAddImage objImage

```

### Sub **AppIsOKToCreateImage**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iImageDoc`,  boolean  `oBYes`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oNLSFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oNLSFileKeyToMessage`)

   Check if OK to create an image of this master object.

**Parameters:**

` iImageDoc`      Pointer to the document the image is in.
` oBYes`      TRUE if this object is valid to be the master of a MIO relationship.
` oNLSFileName`      File name for the NLS messages.
` oNLSFileKeyToMessage`      Message key to the application specific diagnostics.

**Example:**

```VBScript
     Dim objThisIntf As SchAppMultiImageMaster
     Dim objImageDoc As Document
     Dim bYes As boolean
     Dim strFileName As String
     Dim strFileKeyToMsg As String
      ...
     objThisIntf.AppIsOKToCreateImage objImageDoc,bYes,strFileName,strFileKeyToMsg

```

### Sub **AppListImages**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLFilter`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLImages`)

   List the images of this master object.

**Parameters:**

` iLFilter`      A list of image class names for filtering (can be NULL).
` oLUKImages`      A list of image pointers (a list of CATIASchAppMultiImage pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchAppMultiImageMaster
     Dim objLFilter As SchListOfBSTRs
     Dim objLImages As SchListOfObjects
      ...
     objThisIntf.AppListImages objLFilter,objLImages

```