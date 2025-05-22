# ArrangementNodes (Collection)

**_A Collection object for ArrangementNode objects._**
Use this object to access individual ArrangementNode objects of an ArrangementRun, ArrangementPathway and ArrangementBoundary.

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementNode](../CATArrangementInterfaces/interface_ArrangementNode_47648.md)

Returns the specified ArrangementNode item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementNode to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementNode in that collection.
Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementNode by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementNode object.