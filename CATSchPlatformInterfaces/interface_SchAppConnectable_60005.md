# SchAppConnectable (Object)

**_Represents an application object that can be connected to others._**

## Methods

### Sub **AppAddConnector**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iClassType`,| | [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md) | `oNewAppCntr`)

   Add a connector.

**Parameters:**

` iClassType`      Class type of the connector to be added.
` oNewAppCntr`      The new Application Connector object created.

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim strVar1 As String
     Dim objArg2 As SchAppConnector
      ...
     objThisIntf.AppAddConnectorstrVar1,objArg2

```

### Sub **AppGetReferenceName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oReferenceName`)

   Get the reference name of a connectable. It will be displayed in catalogs.

**Parameters:**

` oReferenceName`      The name of the reference

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim strVar1 As String
      ...
     objThisIntf.AppGetReferenceNamestrVar1

```

### Sub **AppListConnectables**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntbleClassFilter`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntbles`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntrsOnThisObj`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntrsOnConnected`)

   Find all the application objects connected to this object through their connectors.

**Parameters:**

` oLCntrClassFilter`      A list of all the class types for filtering the output application objects list.
` oLCntbles`      A list of application objects connected to this object. (members are CATISchAppConnectable interface pointers).
` oLCntrsOnThisObj`      A list of connectors on this object through which the connection is made. (members are CATISchAppConnector interface pointers).
` oLCntrsOnConnected`      A list of connectors on the connected objects through which the connection is made. (members are CATISchAppConnector interface pointers). Members in this list corresponds to those in oLCntrsOnThisObj in making the corresponding connections.

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim objArg1 As SchListOfBSTRs
     Dim objArg2 As SchListOfObjects
     Dim objArg3 As SchListOfObjects
     Dim objArg4 As SchListOfObjects
      ...
     objThisIntf.AppListConnectablesobjArg1,objArg2,objArg3,objArg4

```

### Func **AppListConnectors**( [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntrClassFilter`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Find all the connectors of this application object.

**Parameters:**

` oLCntrClassFilter`      A list of all the class types for filtering the output connector list.
` oLCntrs`      A list of connectors included in this connection. (members are CATISchAppConnector interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim objArg1 As SchListOfBSTRs
     Dim objArg2 As SchListOfObjects
      ...
     Set objArg2 = objThisIntf.AppListConnectors(objArg1)

```

### Func **AppListValidCntrTypes**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

   List the valid application connector types allowed to be created.

**Parameters:**

` oLValidCntrTypes`      A list of connector class types allowed.

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim objArg1 As SchListOfBSTRs
      ...
     Set objArg1 = objThisIntf.AppListValidCntrTypes

```

### Sub **AppRemoveConnector**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrToRemove`)

   Remove a connector.

**Parameters:**

` iCntrToRemove`      The application connector object to be removed

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim objArg1 As SchAppConnector
      ...
     objThisIntf.AppRemoveConnectorobjArg1

```

### Sub **AppSetReferenceName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iReferenceName`)

   Set the reference name of a connectable. It will be displayed in catalogs.

**Parameters:**

` iReferenceName`      The name of the reference

**Example:**

```VBScript
     Dim objThisIntf As SchAppConnectable
     Dim strVar1 As String
      ...
     objThisIntf.AppSetReferenceNamestrVar1

```