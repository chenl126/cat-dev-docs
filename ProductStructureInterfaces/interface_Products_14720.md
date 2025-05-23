# Products (Collection)

**_The collection of the Product objects contained in a given Product object of a ProductDocument object._**
A Product object can aggregate one or zero Products collection.

## Methods

### Func **AddComponent**(| [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iReferenceProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component and adds it to the Products collection. A component is a Product object created from another Product object used as reference.

**Parameters:**

` iReferenceProduct`      The product used as reference

**Example:**      The following example creates the `SpareWheel` component from the reference product `FrontRightWheel` and adds the component to the `ToolKits` collection.

```VBScript
     Dim SpareWheel As Product
     Set SpareWheel = ToolKits.AddComponent(FrontRightWheel)

```

### Sub **AddComponentsFromFiles**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iFilesList`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMethod`)

   Creates a component for each file. The components are added to the Products collection.

**Parameters:**

` iFilesList`      The paths of the files used to retrieve the reference or the shape of th component
` iMethod`      A string describing the expected type of the files

### Func **AddExternalComponent**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iProductDocument`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component from the root product of another ProductDocument object. This root product is used as a reference to create the component. The component is added to the Products collection.

**Parameters:**

` iProductDocument`      The product document whose root object is to be used as reference to create the component

**Example:**      The following example creates the `GearBox` component by referencing the `GearBoxDocument` and adds it to the `PowerTrains` collection.

```VBScript
     Dim GearBox As Product
     Set GearBox = PowerTrains.AddExternalComponent(GearBoxDocument)

```

### Func **AddNewComponent**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumenType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component from the root product of a new ProductDocument object. This root product is used as a reference to create the component. The component is added to the Products collection.

**Parameters:**

` iProductDocument`      The product document whose root object is to be used as reference to create the component

**Example:**      The following example creates the `GearBox` component by referencing the `GearBoxDocument` and adds it to the `PowerTrains` collection.

```VBScript
     Dim GearBox As Product
     Set GearBox = PowerTrains.AddNewComponent(GearBoxDocument, "A120-253X-7")

```

### Func **AddNewProduct**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a Product reference object. This creates a Product reference object and the associated component by specifying its type and adds it to the Products collection.

**Parameters:**

` iPartNumber`      The part number of the product to be created and added to the to the collection

**Example:**      The following example creates the `Engine` product and adds the created component to the `PowerTrains` collection.

```VBScript
     Dim Engine As Product
     Set Engine = PowerTrains.AddNewProduct(V6Engine)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns a product from its index in the Products collection.

**Parameters:**

` iIndex`      The index of the product to retrieve in the collection of products. This index can either be the rank of the product in the collection or the name you assign to the product. As a numerics, this index is the rank of the product in the collection. The index of the first product in the collection is 1, and the index of the last product is Count. As a string, it is the name you assigned to the product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Returns:**      The retrieved product  **Example:**      The following example returns in `ThisProduct` the third product, and in `ThatProduct` the product named `Wheel` in the `CarParts` product collection.

```VBScript
     Dim ThisProduct As Product
     Set ThisProduct = CarParts.Item(3)
     Dim ThatProduct As Product
     Set ThatProduct = CarParts.Item("Wheel")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a product from the Products collection.

**Parameters:**

` iIndex`      The index of the product to remove. This index can either be the rank of the product in the collection or the name you assigned to the product. As a numerics, this index is the rank of the product in the collection. The index of the first product in the collection is 1, and the index of the last product is Count. As a string, it is the name you assigned to the product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property  **Example:**      The following example removes the sixth product and the product named `LeftRearDisc` from the `Brakes` product collection.

```VBScript
     Brakes.Remove(6)
     Brakes.Remove("LeftRearDisc")

```

### Func **ReplaceComponent**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iOldComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilePath`,  boolean  `iMultiInstances`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component which replace the given one.

**Parameters:**

` iOldComponent`      The component which will be replaced
` iFilePath`      the document to replace with
` oNewComponent`      the component replacing iOldComponent

### Func **ReplaceProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iOldComponent`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iNewReference`,  boolean  `iMultiInstances`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Creates a component which replace the given one.

**Parameters:**

` iOldComponent`      The component which will be replaced
` iNewReference`      the reference whom the old copmponent will be reconnected
` oNewComponent`      the component replacing iOldComponent