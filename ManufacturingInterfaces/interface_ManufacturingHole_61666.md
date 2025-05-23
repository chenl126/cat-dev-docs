# ManufacturingHole (Object)

**_Hole Feature in Machining domain._**

## Properties

### Property **Depth**(| ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole depth.

**Returns:**      oDepth A CATIALength object controlling the hole depth (@see CATIALength for more information)

**Example:**     The following example returns in `holeDepth` the depth of hole `firstHole`:

```VBScript
     Set holeDepth = firstHole.Depth

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole diameter.

**Returns:**      oDiameter A CATIALength object controlling the hole diameter (@see CATIALength for more information)

**Example:**     The following example returns in `holeDiam` the diameter of hole `firstHole`:

```VBScript
     Set holeDiam = firstHole.Diameter

```

Methods

### Sub **GetDirection**( double  `oX`,  double  `oY`,  double  `oZ`)

   Returns the hole direction with absolute coordinates.

**Returns:**      3 doubles: X, Y, Z - direction coordinates

**Example:**     The following example returns in `X, Y, Z` the direction coordinates of hole `firstHole`:

```VBScript
     call firstHole.GetDirection(X,Y,Z)

```

### Sub **GetOrigin**( double  `oX`,  double  `oY`,  double  `oZ`)

   Returns the origin point which the hole is anchored to.

**Returns:**      3 doubles: X, Y, Z - Hole origin point coordinates

**Example:**     The following example returns in `X, Y, Z` the origin coordinates of hole `firstHole`:

```VBScript
     call firstHole.GetOrigin(X,Y,Z)

```