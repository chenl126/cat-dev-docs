# ArrangementContours (Collection)

**_A collection object for ArrangementContours of an Area._**
**Role:** Use this to manage (create, retrieve and remove) ArrangementContours of an ArrangementArea.

## Methods

### Func **AddRectangularContour**( [CATIAArrangementRectangle](../CATArrangementInterfaces/interface_ArrangementRectangle_84792.md)  `iRectangle`) As [CATIAArrangementContour](../CATArrangementInterfaces/interface_ArrangementContour_70746.md)

Creates a Rectangular Contour by adding a ArrangementRectangle to the collection.

**Parameters:**

` iRectangle`      ArrangementRectangle to create the contour from.
**Returns:**      Returns the newly created ArrangementContour object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementContour](../CATArrangementInterfaces/interface_ArrangementContour_70746.md)

Returns the specified ArrangementContour item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementContour to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementContour in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementContour by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementContour object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes the specified ArrangementContour object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementContour to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementContour in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementContour by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.