# ElecSchematicItf Framework

## Object Index

  * [ElecSchWire](ElecSchematicItf/interface_ElecSchWire_24996.md)
  * [ElecSchematicObject](ElecSchematicItf/interface_ElecSchematicObject_74447.md)

---

# ElecSchematicObject (Object)

**_Represents the electrical schematic objects._**

## Properties

### Property **ConnectedElecSchObjects**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) (Read Only)

   This method returns the collection of Electrical Schematic Connected Objects.  
### Property **ElecSchematicChildren**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) (Read Only)

   This method returns the collection of Electrical Schematic Object's Children (component in Pipe Line, Assembly).  
### Property **ElecSchematicParent**( ) As [CATIAElecSchematicObject](../ElecSchematicItf/interface_ElecSchematicObject_74447.md) (Read Only)

   This method returns the electrical schematic parent.  
### Property **IsSpaceReserved**( ) As boolean (Read Only)

   Defines if the electrical schematic object has a reservation box in 3D world  
### Property **RootType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the Electrical Schematic Object's Root Type (Equipment, Signal, Bundle, Wire).  
### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the Electrical Schematic Object's Type (Alternator, Signal, Bundle, Wire, ...).  Methods

### Func **GetPinAttribute**( [CATIAElecSchematicObject](../ElecSchematicItf/interface_ElecSchematicObject_74447.md)  `iConnectedObject`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttrName`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get the value of an attribute of the pin which connects this and the specified object.

---

# ElecSchWire (Object)

**_For technical electrical wire attributes._**

## Properties

### Property **Color**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Wire color