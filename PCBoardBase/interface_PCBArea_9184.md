# PCBArea (Object)

**__**

## Properties

### Property **AreaType**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Allow to get the Type of a constraint area The possible values are : ROUTE_OUTLINE,

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **Heightmax**( ) As double

   Allow to get and set the Height max of the constraint area This property is valid for the following constraints areas: OTHER_OUTLINE, PLACE_REGION

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **Heightmin**( ) As double

   Allow to get and set the Height min of the constraint area This property is valid for the following constraints areas: PLACE_KEEPOUT

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **Identifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the Identifier of the constraint area This property is valid for the following constraints areas: OTHER_OUTLINE, PLACE_REGION

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **LAYER**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Allow to get the position of a hole The possible values are : TOP,BOTTOM,BOTH,INNER,ALL It depends on the the type of the constraints area according to the IDF format This property is valid for the following constraints areas: OTHER_OUTLINE, ROUTING_OUTLINE, PLACE_OUTLINE, ROUTE_KEEPOUT, PLACE_KEEPOUT, PLACE_REGION,

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **OWNER**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the OWNER of the constraint area The possible value are MCAD,ECAD, UNOWNED

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed