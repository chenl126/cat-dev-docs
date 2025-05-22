# ArrangementItemReservations (Collection)

**_A collection object for ArrangementItemReservation objects._**
**Role:** Use this collection object to manage (create, retrieve and remove) ArrangementItemReservation objects.

## Methods

### Func **AddItemReservation**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPosition`,  double  `iXMin`,  double  `iYMin`,  double  `iZMin`,  double  `iXMax`,  double  `iYMax`,  double  `iZMax`) As [CATIAArrangementItemReservation](../CATArrangementInterfaces/interface_ArrangementItemReservation_144876.md)

Creates an ArrangementItemReservation and adds it to the collection.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the ItemReservation (rotation and location).
` iXMin`      Minium X Coordinate of the bounding box on the Item Reservation.
` iYMin`      Minium Y Coordinate of the bounding box on the Item Reservation.
` iZMin`      Minium Z Coordinate of the bounding box on the Item Reservation.
` iXMax`      Maximum X Coordinate of the bounding box on the Item Reservation.
` iYMax`      Maximum Y Coordinate of the bounding box on the Item Reservation.
` iZMax`      Maximum Z Coordinate of the bounding box on the Item Reservation.
**Returns:**      Returns the newly created ArrangementItemReservation object and adds it to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementItemReservation](../CATArrangementInterfaces/interface_ArrangementItemReservation_144876.md)

Returns the specified ArrangementItemReservation item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementItemReservation to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementItemReservation in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementItemReservation by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementItemReservation object.  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

Removes the specified ArrangementItemReservation object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementItemReservation to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementItemReservation in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementItemReservation by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.