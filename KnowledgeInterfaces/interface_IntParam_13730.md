# IntParam (Object)

**_Represents the integer parameter._**
The following example shows how to create it:

```VBScript
Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Dccument
Set part1   = CATDocs.Add("CATPart")
Dim  year As IntParam
Set year    = part1.Part.Parameters.CreateInteger("year", 1998)

```

## Properties

### Property **RangeMax**( ) As long

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
### Property **RangeMin**( ) As long

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
### Property **Value**( ) As long

Returns or sets the value of the integer parameter. Units are expressed in the IS unit system.

**Example:**      This example sets the `year` value to 0 if its value is equal to 2000:

```VBScript
If (year.Value = 2000)  Then
    year.Value = 0
End If

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

Returns an array containing the different values that the int param can take in the case of multiple values.

**Example:**

```VBScript
Dim enumValues () as Variant
ReDim enumValues (anIntegerParameter.GetEnumerateValuesSize() - 1)
anIntegerParameter.GetEnumerateValues(enumValues)
For i = LBound(enumValues) to UBound(enumValues)
  ...
Next

```

### Func **GetEnumerateValuesSize**( ) As long

Returns the number of enumerate values.  
### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

Sets an array containing the different values that the real param can take in the case of multiple values.  
### Sub **SuppressEnumerateValues**( )

Resets the status of the object to a single value object.