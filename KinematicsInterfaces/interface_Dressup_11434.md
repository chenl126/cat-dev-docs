# Dressup (Object)

**_Interface to access the Dressup object._**

## Properties

### Property **Context**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

Returns the context product on which the mechanism is defined. This property is read only.

**Returns:**      The dressup mechanism's context  **Example:**      This example sets in `MecaContext` the context product of `MyDressup`.

```VBScript
   Dim MecaContext As Product
   Set MecaContext = MyDressup.Context

```

### Property **Mechanism**( ) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md) (Read Only)

Returns the mechanism on which a dressup is applied. This property is read only.

**Returns:**      The dressup's mechanism  **Example:**      This example sets in `Meca` the mechanism of `MyDressup`.

```VBScript
 Dim Meca As Mechanism
 Set Meca = MyDressup.Mechanism

```

Methods

### Sub **Attach**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLink`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iAttachedProd`)

Attaches a given product to a link of the mechanism pointed by the dressup.

**Parameters:**

` iLink`      The link (Product) on which the attachment should be done. It should be a product that belongs to the mechanism pointed by the dressup, otherwise the method will fail.
` iAttachedProd`      The Product that will be attached to the link. This product should not be a product that is already attached by another link, otherwise the method will fail.
**Returns:**      Nothing  **Example:**      This example attaches inside `MyDressup`, `Link1` as mechanism's part to `Product1`.

```VBScript
   Dim Link1 As Product
   Dim Product1 As Product
   ...
   MyDressup.Attach(Link1,Product1)

```

### Sub **Detach**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iAttachedProd`)

Detaches an attached product from its link.

**Parameters:**

` iAttachedProd`      The Product that will be detached. It should be a product that is currently attached in the dressup, otherwise the method will fail.
**Returns:**      Nothing  **Example:**      This example detaches `Product1` previously attached to a mechanism's part inside `MyDressup`.

```VBScript
   Dim Product1 As Product
   ...
   MyDressup.Detach(Product1)

```

### Func **ListAttached**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLink`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

Returns the list of products attached to a given link.

**Parameters:**

` iLink`      The Product on which the returned product list is attached to.
**Returns:**      The Product list that is attached to iLink.  **Example:**      The following example loops for all the products attached to `Link1`.

```VBScript
   Dim ListAttached1 as Product
   ListAttached1 = MyDressup.ListAttached(Link1)
   Dim Maxi as Integer
   Set Maxi = ubound(ListAttached1)
   Dim Prod_i as Product
   For i = 0  To  Maxi
      Set Prod_i = ListAttached1(i)
      ..
   Next

```