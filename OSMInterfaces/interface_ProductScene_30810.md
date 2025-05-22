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