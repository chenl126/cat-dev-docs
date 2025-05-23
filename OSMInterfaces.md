# OSMInterfaces Framework

## Object Index

  * [ProductScene](OSMInterfaces/interface_ProductScene_30810.md)
  * [ProductScenes](OSMInterfaces/interface_ProductScenes_36526.md)
  * [Scene](OSMInterfaces/interface_Scene_5528.md)
  * [SceneProductData](OSMInterfaces/interface_SceneProductData_53304.md)
  * [SceneWorkbench](OSMInterfaces/interface_SceneWorkbench_41664.md)
  * [Scenes](OSMInterfaces/interface_Scenes_8092.md)

## Enumerated Types Index

  * [CatSceneType](OSMInterfaces/enum_CatSceneType_30364.md)

---

# CatSceneType (Enumeration)

**_The different types of a new ProductScene scene._**

**See also:**      [Marker2D](../NavigatorInterfaces/interface_Marker2D_12072.md) **See also:**      [Marker3D](../NavigatorInterfaces/interface_Marker3D_12094.md) **Values:**

` CatSceneTypeDelta`      The product scene is a DELTA scene.
` CatSceneTypeFull`      The product scene is a FULL scene.

---

# ProductScene (Object)

**_Represent the Product-Scene._**
A Product-Scene stores a state of a product in a given ProductDocument.

This state is composed of product properties, graphical attibutes, activation status and position for each component of the product.

## Properties

### Property **Type**( ) As [CatSceneType](../OSMInterfaces/enum_CatSceneType_30364.md) (Read Only)

   Returns the type of the Product-Scene.

**Example:**      This example reads the type of `NewSceneDelta` Product-Scene.

```VBScript
        Dim type As CatSceneType
        type = NewSceneDelta.Type

```

Methods

### Func **Copy**( [CatSceneType](../OSMInterfaces/enum_CatSceneType_30364.md)  `iType`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Creates another Product-Scene from the current one with the possibility to have a different mode.

**Parameters:**

` iType`      The Product-Scene type

**Returns:**      The Product-Scene created from the current one.  **Example:**      This example returns whether the `CopyScene` Product-Scene created from the `Configuration1` Product-Scene, with the DELTA mode.

```VBScript
        Dim type As CatSceneType
        type = CatSceneTypeDelta
        Dim CopyScene As ProductScene
        CopyScene = Configuration1.Copy(type)

```

### Func **ExistsInScene**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As boolean

   Returns whether the product has overloaded attributes in the Product-Scene.

**Parameters:**

` iProduct`      The product

**Returns:**      True if the Product-Scene overloads some of the product attributes.  **Example:**      This example returns whether the `Engine` product exists in the `Configuration1` Product-Scene.

```VBScript
        ExistsInSc = Configuration1.ExistsInScene(Engine)

```

### Func **GetSceneProductData**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIASceneProduct](../OSMInterfaces/interface_SceneProductData_53304.md)

   Returns the SceneProductData associated to the given product in the Product-Scene. If it does not exist yet, it is created.

**Parameters:**

` iProduct`      The product

**Returns:**      The SceneProductData associated to the given product.  **Example:**      This example returns SceneProductData associated to `Engine` in the `NewSceneDelta` Product-Scene.

```VBScript
        Dim scenePrd As SceneProductData
        type = NewSceneDelta.GetSceneProductData(Engine)

```

---

# ProductScenes (Collection)

**_A collection of ProductScenes contained in a given ProductDocument._**

## Methods

### Func **AddProductSceneFull**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferenceProducts`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Creates a new FULL scene from a set of products and adds it to the ProductScenes collection.

**Parameters:**

` iName`      The name of the new scene
` iReferenceProducts`      Products used as root nodes of the new scene

**Returns:**      The created new full scene  **Example:**      This example creates the `SpareWheel` new scene from the reference product `FrontRightWheel` and adds the scene to the `ToolKits` collection.

```VBScript
        Dim SpareWheel As ProductScene
        Set SpareWheel = ToolKits.AddProductSceneFull("SpareWheel", FrontRightWheel)

```

### Func **AddProductScenePartial**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iReferenceProducts`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Creates a new DELTA scene from a set of products and adds it to the ProductScenes collection.

**Parameters:**

` iName`      The name of the new scene
` iReferenceProducts`      Products used as root nodes of the new scene

**Returns:**      The created new delta scene  **Example:**      This example creates the `SpareWheel` new scene from the reference product `FrontRightWheel` and adds the scene to the `ToolKits` collection.

