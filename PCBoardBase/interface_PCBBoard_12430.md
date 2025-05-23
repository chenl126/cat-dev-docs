# PCBBoard (Object)

**__**

## Properties

### Property **Owner**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the attribute owner of a Panel or a Board The possible values are MCAD, ECAD, UNKNOWN

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **Part**( ) As [CATIAPad](../PartInterfaces/interface_Pad_1979.md)

   set the pad of a Board or a component or a panel.  Methods

### Sub **create_pcbhole**( [CATIAHole](../PartInterfaces/interface_Hole_3612.md)  `iHole`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iplatingStyle`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAssociatedPartName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iHoleType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iHoleOwner`)

   This method allows to add a Pcb hole to a board or a panel.

**Parameters:**

` iHole`      This parameter represents the hole to transform in Pcb hole
` iplatingStyle`      This parameter represents the plating style of the hole. The differents values are PTH or NPTH
` iAssociatedPartName`      This parameter represents name of the associated part to the hole. The possible values are : the name of the instance of component in which the hole is defined. BOARD if the hole is defined in the Board part PANEL If the hole is defined in the Panel part NOREFDES is the hole is defined in a non Electronic Part.
` iHoleType`      This parameter represents the function of the hole. The differents values are : PIN if the hole is associated with a component pin VIA if the hole is associated with a conductive via MTG if the hole is used for mounting purposes TOOL if the hole is used for tooling purposes Other ( User defined )
` iHoleOwner`      The parameter represents the owner of the hole. The possible values are : MCAD, ECAD, UNOWNED

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Sub **create_pcbpattern**( [CATIAPattern](../PartInterfaces/interface_Pattern_11228.md)  `iPattern`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iplatingStyle`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAssociatedPartName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iHoleType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iHoleOwner`)

   This method allows to add a Pcb pattern of hole to a board or a panel. If the motif hole of the pattern is pcb hole, the input value are not taken into account

**Parameters:**

` iPattern`      This parameter represents the Pattern to transform in Pcb Pattern
` iplatingStyle`      This parameter represents the plating style of the hole. The differents values are PTH or NPTH
` iAssociatedPartName`      This parameter represents name of the associated part to the hole. The possible values are : the name of the instance of component in which the hole is defined. BOARD if the hole is defined in the Board part PANEL If the hole is defined in the Panel part NOREFDES is the hole is defined in a non Electronic Part.
` iHoleType`      This parameter represents the function of the hole. The differents values are : PIN if the hole is associated with a component pin VIA if the hole is associated with a conductive via MTG if the hole is used for mounting purposes TOOL if the hole is used for tooling purposes Other ( User defined )
` iHoleOwner`      The parameter represents the owner of the hole. The possible values are : MCAD, ECAD, UNOWNED

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Sub **create_zone**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `zonetype`,  [CATIAPad](../PartInterfaces/interface_Pad_1979.md)  `iPad`)

   This method allows to add a constraint area to a board.

**Parameters:**

` zonetype`      This parameter represents the type of the zone to create The differents values are ROUTE_OUTLINE, PLACE_OUTLINE, OTHER_OUTLINE, VIA_KEEPOUT, PLACE_KEEPOUT, PLACE_REGION, ROUTE_KEEPOUT

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed