# HybridBodies (Collection)

**_A collection of the HybridBody objects._**

## Methods

### Func **Add**(| ) As [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)

   Creates a new hybrid body and adds it to the HybridBodies collection. This body becomes the current one

**Returns:**      The created body  **Example:**      The following example creates a body named `newHybridBody` in the hybrid body collection of the `rootPart` part in the `partDoc` part document. `NewPartBody` becomes the current body in `partDoc`.

```VBScript
     Set NewPartBody = rootPart.Bodies.AddPartBody()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)

   Returns a body using its index or its name from the Bodies collection.

**Parameters:**

` iIndex`      The index or the name of the hybrid body to retrieve from the collection of hybrid bodies. As a numerics, this index is the rank of the hybrid body in the collection. The index of the first hybrid body in the collection is 1, and the index of the last hybrid body is Count. As a string, it is the name you assigned to the hybrid body using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved hybrid body **Example:**      This example retrieves in `ThisHybridBody` the fifth hybrid body in the collection and in `ThatHybridBody` the hybrid body named `MyHybridBody` in the hybrid body collection of the `partDoc` part document.

```VBScript
     Set hybridBodyColl = partDoc.Part.HybridBodies
     Set ThisHybridBody = hybridBodyColl.Item(5)
     Set ThatHybridBody = hybridBodyColl.Item("MyHybridBody")

```