```VBScript
        Dim SpareWheel As ProductScene
        Set SpareWheel = ToolKits.AddProductScenePartial("SpareWheel", FrontRightWheel)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Returns a scene using its index or its name from the ProductScenes collection.

**Parameters:**

` iIndex`      The index or the name of the ProductScene to retrieve from the collection of ProductScenes. As a numerics, this index is the rank of the ProductScene in the collection. The index of the first ProductScene in the collection is 1, and the index of the last ProductScene is Count. As a string, it is the name you assigned to the ProductScene.

**Returns:**      The retrieved ProductScene.  **Example:**      This example retrieves in `ThisProductScene` the ninth ProductScene, and in `ThatProductScene` the ProductScene named `ProductScene3` from the `TheProductScenes` collection.

```VBScript
        Dim ThisProductScene As ProductScene
        Set ThisProductScene = TheProductScenes.Item(9)
        Dim ThatProductScene As ProductScene
        Set ThatProductScene = TheProductScenes.Item("ProductScene3")

```

### Sub **Remove**( [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)  `iProductScene`)

   Removes a product-scene from the ProductScenes collection.

**Parameters:**

` iScene`      The scene to remove.

**Example:**      This example removes the `Engine` product-scene from the `ToolKits` collection.

```VBScript
        ToolKits.Remove Engine

```

---

# Scene (Object)

**_Represent the scene._**
A scene stores a state of a product in a given ProductDocument.

This state is composed of product properties, graphical attibutes, activation status and position for each component of the product.

## Methods

### Func **GetDefinition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the product's definition.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's definition.  **Example:**      This example retrieves the `Engine` product's definition in the `Configuration1` scene.

```VBScript
        Dim Definition As String
        Definition = Configuration1.GetDefinition(Engine)

```

### Func **GetDescription**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the product's description.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's description.  **Example:**      This example retrieves the `Engine` product's description in the `Configuration1` scene.

```VBScript
        Dim Description As String
        Description = Configuration1.GetDescription(Engine)

```

### Func **GetMasterShapeRepresentation**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  boolean  `iLoadIfNecessary`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Retrieves the product's master shape representation.

**Parameters:**

` iProduct.`      The product
` iLoadIfNecessary`      Parameter to set to True if the master shape representation should be loaded to determine if it exists, or to False otherwise.

**Returns:**      The product's master shape representation.  **Example:**      This example retrieves the `Engine` product's master shape representation in the `Configuration1` scene.

```VBScript
        Dim MSRep As Object
        Set MSRep = Configuration1.GetMasterShapeRepresentation(Engine)

```

### Func **GetMove**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAMove](../InfInterfaces/interface_Move_3742.md)

   Returns the product's move object. The move object is aggregated by the product object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your product master shape representation according to this isometry.

**Parameters:**

` iProduct`      The product

**Returns:**      The move.  **Example:**      This example retrieves the `EngineMove` move from the `Engine` product in the `Configuration1` scene.

```VBScript
        Dim EngineMove As Move
        Set EngineMove = Configuration1.GetMove(Engine)

```

### Func **GetNomenclature**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the product's nomenclature.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's nomenclature.  **Example:**      This example retrieves the `Engine` product's nomenclature in the `Configuration1` scene.

```VBScript
        Dim Nomenclature As String
        Nomenclature = Configuration1.GetNomenclature(Engine)

```

### Func **GetPartNumber**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the product's part number.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's part number.  **Example:**      This example retrieves the `Engine` product's part number in the `Configuration1` scene.

```VBScript
        Dim PartNumber As String
        PartNumber = Configuration1.GetPartNumber(Engine)

```

### Func **GetPosition**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md)

   Returns the product's position object in the scene. The position object is the object aggregated by the product object that holds the position of the master shape representation in the space.

**Parameters:**

` iProduct`      The product

**Returns:**      The position.  **Example:**      This example retrieves the `EnginePosition` position from the `Engine` product in the `Configuration1` scene.

```VBScript
        Dim EnginePosition As Position
        Set EnginePosition = Configuration1.GetPosition(Engine)

```

### Func **GetRevision**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the product's revision number.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's revision number.  **Example:**      This example retrieves the `Engine` product's revision number in the `Configuration1` scene.

```VBScript
        Dim Revision As String
        Revision = Configuration1.GetRevision(Engine)

```

### Func **GetSource**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CatProductSource](../ProductStructureInterfaces/enum_CatProductSource_54902.md)

   Returns the product's source.

**Parameters:**

` iProduct`      The product.

**Returns:**      The product's source.  **Example:**      This example retrieves the `Engine` product's source in the `Configuration1` scene.

```VBScript
        Dim Source
        Source = Configuration1.GetSource(Engine)

```

### Func **HasAMasterShapeRepresentation**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As boolean

   Returns whether the product has a master shape representation in the scene.

**Parameters:**

` iProduct`      The product

**Returns:**      True if the product has a master shape representation.  **Example:**      This example returns whether the `Engine` product has a master shape representation in the `Configuration1` scene.

```VBScript
        HasMSRep = Configuration1.HasAMasterShapeRepresentation(Engine)

```

### Func **UpgradeToFull**( ) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Create a ProductScene in Full mode from the current Scene.

**Returns:**      The new ProductScene.  **Example:**      This example creates the `FullScene` ProductScene from the `Configuration1` scene.

```VBScript
        Dim FullScene As ProductScene
        Set FullScene = Configuration1.UpgradeToFull

