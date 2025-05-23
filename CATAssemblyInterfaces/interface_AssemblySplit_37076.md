# AssemblySplit (Object)

**_Represents the AssemblySplit object._**

## Properties

### Property **SplittingComponent**(| ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the splitting element.

**Example:**     The following example retrieves in `sptComponent` the splitting component containing the splitting element of the assembly split `assemblySplit`:

```VBScript
     Dim sptComponent As Product
     Set sptComponent = assemblySplit.SplittingComponent

```

### Property **SplittingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md) (Read Only)

   Returns the splitting element.

**Example:**     The following example retrieves in `sptElement` the splitting element of the assembly split `assemblySplit`:

```VBScript
     Dim sptElement As Reference
     Set sptElement = assemblySplit.SplittingElement

```

### Property **SplittingSide**( ) As [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)

   Returns or sets the splitting side. The splitting side is the side of the split object kept after the split, with respect to the splitting element. A positive side refers to the split object side shown by the splitting element normal vector.

**Example:**     The following example returns in `sptSide` the splitting side of the assembly split `assemblySplit`, and then sets it to `catPositiveSide`:

```VBScript
     Set sptSide = assemblySplit.SplittingSide
     assemblySplit.SplittingSide = catPositiveSide

```

Methods

### Sub **ModifySplittingElement**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplittingElement`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iSplittingElemComp`)

   Replaces the splitting element by a new one.

**Parameters:**

` iSplittingElement`      The new face or plane that will split the current body
` iSplittingElemComp`      The component that contains the new splitting element  **Example:**     The following example replaces the existing splitting element of the assembly split `assemblySplit` by `sptElem` contained in the `sptComponent` splitting component

```VBScript
     assemblySplit.ModifySplittingElement(sptElem, _
                                          sptComponent)

```