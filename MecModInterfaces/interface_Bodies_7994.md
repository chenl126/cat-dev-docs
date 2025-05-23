# Bodies (Collection)

**_A collection of all the Body objects contained in the part._**

## Methods

### Func **Add**(| ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

   Creates a new body and adds it to the Bodies collection. This body becomes the current one

**Returns:**      The created body  **Example:**      The following example creates a body names `NewBody` in the body collection of the `rootPart` part in the `partDoc` part document. `NewBody` becomes the current body in `partDoc`.

```VBScript
     Set rootPart = partDoc.Part
     Set NewBody = rootPart.Bodies.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

   Returns a body using its index or its name from the Bodies collection.

**Parameters:**

` iIndex`      The index or the name of the body to retrieve from the collection of bodies. As a numerics, this index is the rank of the body in the collection. The index of the first body in the collection is 1, and the index of the last body is Count. As a string, it is the name you assigned to the body using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved body **Example:**      This example retrieves in `ThisBody` the fifth body in the collection and in `ThatBody` the body named `MyBody` in the body collection of the `partDoc` part document.

```VBScript
     Set BodyColl = partDoc.Part.Bodies
     Set ThisBody = BodyColl.Item(5)
     Set ThatBody = BodyColl.Item("MyBody")

```