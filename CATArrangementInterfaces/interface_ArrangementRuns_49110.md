# ArrangementRuns (Collection)

**_A collection object of ArrangementRun objects._**

**Role:** Use this collection object to manage ArrangementRun objects.

## Methods

### Func **AddRun**(| [CATIAMove](../InfInterfaces/interface_Move_3742.md) | `iRelAxis`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iListofMathPoints`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iMathDirection`) As [CATIAArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md)

   Creates an ArrangementRun and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iListofMathPoints`      List of points through which to route.
` iMathDirection`      Starting routing direction.

**Returns:**      Returns the newly created ArrangementRun object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementRun](../CATArrangementInterfaces/interface_ArrangementRun_42486.md)

   Returns the specified ArrangementRun item of the collection object.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRun to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementRun in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementRun by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementRun object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementRun object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRun to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementRun in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementRun by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.