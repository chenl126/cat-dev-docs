# Scene (Object)

**_Represent the scene._**
A scene stores a state of a product in a given ProductDocument.

This state is composed of product properties, graphical attibutes, activation status and position for each component of the product.

## Methods

### Func **GetDefinition**(| [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iProduct`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

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