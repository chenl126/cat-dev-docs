# ArrNomenclatures (Collection)

**_The collection of UserNomenclature objects._**

## Methods

### Func **AddUserNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIconName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iClassType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSuperType`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

Creates a new UserNomenclature and adds it to this collection. The NomenclatureType of the new UserNomenclature will be "User". The base objects in the UserDictionary are created when the UserDictionary is created.

**Parameters:**

` iName`      The user nomenclature name.
` iIconName`      The icon name associated to this nomenclature name.
**Returns:**      The new UserNomenclature.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

Returns the specified item of the collection

**Parameters:**

` iItem`      The list index (long) or name (CATBSTR) of the member to retrieve.
**Returns:**      The retrieved member object.