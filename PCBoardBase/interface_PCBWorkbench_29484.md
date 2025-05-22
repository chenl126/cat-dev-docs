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