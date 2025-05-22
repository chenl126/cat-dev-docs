# PspConnectable (Object)

**_Represents an Interface to manage object behaviors in making connections._**
**Role** : To specify object behaviors such as adding a connector and removing a connector.

## Properties

### Property **Connectors**( ) As [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md) (Read Only)

Returns a list of connectors of the object.

**Example:**

```VBScript
Dim objThisIntf As PspConnectable
Dim objArg1 As CatPspIDLDomainID
Dim objArg2 As PspListOfBSTRs
 ...
Set objArg2 = objThisIntf.Connectors

```

### Property **ValidConnectorTypes**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

Returns a list of Valid connector types on this object.

**Example:**

```VBScript
Dim objThisIntf As PspConnectable
Dim objArg1 As PspListOfBSTRs
 ...
Set objArg1 = objThisIntf.ValidConnectorTypes

```

Methods

### Func **GetConnectorByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iuConnectorName`) As [CATIAPspConnector](../CATPlantShipInterfaces/interface_PspConnector_31646.md)

Retrieves a connector with the given name.

**Parameters:**

` iConnectorName`      Connector name to look for.
**Returns:**      Connector with given name.  **Example:**

```VBScript
Dim objThisIntf As PspConnectable
Dim strVar1 As PspListOfBSTRs
Dim objArg2 As PspConnector
 ...
Set objArg2 = objThisIntf.GetConnectorByName (strVar1)

```

### Sub **ListConnectables**( [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md)  `iuClassFilter`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntbles`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntrsOnThisObj`,  [CATIAPspListOfObjects](../CATPlantShipInterfaces/interface_PspListOfObjects_53716.md)  `oLCntrsOnConnected`)

Retrieve a list of connectors of the object.

**Parameters:**

` iuClassFilter`      Class filter list. If iuClassFilter is an empty list then it will get connectors for all the application connector types.
` oLCntbles`      a list of CATIAPspConnectable objects that connect this object
` oLCntrsOnThisObj`      a list of connectors on "this" object in the connections ( A list of CATIAPspConnector)
` oLCntrsOnConnected`      a list of connectors on the other objects that the member of the former list is connected to (positions in oLCntrsOnThisObj and oLCntrsOnConnected corresponds to each other) ( A list of CATIAPspConnector)
**Example:**

```VBScript
Dim objThisIntf As PspConnectable
Dim objArg1 As PspListOfBSTRs
Dim objArg2 As PspListofObjects
Dim objArg3 As PspListofObjects
Dim objArg4 As PspListofObjects
 ...
objThisIntf.ListConnectables objArg1,objArg2,objArg3,objArg4

```