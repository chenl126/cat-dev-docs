# SchTempListFactory (Object)

**_Create temporary (non-persistent) lists to be used in VB environment._**

## Methods

### Func **CreateListOfBSTRs**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

This method returns a new empty list of strings.

**Returns:**      a empty list of strings.  **Example:**      This example illustrates how to create a new empty list of strings.

```VBScript
Dim SchListFact As SchTempListFactory
Dim NewList As SchListOfBSTRs
Set NewList = SchListFact.CreateListOfBSTRs

```

### Func **CreateListOfDoubles**( ) As [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)

This method returns a new empty list of doubles.

**Returns:**      a empty list of doubles.  **Example:**      This example illustrates how to create a new empty list of doubles.

```VBScript
Dim SchListFact As SchTempListFactory
Dim NewList As SchListOfDoubles
Set NewList = SchListFact.CreateListOfDoubles

```

### Func **CreateListOfLongs**( ) As [CATIASchListOfLongs](../CATSchPlatformInterfaces/interface_SchListOfLongs_40964.md)

This method returns a new empty list of long integers.

**Returns:**      a empty list of long integers.  **Example:**      This example illustrates how to create a new empty list of long integers.

```VBScript
Dim SchListFact As SchTempListFactory
Dim NewList As SchListOfLongs
Set NewList = SchListFact.CreateListOfLongs

```

### Func **CreateListOfObjects**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

This method returns a new empty list of objects.

**Returns:**      a empty list of objects.  **Example:**      This example illustrates how to create a new empty list of objects.

```VBScript
Dim SchListFact As SchTempListFactory
Dim NewList As SchListOfObjects
Set NewList = SchListFact.CreateListOfObjects

```