# Stiffener (Object)

**_Represents the stiffener shape._**
A stiffener is made up of a sketch used as the stiffener profile, that is extruded (offset) and that fills the nearest shape. This is a "positive" shape: it adds material to the body it belongs to.

## Properties

### Property **IsFromTop**( ) As boolean

Returns or sets whether the stiffener is From Side or From Top.
**True** if the stiffener is From Top stiffener with respect to the base sketch. **False** if the stiffener is From Side stiffener with respect to the base sketch.

**Example:**     The following example returns in `FromTopFlag` whether the `firstStiffener` stiffener is From Top, and then sets it as From Top stiffener with respect to its base sketch:

```VBScript
Set FromTopFlag = firstStiffener.IsFromTop
firstStiffener.IsFromTop  = True

```

### Property **IsSymmetric**( ) As boolean

Returns or sets whether the stiffener is symmetric.
**True** if the stiffener is symmetric with respect to the base sketch.

**Example:**     The following example returns in `symFlag` whether the `firstStiffener` stiffener is symmetric, and then sets it as symmetric with respect to its base sketch:

```VBScript
Set symFlag = firstStiffener.IsSymmetric
firstStiffener.IsSymmetric  = True

```

### Property **Thickness**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the stiffener thickness. This is half of the thickness if the stiffener is symmetrical, and the thickness otherwise.

**Example:**     The following example returns in `thickness` the thickness of the `firstStiffener` stiffener:

```VBScript
Set thickness = firstStiffener.Thickness

```

### Property **ThicknessFromTop**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the stiffener thickness top in case of From Top stiffener. This is equal to first thickness if the stiffener is symmetrical,

**Example:**     The following example returns in `thicknessfromtop` the thickness of the `firstStiffener` stiffener:

```VBScript
Set thicknessfromtop = firstStiffener.ThicknessFromTop

```

Methods

### Sub **ReverseDepth**( )

Reverses the stiffener direction. This is useful for finding the shape to reach.

**Example:**     The following example reverses the current direction of the `firstStiffener` stiffener:

```VBScript
firstStiffener.ReverseDepth

```

### Sub **ReverseThickness**( )

Reverses the stiffener thickness direction. The stiffener thickness is swapped with respect to the base sketch.

**Example:**     The following example reverses the current direction of the `firstStiffener` stiffener:

```VBScript
firstStiffener.ReverseThickness

```