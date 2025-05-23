# SchZoneGraphic (Object)

**_Manage graphical representations of a schematic zone._**

## Methods

### Sub **AddGraphicalRepresentation**(| [CATIASchGRRZone](../CATSchPlatformInterfaces/interface_SchGRRZone_19924.md) | `iGRRToAdd`)

   Add a graphical representation to a zone.

**Parameters:**

` iGRRToAdd`      The graphical representation to be added to the zone.

**Example:**

```VBScript
     Dim objThisIntf As SchZoneGraphic
     Dim objArg1 As SchGRRZone
      ...
     objThisIntf.AddGraphicalRepresentationobjArg1

```

### Func **ListGraphicalRepresentations**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List all graphical representations of a zone.

**Parameters:**

` oLGRR`      A list of graphical representations (members are CATISchGRRZone interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchZoneGraphic
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListGraphicalRepresentations

```

### Sub **RemoveGraphicalRepresentation**( [CATIASchGRRZone](../CATSchPlatformInterfaces/interface_SchGRRZone_19924.md)  `iGRRToRemove`)

   Remove a graphical representation from a zone.

**Parameters:**

` iGRRToRemove`      The graphical representation to be removed from the zone.

**Example:**

```VBScript
     Dim objThisIntf As SchZoneGraphic
     Dim objArg1 As SchGRRZone
      ...
     objThisIntf.RemoveGraphicalRepresentationobjArg1

```