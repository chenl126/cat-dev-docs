# Roughness (Object)

**_Interface to manage Roughness TPS._**
TPS for Technological Product Specifications.

## Properties

### Property **Applicability**( ) As short

Retrieves or sets roughness applicability.  
### Property **Obtention**( ) As short

Retrieves or sets roughness obtention mode.  Methods

### Func **Field**( short  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves roughness field.

```VBScript
                                     Field 4
                     Field 1     ------------------
                                /         (Field 9)
                     Field 2   /
                              / (Field 8)  Field 5
                         \   /
               Field 3    \ /    Field 7   Field 6

 Pour le champs 7 les lettres autorisees sont :
 M, C, R, P, X, = ,L (symbole perpendicularite de la DSES)

```

**Parameters:**

` iIndex`      Field index, from 1 to 9 from V5R13 (Fields 8 and 9 added). from 1 to 7 before V5R13
` oField`      The contain of the iIndex field.

### Sub **SetField**( short  `iIndex`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iField`)

Set roughness field.

```VBScript
                                     Field 4
                     Field 1     ------------------
                                /         (Field 9)
                     Field 2   /
                              / (Field 8)  Field 5
                         \   /
               Field 3    \ /    Field 7   Field 6

 Pour le champs 7 les lettres autorisees sont :
 M, C, R, P, X, = ,L (symbole perpendicularite de la DSES)

```

**Parameters:**

` iIndex`      Field index, from 1 to 9 from V5R13 (Fields 8 and 9 added). from 1 to 7 before V5R13
` iField`      The contain of the iIndex field.