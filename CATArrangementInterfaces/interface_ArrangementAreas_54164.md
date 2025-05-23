# ArrangementAreas (Collection)

**_A Collection object for ArrangementArea objects._**

**Role:** Use this interface to add, retrieve and remove ArrangementArea objects from this collection.

## Methods

### Func **AddArea**(| [CATIAMove](../InfInterfaces/interface_Move_3742.md) | `iRelAxis`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iPosition`,| | double | `iHeight`) As [CATIAArrangementArea](../CATArrangementInterfaces/interface_ArrangementArea_47127.md)

   Creates a ArrangementArea and adds it to the collection. The Area created will be without any contour. Hence only the height of the area is specified.

**Parameters:**

` iRelAxis`      Relative Axis to be considered.
` iPosition`      Position information for the Area (rotation and location).
` iHeight`      Height of the Area.

**Returns:**      The newly created ArrangementArea object that is also added to the collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrangementArea](../CATArrangementInterfaces/interface_ArrangementArea_47127.md)

   Returns the specified item of the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementArea to retrieve from this collection.

To retrieve a specific object by number, use the rank of the ArrangementArea in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To retrieve a specific ArrangementArea by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ArrangementArea object.

**Example:**      This example retrieves ArrangementArea, `objArea1`, of rank 1 under the ` Areas ` collection.

```VBScript
     Dim objArea1 As ArrangementArea
     Set objArea1= Areas.Item(1)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes the specified ArrangementArea object from the collection.

**Parameters:**

` iIndex`      The index or the name of the ArrangementArea to remove from this collection.

To remove a specific object by number, use the rank of the ArrangementArea in that collection.
   Note that the index of the first element in the collection is 1, and the index of the last element is Count.
To remove a specific ArrangementArea by name, use name that you assigned using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

**Example:**      This example removes ArrangementArea of rank 1 under the ` Areas ` collection.

```VBScript
     Areas.Remove(1)

```