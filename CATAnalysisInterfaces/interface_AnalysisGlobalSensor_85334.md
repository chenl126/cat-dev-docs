# AnalysisGlobalSensor (Object)

**_Represent the analysis global sensor._**

This object is a kind of AnalysisSensor based on analysis feature global results. For example, extract the Energy value of a solution.

## Methods

### Sub **GetIdentifier**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oTypeBSTR`,| | [CATBSTR](../System/typedef_CATBSTR_8129.md) | `oSubTypeBSTR`)

   Retreives the Physical type and sub physical type that will be computed by the sensor.

**Parameters:**

` oTypeBSTR`      The physical type identifier.
` oSubTypeBSTR`      The "sub" physical type identifier.

### Sub **SetIdentifier**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeBSTR`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSubTypeBSTR`)

   Sets the Physical type and sub physical type that will be computed by the sensor.

**Parameters:**

` iTypeBSTR`      The physical type identifier.
` iSubTypeBSTR`      The "sub" physical type identifier.