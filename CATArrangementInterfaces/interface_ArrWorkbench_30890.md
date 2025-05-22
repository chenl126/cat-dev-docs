# ArrWorkbench (Object)

**_Returns the Arrangement Workbench._**
**Role:** Use this interface to manage the ArrNomenclatureTree object, create Arrangement objects (such as ArrangementArea, ArrangementRun etc).

## Properties

### Property **ArrNomenclatureTree**( ) As [CATIAArrNomenclatureTree](../CATArrangementInterfaces/interface_ArrNomenclatureTree_76774.md) (Read Only)

Returns the ArrNomenclatureTree.  Methods

### Func **AddNomenclatureTree**( ) As [CATIAArrNomenclatureTree](../CATArrangementInterfaces/interface_ArrNomenclatureTree_76774.md)

This method allows the user to add a nomenclature tree if the get_ArrNomenclatureTree returns a Return code of E_FAIL. Basically, the workbench could not locate the startup instance to generate the necessary NomenclatureTree information.  
### Func **ConvertArrangementProductToProduct**( [CATIAArrangementProduct](../CATArrangementInterfaces/interface_ArrangementProduct_70174.md)  `iArrProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

This method converts an ArrangementProduct back to a Product.

**Parameters:**

` iArrProduct`      Input ArrangementProduct to be converted.
**Returns:**      oProduct As CATIAProduct Converted Product.  **See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Func **ConvertProductToArrangementProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAArrangementProduct](../CATArrangementInterfaces/interface_ArrangementProduct_70174.md)

This method converts a Product to an ArrangementProduct.

**Parameters:**

` iProduct`      Input Product to be converted.
**Returns:**      oArrProduct Converted ArrangementProduct.  **See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Func **FindInterface**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iObject`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

This method returns a interface handle as specified by the input interface name and the input interface handle.

```VBScript
Dim interfaceFound As AnyObject
Set interfaceFound = CATIAArrWorkbench.FindInterface("InterfaceNameToFind",CATIAProduct_iObject)

```

**Parameters:**

` iInterfaceName`      interface name to search for ("CATIAxxxx")
` iObject`      The object to search for the required interface.
**Returns:**      oInterfaceFound interface handle found