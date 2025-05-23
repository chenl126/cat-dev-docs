# SolidCombine (Object)

**_The interface to access a CATIASolidCombine._**

## Properties

### Property **FirstComponentDirection**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the direction of first component of SolidCombine.

**Example:**     The following example returns in `firstDirection` the direction of first component of `firstSolidCombine` SolidCombine feature, and then sets it to the `firstDirection2` direction element.

```VBScript
     Set firstDirection = firstSolidCombine.FirstComponentDirection
     Set firstSolidCombine.FirstComponentDirection = firstDirection2

```

### Property **FirstComponentProfile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the profile of first component of SolidCombine.

**Example:**     The following example returns in `firstProfile` the profile of first component of `firstSolidCombine` SolidCombine feature, and then sets it to the `firstProfile2` profile element:

```VBScript
     Set firstProfile = firstSolidCombine.FirstComponentProfile
     Set firstSolidCombine.FirstComponentProfile = firstProfile2

```

### Property **SecondComponentDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the direction of second component of SolidCombine.

**Example:**     The following example returns in `secondDirection` the direction of second component of `firstSolidCombine` SolidCombine feature, and then sets it to the `secondDirection2` direction element.

```VBScript
     Set secondDirection = firstSolidCombine.SecondComponentDirection
     Set firstSolidCombine.SecondComponentDirection = secondDirection2

```

### Property **SecondComponentProfile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the profile of second component of SolidCombine.

**Example:**     The following example returns in `secondProfile` the profile of second component of `firstSolidCombine` SolidCombine feature, and then sets it to the `secondProfile2` profile element:

```VBScript
     Set secondProfile = firstSolidCombine.SecondComponentProfile
     Set firstSolidCombine.SecondComponentProfile = secondProfile2

```