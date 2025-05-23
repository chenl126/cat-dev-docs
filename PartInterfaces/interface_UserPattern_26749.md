# UserPattern (Object)

**_Represents the user pattern._**
The shape is copied along user's positions.

## Properties

### Property **AnchorPoint**(| ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns the anchor point of the user pattern.

**Example:**     The following example returns in `anchor` the anchor point of the Pattern `firstPattern`:

```VBScript
     Set anchor = firstPattern.AnchorPoint

```

### Property **FeatureToLocatePositions**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the collection of feature to locate instances.

**Example:**     The following example returns in `list` the list of feature to locate instances of the Pattern `firstPattern`:

```VBScript
     Set list = firstPattern.FeatureToLocatePositions

```

Methods

### Sub **AddFeatureToLocatePositions**( [CATIABase](../System/interface_AnyObject_17321.md)  `iFeatureToLocatePositions`)

   Adds a new feature to locate instances.

**Parameters:**

` iFeatureToLocatePositions`      The new object containing points of positioning  **Example:**     The following example adds the new feature `feature` to locate instances of the Pattern `firstPattern`:

```VBScript
     call firstPattern.AddFeatureToLocatePositions(object)

```