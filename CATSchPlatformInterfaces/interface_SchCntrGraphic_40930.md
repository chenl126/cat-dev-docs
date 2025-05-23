# SchCntrGraphic (Object)

**_Manage the graphical representation of a schematic connector._**

## Methods

### Sub **AddGraphicalPrimitive**(| [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `iGRRToAdd`,| | [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `iGRR`)

   Add a graphical primitive to a connector.

**Parameters:**

` iGRRToAdd`      The connector graphical primitive to be added to the connector.
` iGRR`      The component or route graphical representation that points to the connector graphical primitive.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrGraphic
     Dim objArg1 As SchGRR
     Dim objArg2 As SchGRR
      ...
     objThisIntf.AddGraphicalPrimitiveobjArg1,objArg2

```

### Func **ListGraphicalPrimitives**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all graphical primitives of a connector.

**Parameters:**

` oLGRR`      A list of graphical primitives (members are CATISchGRR interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchCntrGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGraphicalPrimitives

```

### Sub **RemoveGraphicalPrimitive**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRRToRemove`)

   Remove a graphical primitive from a connector.

**Parameters:**

` iGRRToRemove`      The connector graphical primitive to be removed from the connector.

**Example:**

```VBScript
     Dim objThisIntf As SchCntrGraphic
     Dim objArg1 As SchGRR
      ...
     objThisIntf.RemoveGraphicalPrimitiveobjArg1

```