```

### Func **UpgradeToPartial**( ) As [CATIAScene](../OSMInterfaces/interface_ProductScene_30810.md)

   Create a ProductScene in Partial mode from the current Scene.

**Returns:**      The new ProductScene.  **Example:**      This example creates the `PartialScene` ProductScene from the `Configuration1` scene.

```VBScript
        Dim PartialScene As ProductScene
        Set PartialScene = Configuration1.UpgradeToPartial

```

---

# SceneProductData (Object)

**_The interface to access a CATIASceneProduct

Using this prefered syntax will enable mkdoc to document your class._**

## Properties

### Property **Activation**( ) As boolean

   Returns / Set the scene product's activation state.

**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
        IsActivated = scenePrd.Hidden

```

### Property **Hidden**( ) As boolean

   Returns / Set the scene product's hide/show mode.

**Example:**      This example retrieves the hide/show mode of the `scenePrd` SceneProductData.

```VBScript
        IsHidden = scenePrd.Hidden

```

### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the scene product's move object. It aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves your product shape representation according to this isometry.

**Example:**      This example retrieves the `EngineMove` move in the `scenePrd` SceneProductData.

```VBScript
        Dim EngineMove As Move
        Set EngineMove = scenePrd.GetMove

```

### Property **Position**( ) As [CATIAPosition](../InfInterfaces/interface_Position_14692.md) (Read Only)

   Returns the scene product's position object. The position object is the object aggregated by the SceneProductData object that holds the position of the master shape representation in the space in scene.

**Example:**      This example retrieves the `EnginePosition` position in the `scenePrd` SceneProductData.

```VBScript
        Dim EnginePosition As Position
        Set EnginePosition = scenePrd.GetPosition

```

Methods

### Sub **GetRealColor**( long  `oRed`,  long  `oGreen`,  long  `oBlue`,  long  `oInheritance`)

   Returns / Set the scene product's color and inheritance.

**Parameters:**

` iRed`      A value between 0 and 255
` iGreen`      A value between 0 and 255
` iBlue`      A value between 0 and 255
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance

**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
    	Dim r, g, b, inh
        scenePrd.GetRealColor r, g, b, inh

```

### Sub **SetRealColor**( long  `iRed`,  long  `iGreen`,  long  `iBlue`,  long  `iInheritance`)

   Returns / Set the scene product's color and inheritance.

**Parameters:**

` iRed`      A value between 0 and 255
` iGreen`      A value between 0 and 255
` iBlue`      A value between 0 and 255
` iInheritance`      **Legal value:**

`0`     No heritance `1`     Heritance

**Example:**      This example retrieves the activation state of the `scenePrd` SceneProductData.

```VBScript
        scenePrd.SetRealColor 255,0,0,1

```

---

# Scenes (Collection)

**_A collection of scenes contained in a given ProductDocument._**

## Methods

### Func **AddCopyScene**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md)  `iReferenceScene`) As [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md)

   Creates a scene from another and adds it to the Scenes collection.

**Parameters:**

` iName`      The name of the scene
` iReferenceScene`      The scene to be copied

**Returns:**      The created scene  **Example:**      This example creates the `Engine` scene from the `SpareWheel` scene and adds the scene to the `ToolKits` collection.

```VBScript
        Dim Engine As Scene
        Set Engine = ToolKits.AddNewScene("Engine", SpareWheel)

```

### Func **AddNewScene**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`) As [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md)

   Creates a scene from a product and adds it to the Scenes collection.

**Parameters:**

` iName`      The name of the scene
` iReferenceProduct`      The product used as reference

**Returns:**      The created scene  **Example:**      This example creates the `SpareWheel` scene from the reference product `FrontRightWheel` and adds the scene to the `ToolKits` collection.

```VBScript
        Dim SpareWheel As Scene
        Set SpareWheel = ToolKits.AddNewScene("SpareWheel", FrontRightWheel)

```

### Sub **Remove**( [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md)  `iScene`)

   Removes a scene from the Scenes collection.

**Parameters:**

` iScene`      The scene to remove.

**Example:**      This example removes the `Engine` scene from the `ToolKits` collection.

```VBScript
        ToolKits.Remove Engine

```

---

# SceneWorkbench (Object)

**_Represent the access point to scenes management._**

## Properties

### Property **WorkScenes**( ) As [CATIAWorkScenes](../OSMInterfaces/interface_Scenes_8092.md) (Read Only)

   Returns the Scenes collection.

**Example:**      This example retrieves the WorkScenes collection of the active document.

```VBScript
        Dim TheWorkSceneWorkbench As Workbench
        Set TheWorkSceneWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SceneWorkbench" )
        Dim TheScenesList As WorkScenes
        Set TheScenesList = TheWorkSceneWorkbench.WorkScenes

```