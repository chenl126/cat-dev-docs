# PspAppFactory (Object)

**_Represents the application factory._**
**Role** : To create, instanciate, delete and query groups, logical lines, compartments and parts.

## Methods

### Func **CreateGroup**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGroupType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGroupID`) As [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)

Creates a group in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query.
` iGroupType`      Group Startup type.
` iGroupID`      Group ID. A default ID will be generated if input is NULL.
**Returns:**      Created Group instance.  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim iStrVar2 As String
Dim iStrVar3 As String
Dim iObj4 As PspGroup
 ...
Set iObj4=objThisIntf.CreateGroup (iobj1,iStrVar2,iStrVar3 )

```

### Sub **DeleteCompartment**( [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)  `iCompartment`)

Delete a compartment instance.

**Parameters:**

` iCompartment`      Compartment to be deleted
**Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As PspGroup

 ...
objThisIntf.DeleteCompartment iobj1

```

### Sub **DeleteGroup**( [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)  `iGroup`)

Delete a group.

**Parameters:**

` iGroup`      Group to be deleted.
**Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As PspGroup

 ...
objThisIntf.DeleteGroup iobj1

```

### Sub **DeleteLogicalLine**( [CATIAPspLogicalLine](../CATPlantShipInterfaces/interface_PspLogicalLine_40658.md)  `iLogicalLine`)

Delete a logical line instance.

**Parameters:**

` iLogicalLine`      Logical Line to be deleted
**Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As PspLogicalLine

 ...
objThisIntf.DeleteLogicalLine iobj1

```

### Sub **DeletePart**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iPart`)

Delete a part.

**Parameters:**

` iProduct`      Part to be deleted.
**Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product

 ...
objThisIntf.DeletePart iobj1

```

### Func **GetCompartment**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCompartmentID`) As [CATIAPspGroup](../CATPlantShipInterfaces/interface_PspGroup_14418.md)

Instanciate a compartment from the catalog into the current Product.

**Parameters:**

` iCurrentProduct`      The current Product into which a compartment will be instanciated.
` iCompartmentID`      Compartment ID to get from the compartment catalog.
**Returns:**      Compartment instance.  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim iStrVar2 As String
Dim iObj3 As PspGroup
 ...
Set iObj3=objThisIntf.GetCompartment (iobj1,iStrVar2 )

```

### Func **GetLogicalLine**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogicalLineID`) As [CATIAPspLogicalLine](../CATPlantShipInterfaces/interface_PspLogicalLine_40658.md)

Returns a PspLogicalLine Logical line Instance.

**Parameters:**

` iCurrentProduct`      The current Product into which a logical line will be instanciated.
` iLogicalLineID`      Logical line ID to get from the logical line catalog.
**Returns:**      Logical line instance.  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim iStrVar2 As String
 ...
objThisIntf.GetLogicalLine (iobj1,iStrVar2 )

```

### Func **ListCompartments**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

Retrieves a list of Compartments in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query.
**Returns:**      A list of Compartmemts ( A list of CATIAPspGroup)  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim objArg2 As PspListOfObjects

 ...
Set ObjArg2 = objThisIntf.ListCompartments (iobj1 )

```

### Func **ListGroups**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

Retrieve a list of Groups in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query..
**Returns:**      A list of Groups ( A list of CATIAPspGroup)  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim objArg2 As ListOfObjects

 ...
Set ObjArg2 = objThisIntf.ListGroups (iobj1)

```

### Func **ListLogicalLines**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

Returns a list of logical lines in the current Product.

**Parameters:**

` iCurrentProduct`      The current Product to query..
**Returns:**      A list of logical Lines (A list of PspLogicalLine)  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim objArg2 As PspListOfObjects

 ...
Set ObjArg2 = objThisIntf.ListLogicalLines (iobj1 )

```

### Func **ListPhysicals**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iCurrentProduct`,  [CatPspIDLDomainID](../CATPlantShipInterfaces/enum_CatPspIDLDomainID_53923.md)  `iDomainID`) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)

Returns a list of Physical objects in the node.

**Parameters:**

` iCurrentProduct`      The current Product to query.
` iDomainID`      Physical objects that have this domain ID. To get list of all in all domains set iDomainID= catPspIDLNone.
**Returns:**      A list of physical objects (A list of PspPhysical objects)  **Example:**

```VBScript
Dim objThisIntf As PspAppFactory
Dim iobj1 As Product
Dim iobjArg2 As CatPspIDLDomainID
Dim objArg3 As PspListOfObjects

 ...
Set ObjArg3 = objThisIntf.ListPhysicals (iobj1, iobjArg2 )

```