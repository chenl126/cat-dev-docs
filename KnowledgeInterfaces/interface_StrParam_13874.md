# StrParam (Object)

**_Represents the string parameter._**
The following example shows how to create it:

```VBScript
    	Dim CATDocs As Documents
Set CATDocs = CATIA.Documents
Dim part1 As Document
Set part1   = CATDocs.Add("CATPart")
Dim material As String
Set material = part1.Parameters.CreateString("material", "glass")

```

## Properties

### Property **Value**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the string parameter value.

**Example:**     This example returns in `myValue` the value of the string parameter `material`:

```VBScript

```VBScript
myValue = material.Value

```

Methods

### Sub **GetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSafeArray`)

Returns an array containing the different values that the real param can take in the case of multiple values.

**Example:**

```VBScript
Dim enumValues () as Variant
ReDim enumValues (aStrParameter.GetEnumerateValuesSize() - 1)
aStrParameter.GetEnumerateValues(enumValues)
For i = LBound(enumValues) to UBound(enumValues)
  ...
Next

```

### Func **GetEnumerateValuesSize**( ) As long

Returns the number of enumerate values.  
### Sub **SetEnumerateValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iSafeArray`)

Sets an array containing the different values that the StrParam object can take in the case of multiple values.

**Parameters:**

` The`      array of enumerated values.

### Sub **SuppressEnumerateValues**( )

Resets the status of the object to a single value object.