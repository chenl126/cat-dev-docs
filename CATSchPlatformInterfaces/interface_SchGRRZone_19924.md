# SchGRRZone (Object)

**_Manage the graphical representation of a schematic zone._**

## Methods

### Sub **AddBoundaryElement**( [CATIASchBoundaryElem](../CATSchPlatformInterfaces/interface_SchBoundaryElem_47253.md)  `iZoneBndyToAdd`)

Add a boundary element to the zone.

**Parameters:**

` iZoneBndy`      The geometric boundary elements to be added.
**Example:**

```VBScript
Dim objThisIntf As SchGRRZone
Dim objArg1 As SchBoundaryElem
 ...
objThisIntf.AddBoundaryElementobjArg1

```

### Sub **IsBoundaryValid**( boolean  `BIsValid`)

Check whether the boundary of this zone graphical representation is valid.

**Parameters:**

` oLZoneBndy`      Set to TRUE if the boundary is a closed polygon
**Example:**

```VBScript
Dim objThisIntf As SchGRRZone
Dim bVar1 As boolean
 ...
objThisIntf.IsBoundaryValidbVar1

```

### Func **ListBoundaryElements**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

List all boundary elements of this zone graphical representation.

**Parameters:**

` oLZoneBndy`      List of geometric boundaries of this zone graphical representation
**Example:**

```VBScript
Dim objThisIntf As SchGRRZone
Dim objArg1 As SchListOfObjects
 ...
Set objArg1 = objThisIntf.ListBoundaryElements

```

### Sub **RemoveBoundaryElement**( [CATIASchBoundaryElem](../CATSchPlatformInterfaces/interface_SchBoundaryElem_47253.md)  `iZoneBndyToRemove`)

Remove a boundary element to the zone.

**Parameters:**

` iZoneBndy`      The geometric boundary elements to be added.
**Example:**

```VBScript
Dim objThisIntf As SchGRRZone
Dim objArg1 As SchBoundaryElem
 ...
objThisIntf.RemoveBoundaryElementobjArg1

```