# Fillet (Object)

**_Represents the fillet shape._**
It is the base object for face fillets and edge fillets.

**See also:**      [FaceFillet](../PartInterfaces/interface_FaceFillet_21018.md), [EdgeFillet](../PartInterfaces/interface_EdgeFillet_21112.md)

## Properties

### Property **FilletBoundaryRelimitation**(| ) As [CatFilletBoundaryRelimitation](../PartInterfaces/enum_CatFilletBoundaryRelimitation_178785.md)

   Returns or sets the fillet boundary relimitation mode. This boundary relimitation mode is used when computing the fillet.

**Example:**     The following example returns in `mode` the fillet boundary relimitation mode of the `firstFillet` fillet, and then sets it to `catMinimumFilletBoundaryRelimitation`, so that the fillet expands up to the limits of the smallest shell:

```VBScript
     Set mode = firstFillet.FilletBoundaryRelimitation
     Set FirstFillet.FilletBoundaryRelimitation = catMinimumFilletBoundaryRelimitation

```

### Property **FilletTrimSupport**( ) As [CatFilletTrimSupport](../PartInterfaces/enum_CatFilletTrimSupport_86376.md)

   Returns or sets the fillet Trim Support mode. This Trim Support mode is used when computing the fillet.

**Example:**     The following example returns in `mode` the fillet Trim Support mode of the `firstFillet` fillet, and then sets it to `catMinimumFilletTrimSupport`, so that the fillet expands up to the limits of the smallest shell:

```VBScript
     Set mode = firstFillet.FilletTrimSupport
     Set FirstFillet.FilletTrimSupport = catNoTrimFilletSupport

```