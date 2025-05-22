# SetOfEquation (Object)

**_Represents the set of equations object._**

## Methods

### Func **GetMaxCalculationTime**( ) As long

Returns the maximum time of the model calculations.  
### Func **GetPrecision**( ) As double

Returns the calculation precision.  
### Func **GetSymbolcTransformations**( ) As boolean

Returns whether the Gauss method is used during the symbolic transformation.
**TRUE** if the Gauss method is used during the symbolic transformation.  
### Func **IsStopDialog**( ) As boolean

Returns whether the "Stop Dialog" will be shown during calculations.
**TRUE** if the 'Stop Dialog' will be shown during calculations.  
### Sub **SetMaxCalculationTime**( long  `iMaxTime`)

Sets a maximum time to the model calculations.  
### Sub **SetParameterAsInput**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`)

Specifies that the parameter must be considered as input parameter.

**Parameters:**

` iParameter`      The parameter to set up as input of the SetOfEquationObject

### Sub **SetParameterAsOutput**( [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)  `iParameter`)

Specifies that the parameter must be considered as an output parameter.

**Parameters:**

` iParameter`      The parameter to set up as output of the SetOfEquationObject

### Sub **SetPrecision**( double  `iEps`)

Sets the calculation precision.

**Parameters:**

` iEps`      a precision
**Legal values** : 1e-10 ≤ iEps ≤ 0.1

### Sub **UseStopDialog**( boolean  `iUsed`)

Specifies whether the 'Stop Dialog' should be shown during calculations.
**TRUE** to show the 'Stop Dialog' during calculations.  
### Sub **UseSymbolcTransformations**( boolean  `iGauss`)

Specifies whether the Gauss method should be used during the symbolic transformation.
**TRUE** to use the Gauss method during the symbolic transformation.