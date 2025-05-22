# PspBuildPart (Object)

**_Represents Interface to create and modify a part._**
**Role** : To build and define a part.

## Methods

### Func **ChangePartType**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `uPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Returns the part after changing the part type of an existing part.

**Parameters:**

` iReferencePart`      Reference Product in CATPart document to modify.
` iPartType`      New part class type.
` iPartNumber`      New Part number.
**Returns:**      New reference Product in CATPart document  **Example:**

```VBScript
Dim objThisIntf As PspBuildPart
Dim iRefPart As   Product
Dim iuPartType As CATBSTR
Dim uPartNumber As CATBSTR
Dim oNewRefPart As Product
 ...
Set oNewRefPart= objThisIntf.ChagePartType (iRefPart, iuPartType, uPartNumber )

```

### Func **ListPartParametricAttributes**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Returns the part parametric attribute names.

**Parameters:**

` iRefPart`      Reference Product in new CATPart document.
**Returns:**      List of parametric attribute names.  **Example:**

```VBScript
Dim objThisIntf As PspBuildPart
Dim iRefPart As Product
Dim oLAttributeNames As PspListOfBSTRs

 ...
Set oLAttributeNames = objThisIntf.ListPartParametricAttributes (iRefPart)

```

### Func **NewPart**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuPartType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `uPartNumber`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Create a new part.

**Parameters:**

` iPartType`      Part class type.
` iPartNumber`      Part number.
**Returns:**      Retruns Reference Product pointer in new CATPart document.  **Example:**

```VBScript
Dim objThisIntf As PspBuildPart
Dim iuPartType As CATBSTR
Dim uPartNumber As CATBSTR
Dim oNewRefPart As Product
 ...
Set oNewRefPart = objThisIntf.NewPart (iuPartType, uPartNumber)

```

### Sub **SetPartParametricAttributes**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iRefPart`,  [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `iLAttributeNames`)

Sets the part parametric attribute names.

**Parameters:**

` iRefPart`      Reference Product in new CATPart document.
` iLAttributeNames`      List of parametric attribute names.
**Example:**

```VBScript
Dim objThisIntf As PspBuildPart
Dim iRefPart As Product
Dim iLAttributeNames As PspListOfBSTRs

 ...
objThisIntf.SetPartParametricAttributes iRefPart, iLAttributeNames

```