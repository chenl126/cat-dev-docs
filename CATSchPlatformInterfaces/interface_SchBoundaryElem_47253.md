# SchBoundaryElem (Object)

**_Manage a boundary element of a schematic zone._**

## Methods

### Sub **GetBoundaryPoints**(| [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md) | `oLDbPts`)

   Get the definition points (segments end points) of one side of the boundary. If the side is a curve, these points are the end points of the chords approximating the curve.

**Parameters:**

` oLDbPts`      A list of X-Y coordinates of the points. 2 doubles per point.

**Example:**

```VBScript
     Dim objThisIntf As SchBoundaryElem
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetBoundaryPointsobjArg1

```

### Sub **GetEndPoints**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oLDb4Pts`)

   Get the end points (segments end points) of one side of the boundary.

**Parameters:**

` oLDb4Pts`      An array of 4 doubles.

**Example:**

```VBScript
     Dim objThisIntf As SchBoundaryElem
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetEndPointsobjArg1

```

### Func **ListGRRZoneOwners**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Get the list of owners of this zone.

**Parameters:**

` oLGRRZoneOwners`      A list of GRRZone which has included this boundary element.

**Example:**

```VBScript
     Dim objThisIntf As SchBoundaryElem
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGRRZoneOwners

```