# Shapes (Collection)

**_The collection of the shapes making up a body._**

## Methods

### Func **GetBoundary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAShape](../MecModInterfaces/interface_Shape_5555.md)

Returns a shape using its index or its name from the Shapes collection.

**Parameters:**

` iIndex`      The index or the name of the shape to retrieve from the collection of shapes. As a numerics, this index is the rank of the shape in the collection. The index of the first shape in the collection is 1, and the index of the last shape is
[Collection.Count](../System/interface_Collection_22150.htm#Count). As a string, it is the name you assigned to the shape using the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved shape  **Example:**      This example retrieves in `ThisShape` the third shape, and in `ThatShape` the shape named `MyShape` in the shape collection of the active document, supposed to be a part document.

```VBScript
Set ThisShape = CATIA.ActiveDocument.Shapes.Item(3)
Set ThatShape = CATIA.ActiveDocument.Shapes.Item("MyShape")

```