# SchAppConnection (Object)

**_Manage a schematic connection._**

## Methods

### Sub **AppAddConnector**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToAdd`)

Add a connector.

**Parameters:**

` iCntrToAdd`      The Application Connector to be added to the connection
**Example:**

```VBScript
Dim objThisIntf As SchAppConnection
Dim objArg1 As SchAppConnector
 ...
objThisIntf.AppAddConnectorobjArg1

```

### Sub **AppListConnectables**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntbleClassFilter`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntbles`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntrs`)

Find all the application object connected to this connection through their connectors.

**Parameters:**

` oLCntrClassFilter`      A list of all the class types for filtering the output application objects list.
` oLCntbles`      A list of application objects connected to this connection. (members are CATISchAppConnectable interface pointers).
` oLCntrs`      A list of connectors through which this connection is made. (members are CATISchAppConnector interface pointers).
**Example:**

```VBScript
Dim objThisIntf As SchAppConnection
Dim objArg1 As SchListOfBSTRs
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchListOfObjects
 ...
objThisIntf.AppListConnectablesobjArg1,objArg2,objArg3

```

### Func **AppListConnectors**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntrClassFilter`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

Find all the connectors included in this connection.

**Parameters:**

` oLCntrClassFilter`      A list of all the class types for filtering the output connector list.
` oLCntrs`      A list of connectors included in this connection. (members are CATISchAppConnector interface pointers).
**Example:**

```VBScript
Dim objThisIntf As SchAppConnection
Dim objArg1 As SchListOfBSTRs
Dim objArg2 As SchListOfObjects
 ...
Set objArg2 = objThisIntf.AppListConnectors(objArg1)

```

### Sub **AppRemoveConnector**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToRemove`)

Remove a connector.

**Parameters:**

` iCntrToRemove`      The Application Connector to be removed
**Example:**

```VBScript
Dim objThisIntf As SchAppConnection
Dim objArg1 As SchAppConnector
 ...
objThisIntf.AppRemoveConnectorobjArg1

```