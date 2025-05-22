# EnumParam (Object)

**_Represents the enum parameter._**

## Properties

### Property **ValueEnum**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Returns or sets the value of the EnumParameter object. Units are expressed in the IS unit system, except for lengthes expressed in millimeters, and angles expressed in decimal degrees.

**Example:**      This example sets the `param1` value to 1 if its value is greater than 2.5:

```VBScript
If (density.Value > 2.5)  Then
    density.Value = 1
End If

```