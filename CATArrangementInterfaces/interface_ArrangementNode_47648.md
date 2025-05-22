# ArrangementNode (Object)

**_This interface provides access to a CATIAArrangementNode object._**
Use this object to fetch the properties of an ArrangementNode object. **Role:** Use this object to retrieve the bend angle, bend radius and location of an ArrangementNode object.

## Properties

### Property **BendAngle**( ) As double (Read Only)

Returns the BendAngle of the current ArrangementNode.

**Example:**      This example retrieves the BendAngle of the `objNode1` object.

```VBScript
Dim dblBendAngle   As Double
dblBendBendAngle  = objNode1.BendAngle

```

### Property **BendRadius**( ) As double

Returns or sets the BendRadius of the current ArrangementNode.

**Example:**      This example retrieves the BendRadius of the `objNode1` object.

```VBScript
Dim dblBendRadius   As Double
dblBendRadius  = objNode1.BendRadius

```

Methods

### Sub **GetPoint**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioNodeLocation`)

Returns the location of the current ArrangementNode.

**Parameters:**

` iRelAxis`      The relative axis to be considered when calculating the coordinate.
` ioNodeLocation`      The location of the ArrangementNode.

**Example:**      This example retrieves the location of the ArrangementNode object `objNode1`.

```VBScript
Dim dblCoords(3)   As Double
Dim iRelAxis       As Move
'Fetch iRelAxis from the object containing the node
...
objNode1.GetPoint(iRelAxis, dblCoords)

```

### Sub **SetPoint**( [CATIAMove](../InfInterfaces/interface_Move_3742.md)  `iRelAxis`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iNodeLocation`)

Sets the location of the current ArrangementNode.

**Parameters:**

` iRelAxis`      The relative axis to be considered when calculating the coordinate.
` ioNodeLocation`      The location of the ArrangementNode.

**Example:**      This example sets the location of the ArrangementNode object `objNode1`.

```VBScript
Dim dblCoords(3)   As Double
Dim iRelAxis       As Move
'Fetch iRelAxis from the object containing the node
...
dblCoords(0)       = 300.0 '//X
dblCoords(1)       = 500.0 '//Y
dblCoords(2)       = 300.0 '//Z
objNode1.SetPoint(iRelAxis, dblCoords)

```