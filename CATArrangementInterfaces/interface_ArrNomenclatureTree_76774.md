# ArrNomenclatureTree (Object)

**_Represents the root User Dictionary object._**
The user dictionary defines a hierarchy of user object type names used for dynamically classifying objects. These type names are defined by the user organization according to the needs of the disciplines represented in the data. The user type of any object may be changed as the data becomes more precise. The hierarchy of type names starts with base names, defined by the system, for each type of object. The user organization may define or change the hierarchy of type names under each base name.

## Properties

### Property **BaseNomenclatures**(| ) As [CATIAArrNomenclatures](../CATArrangementInterfaces/interface_ArrNomenclatures_55994.md) (Read Only)

   Returns the collection of BaseNomenclatures within this UserDictionary.  Methods

### Func **GetNomenclature**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeName`) As [CATIAArrNomenclature](../CATArrangementInterfaces/interface_ArrNomenclature_48920.md)

   Finds a UserNomenclature by Name from this UserDictionary.