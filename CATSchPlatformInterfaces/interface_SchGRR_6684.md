# SchGRR (Object)

**_Manage the graphical representation of a schematic object._**

## Methods

### Sub **GetGRRName**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oGRRName`)

   Get current name of the GRR.

**Parameters:**

` oGRRName`      The name of this GRR. A component can be associated with more than one GRRs. Each GRR is identified by a specific name. Valid names are specified by the application when building the component. Every component should have a GRR named "Primary". The GRR by this name is used in the catalog.

**Example:**

```VBScript
     Dim objThisIntf As SchGRR
     Dim strVar1 As String
      ...
     objThisIntf.GetGRRNamestrVar1

```

### Sub **GetSchCntrOwners**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `oCntrOwner`,  [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `oGRROwner`)

   Get the schematic objects that own this connector graphic representation.

**Parameters:**

` oCntrOwner.`      A schematic connector that owns this connector graphic representation.
` oGRROwner`      A component or route graphic representation that owns this connector graphic representation.

**Example:**

```VBScript
     Dim objThisIntf As SchGRR
     Dim objArg1 As SchAppConnector
     Dim objArg2 As SchGRR
      ...
     objThisIntf.GetSchCntrOwnersobjArg1,objArg2

```

### Func **GetSchObjOwner**( ) As [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)

   Get the schematic object that owns this graphic representation.

**Parameters:**

` oGRROwner`      A schematic object that owns this graphic representation.

**Example:**

```VBScript
     Dim objThisIntf As SchGRR
     Dim objArg1 As SchAppConnectable
      ...
     Set objArg1 = objThisIntf.GetSchObjOwner

```

### Sub **ListConnectedGRRs**( [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iGRROwner`,  [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)  `iLCntbleClassFilter`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntbleGRRs`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntbles`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntrsOnThisObj`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLCntrsOnConnected`)

   Get a list of graphical objects that connects to this graphic representation.

**Parameters:**

` iGRROwner`      A CATISchAppConnectable that owns this graphic representation. In the case of GRRCntr (this object), iGRROwner is the owner **of the owner** of this graphic.
` oLCntrClassFilter`      A list of all the class types for filtering the output application objects list.
` oLCntbleGRRs`      A list of GRRs connected to this GRR. (members are CATISchGRR interface pointers).
` oLCntbles`      A list of application objects connected to this object. (members are CATISchAppConnectable interface pointers).
` oLCntrsOnThisObj`      A list of connectors on this object through which the connection is made. (members are CATISchAppConnector interface pointers).
` oLCntrsOnConnected`      A list of connectors on the connected objects through which the connection is made. (members are CATISchAppConnector interface pointers). Members in this list corresponds to those in oLCntrsOnThisObj in making the corresponding connections.

**Example:**

```VBScript
     Dim objThisIntf As SchGRR
     Dim objArg1 As SchAppConnectable
     Dim objArg2 As SchListOfBSTRs
     Dim objArg3 As SchListOfObjects
     Dim objArg4 As SchListOfObjects
     Dim objArg5 As SchListOfObjects
     Dim objArg6 As SchListOfObjects
      ...
     objThisIntf.ListConnectedGRRsobjArg1,objArg2,objArg3,objArg4,objArg5,objArg6

```

### Sub **SetGRRName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iGRRName`)

   Set current name of the GRR.

**Parameters:**

` iGRRName`      The name of this GRR to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRR
     Dim strVar1 As String
      ...
     objThisIntf.SetGRRNamestrVar1

```