# SystemConfiguration (Object)

**_Provides abstractions to resources which depend on the platform or the current configuration._**

## Properties

### Property **OperatingSystem**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns a string which identifies the operating system on which the application is currently running. Examples of identifiers include: `intel_a`, `solaris_a`, `aix_a`, `win_a` and `hpux_a`.

**Parameters:**

` oOperatingSystem`      The operating system identifier.

### Property **ProductCount**( ) As long (Read Only)

   Returns the number of product names names currently known to the system.

**Parameters:**

` oProductCount`      The number of product names currently known to the system.

### Property **Release**( ) As long (Read Only)

   Returns the CATIA release number.

**Parameters:**

` oVersion`      The CATIA release number.

### Property **ServicePack**( ) As long (Read Only)

   Returns the CATIA service pack number.

**Parameters:**

` oServicePack`      The CATIA service pack number.

### Property **Version**( ) As long (Read Only)

   Returns the CATIA version number (usually version 5).

**Parameters:**

` oVersion`      The CATIA version.
Methods

### Sub **GetProductNames**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioProductNames`)

   Returns the product names of all the licenses currently known to the system.

**Parameters:**

` CATSafeArrayVariant`      An properly dimensioned array of strings in which the product names will be stored.

**Example:**      This example determines if the first product in the list of known product names is authorized.

```VBScript
     Dim SystemConfiguration1 As SystemConfiguration
     Set SystemConfiguration1 = CATIA.SystemConfiguration
     ReDim NameArray(SystemConfiguration1.ProductNamesCount)
     SystemConfiguration1.GetProductNames NameArray
     MsgBox "IsProductAuthorized for product " & NameArray(0) & "  returns " & SystemConfiguration1.IsProductAuthorized(NameArray(0))

```

### Func **IsProductAuthorized**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProductName`) As boolean

   Returns `True` if the specified product is authorized, `False` otherwise.

**Parameters:**

` iProductName`      The name of the product to check.
` oAuthorized`      A boolean which specifies if the product is authorized.