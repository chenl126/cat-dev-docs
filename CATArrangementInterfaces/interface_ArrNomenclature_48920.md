# ArrNomenclature (Object)

**_Represents the UserNomenclature object._**
The UserNomenclature object is used in the CATIAArrNomenclatureTree object to maintain the hierarchy of user type names and associated icons. CATIAArrNomenclatureTree | |_______ Area - (I_ArrArea) | |_______ Building - (I_ArrBuilding) | |_______ Safety Zone - (I_ArrSafetyZone) | |-------- Run - (I_ArrRun) | |_______ Conduit Run |_______ Raceway Run In the diagram shown above, Area (along with its subtypes) and and Run (also along with it's subtypes) are all UserNomenclature objects. Entries such as the Area and Run are called System or SuperClass objects that have to be defined first before the subclasses such as Building and Safety Zone are defined. SuperClasses will not have a supertype. Each Nomenclature holds the following information... (1) NLSName - So as to support names in different languages (2) IconName - So as to allow user's to define their own icons (3) SuperType - For subtypes to fetch their parent names (4) SubTypes - SubTypes defined under this User Nomenclature

## Properties

### Property **IconName**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the Icon Name associated to the Type Name. The IconName is the file name, without the extension, of the Icon bitmap representing this user type. The icon definition file must be in one of the icon directories defined in the search paths used by CATIA.  
### Property **IntSysClassName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the internal class names for System nomenclatures. This value is set only for System nomenclatures  
### Property **NLSInstanceName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets/Sets the InstanceName  
### Property **SubTypes**( ) As [CATIAArrNomenclatures](../CATArrangementInterfaces/interface_ArrNomenclatures_55994.md) (Read Only)

   Returns the collection of subtype UserNomenclatures within this UserNomenclature.  
### Property **SuperTypeName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get/Set the Supertype Information This property is used to set the subtypes for system classes  Methods

### Func **IsSystemNomenclature**( ) As boolean

   Returns TRUE if the nomenclature happens to be a system nomenclature. Returns FALSE if it is a user specified nomenclature.