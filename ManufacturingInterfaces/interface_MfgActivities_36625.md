# MfgActivities (Collection)

**_The collection of MfgActivities related to the Manufacturing Document ._**

## Methods

### Sub **Add**(| [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md) | `iRealObj`)

   This method adds the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example adds in CATIAMfgActivities `ListActivities` the CATIAManufacturingActivity `ThisActivity` in position `NumPos`:

```VBScript
     ListActivities.Add(ThisActivity)

```

### Func **GetElement**( long  `iIndex`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This method return the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example return the CATIAManufacturingActivity `ThisActivity` in CATIAMfgActivities `ListActivities` in position `NumPos`:

```VBScript
     Set ThisActivity = ListActivities.GetElement(Numpos)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAManufacturingActivity](../ManufacturingInterfaces/interface_ManufacturingActivity_95999.md)

   This method return the specified CATIAManufacturingActivity in the current list CATIAMfgActivities.

**Example:**     The following example return the CATIAManufacturingActivity `ThisActivity` in CATIAMfgActivities `ListActivities` in position `NumPos`:

```VBScript
     Set ThisActivity = ListActivities.Item(Numpos)

```