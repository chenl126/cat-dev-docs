# ArrangementBoundaries (Collection)

**_A collection object for ArrangementBoundary objects._**

**Role:** This collection object is used to manage (create, retrieve and remove )ArrangementBoundary objects.

## Methods

### Func **AddBoundary**(| [CATIAMove](../InfInterfaces/interface_Move_3742.md) | `iRelAxis`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iListofMathPoints`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iMathDirection`) As [CATIAArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md)

   Creates an ArrangementBoundary and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iListofMathPoints`      List of points through which to route.
` iMathDirection`      Starting routing direction.

**Returns:**      The newly created ArrangementBoundary object.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementBoundary](../CATArrangementInterfaces/interface_ArrangementBoundary_77900.md)

   Returns the specified ArrangementBoundary item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementBoundary to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementBoundary in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementBoundary by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementBoundary object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementBoundary object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementBoundary to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementBoundary in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementBoundary by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.