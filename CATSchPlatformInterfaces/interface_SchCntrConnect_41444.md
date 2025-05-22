# SchCntrConnect (Object)

**_Manage the a schematic connector._**

## Methods

### Sub **GetTransformMatrix**( [CATIASchGRRCntr](../CATSchPlatformInterfaces/interface_SchGRRCntr_19904.md)  `iGRRCntr`,  [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb6Matrix`)

Get the transformation matrix needed to transform 'this' connector to be coincident and aligned with the 'connect to' connector. NOTE: "alignment" in this context means that the connectors' alignment vectors are facing opposite directions.

**Parameters:**

` iGRRCntr`      Pointer to the image of the 'connect to' connector.
` oDb6Matrix`      Transformation matrix. for explanation of this argument.
**Example:**

```VBScript
Dim objThisIntf As SchCntrConnect
Dim objArg1 As SchGRRCntr
Dim objArg2 As SchListOfDoubles
 ...
objThisIntf.GetTransformMatrixobjArg1,objArg2

```

### Sub **OKToConnect**( [CATIASchGRRCntr](../CATSchPlatformInterfaces/interface_SchGRRCntr_19904.md)  `iGRRCntr`,  boolean  `oBYes`)

Query whether 'this' connector can be connected to the specified connector, that is, whether their positions are coincident.

**Parameters:**

` iGRRCntr`      Pointer to the image of the 'connect to' connector.
` oBYes`      If TRUE, then it is OK to connect.
**Example:**

```VBScript
Dim objThisIntf As SchCntrConnect
Dim objArg1 As SchGRRCntr
Dim bVar2 As boolean
 ...
objThisIntf.OKToConnectobjArg1,bVar2

```