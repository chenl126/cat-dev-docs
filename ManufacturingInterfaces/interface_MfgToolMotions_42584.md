# MfgToolMotions (Collection)

**_The collection of MfgToolMotions related to the Manufacturing Document ._**

## Methods

### Sub **Add**( [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)  `iRealObj`)

This method adds the specified CATIAManufacturingToolMotion in the current list CATIAMfgToolMotions.

**Example:**     The following example adds in CATIAMfgToolMotions `ListToolMotions` the CATIAManufacturingToolMotion `ThisToolMotion`

```VBScript
ListToolMotions.Add(ThisToolMotion)

```

### Func **GetElement**( long  `iIndex`) As [CATIAManufacturingToolMotion](../ManufacturingInterfaces/interface_ManufacturingToolMotion_113852.md)

This method return the specified CATIAManufacturingToolMotion in the current list CATIAMfgToolMotions.

**Example:**     The following example return the CATIAManufacturingToolMotion `ThisToolMotion` in CATIAMfgToolMotions `ListToolMotions` in position `NumPos`:

```VBScript
Set ThisToolMotion = ListToolMotions.GetElement(Numpos)

```