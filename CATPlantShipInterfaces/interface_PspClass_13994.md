# PspClass (Object)

**_Represent Interface to list the start up object classes of an application._**
**Role** : Application object classes.

## Properties

### Property **StartUpConnectors**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

Returns a List of start-up Connector object classes.

**Example:**

```VBScript
Dim objThisIntf As PspClass
Dim objArg1 As PspListOfBSTRs
 ...
Set objArg1 = objThisIntf.StartUpConnectors

```

### Property **StartUpFunctions**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

Returns a List of start-up Function object classes.

**Example:**

```VBScript
Dim objThisIntf As PspClass
Dim objArg1 As PspListOfBSTRs
 ...
Set objArg1 = objThisIntf.StartupFunctions

```

### Property **StartUpPhysicals**( ) As [CATIAPspListOfBSTRs](../CATPlantShipInterfaces/interface_PspListOfBSTRs_38188.md) (Read Only)

Returns a List of start-up physical object classes.

**Example:**

```VBScript
Dim objThisIntf As PspClass
Dim objArg1 As PspListOfBSTRs
 ...
Set objArg1 = objThisIntf.StartupPhysicals

```