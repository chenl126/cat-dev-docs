# PCBHoleAndPattern (Object)

**__**

## Properties

### Property **AssociatedPartName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Allow to get and set the Associated Part of a hole The possible values are : the name of the instance of component in which the hole is defined. BOARD if the hole is defined in the Board part PANEL If the hole is defined in the Panel part NOREFDES is the hole is defined in a non Electronic Part.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **HoleOwner**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Allow to get and set the Operating power rating of a component The possible value are MCAD,ECAD, UNOWNED

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **HoleType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Allow to get and set the function of the hole The differents values are : PIN if the hole is associated with a component pin VIA if the hole is associated with a conductive via MTG if the hole is used for mounting purposes TOOL if the hole is used for tooling purposes Other ( User defined )

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **PlatingStyle**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Allow to get and set the Plating Style of a hole The possible values are : PTH, NPTH

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed