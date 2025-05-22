# ProductDocument (Object)

**_Represents the Document object for product structures._**
When a ProductDocument is created, a root product is created whose parent is the ProductDocument object. Its default name is RootProduct, which can be overwritten thanks to the the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property. This root product is at the top of the product tree structure contained in the document. It has no difference with the other contained products, except it has no father product in the product tree structure within the document.

## Properties

### Property **Product**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

Returns the root product.

**Example:**      This example retrieves the root product of the `MyProductDoc` ProductDocument in `RootProduct`.

```VBScript
Dim RootProduct As Product
Set RootProduct = MyProductDoc.Product

```