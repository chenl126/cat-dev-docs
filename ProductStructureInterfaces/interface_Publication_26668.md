# Publication (Object)

**_The interface to access a CATIAPublication._**

## Properties

### Property **Relay**( [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iPub`) (Write Only)

Valuates a publication object with another publication object. **Role:** This method allows to valuate a publication with an intermediate one.

**Parameters:**

` iPub`      The intermediate publication object

**Example:** The following example valuates the publication object `Pub1` with the publication object `Pub2`

```VBScript
Pub1.Relay(Pub2)

```

### Property **Valuation**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns published object. **Role:** This method gives access to the finally published object.

**Parameters:**

` oRef`      The final reference of the publication object.

**Example:** This example returns the final reference `Ref` of the publication object `Pub1`.

```VBScript
Dim Ref As Reference
Ref = Pub1.Valuation

```