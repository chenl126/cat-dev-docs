# PartDocument (Object)

**_Represents the Document object for parts._**

**Role** : When a PartDocument object is created, a Part object is also created. This Part object is the root object of the Part structure.

A reference Product object is also created in each PartDocument. It is used to access Publications, PartNumber.

**See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md), [Part](../MecModInterfaces/interface_Part_3788.md)

## Properties

### Property **Part**( ) As [CATIAPart](../MecModInterfaces/interface_Part_3788.md) (Read Only)

Returns the root Part object from the current part document.

**Example:**     The following example retrieves in `RootPart` the root Part object of the active document, assumed to be a part document:

```VBScript
Set RootPart = CATIA.ActiveDocument.Part

```

### Property **Product**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

Returns the root Product object from the current part document.

**Example:**     The following example retrieves in `RootProd` the root Product object of the active document, assumed to be a part document:

```VBScript
Set RootProd = CATIA.ActiveDocument.Part

```