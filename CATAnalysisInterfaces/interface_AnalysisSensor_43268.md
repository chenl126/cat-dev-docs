# AnalysisSensor (Object)

**_Represent the analysis sensor._**

## Properties

### Property **OutPutParameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

Returns the collection object containing the sensor parameters.

**Example:**     The following example returns in `params` the parameters computed by the sensor:

```VBScript
Dim AnalysisSensor1 As AnalysisSensor
Dim params As CATIAParameters
Set params = AnalysisSensor1.OutPutParameters

```

Methods

### Sub **Update**( )

Update the sensor. Computation of OutPutParameters if needed.

**Example:**     The following example computes the sensor:

```VBScript
Dim AnalysisSensor1 As AnalysisSensor
AnalysisSensor1.Update

```