# ManufacturingProcess (Object)

**_A ManufacturingProcess for a Manufacturing Document._**

## Properties

### Property **Setups**(| ) As [CATIAMfgActivities](../ManufacturingInterfaces/interface_MfgActivities_36625.md) (Read Only)

   Give the List of Setups linked to a Manufacturing Process.

**Example:**     The following example returns the list of Setups `SetupsList` linked to the manufacturing Process `CurrentProcess`

```VBScript
     Set SetupsList = CurrentProcess.Setups

```