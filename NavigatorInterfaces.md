# NavigatorInterfaces Framework

## Object Index

  * [AnnotatedView](NavigatorInterfaces/interface_AnnotatedView_36411.md)
  * [AnnotatedViews](NavigatorInterfaces/interface_AnnotatedViews_42578.md)
  * [DMUDataFlow](NavigatorInterfaces/interface_DMUDataFlow_24296.md)
  * [Group](NavigatorInterfaces/interface_Group_5945.md)
  * [Groups](NavigatorInterfaces/interface_Groups_8540.md)
  * [Hyperlink](NavigatorInterfaces/interface_Hyperlink_18250.md)
  * [Hyperlinks](NavigatorInterfaces/interface_Hyperlinks_22650.md)
  * [Marker2D](NavigatorInterfaces/interface_Marker2D_12072.md)
  * [Marker2Ds](NavigatorInterfaces/interface_Marker2Ds_15905.md)
  * [Marker3D](NavigatorInterfaces/interface_Marker3D_12094.md)
  * [Marker3Ds](NavigatorInterfaces/interface_Marker3Ds_15928.md)
  * [MarkerSettingAtt](NavigatorInterfaces/interface_MarkerSettingAtt_54542.md)
  * [N4DNavigatorSettingAtt](NavigatorInterfaces/interface_N4DNavigatorSettingAtt_100038.md)
  * [NavigatorWorkbench](NavigatorInterfaces/interface_NavigatorWorkbench_69502.md)

## Enumerated Types Index

  * [CatAnnotatedViewBehavior](NavigatorInterfaces/enum_CatAnnotatedViewBehavior_120528.md)
  * [CatDMUGroupPreviewHiddenObjectsDisplayMode](NavigatorInterfaces/enum_CatDMUGroupPreviewHiddenObjectsDisplayMode_359864.md)
  * [CatMarker2DType](NavigatorInterfaces/enum_CatMarker2DType_44552.md)
  * [CatMarker3DType](NavigatorInterfaces/enum_CatMarker3DType_44587.md)
  * [CatMarkerTextOrientation](NavigatorInterfaces/enum_CatMarkerTextOrientation_123088.md)
  * [CatSacSettingsEnum](NavigatorInterfaces/enum_CatSacSettingsEnum_68200.md)

---

# CatAnnotatedViewBehavior (Enumeration)

**_The different behavior of annotated view_**

**See also:**      [AnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md) **Values:**

` CatAnnotatedViewBehaviorLink`      The annotated view is linked to the viewpoint.
` CatAnnotatedViewBehaviorUnlink`      The annotated view is notlinked to the viewpoint. Viewpoint modification will not alter the annotared view.

---

# CatDMUGroupPreviewHiddenObjectsDisplayMode (Enumeration)

**_The different modes for the display of hidden objects in DMU Group Preview._**

**See also:**      [N4DNavigatorSettingAtt](../NavigatorInterfaces/interface_N4DNavigatorSettingAtt_100038.md) **Values:**

` ShowHidden`      Hidden objects are visualized as in main 3D viewer.
` ShowHiddenCustom`      Hidden objects are visualized with customized graphic properties.

---

# CatMarker2DType (Enumeration)

**_The different types of Marker2Ds_**

**See also:**      [Marker2D](../NavigatorInterfaces/interface_Marker2D_12072.md) **Values:**

` catMarker2DTypeLine`      The marker is a line between two points.
` catMarker2DTypeArrow`      The marker is an arrow between two points.
` catMarker2DTypeRectangle`      The marker is a rectangle between two points.
` catMarker2DTypeCircle`      The marker is a circle centered on a first point and lying on a second point.
` catMarker2DTypeFreeHand`      The marker is a curve along a series of points.
` catMarker2DTypeText`      The marker is a text on a point.
` catMarker2DTypePicture`      The marker is a picture between two points.

---

# CatMarker3DType (Enumeration)

**_The different types of Marker3Ds_**

**See also:**      [Marker3D](../NavigatorInterfaces/interface_Marker3D_12094.md) **Values:**

` catMarker3DTypeText`      The marker is a text on a collection of objects.

---

# CatMarkerTextOrientation (Enumeration)

**_The different orientations of a text Marker2D or Marker3D._**

**See also:**      [Marker2D](../NavigatorInterfaces/interface_Marker2D_12072.md) **See also:**      [Marker3D](../NavigatorInterfaces/interface_Marker3D_12094.md) **Values:**

` CatMarkerTextOrientationRight`      The texte is written left to right.
` CatMarkerTextOrientationUp`      The texte is written top to bottom.
` CatMarkerTextOrientationLeft`      The texte is written right to left.
` CatMarkerTextOrientationDown`      The texte is written bottom to top.

---

# CatSacSettingsEnum (Enumeration)

**_The different types for the Import Data settings._**

**See also:**      [N4DNavigatorSettingAtt](../NavigatorInterfaces/interface_N4DNavigatorSettingAtt_100038.md) **Values:**

` NoInsert`      Import applicative data not available when inserting existing component.
` Automatic`      Import of applicative data is automatically done when inserting existing component.
` UserPrompt`      Import of applicative data is done with user selection.

---

# AnnotatedView (Object)

**_Represents an annotated view._**

## Properties

### Property **BehaviorMode**( ) As [CatAnnotatedViewBehavior](../NavigatorInterfaces/enum_CatAnnotatedViewBehavior_120528.md)

   Returns or sets the behavior mode of the annotated view. This behavior mode enables the annotated view to be independant from the viewpoint.

**Example:**      This example retrieves the behavior mode of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Mode
        Mode = NewAnnotatedView.BehaviorMode

```

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the comment associated with the annotated view.

**Example:**      This example retrieves the comment of `NewAnnotatedView` annotated view.

```VBScript
        Dim text As String
        text = NewAnnotatedView.Comment

```

### Property **FieldOfView**( ) As double (Read Only)

   Returns the field of view associated with the annotated view. The field of view is half of the vertical angle of the viewpoint, expressed in degrees. This property exists with the perspective (conic) projection mode only.

**Example:**      This example retrieves the field of view` of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Field As Double
        Field = NewAnnotatedView.FieldOfView

```

### Property **Marker2Ds**( ) As [CATIAMarker2Ds](../NavigatorInterfaces/interface_Marker2Ds_15905.md) (Read Only)

   Returns the Marker2D Collection associated with the annotated view.

**Example:**      This example retrieves the `TheMarker2Ds` collection from the `NewAnnotatedView` annotated view.

```VBScript
        Dim TheMarker2Ds As AnnotatedView
        Set TheMarker2Ds = NewAnnotatedView.Marker2Ds(9)

```

### Property **ProjectionMode**( ) As [CatProjectionMode](../InfInterfaces/enum_CatProjectionMode_60760.md) (Read Only)

   Returns the projection mode of the annotated view. This projection mode is the one of the associated 3D View point.

**Example:**      This example retrieves the projection mode of the `NewAnnotatedView` annotated view.

```VBScript
        Dim Mode
        Mode = NewAnnotatedView.ProjectionMode

```

### Property **Sound**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path of the sound file associated with the annotated view.

**Parameters:**

` iPath`      The path of the sound file. If this path is not empty, the sound replaces the old associated one (if it exists) or creates a new association (if not). If this path is empty, the sound is removed.

**Returns:**      The path of the sound file. If this path is empty, the annotated view has no associated sound.  **Example:**      This example retrieves the path of the sound file associated with the `NewAnnotatedView` annotated view.

```VBScript
        Dim path As String
        path = NewAnnotatedView.Sound

```

### Property **Zoom**( ) As double (Read Only)

   Returns the zoom factor associated with the annotated view. This property exists with the parallel (cylindric) projection mode only. This zoom factor is the one of the associated 3D View point.

**Example:**      This example retrieves in `ZoomFactor` the zoom of the `NewAnnotatedView` annotated view.

```VBScript
        Dim ZoomFactor As Double
        ZoomFactor = NewAnnotatedView.Zoom

```

Methods

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Retrieves the coordinates of the origin of the 3D viewpoint of the annotated view.

**Parameters:**

` oOrigin`      The coordinates of the view point origin expressed as an array of 3 variants are:

  * oOrigin(0) is the X coordinate of the origin
  * oOrigin(1) is the Y coordinate of the origin
  * oOrigin(2) is the Z coordinate of the origin

**Example:**      This example retrieves the origin of the 3D viewpoint of the `NewAnnotatedView` annotated view.

```VBScript
        Dim origin(2)
        NewAnnotatedView.GetOrigin origin

```

### Sub **GetSightDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSight`)

   Retrieves the components of the sight direction of the 3D viewpoint of the annotated view. The sight direction is the line that passes by the origin of the viewpoint and by the target.

**Parameters:**

` oSight`      The components of the viewpoint sight direction expressed as an array of 3 variants are:

  * oSight(0) is the X component of the sight direction
  * oSight(1) is the Y component of the sight direction
  * oSight(2) is the Z component of the sight direction

**Example:**      This example retrieves the sight direction of the `NewAnnotatedView` annotated view.

```VBScript
        Dim sight(2)
        NewAnnotatedView.GetSightDirection sight

```

