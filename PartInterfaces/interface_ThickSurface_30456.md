# ThickSurface (Object)

**_Represents the ThickSurface feature._**
It thicks surface using an offset element (such as a surface or a skin) and two offset values TopOffset and Botoffset. TopOffset is the offset between the offset element and the top skin of the feature. BotOffset is the offset between the offset element and the bottom skin of the feature.

## Properties

### Property **BotOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the value of the bottom offset.

**Example:**     The following example returns in `botoffset` the bottom offset of the thicksurface `firstThickSurface`:

```VBScript
Set botoffset = firstThickSurface.BotOffset

```

### Property **OffsetSide**( ) As long (Read Only)

Returns the offset direction (defines in regards of the normal direction) .

**Example:**     The following example returns in `offsetside` the side of the ThickSurface `firstThickSurface`:

```VBScript
Set offsetside = firstThickSurface.OffsetSide

```

### Property **TopOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the value of the top offset.

**Example:**     The following example returns in `topoffset` the top offset of the ThickSurface `firstThickSurface`:

```VBScript
Set topoffset = firstThickSurface.TopOffset

```

Methods

### Sub **swap_OffsetSide**( )

Swap the side of the offset.  **Example:**     The following example changes the side of the ThickSurface `firstThickSurface`:

```VBScript
call firstThickSurface.swap_OffsetSide()

```