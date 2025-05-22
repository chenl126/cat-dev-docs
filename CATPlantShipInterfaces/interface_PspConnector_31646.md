# PspConnector (Object)

**_Represents connector object._**
**Role** : To specify connector behaviors such as connect and disconnect.

## Properties

### Property **AttrNames**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)

Returns or Sets Attribute names of the connector.

**Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim ojArg1 As CATIAPspListOfBSTRs
 ...
Set ojArg1 = objThisIntf.AttrNames

```

### Property **ConnectorName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets name of the connector.

**Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim strVar1 As CATBSTR
 ...
Set strVar1 = objThisIntf.Name
Dim strVar1 As CATBSTR
 ...
objThisIntf.ConnectorName = strVar2

```

Methods

### Sub **Connect**( [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)  `iCntrToConnect`)

Connect the connector to another connector.

**Parameters:**

` iCntrToConnect`      the connector to be connected to
**Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim objArg1 As PspConnector
 ...
objThisIntf.Connect objArg1

```

### Sub **Disconnect**( [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)  `iCntrToDisconnect`)

DisConnect the connector from another connector.

**Parameters:**

` iCntrToDisconnect`      The connector to be disconnected from
**Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim objArg1 As PspConnector
 ...
objThisIntf.Disconnect objArg1

```

### Func **GetAssociatedConnectable**( ) As [CATIAPspConnectable](../CATPlantShipInterfaces/interface_PspConnectable_41588.md)

Get the connectable-owner of this connector.

**Parameters:**

` oConnectable`      Connectable owner of this connector
**Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim objArg1 As CATIAPspConnectable
 ...
Set objArg1 = objThisIntf.GetAssociatedConnectable

```

### Func **IsCntrConnected**( ) As boolean

Query whether the connector has been connected.

**Returns:**      TRUE if this connector is connected.  **Example:**

```VBScript
Dim objThisIntf As PspConnector
Dim bArg1 As boolean
 ...
bArg1 = objThisIntf.IsCntrConnected

```