# MechanismCommands (Collection)

**_A collection of all MechanismCommand entities currently managed by the application._**

## Methods

### Func **Add**(| ) As [CATIAMechanismCommand](../KinematicsInterfaces/interface_MechanismCommand_53914.md)

   Creates a new MechanismCommand and adds it to the MechanismCommands collection.

**Returns:**      The created MechanismCommand  **Example:**      This example creates a new MechanismCommand in the `TheCommands` collection.

```VBScript
        Dim NewCommand As MechanismCommand
        Set NewCommand = TheCommands.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMechanismCommand](../KinematicsInterfaces/interface_MechanismCommand_53914.md)

   Returns a MechanismCommand using its index or its name from the Commands collection.

**Parameters:**

` iIndex`      The index or the name of the MechanismCommand to retrieve from the collection of Commands. As a numerics, this index is the rank of the MechanismCommand in the collection. The index of the first MechanismCommand in the collection is 1, and the index of the last MechanismCommand is Count. As a string, it is the name you assigned to the MechanismCommand using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved MechanismCommand  **Example:**      This example returns in `ThisCommand` the third MechanismCommand in the collection, and in `ThatCommand` the MechanismCommand named `MyCommand`.

```VBScript
     Dim ThisCommand As MechanismCommand
     Set ThisCommand = TheCommands.Item(3)
     Dim ThatCommand As MechanismCommand
     Set ThatCommand = CATIA.MechanismCommands.Item("MyCommand")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Remove a MechanismCommand from the MechanismCommands collection.

**Parameters:**

` iIndex`      The index or the name of the MechanismCommand to retrieve from the collection of MechanismCommands. As a numerics, this index is the rank of the MechanismCommand in the collection. The index of the first MechanismCommand in the collection is 1, and the index of the last MechanismCommand is Count. As a string, it is the name you assigned to the MechanismCommand.

**Returns:**      Nothing  **Example:**      The following example removes the tenth MechanismCommand and the MechanismCommand named `CommandTwo` from the `TheCommands` collection.

```VBScript
        TheCommands.Remove(10)
        TheCommands.Remove("CommandTwo")

```