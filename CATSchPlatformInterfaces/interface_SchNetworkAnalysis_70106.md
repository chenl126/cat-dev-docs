# SchNetworkAnalysis (Object)

**_Represents a schematic network._**

## Methods

### Func **FindPaths**(| [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md) | `iFromObject`,| | [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md) | `iToObject`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Given a start and end object in the network, this method returns a list of network objects each representing a path connecting the the 2 input objects.

**Parameters:**

` iFromObject`      The connectable to start from.
` iToObject`      The connectable to finish at.
` oLNetworks`      Pointer to a list of networks. (Members are CATISchNetworkAnalysis interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchNetworkAnalysis
     Dim objArg1 As SchAppConnectable
     Dim objArg2 As SchAppConnectable
     Dim objArg3 As SchListOfObjects
      ...
     Set objArg3 = objThisIntf.FindPaths(objArg1,objArg2)

```

### Func **ListExtremityObjects**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List the extremity objects of the network.

**Parameters:**

` oLExtremityObjs`      Pointer to a list of extremity objects of the network (Members are CATISchAppConnectable interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchNetworkAnalysis
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListExtremityObjects

```

### Func **ListNetworkObjects**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List the connected objects in the network.

**Parameters:**

` oLNetworkObjs`      Pointer to a list of all connected objects in the network. (Members are CATISchAppConnectable interface pointers)

**Example:**

```VBScript
     Dim objThisIntf As SchNetworkAnalysis
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListNetworkObjects

```