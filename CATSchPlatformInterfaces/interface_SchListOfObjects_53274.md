# SchListOfObjects (Object)

**_Represent a non-persistant list of schematic objects._**

## Properties

### Property **Count**(| ) As long (Read Only)

   Returns the number of objects in the list.

**Example:**      This example retrieves in `NumberOfObjects` the number of objects currently gathered in `MyList`.

```VBScript
     NumberOfObjects = MyList.Count

```

Methods

### Sub **Append**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Adds an object to the end of the list.

**Parameters:**

` iObject`      The object to be added to the list.

**Example:**      The following example appends an object to the list.

```VBScript
     Dim MyObject As AnyObject
     Dim MyList As SchListOfObjects
     MyList.Append(MyObject)

```

### Func **Item**( long  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns an object from its index in the list.

**Parameters:**

` iIndex`      The index of the first object in the collection is 1, and the index of the last object is Count.
` iInterfaceName`      The interface name of oObj.

**Returns:**      the retrieved object.  **Example:**      The following example returns in the third object in the list.

```VBScript
     Dim MyObject As AnyObject
     Dim MyList As SchListOfObjects
     Set MyObject = SchListOfObjects.Item(2,"CATIASchComponent")

```

### Sub **RemoveByIndex**( long  `iIndex`)

   Remove an object from the list by specifying its position in the list.

**Parameters:**

` iIndex`      The position of the object to be removed in the list.

**Example:**      The following example removes the second entry in the list. Please note that the list index starts with 1.

```VBScript
     Dim MyList As SchListOfObjects
     MyList.Remove(1)

```