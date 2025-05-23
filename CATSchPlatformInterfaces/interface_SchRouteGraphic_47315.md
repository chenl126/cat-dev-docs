# SchRouteGraphic (Object)

**_Manage graphical primitives representing a schematic route._**

## Methods

### Sub **AddGraphicalPrimitive**(| [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md) | `iGRRToAdd`)

   Add a graphical primitive to a route.

**Parameters:**

` iGRRToAdd`      The route graphical primitive to be added to the route.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteGraphic
     Dim objArg1 As SchGRRRoute
      ...
     objThisIntf.AddGraphicalPrimitiveobjArg1

```

### Func **ListGraphicalPrimitives**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all graphical primitives of a route.

**Parameters:**

` oLGRR`      A list of graphical primitives (members are CATISchGRRRoute interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchRouteGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGraphicalPrimitives

```

### Sub **RemoveAllGraphicalPrimitives**( )

   Remove all graphical primitives of a route, including alternate graphical primitives.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteGraphic
      ...
     objThisIntf.RemoveAllGraphicalPrimitives

```

### Sub **RemoveGraphicalPrimitive**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRRToRemove`)

   Remove a graphical primitive from a route.

**Parameters:**

` iGRRToRemove`      The route graphical primitive to be removed from the component.

**Example:**

```VBScript
     Dim objThisIntf As SchRouteGraphic
     Dim objArg1 As SchGRRRoute
      ...
     objThisIntf.RemoveGraphicalPrimitiveobjArg1

```