# SewSurface (Object)

**_Represents the sewing operation._**
It sews a shape using a sewing element, such as a surface or a face

## Properties

### Property **SewingIntersectionMode**(| ) As [CatSewingIntersectionMode](../PartInterfaces/enum_CatSewingIntersectionMode_131529.md)

   Returns or sets the sewing mode . The sewing side is the side of the body kept after the sewing. A positive side refers to the same orientation than the sewing element normal vector.

**Example:**     The following example returns in `sptSide` the sewing side of the sew shape `mySew`, and then sets it to `catPositiveSide`:

```VBScript
     Set sptSide = mySew.SewingSide
     mySew.SewingSide = catPositiveSide

```

### Property **SewingSide**( ) As [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)

   Returns or sets the sewing side . The sewing side is the side of the body kept after the sewing. A positive side refers to the same orientation than the sewing element normal vector.

**Example:**     The following example returns in `sptSide` the sewing side of the sew shape `mySew`, and then sets it to `catPositiveSide`:

```VBScript
     Set sptSide = mySew.SewingSide
     mySew.SewingSide = catPositiveSide

```

Methods

### Sub **SetVolumeSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolume`)

   Sets the volume support for volume sew surface.

**Parameters:**

` iVolume`      A Reference object to a volume (see
[Reference](../InfInterfaces/interface_Reference_17481.md) for more information)

**Example:**     The following example sets the volume support of SewSurface `firstSewSurface` to `volumeExtrude` volume reference :

```VBScript
     firstSewSurface.SetVolumeSupport volumeExtrudeRef

```