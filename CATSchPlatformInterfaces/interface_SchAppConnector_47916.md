# SchAppConnector (Object)

**_Manage a schematic connector._**

## Methods

### Func **AppConnect**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToConnect`) As [CATIASchAppConnection](../CATSchPlatformInterfaces/interface_SchAppConnection_54308.md)

Connect to an input connector.

**Parameters:**

` iCntrToConnect`      A schematic connector object to connect to
` oConnection`      Connection created
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchAppConnector
Dim objArg2 As SchAppConnection
 ...
Set objArg2 = objThisIntf.AppConnect(objArg1)

```

### Func **AppConnectBranch**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToConnect`) As [CATIASchAppConnection](../CATSchPlatformInterfaces/interface_SchAppConnection_54308.md)

Connect to an input connector for Branch.

**Parameters:**

` iCntrToConnect`      A schematic connector object to connect to
` oConnection`      Connection created
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchAppConnector
Dim objArg2 As SchAppConnection
 ...
Set objArg2 = objThisIntf.AppConnectBranch(objArg1)

```

### Sub **AppDisconnect**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToDisConnect`)

Disconnect from an input connector.

**Parameters:**

` iCntrToDisconnect`      A schematic connector object to disconnect from
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchAppConnector
 ...
objThisIntf.AppDisconnectobjArg1

```

### Func **AppGetAssociatedConnectable**( ) As [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)

Find the application object that owns this connector.

**Parameters:**

` oConnectable`      An application object that the connector belongs to.
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchAppConnectable
 ...
Set objArg1 = objThisIntf.AppGetAssociatedConnectable

```

### Sub **AppIsCntrConnected**( boolean  `oBYes`)

Query whether the connector has been connected.

**Parameters:**

` oBYes`      If TRUE, then it is connected
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim bVar1 As boolean
 ...
objThisIntf.AppIsCntrConnectedbVar1

```

### Func **AppListCompatibleTypes**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

Find all the class types of connector that are compatible with this connector for connections.

**Parameters:**

` oLCntrCompatClassTypes`      A list of all the class types of connectors that are compatible with this connector for connections.
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchListOfBSTRs
 ...
Set objArg1 = objThisIntf.AppListCompatibleTypes

```

### Func **AppListConnections**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntnClassFilter`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

Find all the connections that include this connector.

**Parameters:**

` oLCntnClassFilter`      A list of all the class types for filtering the output connection list.
` oLConnections`      A list of connections that include this connector (members are CATISchAppConnection interface pointers).
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim objArg1 As SchListOfBSTRs
Dim objArg2 As SchListOfObjects
 ...
Set objArg2 = objThisIntf.AppListConnections(objArg1)

```

### Sub **AppOKToNoShowConnectedCntr**( boolean  `oBYes`)

Query whether it is OK to no show the connector after it is connected.

**Parameters:**

` oBYes`      If TRUE, then it is OK to no show.
**Example:**

```VBScript
Dim objThisIntf As SchAppConnector
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToNoShowConnectedCntrbVar1

```