# Scenes (Collection)

**_A collection of scenes contained in a given ProductDocument._**

## Methods

### Func **AddCopyScene**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iName`,| | [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md) | `iReferenceScene`) As [CATIAWorkScene](../OSMInterfaces/interface_Scene_5528.md)

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