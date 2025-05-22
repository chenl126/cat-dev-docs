# ThreeDCuts (Collection)

**_Interface to compute 3D cuts_**

## Methods

### Sub **Compute3DCut**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `ThreeDCutDocument`)

Computes the 3DCut on the selected products.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
**Returns:**      ThreeDCutDocument: Document containing the result.  
### Sub **Compute3DCutWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `ThreeDCutDocument`)

Computes the 3DCut on the selected products, according to a reference product.

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iReferenceProduct`      Product taken as a reference.
**Returns:**      ThreeDCutDocument: Document containing the result.  
### Func **GetCompute3DCut**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes the 3DCut on the selected products (better signature).

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
**Returns:**      ThreeDCutDocument: Document containing the result.  
### Func **GetCompute3DCutWithAReference**( [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)  `GroupOfSelectedProducts`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iReferenceProduct`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

Computes the 3DCut on the selected products, according to a reference product (better signature).

**Parameters:**

` GroupOfSelectedProducts`      The selected products on which you want to perform the 3D cut.
` iReferenceProduct`      Product taken as a reference.
**Returns:**      ThreeDCutDocument: Document containing the result.  
### Sub **SetBox**( double  `OriginX`,  double  `OriginY`,  double  `OriginZ`,  double  `VX`,  double  `VY`,  double  `VZ`)

Sets the RELATIVE box used for the 3D cut computation.
Be aware of the behavior:

```VBScript
       Vz
      ^_________________
     /|               /|
    /                / |
   /  |             /  |
  /                /   |
 /----+-----------/    |
 |                |    |
 |    |       *   |    |
 |            O   |    |
 |    |           |    |
 |                |    |
 |    |           |    |
 |    * - - - - - + - -|> Vy
 |    Origin      |   /
 |  /             |  /
 |                | /
 |/               |/
 /----------------/
<
 Vx

```

In the relative referential, O is (0,0,0)

This method sets the RELATIVE box : the rotation and translation matrix will then set the absolute position of O.
Remember where the center of the relative referential lies !
Can have unexpected results if you don't use it properly.

**Parameters:**

` OriginX`      Origin coordinate (X)
` OriginY`      Origin coordinate (Y)
` OriginZ`      Origin coordinate (Z)
` VX`      Length of the box (along X)
` VY`      Length of the box (along Y)
` VZ`      Length of the box (along Z)

### Sub **SetMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iComponents`)

Sets the rotation AND translation matrix.
Beware : After a SetBox, the matrix is not changed.

**Parameters:**

` iComponents`      Components of the 4x4 matrix, placed in rows.

### Sub **SetOnBorders**( long  `OnBorders`)

Sets the behavior on borders.

**Parameters:**

` Type`      0 : We keep partially included triangles
1 : We keep entirely included triangles

### Sub **SetType**( long  `Type`)

Sets the type of cut we're doing.

**Parameters:**

` Type`      0 : We keep the inner triangles
1 : We keep the outer triangles

### Sub **ThreeDCutShapeName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `Name`)

Returns the name of the associated shape.