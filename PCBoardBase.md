# PCBoardBase Framework

## Object Index

  * [PCBArea](PCBoardBase/interface_PCBArea_9184.md)
  * [PCBBoard](PCBoardBase/interface_PCBBoard_12430.md)
  * [PCBComponent](PCBoardBase/interface_PCBComponent_30246.md)
  * [PCBHoleAndPattern](PCBoardBase/interface_PCBHoleAndPattern_58448.md)
  * [PCBObject](PCBoardBase/interface_PCBObject_16102.md)
  * [PCBWorkbench](PCBoardBase/interface_PCBWorkbench_29484.md)

## Enumerated Types Index

  * [CatElectronicType](PCBoardBase/enum_CatElectronicType_61500.md)

---

# CatElectronicType (Enumeration)

**__**

---

# PCBArea (Object)

**__**

## Properties

### Property **AreaType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

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

---

# PCBBoard (Object)

**__**

## Properties

### Property **Owner**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

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

---

# PCBComponent (Object)

**__**

## Properties

### Property **CAPACITANCE**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the CAPACITANCE Type of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **POWEROPR**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the Operating power rating of a component The possible value are MECHANICAL or ELECTRICAL

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **POWER_MAX**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the POWER MAX of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **PackageNumber**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the Package number of a component

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **RESISTANCE**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the RESISTANCE of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **THERM_COND**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the thermal conductivity of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **THETA_JB**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the junction to board thermal resistance of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **THETA_JC**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the junction to case thermal resistance of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Property **TOLERANCE**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Allow to get and set the TOLERANCE of a component.

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

---

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

---

# PCBObject (Object)

## Properties

### Property **ElectronicType**( ) As [CatElectronicType](../PCBoardBase/enum_CatElectronicType_61500.md) (Read Only)

   Allow to know if : a Product is a BOARD, a PANEL or a COMPONENT, a Hole is a PBD Hole a pattenr is a PCB pattern, a Pad is a contraint area.

**Parameters:**

` oType`      This parameter is the type of the object ( BOARD, PANEL, COMPONENT )

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed
Methods

### Sub **RemoveElectronicBehaviour**( )

   Allow to remove a PCB behaviour of an object

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

---

# PCBWorkbench (Object)

**_Interface to access Circuit Board Design workbench object._**

## Methods

### Func **CreateBoard**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iRoot`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Allows to create a Board.

**Parameters:**

` iRoot`      Root product of the Part to extend
` oBoard`      The board created

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Func **CreateComponent**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iRoot`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iElecPackageNumber`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iElecPartNumber`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iElecType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Allows to create a Component.

**Parameters:**

` iRoot`      Root product of the Part to extend
` iElecPackageNumber`      The package number used to valuate the component attribute
` iElecPartNumber`      The part number used to valuate the part number of the component
` iElecType`      The Type of the component to create : ELECTRICAL or MECHANICAL
` oComponent`      The Component created

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Func **CreatePanel**( [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iRoot`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Allows to create a panel.

**Parameters:**

` iRoot`      Root product of the Part to extend
` oPanel`      The panel created

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed

### Func **GetRootProduct**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `doc`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Allows to get the root product of a document.

**Parameters:**

` doc`      The document to scan
` oRoot`      The root product of the document scanned

**Returns:**

The result of the method:
  * S_OK if succeeded
  * E_FAIL if failed