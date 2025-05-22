# FixTogether (Object)

**_The object that manages a sequence of products or fixTogethers._**

It belongs to the [FixTogether](../MecModInterfaces/interface_FixTogether_26387.md) collection of a [Product](../ProductStructureInterfaces/interface_Product_11223.md).

## Properties

### Property **FixTogethersCount**( ) As long (Read Only)

Returns the number of FixTogether entities in the FixTogether.

**Example:**     The following example retrieves in `fixTogethersCount` the number of FixTogethers of the `myFixTogether` FixTogether :

```VBScript
fixTogethersCount = myFixTogether.FixTogethersCount

```

### Property **ProductsCount**( ) As long (Read Only)

Returns the number of products fixed together in the FixTogether.

**Example:**     The following example retrieves in `productsCount` the number of products of the `myFixTogether` FixTogether :

```VBScript
productsCount = myFixTogether.ProductsCount

```

Methods

### Sub **AddFixTogether**( [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)  `iFixTogether`)

Add a fixTogether to a FixTogether. The fixTogether is fixed together with the products or fixTogethers already contained in the FixTogether.  **Example:**      The following example adds a FixTogether `fixTogether` in a FixTogether `myFixTogether`.

```VBScript
myFixTogether.AddFixTogether(fixTogether)

```

### Sub **AddProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

Add a product to a FixTogether. The product is fixed together with the products and fixTogethers already contained in the FixTogether.  **Example:**      The following example adds a Product `myProduct` in a FixTogether.

```VBScript
myFixTogether.AddProduct(myProduct)

```

### Func **GetFixTogether**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

Returns a FixTogether using its index or its name in the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to retrieve. As a numerics, this index is the rank of the FixTogether in the FixTogethers of the FixTogether. The index of the first FixTogether is 1, and the index of the last FixTogether is FixTogethersCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved FixTogether **Example:**      This example retrieves in `thisFixTogether` the fifth FixTogether and in `thatFixTogether` the FixTogether named `myFixTogether` in the FixTogethers of the FixTogether.

```VBScript
Dim thisFixTogether As FixTogether
Set thisFixTogether = myFixTogether.GetFixTogether(5)
Dim thatFixTogether As FixTogether
Set thatFixTogether = myFixTogether.GetFixTogether("myFixTogether")

```

### Func **GetProduct**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Returns a Product using its index or its name in the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the Product to retrieve. As a numerics, this index is the rank of the Product in the products of the FixTogether. The index of the first Product is 1, and the index of the last Product is ProductsCount. As a string, it is the name you assigned to the Product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Product **Example:**      This example retrieves in `thisProduct` the fifth Product and in `thatProduct` the Product named `myProduct` in the products of the FixTogether.

```VBScript
Dim thisProduct As Product
Set thisProduct = myFixTogether.GetProduct(5)
Dim thatProduct As Product
Set thatProduct = myFixTogether.GetProduct("myProduct")

```

### Sub **RemoveFixTogether**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a FixTogether from the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to remove from the FixTogether. As a numerics, this index is the rank of the FixTogether in the FixTogethers of the FixTogether. The index of the first FixTogether is 1, and the index of the last FixTogether is FixTogethersCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last FixTogether of the FixTogether.

```VBScript
fixTogether.RemoveFixTogether(fixTogether.FixTogethersCount)

```

### Sub **RemoveProduct**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a Product from the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the Product to remove from the FixTogether. As a numerics, this index is the rank of the Product in the products of the FixTogether. The index of the first Product is 1, and the index of the last Product is ProductsCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last Product of the FixTogether.

```VBScript
fixTogether.RemoveProduct(fixTogether.ProductsCount)

```