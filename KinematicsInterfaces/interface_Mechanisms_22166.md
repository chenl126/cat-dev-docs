# Mechanisms (Collection)

**_A collection of all Mechanism entities currently managed by the application._**

## Methods

### Func **Add**( ) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)

Creates a new Mechanism and adds it to the Mechanisms collection.

**Returns:**      The created Mechanism  **Example:**      This example creates a new Mechanism in the `TheMechanisms` collection.

```VBScript
   Dim NewMechanism As Mechanism
   Set NewMechanism = TheMechanisms.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)

Returns a Mechanism using its index or its name from the Mechanisms collection.

**Parameters:**

` iIndex`      The index or the name of the Mechanism to retrieve from the collection of Mechanisms. As a numerics, this index is the rank of the Mechanism in the collection. The index of the first Mechanism in the collection is 1, and the index of the last Mechanism is Count. As a string, it is the name you assigned to the Mechanism using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Mechanism  **Example:**      This example returns in `ThisMechanism` the third Mechanism in the collection, and in `ThatMechanism` the Mechanism named `MyMechanism`.

```VBScript
Dim ThisMechanism As Mechanism
Set ThisMechanism = TheMechanisms.Item(3)
Dim ThatMechanism As Mechanism
Set ThatMechanism = CATIA.Mechanisms.Item("MyMechanism")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes a Mechanism from the Mechanisms collection.

**Parameters:**

` iIndex`      The index or the name of the Mechanism to retrieve from the collection of mechanisms. As a numerics, this index is the rank of the Mechanism in the collection. The index of the first Mechanism in the collection is 1, and the index of the last Mechanism is Count. As a string, it is the name you assigned to the Mechanism.
**Returns:**      Nothing  **Example:**      The following example removes the tenth Mechanism and the Mechanism named `MechanismTwo` from the `TheMechanisms` collection.

```VBScript
   TheMechanisms.Remove(10)
   TheMechanisms.Remove("MechanismTwo")

```