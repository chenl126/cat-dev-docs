# AxisSystems (Collection)

**_A collection of all the AxisSystem objects contained in the part._**

## Methods

### Func **Add**( ) As [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)

Creates a new AxisSystem and adds it to the AxisSystems collection.

**Returns:**      The created AxisSystem  **Example:**      The following example creates a AxisSystem names `NewAxisSystem` in the AxisSystem collection of the `rootPart` part in the `partDoc` part document.

```VBScript
Set rootPart = partDoc.Part
Set NewAxisSystem = rootPart.AxisSystems.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)

Returns an Axis System using its index or its name from the AxisSystems collection.

**Parameters:**

` iIndex`      The index or the name of the AxisSystem to retrieve from the collection of AxisSystems. As a numerics, this index is the rank of the AxisSystem in the collection. The index of the first AxisSystem in the collection is 1, and the index of the last AxisSystem is Count. As a string, it is the name you assigned to the AxisSystem using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved AxisSystem **Example:**      This example retrieves in `ThisAxisSystem` the fifth AxisSystem in the collection and in `ThatAxisSystem` the AxisSystem named `MyAxisSystem` in the AxisSystem collection of the `partDoc` part document.

```VBScript
Set AxisSystemColl = partDoc.Part.AxisSystems
Set ThisAxisSystem = AxisSystemColl.Item(5)
Set ThatAxisSystem = AxisSystemColl.Item("MyAxisSystem")

```