### Sub **GetUpDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oUp`)

   Retrieves the components of the up direction of the 3D viewpoint of the annotated view.

**Parameters:**

` oUp`      The components of the viewpoint up direction expressed as an array of 3 variants are:

  * oUp(0) is the X component of the up direction
  * oUp(1) is the Y component of the up direction
  * oUp(2) is the Z component of the up direction

**Example:**      This example retrieves the up direction of the `NewAnnotatedView` annotated view.

```VBScript
        Dim up(2)
        NewAnnotatedView.GetUpDirection up

```

### Sub **Update**( )

   Updates the annotated view: that is to take into account all modifications which occur since last update.

**Example:**      This example updates the `NewAnnotatedView` annotated view.

```VBScript
        NewAnnotatedView.Update

```

---

# AnnotatedViews (Collection)

**_A collection of AnnotatedView objects._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("AnnotatedViews")` on the root product retrieves this collection.

## Methods

### Func **Add**( ) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Creates an annotated view using the current viewpoint and adds it to the AnnotatedView collection.

**Returns:**      The created AnnotatedView  **Example:**      This example creates a new AnnotatedView in the `TheAnnotatedViews` collection.

```VBScript
        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add

```

### Func **AddFromViewpoint**( [CATIAViewpoint3D](../InfInterfaces/interface_Viewpoint3D_24360.md)  `iViewpoint`) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Creates an annotated view using a given viewpoint and adds it to the AnnotatedView collection.

**Parameters:**

` iViewpoint`      The viewpoint.

**Returns:**      The created AnnotatedView  **Example:**      This example creates a new AnnotatedView in the `TheAnnotatedViews` collection using a `AViewpoint` viewpoint object.

```VBScript
        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.AddFromViewpoint(AViewpoint)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)

   Returns an annotated view using its index or its name from the AnnotatedViews collection.

**Parameters:**

` iIndex`      The index or the name of the AnnotatedView to retrieve from the collection of AnnotatedViews. As a numerics, this index is the rank of the AnnotatedView in the collection. The index of the first AnnotatedView in the collection is 1, and the index of the last AnnotatedView is Count. As a string, it is the name you assigned to the AnnotatedView.

**Returns:**      The retrieved AnnotatedView  **Example:**      This example retrieves in `ThisAnnotatedView` the ninth AnnotatedView, and in `ThatAnnotatedView` the AnnotatedView named `AnnotatedView3` from the `TheAnnotatedViews` collection.

```VBScript
        Dim ThisAnnotatedView As AnnotatedView
        Set ThisAnnotatedView = TheAnnotatedViews.Item(9)
        Dim ThatAnnotatedView As AnnotatedView
        Set ThatAnnotatedView = TheAnnotatedViews.Item("AnnotatedView3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an annotated view from the AnnotatedViews collection.

**Parameters:**

` iIndex`      The index or the name of the AnnotatedView to retrieve from he collection of AnnotatedViews. As a numerics, this index is the rank of the AnnotatedView in the collection. The index of the first AnnotatedView in the collection is 1, and the index of the last AnnotatedView is Count. As a string, it is the name you assigned to the AnnotatedView.

**Example:**      The following example removes the tenth AnnotatedView and the AnnotatedView named `AnnotatedView2` from the `TheAnnotatedViews` collection.

```VBScript
        TheAnnotatedViews.Remove(10)
        TheAnnotatedViews.Remove("AnnotatedView2")

```

---

# DMUDataFlow (Object)

**_Allows the DMU Data Flow Management within the DMU Navigator environment._**

## Methods

### Sub **CacheExport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`,  long  `iData`)

   Exports all documents related to the product in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.
` iData`      To save geometries.

  * 0: no save.
  * 1: save.

### Sub **CacheImport**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`)

   Imports in the cache of marked documents in a directory.

**Parameters:**

` iDirectory`      The directory that contains marked documents.

### Sub **Collapse**( )

   Collapse the product by replacing all sub-product by corresponding components.  
### Sub **ReplaceByCGR**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`)

   Replaces all components of the product by the corresponding CGR located in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.

### Sub **SaveAsFrozen**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDirectory`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPrefix`,  long  `iData`,  long  `iCache`)

   Saves all documents related to the product in a directory.

**Parameters:**

` iDirectory`      The directory that will contain documents.
` iPrefix`      The prefix used to save product documents.
` iData`      To save geometries.

  * 0: no save.
  * 1: save.

` iCache`      To cache data.

  * 0: no save.
  * 1: save.

---

# Group (Object)

**_Represents a DMU group._**
The DMU group is an entity which gathers references to several products in order to automate validation and verification of the Digital Mock-Up.

A user can build a group using several methods: explicitely point out some products or take all products by default. The designated products can be intermediate or terminal node of the product structure. For instance, a user who has to verify the integration of the engine in engine bay may define a group with the engine assembly or with all the parts from the engine in order to detect clashes. In the first case this user has to add the engine assembly (as a product) in the group, and in the second case, to add all the parts to the group. Obviously, when a modification happens to the engine assembly the user has to change the group only in the second case. To manage the explicit definition of the group, one may use the `XxxxExplicit` methods.

When the system takes the group into account to perform a given task, it may be necessary to retrieve:

  * The products designated by the user (For example, the section of these products)
  * The terminal nodes (or leaves) of the product (For example, clash detection takes into account terminal nodes)
  * The set of products in the product structure which are not selected (For example, hide all products which are not in the group)
  * The set of terminal nodes which are not selected (For example, clash of some products against all others).
To perform these treatments one may use `YyyyExtract` or `ZzzzInvert` methods.

## Properties

### Property **ExtractMode**( ) As long

   Returns or sets the mode for the extraction methods.

**Returns:**      The extraction mode

  * 0: the extraction provides the products from the group (intermediate of terminal nodes).
  * 1: the extraction provides terminal nodes of the products from the group.

**Example:**      This example retrieves the extraction mode of the `NewGroup` Group and sets it to 1.

```VBScript
        Dim Mode As Integer
        Mode = NewGroup.ExtractMode
        NewGroup.ExtractMode = 1

```

Methods

### Sub **AddExplicit**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iProduct`)

   Adds a product to the group.

**Parameters:**

` iProduct`      The product to add

**Example:**      This example adds the product `MyProduct` to the group `NewGroup`.

```VBScript
        NewGroup.AddExplicit MyProduct

```

### Func **CountExplicit**( ) As long

   Returns the number of products in the group.

**Example:**      This example retrieves the number of products in the group `NewGroup`.

```VBScript
        Dim number As Integer
        number = NewGroup.CountExplicit

```

### Func **CountExtract**( ) As long

   Returns the number of products which can be extracted from the group. Depending on the extraction mode, the extracted products can be:

  * Mode = 0: the products from the group (intermediate or terminal nodes).
  * Mode = 1: the terminal nodes of the products from the group.

**Returns:**      The number of products  **Example:**      This example reads the number of products in the group `NewGroup`.

```VBScript
        Dim number As Integer
        number = NewGroup.CountExtract

```

### Func **CountInvert**( ) As long

   Returns the number of terminal node products which cannot be extracted from the group.

**Example:**      This example retrieves the number of terminal node products which cannot be extracted from the group `NewGroup`.

```VBScript
        Dim number As Integer
        number = NewGroup.CountInvert

```

### Sub **FillSelWithExtract**( )

   Fills the selection with all products which can be extracted from the group.

**Example:**      This example fills the selection with products which can be extracted from the `NewGroup` group.

```VBScript
        NewGroup.FillSelWithExtract

```

### Sub **FillSelWithInvert**( )

   Fills the selection with all terminal node products which cannot be extracted from the group.

**Example:**      This example fills the selection with all products which cannnot be extracted from the `NewGroup` group.

```VBScript
        NewGroup.FillSelWithInvert

```

### Func **ItemExplicit**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns a product using its index in the group.

**Parameters:**

` iIndex`      The index of the product in the group. The index of the first product is 1, and the index of the last product is CountExplicit.

**Returns:**      The retrieved product  **Example:**      This example retrieves in `ThisProduct` the ninth product from the `NewGroup` group.

```VBScript
        Dim ThisProduct As Product
        Set ThisProduct = NewGroup.ItemExplicit(9)

```

### Func **ItemExtract**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns a product which can be extracted from the group using its index.

**Parameters:**

` iIndex`      The index of the product in the group. The index of the first product is 1, and the index of the last product is CountExtract.

**Returns:**      The retrieved product  **Example:**      This example retrieves in `ThisProduct` the ninth product from the `NewGroup` group.

```VBScript
        Dim ThisProduct As Group
        Set ThisProduct = NewGroup.ItemExtract(9)

```

### Func **ItemInvert**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns a terminal node product which cannot be extracted from the group using its index.

**Parameters:**

` iIndex`      The index of the product in the group. The index of the first product is 1, and the index of the last product is CountExtract.

**Returns:**      The retrieved product  **Example:**      This example retrieves in `ThisProduct` the ninth product which cannot be extracted from the `NewGroup` group.

```VBScript
        Dim ThisProduct As Group
        Set ThisProduct = NewGroup.ItemInvert(9)

```

### Sub **RemoveExplicit**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a product from the group using its index.

**Parameters:**

` iIndex`      The index of the product in the group. The index of the first product is 1, and the index of the last product is CountExplicit.

