# SchConnectable (Object)

**_Represents schematic objects that can be connected to others._**

## Methods

### Func **ListConnectors**(| [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md) | `iLCntrClassFilter`,| | [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `iGRR`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   Find all the connectors of this schematic object on a specific graphical image.

**Parameters:**

` oLCntrClassFilter`      A list of all the class types for filtering the output connector list.
` iGRR`      Pointer to the graphical image
` oLCntrs`      A list of connectors included in this connection. (members are CATISchAppConnector interface pointers).

**Example:**

```VBScript
     Dim objThisIntf As SchConnectable
     Dim objArg1 As SchListOfBSTRs
     Dim objArg2 As SchGRR
     Dim objArg3 As SchListOfObjects
      ...
     Set objArg3 = objThisIntf.ListConnectors(objArg1,objArg2)

```