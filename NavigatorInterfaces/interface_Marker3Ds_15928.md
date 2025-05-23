# Marker3Ds (Collection)

**_A collection of Marker3D objects._**

The method [Product.GetTechnologicalObject](../ProductStructureInterfaces/interface_Product_11223.htm#GetTechnologicalObject) `("Marker3Ds")` on the root product retrieves this collection.

## Methods

### Func **Add3DText**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iTextCoordinates`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iText`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iObjectCoordinates`,| | [CATIABase](../System/interface_AnyObject_17321.md) | `iObject`) As [CATIAMarker3D](../NavigatorInterfaces/interface_Marker3D_12094.md)

   Creates a text marker 3D and adds it to the marker 3D collection. The bottom-left corner of the text is anchored to a given point.

**Parameters:**

` iTextCoordinates`      The coordinates of the text anchor point

  * iTextCoordinates(0) is the X coordinate of the text anchor point
  * iTextCoordinates(1) is the Y coordinate of the text anchor point
  * iTextCoordinates(2) is the Z coordinate of the text anchor point

` iText`      The text
` iObjectCoordinates`      The coordinates of the anchor of the marker 3D on the object

  * iObjectCoordinates(0) is the X coordinate of the object anchor point
  * iObjectCoordinates(1) is the Y coordinate of the object anchor point
  * iObjectCoordinates(2) is the Z coordinate of the object anchor point

` iObject`      The object which supports the text.

**Returns:**      The created marker 3D  **Example:**      This example creates a new marker 3D in the `TheMarker3Ds` collection.

```VBScript
        Dim NewMarker3DText As Marker3D
        Set NewMarker3DText = TheMarker3Ds.Add3DText(Position1, "example", Position2, Product2)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMarker3D](../NavigatorInterfaces/interface_Marker3D_12094.md)

   Returns a marker 3D using its index from the Marker3Ds collection.

**Parameters:**

` iIndex`      The index or the name of the marker 3D to retrieve from the collection of Marker3Ds. As a numerics, this index is the rank of the marker 3D in the collection. The index of the first Marker3D in the collection is 1, and the index of the last Marker3D is Count. As a string, it is the name you assigned to the Marker3D.

**Returns:**      The retrieved marker 3D  **Example:**      This example retrieves in `ThisMarker3D` the ninth marker 3D, and in `ThatMarker3D` the marker 3D named `Marker3D3` from the `TheMarker3Ds` collection.

```VBScript
        Dim ThisMarker3D As Marker3D
        Set ThisMarker3D = TheMarker3Ds.Item(9)
        Dim ThatMarker3D As Marker3D
        Set ThatMarker3D = TheMarker3Ds.Item("Marker3D3")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a marker 3D from the Marker3Ds collection.

**Parameters:**

` iIndex`      The index or the name of the marker 3D to retrieve from the collection of Marker3Ds. As a numerics, this index is the rank of the marker 3D in the collection. The index of the first marker 3D in the collection is 1, and the index of the last marker 3D is Count. As a string, it is the name you assigned to the marker 3D.

**Example:**      The following example removes the tenth marker 3D and the marker 3D named `Marker3D2` from the `TheMarker3Ds` collection.

```VBScript
        TheMarker3Ds.Remove(10)
        TheMarker3Ds.Remove("Marker3D2")

```