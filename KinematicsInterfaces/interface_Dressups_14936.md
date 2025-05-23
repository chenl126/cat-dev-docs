# Dressups (Collection)

**_A collection of all Dressup entities currently managed by the application._**

## Methods

### Func **Add**(| [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md) | `iMechanism`,| | [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) | `iContext`) As [CATIADressup](../KinematicsInterfaces/interface_Dressup_11434.md)

   Creates a new Dressup and adds it to the Dressups collection.

**Parameters:**

` iMechanism`      The mechanism on which the dressup will apply.
` iContext`      The Context product on which the mechanism is defined

**Returns:**      The created Dressup  **Example:**      This example creates a new Dressup in the `TheDressups` collection.

```VBScript
        Dim NewDressup As Dressup
        Set NewDressup = TheDressups.Add(Mechanism)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADressup](../KinematicsInterfaces/interface_Dressup_11434.md)

   Returns a Dressup using its index or its name from the Dressups collection.

**Parameters:**

` iIndex`      The index or the name of the Dressup to retrieve from the collection of Dressups. As a numerics, this index is the rank of the Dressup in the collection. The index of the first Dressup in the collection is 1, and the index of the last Dressup is Count. As a string, it is the name you assigned to the Dressup using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Dressup  **Example:**      This example returns in `ThisDressup` the third Dressup in the collection, and in `ThatDressup` the Dressup named `MyDressup`.

```VBScript
     Dim ThisDressup As Dressup
     Set ThisDressup = TheDressups.Item(3)
     Dim ThatDressup As Dressup
     Set ThatDressup = CATIA.Dressups.Item("MyDressup")

```

### Func **ListMechanismsContext**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Each mechanism of the list given by ListPossibleMechanisms has a context product on which it is defined.

**Parameters:**

` Nothing`

**Returns:**      The list of mechanisms' contexts on which a dressup can be created. The context of oMechanismList(i) is oContextList(i).  **Example:**      The following example returns the first and the last element of the list of mechanisms' contexts. We assume that this list contains at least two values.

```VBScript
        Dim ContextList As Product
        ContextList = MyDressups.ListMechanismsContext()
        Dim FirstContext As Product
        Set FirstContext = ContextList(0)
        Dim LastContext As Product
        Set LastContext = ContextList(ubound(ContextList))

```

### Func **ListPossibleMechanisms**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns information about all possible mechanisms on which a dressup can be created.

**Parameters:**

` Nothing`

**Returns:**      The list of possible mechanisms on which a dressup can be created.  **Example:**      The following example returns the first and the last element of the list of possible mechanisms. We assume that this list contains at least two values.

```VBScript
        Dim PossibleMecList As Mechanism
        PossibleMecList = MyDressups.ListPossibleMechanisms()
        Dim FirstMeca As Mechanism
        Set Meca  = PossibleMecList(0)
        Dim LastMeca As Mechanism
        Set Meca  = PossibleMecList(ubound(PossibleMecList))

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Dressup from the Dressups collection.

**Parameters:**

` iIndex`      The index or the name of the Dressup to retrieve from the collection of Dressups. As a numerics, this index is the rank of the Dressup in the collection. The index of the first Dressup in the collection is 1, and the index of the last Dressup is Count. As a string, it is the name you assigned to the Dressup.

**Returns:**      Nothing  **Example:**      The following example removes the tenth Dressup and the Dressup named `DressupTwo` from the `TheDressups` collection.

```VBScript
        TheDressups.Remove(10)
        TheDressups.Remove("DressupTwo")

```