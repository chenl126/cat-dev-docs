# SchInternalFlow (Object)

**_Represents the internal flow object in a schematic component._**

## Methods

### Sub **GetInsertionType**(| [CatSchIDLInternalFlowType](../CATSchPlatformInterfaces/enum_CatSchIDLInternalFlowType_126856.md) | `oEInternalFlowType`)

   Get insertion flow type.

**Parameters:**

` oEInternalFlowType`      Internal flow type.

**Example:**

```VBScript
     Dim objThisIntf As SchInternalFlow

      ...
     objThisIntf.GetInsertionTypeCatSchIDLInternalFlowType_Enum

```

### Sub **GetStatus**( [CatSchIDLInternalFlowStatus](../CATSchPlatformInterfaces/enum_CatSchIDLInternalFlowStatus_149884.md)  `oEInternalFlowStatus`)

   Get insertion flow status.

**Parameters:**

` oEInternalFlowStatus`      Internal flow status.

**Example:**

```VBScript
     Dim objThisIntf As SchInternalFlow

      ...
     objThisIntf.GetStatusCatSchIDLInternalFlowStatus_Enum

```

### Func **ListSchConnectors**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all schematic connectors associated with an internal flow.

**Parameters:**

` oLSchCntrs`      A list of schematic connector objects (members are CATISchCntrLocation interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchInternalFlow
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListSchConnectors

```

### Sub **SetStatus**( [CatSchIDLInternalFlowStatus](../CATSchPlatformInterfaces/enum_CatSchIDLInternalFlowStatus_149884.md)  `iEInternalFlowStatus`)

   Set insertion flow status.

**Parameters:**

` iEInternalFlowStatus`      Internal flow status.

**Example:**

```VBScript
     Dim objThisIntf As SchInternalFlow

      ...
     objThisIntf.SetStatusCatSchIDLInternalFlowStatus_Enum

```