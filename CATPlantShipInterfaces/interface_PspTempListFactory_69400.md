# PspTempListFactory (Object)

**_Create temporary (non-persistent) lists to be used in VB environment._**
**Role** : Create lists in VB environment.

## Methods

### Func **CreateListOfBSTRs**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Returns a new empty list of strings.

**Returns:**      a empty list of strings.  **Example:**      This example illustrates how to create a new empty list of strings.

```VBScript
Dim PspListFact As PspTempListFactory
Dim NewList As PspListOfBSTRs
Set NewList = PspListFact.CreateListOfBSTRs

```

### Func **CreateListOfDoubles**( ) As [CATIAPspListOfDoubles](../CATPlantShipInterfaces/interface_PspListOfDoubles_53834.md)

Returns a new empty list of doubles.

**Returns:**      a empty list of doubles.  **Example:**      This example illustrates how to create a new empty list of doubles.

```VBScript
Dim PspListFact As PspTempListFactory
Dim NewList As PspListOfDoubles
Set NewList = PspListFact.CreateListOfDoubles

```

### Func **CreateListOfLongs**( ) As [CATIAPspListOfLongs](../CATPlantShipInterfaces/interface_PspListOfLongs_41364.md)

Returns a new empty list of long integers.

**Returns:**      a empty list of long integers.  **Example:**      This example illustrates how to create a new empty list of long integers.

```VBScript
Dim PspListFact As PspTempListFactory
Dim NewList As PspListOfLongs
Set NewList = PspListFact.CreateListOfLongs

```

### Func **CreateListOfObjects**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

Returns a new empty list of objects.

**Returns:**      a empty list of objects.  **Example:**      This example illustrates how to create a new empty list of objects.

```VBScript
Dim PspListFact As PspTempListFactory
Dim NewList As PspListOfObjects
Set NewList = PspListFact.CreateListOfObjects

```