**Example:**      The following example removes the tenth product from the `NewGroup` group.

```VBScript
        NewGroup.RemoveExplicit 10

```

---

# Groups (Collection)

**_A collection of all groups currently managed by the application._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("Groups")` on the root product retrieves this collection.

## Methods

### Func **Add**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Creates an empty Group and adds it to the Groups Collection.

**Returns:**      The created group  **Example:**      This example creates a new group in the `TheGroups` collection.

```VBScript
        Dim NewGroup As Group
        Set NewGroup = TheGroups.Add

```

### Func **AddFromSel**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Creates a Group containing all products in the selection and adds it to the Groups Collection.

**Returns:**      The created group  **Example:**      This example creates a new group containing all products in the selection in the `TheGroups` collection.

```VBScript
        Dim NewGroup As Group
        Set NewGroup = TheGroups.AddFromSel

```

### Func **AllLeaves**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns a group which contains all the terminal nodes of the current root product.

**Example:**      This example retrieves the group in the `TheGroups` collection.

```VBScript
        Dim AllLeavesGroup As Group
        Set AllLeavesGroup = TheGroups.AllLeaves

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns a group using its index or its name from the Groups collection.

**Parameters:**

` iIndex`      The index or the name of the Group to retrieve from the collection of groups. As a numerics, this index is the rank of the Group in the collection. The index of the first Group in the collection is 1, and the index of the last Group is Count. As a string, it is the name you assigned to the Group.

**Returns:**      The retrieved Group  **Example:**      This example retrieves in `ThisGroup` the ninth Group, and in `ThatGroup` the Group named `Group3` from the `TheGroups` collection.

```VBScript
        Dim ThisGroup As Group
        Set ThisGroup = TheGroups.Item(9)
        Dim ThatGroup As Group
        Set ThatGroup = TheGroups.Item("Group3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a group from the Groups collection.

**Parameters:**

` iIndex`      The index or the name of the Group to retrieve from he collection of groups. As a numerics, this index is the rank of the Group in the collection. The index of the first Group in the collection is 1, and the index of the last Group is Count. As a string, it is the name you assigned to the Group.

**Example:**      The following example removes the tenth Group and the Group named `Group2` from the `TheGroups` collection.

```VBScript
        TheGroups.Remove(10)
        TheGroups.Remove("Group2")

```

---

# Hyperlink (Object)

**_Represents a hyperlink marker._**

## Methods

### Sub **AddUrl**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iUrl`)

   Adds a url to an Hyperlink.

**Parameters:**

` iUrl`      The URL to be added to the Hyperlink.

**Example:**      This example links `TheUrl` to the `NewHyperlink` Hyperlink.

```VBScript
        NewHyperlink.AddUrl(TheUrl)

```

### Func **CountObject**( ) As long

   Returns the number of Url which are linked to the Hyperlink.

**Example:**      This example reads the number of Url in the Hyperlink `NewHyperlink `.

```VBScript
        Dim number As Integer
        number = NewHyperlink.CountObject

```

### Func **ItemObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns an Url which is linked to the Hyperlink using its index.

**Parameters:**

` iIndex`      The index of the Url in the Hyperlink. The index of the first object is 1, and the index of the last object is CountObject.

**Returns:**      The retrieved Url  **Example:**      This example retrieves in `ThisUrl` the ninth object from the `NewHyperlink ` Hyperlink.

```VBScript
        Dim ThisUrl As String
        Set ThisUrl = NewHyperlink.ItemObject(9)

```

### Sub **RemoveObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an Url which is linked to the Hyperlink using its index.

**Parameters:**

` iIndex`      The index of the object in the Hyperlink. The index of the first object is 1, and the index of the last object is CountObject.

**Example:**      This example removes the ninth Url from the `NewHyperlink ` Hyperlink.

```VBScript
        NewHyperlink.RemoveObject(9)

```

---

# Hyperlinks (Collection)

**__**

## Methods

### Func **Add**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Adds a Hyperlink to the Hyperlinks collection. Be careful: only one Hyperlink instance is allowed per object which supports the hyperlink. If one adds a Hyperlink on an object which already has a Hyperlink, the call fails. The Hyperlink name is internally generated. If one wants to manage Hyperlink using its name, he has to set it manually.

**Parameters:**

` iObject`      The object which supports the hyperlink.

**Example:**      The following example adds a Hyperlink

```VBScript
        Dim NewHyperlink As Hyperlink
        Set NewHyperlink = TheHyperlinks.Add(iObject)

```

### Func **GetHyperlink**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Retrieve an Hyperlink associated to an object

**Parameters:**

` iObject`      The object which supports the hyperlink. The call fails otherwise.

**Returns:**      The retrieved Hyperlink if it exists  **Example:**      This example retrieves an existing one in the `TheHyperlinks` collection.

