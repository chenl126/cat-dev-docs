# Unit (Object)

**_Represents CATIAUnit object._**
This interface allows convertion.

## Properties

### Property **Magnitude**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the magnitude associated to the unit.  
### Property **Symbol**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the symbol associated to the unit.  Methods

### Func **ConvertFromMKS**( double  `iValueInMKS`) As double

Convert the initial value (expressed in MKS unit) in its equivalent in the current unit.

**Parameters:**

` iValueInThisUnit`      The initial value in MKS unit.
` oValueInMKS`      The final value in the current unit.

### Func **ConvertFromStorageUnit**( double  `iValueInStorageUnit`) As double

Convert the initial value (expressed in storage unit) in its equivalent in the current unit.

**Parameters:**

` iValueInStorageUnit`      The initial value in storage unit.
` oValueInThisUnit`      The final value in the current unit.

### Func **ConvertToMKS**( double  `iValueInThisUnit`) As double

Convert the initial value in its equivalent in MKS unit.

**Parameters:**

` iValueInThisUnit`      The initial value in the current unit.
` oValueInMKS`      The final value in the corresponding MKS unit.

### Func **ConvertToStorageUnit**( double  `iValueInThisUnit`) As double

Convert the initial value in its equivalent in storage unit.

**Parameters:**

` iValueInThisUnit`      The initial value in the current unit.
` oValueInStorageUnit`      The final value in the corresponding storage unit.