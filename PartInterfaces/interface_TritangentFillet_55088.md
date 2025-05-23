# TritangentFillet (Object)

**_The Tritangent Fillet feature : a fillet is built between 3 faces,
2 faces will be relimited, the third one ("face to remove") will
be used for fillet tangency ; this face will disappear within the resulting shape._**

## Properties

### Property **FaceToRemove**(| ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the face to be removed by the tritangent fillet.

**Returns:**      oFaceToRemove The face to be removed by the fillet (@see CATIAReference for more information)

**Example:**     The following example returns in `removedFace` the face to be removed of
tritangent fillet `firstTritangentFillet`:

```VBScript
     Set removedFace = firstTritangentFillet.**FaceToRemove**

```

### Property **FirstFace**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the first face limiting the tritangent fillet.

**Returns:**      oFirstFace The limiting face (@see CATIAReference for more information)

**Example:**     The following example returns in `face1` the first limiting face of
tritangent fillet `firstTritangentFillet`:

```VBScript
     Set face1 = firstTritangentFillet.**FirstFace**

```

### Property **SecondFace**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the second face limiting the tritangent fillet.

**Returns:**      oSecondFace The limiting face (@see CATIAReference for more information)

**Example:**     The following example returns in `face2` the second limiting face of
tritangent fillet `firstTritangentFillet`:

```VBScript
     Set face2 = firstTritangentFillet.**SecondFace**

```