```VBScript
        Dim NewHyperlink As Hyperlink
        Set NewHyperlink = TheHyperlinks.GetHyperlink(iObject)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHyperlink](../NavigatorInterfaces/interface_Hyperlink_18250.md)

   Returns an Hyperlink using its index from the Hyperlinks collection.

**Parameters:**

` iIndex`      The index or the name of the hyperlink to retrieve from the collection of Hyperlinks. As a numerics, this index is the rank of the Hyperlink in the collection. The index of the first Hyperlink in the collection is 1, and the index of the last Hyperlink is Count. As a string, it is the name you assigned to the Hyperlink.

**Returns:**      The retrieved Hyperlink  **Example:**      This example retrieves in `ThisHyperlink` the ninth Hyperlink , and in `ThatHyperlink` the Hyperlink named ` Hyperlink3` from the `TheHyperlinks` collection.

```VBScript
        Dim ThisHyperlink As Hyperlink
        Set ThisHyperlink = TheHyperlinks.Item(9)
        Dim ThatHyperlink As Hyperlink
        Set ThatHyperlink = TheHyperlinks.Item("Hyperlink3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Hyperlink from the Hyperlinks collection.

**Parameters:**

` iIndex`      The index or the name of the Hyperlink to retrieve from the collection of Hyperlinks. As a numerics, this index is the rank of the Hyperlink in the collection. The index of the first Hyperlink in the collection is 1, and the index of the last Hyperlink is Count. As a string, it is the name you assigned to the Hyperlink.

**Example:**      The following example removes the tenth Hyperlink and the Hyperlink named ` Hyperlink 2` from the `TheHyperlinks` collection.

```VBScript
        TheHyperlinks.Remove(10)
        TheHyperlinks.Remove("Hyperlink2")

```

---

# Marker2D (Object)

**_Represents a marker 2D in a specified annotated view._**

## Properties

### Property **Fill**( ) As long

   Returns or sets the Marker2D's filling status (1 the figure is filled, 0 the figure is not filled).

**Example:**      This example retrieves the filling status of the `NewMarker2D` Marker2D.

```VBScript
        Dim status As Integer
        status = NewMarker2D.Fill

```

### Property **Frame**( ) As long

   Returns or sets the Marker2D's framing status (1 the figure is framed, 0 the figure is not framed).

**Example:**      This example retrieves the framing status of the `NewMarker2D` Marker2D.

```VBScript
        Dim status As Integer
        status = NewMarker2D.Frame

```

### Property **Picture**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the path to a picture file for a picture Marker2D.

**Example:**      This example retrieves the path to a picture file of the `NewMarker2D` Marker2D.

```VBScript
        Dim path As String
        path = NewMarker2D.Picture

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text for a text Marker2D.

**Example:**      This example retrieves the text of the `NewMarker2D` Marker2D.

```VBScript
        Dim text As String
        text = NewMarker2D.Text

```

### Property **TextAngle**( ) As double

   Returns or sets the text's angle for a text Marker2D.

**Example:**      This example retrieves the text's angle of the `NewMarker2D` Marker2D.

```VBScript
        Dim angle As Double
        size = NewMarker2D.TextAngle

```

### Property **TextFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text's font for a text Marker2D.

**Example:**      This example retrieves the text's font of the `NewMarker2D` Marker2D.

```VBScript
        Dim font As String
        font = NewMarker2D.TextFont

```

### Property **TextOrientation**( ) As [CatMarkerTextOrientation](../NavigatorInterfaces/enum_CatMarkerTextOrientation_123088.md)

   Return or set the orientation of text.

**Example:**      This example retrieves the orientation of the `NewMarker2D` Marker2D.

```VBScript
        Dim orientation As CatMarkerTextOrientation
        orientation = NewMarker2D.TextOrientation

```

### Property **TextSize**( ) As double

   Returns or sets the text's size for a text Marker2D.

**Example:**      This example retrieves the text's size of the `NewMarker2D` Marker2D.

```VBScript
        Dim size As Double
        size = NewMarker2D.TextSize

```

### Property **Type**( ) As [CatMarker2DType](../NavigatorInterfaces/enum_CatMarker2DType_44552.md) (Read Only)

   Returns the type of the marker 2D.

**Example:**      This example retrieves the type of the `NewMarker2D` Marker2D.

```VBScript
        Dim type As CatMarker2DType
        type = NewMarker2D.Type

```

Methods

### Sub **GetPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the positions of the Marker2D.  These positions depend on the type of the Marker2D :

  * Line: 2 positions.
  * Arrow: 2 positions, the first being the head and the second being the tail.
  * Rectangle: 2 positions, the first being the bottom-left corner and the second being the top-right corner.
  * Circle: 2 positions, the first being the center and the second being a point on the circle.
  * FreeHand: as many positions as points.
  * Text: 1 position, the bottom-left corner.
  * Picture: 2 positions, the first being the bottom-left corner and the second being the top-right corner.

**Parameters:**

` oCoordinates`      The coordinates of the positions expressed as an array of variants are:

  * oCoordinates(0) is the X coordinate of the first point
  * oCoordinates(1) is the Y coordinate of the first point
  * oCoordinates(2) is the X coordinate of the second point
  * oCoordinates(3) is the Y coordinate of the second point
  * oCoordinates(n*2-2) is the X coordinate of the n-th point
  * oCoordinates(n*2-1) is the Y coordinate of the n-th point

**Example:**      This example retrieves the coordinates of the positions of the `NewMarker2D` Marker2D.

```VBScript
        Dim Coordinates (3)
        NewMarker2D.GetPositions Coordinates

```

### Sub **SetPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the positions of the Marker2D.  These positions depend on the type of the Marker2D :

  * Line: 2 positions.
  * Arrow: 2 positions, the first being the head and the second being the tail.
  * Rectangle: 2 positions, the first being the bottom-left corner and the second being the top-right corner.
  * Circle: 2 positions, the first being the center and the second being a point on the circle.
  * FreeHand: as many positions as points.
  * Text: 1 position, the bottom-left corner.
  * Picture: 2 positions, the first being the bottom-left corner and the second being the top-right corner.

**Parameters:**

` iCoordinates`      The coordinates of the positions expressed as an array of variants are:

  * iCoordinates(0) is the X coordinate of the first point
  * iCoordinates(1) is the Y coordinate of the first point
  * iCoordinates(2) is the X coordinate of the second point
  * iCoordinates(3) is the Y coordinate of the second point
  * oCoordinates(n*2-2) is the X coordinate of the n-th point
  * oCoordinates(n*2-1) is the Y coordinate of the n-th point

**Example:**      This example sets the coordinates of the positions of the `NewMarker2D` Marker2D.

```VBScript
        Dim Coordinates (3) 'To be valuated
        NewMarker2D.SetPositions Coordinates

```

---

# Marker2Ds (Collection)

**_A collection of Marker2Ds objects._**

## Methods

### Func **Add2DArrow**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates an arrow marker 2D and adds it to the marker 2D collection. The arrow is defined using the coordinates of its head and tail points.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the head point
  * iCoordinates(1) is the Y coordinate of the head point
  * iCoordinates(2) is the X coordinate of the tail point
  * iCoordinates(3) is the Y coordinate of the tail point

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DArrow As Marker2D
        Set NewMarker2DArrow = TheMarker2Ds.Add2DArrow(Positions)

```

### Func **Add2DCircle**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  long  `iFillStatus`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a circle marker 2D and adds it to the marker 2D collection. The circle is defined using the coordinates of its center and a point through which it passes.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the center
  * iCoordinates(1) is the Y coordinate of the center
  * iCoordinates(2) is the X coordinate of the a point on the circle
  * iCoordinates(3) is the Y coordinate of the a point on the circle

` iFillStatus`      The filling status (1 the figure is filled, 0 the figure is not filled).

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DCircle As Marker2D
        Set NewMarker2DCircle = TheMarker2Ds.Add2DCircle(Positions, 0)

```

### Func **Add2DFreeHand**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a free hand drawing marker 2D and adds it to the marker 2D collection. The free hand drawing is defined using the coordinates of a series of points.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the first point
  * iCoordinates(1) is the Y coordinate of the first point
  * iCoordinates(2) is the X coordinate of the second point
  * iCoordinates(3) is the Y coordinate of the second point
  * iCoordinates(n*2-2) is the X coordinate of the n-th point
  * iCoordinates(n*2-1) is the Y coordinate of the n-th point

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DFreeHand As Marker2D
        Set NewMarker2DFreeHand = TheMarker2Ds.Add2DFreeHand(Positions)

```

### Func **Add2DLine**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a line marker 2D and adds it to the marker 2D collection. The line segment is defined using the coordinates of its two endpoints.

**Parameters:**

` iCoordinates`      The coordinates of the endpoints

  * iCoordinates(0) is the X coordinate of the first endpoint
  * iCoordinates(1) is the Y coordinate of the first endpoint
  * iCoordinates(2) is the X coordinate of the second endpoint
  * iCoordinates(3) is the Y coordinate of the second endpoint

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DLine As Marker2D
        Set NewMarker2DLine = TheMarker2Ds.Add2DLine(Positions)

```

### Func **Add2DPicture**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a picture marker 2D and adds it to the marker 2D collection. The picture is defined as a rectangle whose bottom-left and top-right corners are given.

**Parameters:**

` iCoordinates`      The coordinates of the corners

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point
  * iCoordinates(2) is the X coordinate of the top-right point
  * iCoordinates(3) is the Y coordinate of the top-right point

` iPath`      The path to the picture file

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DPicture As Marker2D
        Set NewMarker2DPicture = TheMarker2Ds.Add2DPicture(Positions, "e:\picture.bmp")

```

### Func **Add2DRectangle**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  long  `iFillStatus`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a rectangle marker 2D and adds it to the marker 2D collection. The rectangle is defined using the coordinates of its bottom-left and top-right corners.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point
  * iCoordinates(2) is the X coordinate of the top-right point
  * iCoordinates(3) is the Y coordinate of the top-right point

` iFillStatus`      The filling status (1 the figure is filled, 0 the figure is not filled).

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DRectangle As Marker2D
        Set NewMarker2DRectangle = TheMarker2Ds.Add2DRectangle(Positions, 0)

```

### Func **Add2DText**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Creates a text marker 2D and adds it to the marker 2D collection. The text is anchored using the coordinates of its bottom-left point.

**Parameters:**

` iCoordinates`      The coordinates

  * iCoordinates(0) is the X coordinate of the bottom-left point
  * iCoordinates(1) is the Y coordinate of the bottom-left point

` iText`      The text

**Returns:**      The created marker 2D  **Example:**      This example creates a new marker 2D in the `TheMarker2Ds` collection.

```VBScript
        Dim NewMarker2DText As Marker2D
        Set NewMarker2DText = TheMarker2Ds.Add2DText(Positions, "example")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMarker2D](../NavigatorInterfaces/interface_Marker2D_12072.md)

   Returns a marker 2D using its index from the Marker2Ds collection.

**Parameters:**

` iIndex`      The index of the marker 2D to retrieve from the collection of Marker2Ds. As a numerics, this index is the rank of the marker 2D in the collection. The index of the first marker 2D in the collection is 1, and the index of the last marker 2D is Count.

**Returns:**      The retrieved marker 2D  **Example:**      This example retrieves in `ThisMarker2D` the ninth marker 2D from the `TheMarker2Ds` collection.

```VBScript
        Dim ThisMarker2D As Marker2D
        Set ThisMarker2D = TheMarker2Ds.Item(9)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a marker 2D from the Marker2Ds collection.

**Parameters:**

` iIndex`      The index of the marker 2D to retrieve from he collection of Marker2Ds. As a numerics, this index is the rank of the marker 2D in the collection. The index of the first marker 2D in the collection is 1, and the index of the last marker 2D is Count.

**Example:**      The following example removes the tenth marker 2D from the `TheMarker2Ds` collection.

```VBScript
        TheMarker2Ds.Remove(10)

```

---

# Marker3D (Object)

**_Represents a marker 3D._**

## Properties

### Property **Fill**( ) As long

   Returns or sets the marker 3D's filling status (1 the figure is filled, 0 the figure is not filled).

**Example:**      This example retrieves the filling status of `NewMarker3D` marker 3D.

```VBScript
        Dim status As Integer
        status = NewMarker3D.Fill

```

### Property **Frame**( ) As long

   Returns or sets the marker 3D's framing status (1 the figure is framed, 0 the figure is not framed).

**Example:**      This example retrieves the framing status of `NewMarker3D` marker 3D.

```VBScript
        Dim status As Integer
        status = NewMarker3D.Frame

```

### Property **Text**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text for a text marker 3D.

**Example:**      This example reads the text of `NewMarker3D` marker 3D.

```VBScript
        Dim text As String
        text = NewMarker3D.Text

```

### Property **TextFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the text's font for a marker 3D.

**Example:**      This example retrieves the text's font of `NewMarker3D` marker 3D.

```VBScript
        Dim font As String
        font = NewMarker3D.TextFont

```

### Property **TextOrientation**( ) As [CatMarkerTextOrientation](../NavigatorInterfaces/enum_CatMarkerTextOrientation_123088.md)

   Returns or sets the orientation of text.

**Example:**      This example retrieves the orientation of `NewMarker3D` marker 3D.

```VBScript
        Dim orientation As CatMarkerTextOrientation
        orientation = NewMarker3D.TextOrientation

```

### Property **TextSize**( ) As double

   Returns or sets the text's size for a marker 3D.

**Example:**      This example retrieves the text's size of `NewMarker3D` marker 3D.

```VBScript
        Dim size As Double
        size = NewMarker3D.TextSize

