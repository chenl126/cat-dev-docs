# DimensionLimit (Object)

**_Represents the limit object of tolerance dimensions._**

## Properties

### Property **DimensionLimitType**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension limit type.

**Legal values** : Valid dimension limit type values are:

  * CATTPSDLNotDefined
  * CATTPSDLNumerical
  * CATTPSDLTabulated
  * CATTPSDLSingleLimit

### Property **Modifier**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension single limit modifier.  
### Property **Nominalvalue**( ) As double (Read Only)

   Returns the dimension limit nominal value.
This value is expressed in millimeters.  
### Property **SymetricValue**( ) As boolean

   Returns or sets whether the dimension limit is symmetric.
TRUE if it is symmetric.  
### Property **TabulatedLimit**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the dimension tabulated limit.
This tabulated limit is expressed as a string.  Methods

### Sub **Limits**( double  `oBottom`,  double  `oUp`)

   Retrieves dimension limit values.
These values are expressed in millimeters.

**Parameters:**

` oBottom`      The dimension limit bottom value
` oUp`      The dimension limit up value

### Sub **PutLimits**( double  `iBottom`,  double  `iUp`)

   Sets dimension limit values.
These values are expressed in millimeters.

**Parameters:**

` iBottom`      The dimension limit bottom value
` iUp`      The dimension limit up value