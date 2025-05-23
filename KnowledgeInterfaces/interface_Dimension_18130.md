# Dimension (Object)

**_Represents the dimension parameter._**
It is an abstract object which is not intended to be created as such, but from which the length and angle parameters derive.

**See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md), [Angle](../KnowledgeInterfaces/interface_Angle_5497.md)

## Properties

### Property **Unit**(| ) As [CATIAUnit](../KnowledgeInterfaces/interface_Unit_3832.md) (Read Only)

   Returns the unit used for this dimension object.  Methods

### Func **ValueAsString2**( long  `iNbDecimals`,  boolean  `iShowTrailingZeros`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Gets the value of the parameter as a string, with a given precision.

**Parameters:**

` iNbDecimals`      the maximum number of decimal places to use to generate the string (minimum 0, maximum 9)
` iShowTrailingZeros`      this argument says if trailing zeros have to be shown  **Example:**      This example gets the value of the existing `dimension` parameter and shows it in a message box

```VBScript
     Dim str
     str = dimension.ValueAsString;
     MessageBox str

```