```

### Property **Type**( ) As [CatMarker3DType](../NavigatorInterfaces/enum_CatMarker3DType_44587.md) (Read Only)

   Returns the type of the marker 3D.

**Example:**      This example reads the type of `NewMarker3D` marker 3D.

```VBScript
        Dim type As CatMarker3DType
        type = NewMarker3D.Type

```

Methods

### Sub **AddObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Adds a link to an object.

**Parameters:**

` iObject`      The object to be linked.

**Example:**      This example links `ThisProduct` to the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.AddObject(ThisProduct)

```

### Func **CountObject**( ) As long

   Returns the number of objects which are linked to the marker 3D.

**Example:**      This example reads the number of objects in the marker3D `NewMarker3D`.

```VBScript
        Dim number As Integer
        number = NewMarker3D.CountObject

```

### Sub **GetObjectPositions**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the anchor point of the marker on the object.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.
` oCoordinates`      The coordinates of the anchor point

  * oCoordinates(0) is the X coordinate of the anchor point
  * oCoordinates(1) is the Y coordinate of the anchor point
  * oCoordinates(2) is the Z coordinate of the anchor point

**Example:**      This example retrieves the coordinates of the anchor in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (3)
        NewMarker3D.GetObjectPositions Coordinates

```

### Sub **GetTextPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the positions of a text marker 3D. The bottom-left corner of the text is anchored to a given point.

**Returns:**      The coordinates of the text anchor point

  * oCoordinates(0) is the X coordinate of the text anchor point
  * oCoordinates(1) is the Y coordinate of the text anchor point
  * oCoordinates(2) is the Z coordinate of the text anchor point

**Example:**      This example retrieves the coordinates of the text in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (2)
        NewMarker3D.GetTextPositions Coordinates

```

### Func **ItemObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Returns an object which is linked to the marker 3D using its index.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.

**Returns:**      The retrieved object  **Example:**      This example retrieves in `ThisObject` the ninth object from the `NewMarker3D` marker 3D.

```VBScript
        Dim ThisObject As Marker3D
        Set ThisObject = NewMarker3D.ItemObject(9)

```

### Sub **RemoveObject**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an object which is linked to the marker 3D using its index.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.

**Example:**      This example removes the ninth object from the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.RemoveObject(9)

```

### Sub **SetObjectPositions**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the anchor point of the marker on the object.

**Parameters:**

` iIndex`      The index of the object in the marker 3D. The index of the first object is 1, and the index of the last object is CountObject.
` iCoordinates`      The coordinates of the anchor point

  * oCoordinates(0) is the X coordinate of the anchor point
  * oCoordinates(1) is the Y coordinate of the anchor point
  * oCoordinates(2) is the Z coordinate of the anchor point

**Example:**      This example sets the coordinates of the anchor in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (3)
        NewMarker3D.SetObjectPositions Coordinates

```

### Sub **SetTextPositions**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCoordinates`)

   Sets the coordinates of the positions of a text marker 3D.

**Parameters:**

` iCoordinates`      The coordinates of the text anchor point

  * oCoordinates(0) is the X coordinate of the text anchor point
  * oCoordinates(1) is the Y coordinate of the text anchor point
  * oCoordinates(2) is the Z coordinate of the text anchor point

**Example:**      This example sets the coordinates of the text in the `NewMarker3D` marker 3D.

```VBScript
        Dim Coordinates (2)
        NewMarker3D.SetTextPositions Coordinates

```

### Sub **Update**( )

   Updates the the marker 3D: that is to take into account all modifications which occur since last update.

**Example:**      This example updates the `NewMarker3D` marker 3D.

```VBScript
        NewMarker3D.Update

```

---

# Marker3Ds (Collection)

**_A collection of Marker3D objects._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("Marker3Ds")` on the root product retrieves this collection.

## Methods

### Func **Add3DText**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iTextCoordinates`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iText`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iObjectCoordinates`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAMarker3D](../NavigatorInterfaces/interface_Marker3D_12094.md)

   Creates a text marker 3D and adds it to the marker 3D collection. The bottom-left corner of the text is anchored to a given point.

**Parameters:**

` iTextCoordinates`      The coordinates of the text anchor point

  * iTextCoordinates(0) is the X coordinate of the text anchor point
  * iTextCoordinates(1) is the Y coordinate of the text anchor point
  * iTextCoordinates(2) is the Z coordinate of the text anchor point

` iText`      The text
` iObjectCoordinates`      The coordinates of the anchor of the marker 3D on the object

  * iObjectCoordinates(0) is the X coordinate of the object anchor point
  * iObjectCoordinates(1) is the Y coordinate of the object anchor point
  * iObjectCoordinates(2) is the Z coordinate of the object anchor point

` iObject`      The object which supports the text.

**Returns:**      The created marker 3D  **Example:**      This example creates a new marker 3D in the `TheMarker3Ds` collection.

