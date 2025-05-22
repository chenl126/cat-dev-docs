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