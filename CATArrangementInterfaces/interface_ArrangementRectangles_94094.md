# ArrangementRectangles (Collection)

**_A Collection object for ArrangementRectangle objects._**
**Role:** Use this object to manage (create, retrieve and remove) ArrangementRectangle objects.

## Methods

### Func **AddRectangle**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`,  double  `iWidth`,  double  `iLength`) As [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)

Creates an ArrangementRectangle and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the Rectangle (rotation and location).
` iWidth`      Width of the Rectangle.
` iLength`      Length of the Rectangle.
**Returns:**      Returns the newly created ArrangementRectangle and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)

Returns the specified ArrangementRectangle item of the collection object.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRectangle to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementRectangle in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementRectangle by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementRectangle object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes the specified ArrangementRectangle object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementRectangle to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementRectangle in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementRectangle by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.