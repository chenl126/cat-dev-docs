# AnalysisImages (Collection)

**_The collection of analysis images._**

## Methods

### Func **Add**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iImageName`,| | [CATVariant](../System/typedef_CATVariant_20656.md) | `iHideExistingImages`,| | [CATVariant](../System/typedef_CATVariant_20656.md) | `iShowMesh`,| | [CATVariant](../System/typedef_CATVariant_20656.md) | `iDuplicate`) As [CATIAAnalysisImage](../CATAnalysisInterfaces/interface_AnalysisImage_35789.md)

   Creates a new image and adds it to the analysis image collection.

**Parameters:**

` iImageName`      The name of the image to create.
` iHideExistingImages`      To deactivate or not all the activated images before create the new image.
` iShowMesh`      To show or not the mesh image.
` iDuplicate`      To duplicate or not the new image, if same image already exists in collection of images.

**Returns:**      The created Analysis Image  **Example:**      This example create `ThisAnalysisImage` in the `analysisImages`analysis
images collection. The image to create is supposed to be a mesh deformed image.

```VBScript
     Dim ThisAnalysisImage As AnalysisImage
     Set ThisAnalysisImage = analysisImages.Add("Mesh_Deformed", True, False, False)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisImage](../CATAnalysisInterfaces/interface_AnalysisImage_35789.md)

   Returns an analysis image using its index or its name from the analysis images collection.

**Parameters:**

` iIndex`      The index or the name of the analysis image to retrieve from the collection of analysis images. This index is the rank of the analysis image in the collection. The index of the first analysis image in the collection is 1, and the index of the last analysis image is Count.

**Returns:**      The retrieved analysis image  **Example:**      This example retrieves in `ThisAnalysisImage` the third analysis image.

```VBScript
     Dim ThisAnalysisImage As AnalysisImage
     Set ThisAnalysisImage = analysisImages.Item(3)

```