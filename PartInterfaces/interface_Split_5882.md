# Split (Object)

**_Represents the split operation._**
It splits a shape using a splitting element, such as a surface, a face or a plane.

## Properties

### Property **SplittingSide**(| ) As [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)

   Returns or sets the splitting side . The splitting side is the side of the splitting element kept after the split. A positive side refers to the same orientation than the splitting element normal vector.

**Example:**     The following example returns in `sptSide` the splitting side of the split shape `mySplit`, and then sets it to `catPositiveSide`:

```VBScript
     Set sptSide = mySplit.SplittingSide
     mySplit.SplittingSide = catPositiveSide

```