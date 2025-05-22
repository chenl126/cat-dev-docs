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