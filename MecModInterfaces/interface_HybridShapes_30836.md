# HybridShapes (Collection)

**_The collection of the HybridShapes making up a body._**

## Methods

### Func **GetBoundary**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

   Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)

   Returns a HybridShape using its index or its name from the HybridShapes collection.

**Parameters:**

` iIndex`      The index or the name of the HybridShape to retrieve from the collection of HybridShapes. As a numerics, this index is the rank of the HybridShape in the collection. The index of the first HybridShape in the collection is 1, and the index of the last HybridShape is
[Collection.Count](../System/interface_Collection_22150.htm#Count). As a string, it is the name you assigned to the HybridShape using the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved HybridShape  **Example:**      This example retrieves in `ThisHybridShape` the third HybridShape, and in `ThatHybridShape` the HybridShape named `MyHybridShape` in the HybridShape collection of the active document, supposed to be a part document.

```VBScript
     Set ThisHybridShape = CATIA.ActiveDocument.HybridShapes.Item(3)
     Set ThatHybridShape = CATIA.ActiveDocument.HybridShapes.Item("MyHybridShape")

```