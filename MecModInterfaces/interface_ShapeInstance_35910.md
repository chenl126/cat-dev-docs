# ShapeInstance (Object)

**_The interface to access a CATIAShapeInstance._**

## Properties

### Property **InputsCount**( ) As long (Read Only)

Returns the number of Inputs.

**Example:**     The following example retrieves in `inputsCount` the number of Inputs of `hybridShapeInstance`:

```VBScript
inputsCount = hybridShapeInstance.InputsCount

```

### Property **OutputsCount**( ) As long (Read Only)

Returns the number of Outputs.

**Example:**     The following example retrieves in `outputsCount` the number of Outputs of `hybridShapeInstance`:

```VBScript
outputsCount = hybridShapeInstance.OutputsCount

```

### Property **ParametersCount**( ) As long (Read Only)

Returns the number of Parameters.

**Example:**     The following example retrieves in `parametersCount` the number of parameters of `hybridShapeInstance`:

```VBScript
parametersCount = hybridShapeInstance.ParametersCount

```

Methods

### Func **GetInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets an input of a shape instance by its name.

**Parameters:**

` iName`      The name of the input of the shape instance
**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
Set input = shapeInstance.GetInput("Input1")
If TypeName(input)="Nothing" Then
     MsgBox "Input not found"
End If

```

### Func **GetInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Gets an input of a shape instance by its name. Use this method if you want to retrieve a Reference.

**Parameters:**

` iName`      The name of the input of the shape instance
**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
Set input = shapeInstance.GetInput("Input1")
If TypeName(input)="Nothing" Then
     MsgBox "Input not found"
End If

```

### Func **GetInputDataFromPosition**( long  `iPosition`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Gets an input of a hybrid shape instance from its position. Use this method if you want to retrieve a Reference.

**Parameters:**

` iPosition`      The position
**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
Set input = hybridShapeInstance.GetInputFromPosition(2)
If TypeName(input)="Nothing" Then
     MsgBox "Input not found"
End If

```

### Func **GetInputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets an input of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position
**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
Set input = hybridShapeInstance.GetInputFromPosition(2)
If TypeName(input)="Nothing" Then
     MsgBox "Input not found"
End If

```

### Func **GetOutput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets a Ouput by its name.

**Parameters:**

` iName`      The name of the output of the shape instance
**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
Set output = shapeInstance.GetOuput("Output1")
If TypeName(output)="Nothing" Then
     MsgBox "Output not found"
End If

```

### Func **GetOutputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets a Ouput from its position.

**Parameters:**

` iPosition`      The position
**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
Set output = shapeInstance.GetOuputFromPosition(2)
If TypeName(output)="Nothing" Then
     MsgBox "Output not found"
End If

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets a parameter of a shape instance by its name.

**Parameters:**

` iName`      The name of the parameter of the shape instance
**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
Set parameter = shapeInstance.GetParameter("Parameter1")
If TypeName(parameter)="Nothing" Then
     MsgBox "Parameter not found"
End If

```

### Func **GetParameterFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

Gets a parameter of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position
**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
Set parameter = hybridShapeInstance.GetParameterFromPosition(2)
If TypeName(input)="Nothing" Then
      MsgBox "Parameter not found"
End If

```

### Sub **PutInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iInput`)

Defines an input of a shape instance.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a shape instance The input will be a point and its name will be Input1.

```VBScript
shapeInstance.PutInput "Input1",point

```

### Sub **PutInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iInput`)

Defines an input of a shape instance. Use this method if you want to set as input a Reference.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a shape instance The input will be a point and its name will be Input1.

```VBScript
shapeInstance.PutInput "Input1",point

```