```VBScript
        Dim NewMarker3DText As Marker3D
        Set NewMarker3DText = TheMarker3Ds.Add3DText(Position1, "example", Position2, Product2)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMarker3D](../NavigatorInterfaces/interface_Marker3D_12094.md)

   Returns a marker 3D using its index from the Marker3Ds collection.

**Parameters:**

` iIndex`      The index or the name of the marker 3D to retrieve from the collection of Marker3Ds. As a numerics, this index is the rank of the marker 3D in the collection. The index of the first Marker3D in the collection is 1, and the index of the last Marker3D is Count. As a string, it is the name you assigned to the Marker3D.

**Returns:**      The retrieved marker 3D  **Example:**      This example retrieves in `ThisMarker3D` the ninth marker 3D, and in `ThatMarker3D` the marker 3D named `Marker3D3` from the `TheMarker3Ds` collection.

```VBScript
        Dim ThisMarker3D As Marker3D
        Set ThisMarker3D = TheMarker3Ds.Item(9)
        Dim ThatMarker3D As Marker3D
        Set ThatMarker3D = TheMarker3Ds.Item("Marker3D3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a marker 3D from the Marker3Ds collection.

**Parameters:**

` iIndex`      The index or the name of the marker 3D to retrieve from the collection of Marker3Ds. As a numerics, this index is the rank of the marker 3D in the collection. The index of the first marker 3D in the collection is 1, and the index of the last marker 3D is Count. As a string, it is the name you assigned to the marker 3D.

**Example:**      The following example removes the tenth marker 3D and the marker 3D named `Marker3D2` from the `TheMarker3Ds` collection.

```VBScript
        TheMarker3Ds.Remove(10)
        TheMarker3Ds.Remove("Marker3D2")

```

---

# MarkerSettingAtt (Object)

**_Interface to handle the Marker settings

The different settings are:

MarkerAutoUpdate
Update on product structure modifications and scenes activation._**

MarkerDefaultsColor

MarkerDefaultsWeight

MarkerDefaultsDashed

Marker2DAutoNaming

Marker3DAutoNaming

MarkerTextColor2D

MarkerTextWeight2D

MarkerTextDashed2D

MarkerTextDefaultsFont2D

MarkerTextDefaultsSize2D

MarkerTextColor3D

MarkerTextWeight3D

MarkerTextDashed3D

MarkerTextDefaultsFont3D

MarkerTextDefaultsSize3D

## Properties

### Property **Marker2DAutoNaming**( ) As boolean

   Returns or sets the activation state for 2D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **Marker3DAutoNaming**( ) As boolean

   Returns or sets the activation state for 3D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **MarkerDefaultsDashed**( ) As long

   Returns or sets the default dashed value of an annotation (oValue the dashed value).  
### Property **MarkerDefaultsWeight**( ) As long

   Returns or sets the default weight value of an annotation (oValue the weight value).  
### Property **MarkerTextDashed2D**( ) As long

   Returns or sets the default dashed value of a 2D text annotation (oValue the dashed value).  
### Property **MarkerTextDashed3D**( ) As long

   Returns or sets the default dashed value of a 3D text annotation (oValue the dashed value).  
### Property **MarkerTextDefaultsFont2D**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the default font of a 2D annotation (oValue the font name).  
### Property **MarkerTextDefaultsFont3D**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iValue`)

   Returns or sets the default font of a 3D annotation (oValue the font name).  
### Property **MarkerTextDefaultsSize2D**( ) As long

   Returns or sets the default size value of a 2d annotation (oValue the size value)..  
### Property **MarkerTextDefaultsSize3D**( long  `iValue`)

   Returns or sets the default size value of a 3d annotation (oValue the size value)..  
### Property **MarkerTextWeight2D**( ) As long

   Returns or sets the default weight value of a 2D text annotation (oValue the weight value).  
### Property **MarkerTextWeight3D**( long  `iValue`)

   Returns or sets the default weight value of a 3D text annotation (oValue the weight value).  Methods

### Func **GetMarker2DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the Marker2DAutoNaming parameter.

**Role** :Retrieves the state of the Marker2DAutoNaming parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker3DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the Marker3DAutoNaming parameter.

**Role** :Retrieves the state of the Marker3DAutoNaming parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerDefaultsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

   Returns the default color of an annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsColor parameter.

**Role** :Retrieves the state of the MarkerDefaultsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsDashed parameter.

**Role** :Retrieves the state of the MarkerDefaultsDashed parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsWeight parameter.

**Role** :Retrieves the state of the MarkerDefaultsWeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor2D**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

   Returns the default color of a 2D text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColor2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextColor2D parameter.

**Role** :Retrieves the state of the MarkerTextColor2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor3D**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

   Returns the default color of a 3D text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColor3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextColor3D parameter.

**Role** :Retrieves the state of the MarkerTextColor3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashed2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextDashed2D parameter.

**Role** :Retrieves the state of the MarkerTextDashed2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashed3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextDashed3D parameter.

**Role** :Retrieves the state of the MarkerTextDashed3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsFont2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsFont2D parameter.

**Role** :Retrieves the state of the MarkerDefaultsFont2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsFont3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsFont3D parameter.

**Role** :Retrieves the state of the MarkerDefaultsFont3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsSize2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsSize2D parameter.

**Role** :Retrieves the state of the MarkerDefaultsSize2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDefaultsSize3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerDefaultsSize3D parameter.

**Role** :Retrieves the state of the MarkerDefaultsSize3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeight2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextWeight2D parameter.

**Role** :Retrieves the state of the MarkerTextWeight2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeight3DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerTextWeight3D parameter.

**Role** :Retrieves the state of the MarkerTextWeight3D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetMarker2DAutoNamingLock**( boolean  `iLocked`)

   Locks or unlocks the Marker2DAutoNaming parameter.

**Role** :Locks or unlocks the Marker2DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker3DAutoNamingLock**( boolean  `iLocked`)

   Locks or unlocks the Marker3DAutoNaming parameter.

**Role** :Locks or unlocks the Marker3DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

   Sets the default color of an annotation (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetMarkerDefaultsColorLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsColor parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsDashedLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsDashed parameter.

**Role** :Locks or unlocks the MarkerDefaultsDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsWeightLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsWeight parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor2D**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

   Sets the default color of a 2D text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColor2DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextColor2D parameter.

**Role** :Locks or unlocks the MarkerTextColor2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor3D**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

   Sets the default color of a 3D text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColor3DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextColor3D parameter.

**Role** :Locks or unlocks the MarkerTextColor3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashed2DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextDashed parameter.

**Role** :Locks or unlocks the MarkerTextDashed2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashed3DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextDashed3D parameter.

**Role** :Locks or unlocks the MarkerTextDashed3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsFont2DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsFont2D parameter.

**Role** :Locks or unlocks the MarkerDefaultsFont2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsFont3DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsFont3D parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsSize2DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsSize2D parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDefaultsSize3DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerDefaultsSize3D parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeight2DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextWeight2D parameter.

**Role** :Locks or unlocks the MarkerTextWeight2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeight3DLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerTextWeight3D parameter.

**Role** :Locks or unlocks the MarkerTextWeight3D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# N4DNavigatorSettingAtt (Object)

**_Interface to handle the settings of the DMU Navigator workbench._**

The different settings are:

DMUClashPreview:
Display of the preview viewer when editing an interference.

DMUDistancePreview:
Display of the preview viewer when editing a distance.

DMUGroupPreview:
Display of the preview viewer when editing a group.

DMUSectionPreview:
Display of the preview viewer when editing a section.

DMUShuttlePreview:
Display of the preview viewer when editing a shuttle.

DMUThicknessPreview:
Display of the preview viewer for the thickness command.

DMUOffsetPreview:
Display of the preview viewer for the offset command.

DMUSweptVolPreview:
Display of the preview viewer for the swept volume command.

DMUSilhouettePreview:
Display of the preview viewer for the silhouette command.

DMUWrappingPreview:
Display of the preview viewer for the wrapping command.

DMUFreeSpacePreview:
Display of the preview viewer for the free space command.

DMUSimplifPreview:
Display of the preview viewer for the simplification command.

DMUVibrationVolPreview:
Display of the preview viewer for the vibration volume command.

DMUCut3DPreview:
Display of the preview viewer for the 3D cut command.

DMUMergerPreview:
Display of the preview viewer for the merger command.

NumUrlName:
Display of the hyperlink name.

MarkerAutoUpdate:
Update on product structure modifications and scenes activation.

MarkerDefaultsColor:
Default color of an annotation.

SceneDefaultsColor:
Default background color for scene environment.

MarkerTextColor:
Default color of a text annotation.

MarkerDefaultsWeight:
Default weight value of an annotation.

MarkerDefaultsDashed:
Default dashed value of an annotation.

MarkerDefaultsSize:
Default size value of an annotation.

MarkerDefaultsFont:
Default font of an annotation.

MarkerTextDashed:
Default dashed value of a text annotation.

MarkerTextWeight:
Default weight value of a text annotation.

PublishAutoLaunchBrowser:
Automatic launching of publish results in a browser.

Marker2DAutoNaming:
Automatically use a Part's name as the default for the creation of text annotations.

Marker3DAutoNaming:
Activation of the mechanism that enables to transform temporary markers into persistent 3D annotations.

DMUReviewName:
The desired default name for DMU Reviews

ForceVoxel:
Force users of the Spatial Query command to use the defined Released Accuracy.

ClearanceVoxel:
Definition of the Clearance value.

ForceClearanceVoxel:
Force users of the Spatial Query command to use the defined Clearance value.

InsertMode:
Mode for the Import applicative data command.

DMUGroupPreviewHiddenObjectsDisplayMode:
Display mode for hidden objects of a DMU Group in its preview: visualized as in main 3D viewer or visualized with customized graphic properties

DMUGroupPreviewHiddenObjectsColor:
Color for hidden objects in DMU Group Preview.

DMUGroupPreviewHiddenObjectsOpacity:
Opacity for hidden objects in DMU Group Preview.

DMUGroupPreviewHiddenObjectsLowIntMode:
Hidden objects are low intensified or not in DMU Group Preview.

DMUGroupPreviewHiddenObjectsPickMode:
Hidden objects can be picked or not in DMU Group Preview.

## Properties

### Property **ClearanceVoxel**( ) As float

   Returns or sets the clearance value (oValue the clearance value in mm).  
### Property **DMUClashPreview**( ) As boolean

   Returns or sets the preview activation state for Interference (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUCut3DPreview**( ) As boolean

   Returns or sets the preview activation state for 3D Cut (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUDistancePreview**( ) As boolean

   Returns or sets the preview activation state for Distance (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUFreeSpacePreview**( ) As boolean

   Returns or sets the preview activation state for Free Space (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUGroupPreview**( ) As boolean

   Returns or sets the preview activation state for Group (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUGroupPreviewHiddenObjectsDisplayMode**( ) As [CatDMUGroupPreviewHiddenObjectsDisplayMode](../NavigatorInterfaces/enum_CatDMUGroupPreviewHiddenObjectsDisplayMode_359864.md)

   Returns or sets the mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsLowInt**( ) As boolean

   Returns or sets the Low Intensity mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsOpacity**( ) As long

   Returns or sets the opacity for the display of hidden objects in DMU Group Preview.  
### Property **DMUGroupPreviewHiddenObjectsPick**( ) As boolean

   Returns or sets the pick mode for the display of hidden objects in DMU Group Preview.  
### Property **DMUMergerPreview**( ) As boolean

   Returns or sets the preview activation state for Merger (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUOffsetPreview**( ) As boolean

   Returns or sets the preview activation state for Offset (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUReviewName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the default name for the DMU Reviews (oValue, the DMU Review name).  
### Property **DMUSectionPreview**( ) As boolean

   Returns or sets the preview activation state for Section (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUShuttlePreview**( ) As boolean

   Returns or sets the preview activation state for Shuttle (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSilhouettePreview**( ) As boolean

   Returns or sets the preview activation state for Silhouette (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSimplifPreview**( ) As boolean

   Returns or sets the preview activation state for Simplification (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUSweptVolPreview**( ) As boolean

   Returns or sets the preview activation state for Swept Volume (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUThicknessPreview**( ) As boolean

   Returns or sets the preview activation state for Thickness (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUVibrationVolPreview**( ) As boolean

   Returns or sets the preview activation state for Vibration volume (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **DMUWrappingPreview**( ) As boolean

   Returns or sets the preview activation state for Wrapping (TRUE the preview window is automatically displayed, FALSE the preview window is not displayed).  
### Property **ForceClearanceVoxel**( ) As boolean

   Returns or sets the activation state for the use of the clearance value (TRUE the clearance value is used, FALSE the clearance value is not used);  
### Property **ForceVoxel**( ) As boolean

   Returns or sets the activation state for the use of the Released accuracy value (TRUE the released accuracy value is used, FALSE the released accuracy value is not used);  
### Property **InsertLevel**( ) As boolean

   Returns or sets the level for the Import Applicative Data command (True : at highest review level, False : in current review).  
### Property **InsertMode**( ) As [CatSacSettingsEnum](../NavigatorInterfaces/enum_CatSacSettingsEnum_68200.md)

   Returns or sets the mode for the Import Applicative Data command (CatSacSettingsEnumNoInsert no import of applicative data, CatSacSettingsEnumAutomatic the import of applicative is automatic, CatSacSettingsEnumUserPrompt the user can select the applicative data to import).  
### Property **Marker2DAutoNaming**( ) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_Marker2DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_Marker2DAutoNaming) This method will be replaced by [MarkerSettingAtt.put_Marker2DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_Marker2DAutoNaming) Returns or sets the activation state for 2D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **Marker3DAutoNaming**( ) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_Marker3DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_Marker3DAutoNaming) This method will be replaced by [MarkerSettingAtt.put_Marker3DAutoNaming](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_Marker3DAutoNaming) Returns or sets the activation state for 3D annotations automatic naming (TRUE naming is automatic, FALSE the naming is not automatic).  
### Property **MarkerAutoUpdate**( ) As boolean

   Returns or sets the activation of the automatic update on product structure modification (TRUE update is done automatically, FALSE update is done manually).  
### Property **MarkerDefaultsDashed**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerDefaultsDashed](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerDefaultsDashed) This method will be replaced by [MarkerSettingAtt.put_MarkerDefaultsDashed](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerDefaultsDashed) Returns or sets the default dashed value of an annotation (oValue the dashed value).  
### Property **MarkerDefaultsFont**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDefaultsFont2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDefaultsFont2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDefaultsFont2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDefaultsFont2D) Returns or sets the default font of an annotation (oValue the font name).  
### Property **MarkerDefaultsSize**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDefaultsSize2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDefaultsSize2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDefaultsSize2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDefaultsSize2D) Returns or sets the default size value of an annotation (oValue the size value)..  
### Property **MarkerDefaultsWeight**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerDefaultsWeight](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerDefaultsWeight) This method will be replaced by [MarkerSettingAtt.put_MarkerDefaultsWeight](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerDefaultsWeight) Returns or sets the default weight value of an annotation (oValue the weight value).  
### Property **MarkerTextDashed**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextDashed2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextDashed2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextDashed2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextDashed2D) Returns or sets the default dashed value of a text annotation (oValue the dashed value).  
### Property **MarkerTextWeight**( ) As long

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.get_MarkerTextWeight2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#get_MarkerTextWeight2D) This method will be replaced by [MarkerSettingAtt.put_MarkerTextWeight2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#put_MarkerTextWeight2D) Returns or sets the default weight value of a text annotation (oValue the weight value).  
### Property **NumUrlName**( ) As boolean

   Returns or sets the name activation state for Hyperlink (TRUE the hyperlink name is displayed, FALSE the hyperlink name is not displayed).  
### Property **PublishAutoLaunchBrowser**( ) As boolean

   Returns or sets the activation state of the automatic launching of the publish browser (TRUE the publish browser is automatically opened, FALSE the publish browser is not automatically opened).  Methods

### Func **GetClearanceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ClearanceVoxel parameter.

**Role** :Retrieves the state of the ClearanceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUClashPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUClashPreview parameter.

**Role** :Retrieves the state of the DMUClashPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUCut3DPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUCut3DPreview parameter.

**Role** :Retrieves the state of the DMUCut3DPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUDistancePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUDistancePreview parameter.

**Role** :Retrieves the state of the DMUDistancePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUFreeSpacePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUFreeSpacePreview parameter.

**Role** :Retrieves the state of the DMUFreeSpacePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetDMUGroupPreviewHiddenObjectsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

   Returns the color for the display of hidden objects in DMU Group Preview.  
### Func **GetDMUGroupPreviewHiddenObjectsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsColor parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsDisplayModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsDisplayMode parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsDisplayMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsLowIntInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsLowInt parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsLowInt parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsOpacityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsOpacity parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsOpacity parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewHiddenObjectsPickInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreviewHiddenObjectsPick parameter.

**Role** :Retrieves the state of the DMUGroupPreviewHiddenObjectsPick parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUGroupPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUGroupPreview parameter.

**Role** :Retrieves the state of the DMUGroupPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUMergerPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUMergerPreview parameter.

**Role** :Retrieves the state of the DMUMergerPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUOffsetPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUOffsetPreview parameter.

**Role** :Retrieves the state of the DMUOffsetPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUReviewNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUReviewName parameter.

**Role** :Retrieves the state of the DMUReviewName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSectionPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSectionPreview parameter.

**Role** :Retrieves the state of the DMUSectionPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUShuttlePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUShuttlePreview parameter.

**Role** :Retrieves the state of the DMUShuttlePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSilhouettePreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSilhouettePreview parameter.

**Role** :Retrieves the state of the DMUSilhouettePreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSimplifPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSimplifPreview parameter.

**Role** :Retrieves the state of the DMUSimplifPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUSweptVolPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUSweptVolPreview parameter.

**Role** :Retrieves the state of the DMUSweptVolPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUThicknessPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUThicknessPreview parameter.

**Role** :Retrieves the state of the DMUThicknessPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUVibrationVolPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUVibrationVolPreview parameter.

**Role** :Retrieves the state of the DMUVibrationVolPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDMUWrappingPreviewInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DMUWrappingPreview parameter.

**Role** :Retrieves the state of the DMUWrappingPreview parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetForceClearanceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ForceClearanceVoxel parameter.

**Role** :Retrieves the state of the ForceClearanceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetForceVoxelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ForceVoxel parameter.

**Role** :Retrieves the state of the ForceVoxel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetInsertLevelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the InsertLevel parameter.

**Role** :Retrieves the state of the InsertLevel parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetInsertModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the InsertMode parameter.

**Role** :Retrieves the state of the InsertMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker2DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarker2DAutoNamingInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarker2DAutoNamingInfo) Retrieves environment informations for the Marker2DAutoNaming parameter.

**Role** :Retrieves the state of the Marker2DAutoNaming parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarker3DAutoNamingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarker3DAutoNamingInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarker3DAutoNamingInfo) Retrieves environment informations for the Marker3DAutoNaming parameter.

**Role** :Retrieves the state of the Marker3DAutoNaming parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerAutoUpdateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the MarkerAutoUpdate parameter.

**Role** :Retrieves the state of the MarkerAutoUpdate parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerDefaultsColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsColor](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsColor) Returns the default color of an annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsColorInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsColorInfo) Retrieves environment informations for the MarkerDefaultsColor parameter.

**Role** :Retrieves the state of the MarkerDefaultsColor parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsDashedInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsDashedInfo) Retrieves environment informations for the MarkerDefaultsDashed parameter.

**Role** :Retrieves the state of the MarkerDefaultsDashed parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsFontInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsFont2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsFont2DInfo) Retrieves environment informations for the MarkerDefaultsFont parameter.

**Role** :Retrieves the state of the MarkerDefaultsFont parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by CATIAmarkerSettingAtt Retrieves environment informations for the MarkerDefaultsSize parameter.

**Role** :Retrieves the state of the MarkerDefaultsSize parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerDefaultsWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerDefaultsWeightInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerDefaultsWeightInfo) Retrieves environment informations for the MarkerDefaultsWeight parameter.

**Role** :Retrieves the state of the MarkerDefaultsWeight parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetMarkerTextColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextColor2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextColor2DInfo) Returns the default color of a text annotation (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetMarkerTextColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextColor2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextColor2DInfo) Retrieves environment informations for the MarkerTextColor parameter.

**Role** :Retrieves the state of the MarkerTextColor parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextDashedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextDashed2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextDashed2DInfo) Retrieves environment informations for the MarkerTextDashed parameter.

**Role** :Retrieves the state of the MarkerTextDashed parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetMarkerTextWeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.GetMarkerTextWeight2DInfo](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#GetMarkerTextWeight2DInfo) Retrieves environment informations for the MarkerTextWeight parameter.

**Role** :Retrieves the state of the MarkerTextWeight parameter in the current environment.  **Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNumUrlNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the NumUrlName parameter.

**Role** :Retrieves the state of the NumUrlName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPublishAutoLaunchBrowserInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PublishAutoLaunchBrowser parameter.

**Role** :Retrieves the state of the PublishAutoLaunchBrowser parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetSceneDefaultsColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the scene background color (oRed, oGreen, oBlue: RGB values of the color).  
### Func **GetSceneDefaultsColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SceneDefaultsColor parameter.

**Role** :Retrieves the state of the SceneDefaultsColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetClearanceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ClearanceVoxel parameter.

**Role** :Locks or unlocks the ClearanceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUClashPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUClashPreview parameter.

**Role** :Locks or unlocks the DMUClashPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUCut3DPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUCut3DPreview parameter.

**Role** :Locks or unlocks the DMUCut3DPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUDistancePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUDistancePreview parameter.

**Role** :Locks or unlocks the DMUDistancePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUFreeSpacePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUFreeSpacePreview parameter.

**Role** :Locks or unlocks the DMUFreeSpacePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

   Sets the color for the display of hidden objects in DMU Group Preview.  
### Sub **SetDMUGroupPreviewHiddenObjectsColorLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsColor parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsDisplayModeLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsDisplayMode parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsDisplayMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsLowIntLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsLowInt parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsLowInt parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsOpacityLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsOpacity parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsOpacity parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewHiddenObjectsPickLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreviewHiddenObjectsPick parameter.

**Role** :Locks or unlocks the DMUGroupPreviewHiddenObjectsPick parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUGroupPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUGroupPreview parameter.

**Role** :Locks or unlocks the DMUGroupPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUMergerPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUMergerPreview parameter.

**Role** :Locks or unlocks the DMUMergerPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUOffsetPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUOffsetPreview parameter.

**Role** :Locks or unlocks the DMUOffsetPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUReviewNameLock**( boolean  `iLocked`)

   Locks or unlocks the DMUReviewName parameter.

**Role** :Locks or unlocks the DMUReviewName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSectionPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSectionPreview parameter.

**Role** :Locks or unlocks the DMUSectionPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUShuttlePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUShuttlePreview parameter.

**Role** :Locks or unlocks the DMUShuttlePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSilhouettePreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSilhouettePreview parameter.

**Role** :Locks or unlocks the DMUSilhouettePreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSimplifPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSimplifPreview parameter.

**Role** :Locks or unlocks the DMUSimplifPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUSweptVolPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUSweptVolPreview parameter.

**Role** :Locks or unlocks the DMUSweptVolPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUThicknessPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUThicknessPreview parameter.

**Role** :Locks or unlocks the DMUThicknessPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUVibrationVolPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUVibrationVolPreview parameter.

**Role** :Locks or unlocks the DMUVibrationVolPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDMUWrappingPreviewLock**( boolean  `iLocked`)

   Locks or unlocks the DMUWrappingPreview parameter.

**Role** :Locks or unlocks the DMUWrappingPreview parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetForceClearanceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ForceClearanceVoxel parameter.

**Role** :Locks or unlocks the ForceClearanceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetForceVoxelLock**( boolean  `iLocked`)

   Locks or unlocks the ForceVoxel parameter.

**Role** :Locks or unlocks the ForceVoxel parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetInsertLevelLock**( boolean  `iLocked`)

   Locks or unlocks the InsertMode parameter.

**Role** :Locks or unlocks the InsertMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetInsertModeLock**( boolean  `iLocked`)

   Locks or unlocks the InsertMode parameter.

**Role** :Locks or unlocks the InsertMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker2DAutoNamingLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarker2DAutoNamingLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarker2DAutoNamingLock) Locks or unlocks the Marker2DAutoNaming parameter.

**Role** :Locks or unlocks the Marker2DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarker3DAutoNamingLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarker3DAutoNamingLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarker3DAutoNamingLock) Locks or unlocks the Marker3DAutoNaming parameter.

**Role** :Locks or unlocks the Marker3DAutoNaming parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerAutoUpdateLock**( boolean  `iLocked`)

   Locks or unlocks the MarkerAutoUpdate parameter.

**Role** :Locks or unlocks the MarkerAutoUpdate parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsColor](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsColor) Sets the default color of an annotation (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetMarkerDefaultsColorLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsColorLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsColorLock) Locks or unlocks the MarkerDefaultsColor parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsDashedLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsDashedLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsDashedLock) Locks or unlocks the MarkerDefaultsDashed parameter.

**Role** :Locks or unlocks the MarkerDefaultsDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsFontLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsFont2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsFont2DLock) Locks or unlocks the MarkerDefaultsFont parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsSizeLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextDefaultsSize2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextDefaultsSize2DLock) Locks or unlocks the MarkerDefaultsSize parameter.

**Role** :Locks or unlocks the MarkerDefaultsSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerDefaultsWeightLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerDefaultsWeightLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerDefaultsWeightLock) Locks or unlocks the MarkerDefaultsWeight parameter.

