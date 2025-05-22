# RealParam (Object)

**_Represents the real parameter._**
The following example shows how to create it:

```VBScript
 Dim CATDocs As Documents
 Set CATDocs = CATIA.Documents
 Dim part1 As Document
 Set part1   = CATDocs.Add("CATPart")
 Dim density As RealParam
 Set density = part1.Part.Parameters.CreateReal("density", 2.5)

```

The real parameter is the base object for dimensions.

**See also:**      [Dimension](../KnowledgeInterfaces/interface_Dimension_18130.md)

## Properties

### Property **MaximumTolerance**( ) As double

Returns or sets the value of the maximum tolerance of a parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `MaximumTolerance` value to 0 if its value is bigger than 0:

```VBScript
If (Length.MaximumTolerance < 0.0)  Then
    Length.MaximumTolerance = 0.0
End If

```

### Property **MinimumTolerance**( ) As double

Returns or sets the value of the minimum tolerance of a parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `MinumumTolerance` value to 0 if its value is bigger than 0:

```VBScript
If (Length.MinimumTolerance > 0.0)  Then
    Length.MinimumTolerance = 0.0
End If

```

### Property **RangeMax**( ) As double

Returns or sets the value of the upper bound that the parameter object value can take.

**Example:**      This example sets the `RangeMax` value to 0 if its value is smaller than 0:

```VBScript
If (Length.RangeMax < 0.0 and Length.RangeMaxValidity <> 0)  Then
    Length.RangeMax = 0.0
End If

```

### Property **RangeMaxValidity**( ) As long

Returns or sets the type of the upper bound of the parameter.

0    the upper bound is meaningless 1    the upper bound can be reached 2    the upper bound cannot be reached  
### Property **RangeMin**( ) As double

Returns or sets the value of the lower bound that the parameter object value can take.

**Example:**      This example sets the `RangeMin` value to 0 if its value is bigger than 0:

```VBScript
If (Length.RangeMin > 0.0 and Length.RangeMinValidity <> 0)  Then
    Length.RangeMin = 0.0
End If

```

### Property **RangeMinValidity**( ) As long

Returns or sets the type of the lower bound of the parameter.

0    the lower bound is meaningless 1    the lower bound can be reached 2    the lower bound cannot be reached  
### Property **Value**( ) As double

Returns or sets the value of the real parameter. Units are expressed in the IS unit system, except for lengthes expressed in millimeters, and angles expressed in decimal degrees.

**Example:**      This example sets the `density` value to 1 if its value is greater than 2.5:

```VBScript
If (density.Value > 2.5)  Then
    density.Value = 1
End If

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

Returns an array containing the different values that the real param can take in the case of multiple values.

**Example:**

```VBScript
Dim enumValues () as Variant
ReDim enumValues (aRealParameter.GetEnumerateValuesSize() - 1)
aRealParameter.GetEnumerateValues(enumValues)
For i = LBound(enumValues) to UBound(enumValues)
  ...
Next

```

### Func **GetEnumerateValuesSize**( ) As long

Returns the number of enumerate values.  
### Func **IsEqualTo**( double  `iValueToCompare`) As boolean

Tests the equality of the parameter value with a given value.

**Parameters:**

` iValueToCompare`      The value to compare the parameter value with
**Returns:**

True
    If the current value of the parameter (the one get by the get_Value property, for dimensions notice that it is not the MKS value) is equal to the one given in argument. Notice that two values are considered as equal if their difference is insignificant faced with the two compared values. This method allows you to avoid problems due to computation errors.
False
    If the two values are different.

### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

Sets an array containing the different values that the real param can take in the case of multiple values.  
### Sub **SuppressEnumerateValues**( )

Resets the status of the object to a single value object.