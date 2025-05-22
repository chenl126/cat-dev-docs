# SchCompFlow (Object)

**_Manage the internal flow of a schematic component._**

## Methods

### Func **AddInternalFlow**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLFlowCntrs`) As [CATIASchInternalFlow](../CATSchPlatformInterfaces/interface_SchInternalFlow_47807.md)

Add an internal flow to a component.

**Parameters:**

` iLFlowCntrs`      List of connectors (2) to be connected by the flow. (members should be CATISchAppConnector interface pointer)
` oInternalFlowAdded`      Internal flow object added/created (CATISchInternalFlow interface pointer).
**Example:**

```VBScript
Dim objThisIntf As SchCompFlow
Dim objArg1 As SchListOfObjects
Dim objArg2 As SchInternalFlow
 ...
Set objArg2 = objThisIntf.AddInternalFlow(objArg1)

```

### Func **AddInternalFlowSpecifyGRR**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLFlowCntrs`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLOwnerGRR`) As [CATIASchInternalFlow](../CATSchPlatformInterfaces/interface_SchInternalFlow_47807.md)

Add an internal flow to a component. Specifying which graphical images the connector graphics are on.

**Parameters:**

` iLFlowCntrs`      List of connectors (2) to be connected by the flow. (members should be CATISchAppConnector interface pointer)
` iLOwnerImages`      List of CATISchGRRComp interface pointers
` oInternalFlowAdded`      Internal flow object added/created (CATISchInternalFlow interface pointer).
**Example:**

```VBScript
Dim objThisIntf As SchCompFlow
Dim objArg1 As SchListOfObjects
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchInternalFlow
 ...
Set objArg3 = objThisIntf.AddInternalFlowSpecifyGRR(objArg1,objArg2)

```

### Func **ListInternalFlows**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

List all internal flow objects of a component.

**Parameters:**

` oLInternalFlow`      A list of internal flow objects (members are CATISchInternalFlow interface pointers).
**Example:**

```VBScript
Dim objThisIntf As SchCompFlow
Dim objArg1 As SchListOfObjects
 ...
Set objArg1 = objThisIntf.ListInternalFlows

```

### Sub **RemoveInternalFlow**( [CATIASchInternalFlow](../CATSchPlatformInterfaces/interface_SchInternalFlow_47807.md)  `iInternalFlowToRemove`)

Remove an internal flow from a component.

**Parameters:**

` iInternalFlowToRemove`      Internal flow object to be removed.
**Example:**

```VBScript
Dim objThisIntf As SchCompFlow
Dim objArg1 As SchInternalFlow
 ...
objThisIntf.RemoveInternalFlowobjArg1

```