**Role** :Locks or unlocks the MarkerDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextColor2D](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextColor2D) Sets the default color of a text annotation (iRed, iGreen, iBlue: RGB values for the desired color).  
### Sub **SetMarkerTextColorLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextColor2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextColor2DLock) Locks or unlocks the MarkerTextColor parameter.

**Role** :Locks or unlocks the MarkerTextColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextDashedLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextDashed2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextDashed2DLock) Locks or unlocks the MarkerTextDashed parameter.

**Role** :Locks or unlocks the MarkerTextDashed parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetMarkerTextWeightLock**( boolean  `iLocked`)

**Deprecated:**      R17 This method will be replaced by [MarkerSettingAtt.SetMarkerTextWeight2DLock](../NavigatorInterfaces/interface_MarkerSettingAtt_54542.htm#SetMarkerTextWeight2DLock) Locks or unlocks the MarkerTextWeight parameter.

**Role** :Locks or unlocks the MarkerTextWeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.  **Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNumUrlNameLock**( boolean  `iLocked`)

   Locks or unlocks the NumUrlName parameter.

**Role** :Locks or unlocks the NumUrlName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPublishAutoLaunchBrowserLock**( boolean  `iLocked`)

   Locks or unlocks the PublishAutoLaunchBrowser parameter.

**Role** :Locks or unlocks the PublishAutoLaunchBrowser parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSceneDefaultsColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the scene background color (iRed, iGreen, iBlue: RGB values for the desired color)  
### Sub **SetSceneDefaultsColorLock**( boolean  `iLocked`)

   Locks or unlocks the SceneDefaultsColor parameter.

**Role** :Locks or unlocks the SceneDefaultsColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# NavigatorWorkbench (Object)

**_The object to manage all DMU Navigator entities._**

This version allows to manage groups and annotated views.

## Properties

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

   Returns the AnnotatedViews collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("AnnotatedViews")` on the root product, to retrieve the `AnnotatedViews` collection.

**Example:**      This example retrieves the AnnotatedViews collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheAnnotatedViewsList As AnnotatedViews
        Set TheAnnotatedViewsList = TheNavigatorWorkbench.AnnotatedViews

```

### Property **DMUDataFlow**( ) As [CATIADMUDataFlow](../NavigatorInterfaces/interface_DMUDataFlow_24296.md) (Read Only)

   Returns the DMU DataFlow object.  
### Property **Groups**( ) As [CATIAGroups](../NavigatorInterfaces/interface_Groups_8540.md) (Read Only)

   Returns the Groups collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Groups")` on the root product, to retrieve the `Groups` collection.

**Example:**      This example retrieves the Groups collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheGroupsList As Groups
        Set TheGroupsList = TheNavigatorWorkbench.Groups

```

### Property **Hyperlinks**( ) As [CATIAHyperlinks](../NavigatorInterfaces/interface_Hyperlinks_22650.md) (Read Only)

   Returns the Hyperlinks collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Hyperlinks")` on the root product, to retrieve the `Hyperlinks` collection.

**Example:**      This example retrieves the Hyperlinks collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim HyperlinksList As Hyperlinks
        Set HyperlinksList = TheNavigatorWorkbench.Hyperlinks

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

   Returns the Marker3Ds collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Marker3Ds")` on the root product, to retrieve the `Marker3Ds` collection.

**Example:**      This example retrieves the Marker3Ds collection of the active document.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )
        Dim TheMarker3DsList As AnnotatedViews
        Set TheMarker3DsList = TheNavigatorWorkbench.Marker3Ds

