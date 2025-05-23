# SchAppCompatible (Object)

**_Provide application rules of how to connect objects._**

## Methods

### Sub **AppIsTargetOKForInsert**(| [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `iLCompSourceCntrs`,| | [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `oLSourceCntrs`,| | boolean | `oBYes`)

   Query whether a component (source) is compatible to be inserted into this route. This method is used when inserting a component into a route. This mehtod should only be implemented on a route object. For a component object, the method should simply returns oBYes=FALSE.

**Parameters:**

` iLCompSourceCntrs`      A list of connectors on the source component. The target (to be connected) is "this" route.
` oLSourceCntrs`      A list of compatible and available connectors on the source component (the input) that can be connected to the target ("this" route) (members are CATISchAppConnector interface pointers)
` oBYes`      If TRUE, the object is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCompatible
     Dim objArg1 As SchListOfObjects
     Dim objArg2 As SchListOfObjects
     Dim bVar3 As boolean
      ...
     objThisIntf.AppIsTargetOKForInsertobjArg1,objArg2,bVar3

```

### Sub **AppIsTargetOKForPlace**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLCompSourceCntrs`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLTargetCntrs`,  boolean  `oBYes`)

   Query whether a component (source) is compatible to be connected to "this" object (the target, which can be a route or a component). This method is used when placing a component to be connected to another object.

**Parameters:**

` iLCompSourceCntrs`      A list of connectors on the source component. The target (to be connected) is "this" component.
` oLOKCntrs`      A list of compatible and available connectors on "this" component (the target) to be connected to the source component (the input source). (members are CATISchAppConnector interface pointers)
` oBYes`      If TRUE, the object is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCompatible
     Dim objArg1 As SchListOfObjects
     Dim objArg2 As SchListOfObjects
     Dim bVar3 As boolean
      ...
     objThisIntf.AppIsTargetOKForPlaceobjArg1,objArg2,bVar3

```

### Sub **AppIsTargetOKForRoute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRouteCntrClassType`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLOKCntrs`,  boolean  `oBYes`)

   Query whether a route of the input class type can be connected to "this" object (the target, which can be a route or a component). This method is used when routing a route.

**Parameters:**

` iRouteCntrClassType`      Class type of a schematic route connector.
` oLOKCntrs`      A list of compatible and available connectors on this object. (members are CATISchAppConnector interface pointers)
` oBYes`      If TRUE, the object is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchAppCompatible
     Dim strVar1 As String
     Dim objArg2 As SchListOfObjects
     Dim bVar3 As boolean
      ...
     objThisIntf.AppIsTargetOKForRoutestrVar1,objArg2,bVar3

```