```

Methods

### Sub **AdvancedView**( [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)  `iAnnotatedView`,  short  `iViewOption`)

   Applies the annotated view to the current viewer.

**Parameters:**

` iAnnotatedView`      The annotated view to apply.
` iViewOptions`      The option to launch the annotated view command, possible values are

  * CatAnnotatedViewCmdOption_NoToolbar : No Toolbar for annotation creation
  * CatAnnotatedViewCmdOption_NoAnimation : No Animation when applying the view

**Example:**      This example applies the view of the `NewAnnotatedView` AnnotatedView.

```VBScript
        TheNavigatorWorkbench.View,CatAnnotatedViewCmdOption_NoAnimation+CatAnnotatedViewCmdOption_NoToolbar(NewAnnotatedView)

```

### Func **GetOrder**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`) As long

   Returns the order of an object.

**Parameters:**

` iObject`      The object whose rank has to be returned.
` oCurrentRank`      The current rank of the object (from 1 to n the number of objects in the collection).

**Example:**      This example creates an annotated view `NewAnnotatedView` and returns its position.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )

        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add

        Dim iOrder As Integer
        iOrder = TheNavigatorWorkbench.GetOrder(NewAnnotatedView)

```

### Sub **SetOrder**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`,  long  `iNewRank`)

   Sets the order of an object.

**Parameters:**

` iObject`      The object whose rank has to be modified.
` iNewRank`      The new rank of the object (from 1 to n the number of objects in the collection).

**Example:**      This example creates an annotated view `NewAnnotatedView` and move it to the first position.

```VBScript
        Dim TheNavigatorWorkbench As Workbench
        Set TheNavigatorWorkbench = CATIA.ActiveDocument.GetWorkbench ( "NavigatorWorkbench" )

        Dim NewAnnotatedView As AnnotatedView
        Set NewAnnotatedView = TheAnnotatedViews.Add
        TheNavigatorWorkbench.SetOrder NewAnnotatedView, 1

```

### Sub **View**( [CATIAAnnotatedView](../NavigatorInterfaces/interface_AnnotatedView_36411.md)  `iAnnotatedView`)

   Applies the annotated view to the current viewer.

**Parameters:**

` iAnnotatedView`      The annotated view to apply.

**Example:**      This example applies the view of the `NewAnnotatedView` AnnotatedView.

```VBScript
        TheNavigatorWorkbench.View(NewAnnotatedView)

```