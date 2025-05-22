# ManufacturingToolMotion (Object)

**_A ManufacturingToolMotion for a Manufacturing Document._**

## Methods

### Func **GetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAttribut`) As [CATIAParameter](../KnowledgeInterfaces/interface_Parameter_17963.md)

Retrieve by is name the attribute of a Manufacturing ToolMotion.
Each attribute is a CKE object.

**Example:**     The following example retreives in `Diameter` the attribute `MfgDiameter` of the Manufacturing ToolMotion `firstToolmotion`

```VBScript
Set Diameter = firstToolmotion.GetAttribute(MfgDiameter)

```

### Func **GetFeedrate**( double  `oFeedrate`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the Feedrate of a Manufacturing Point to point ToolMotion.
If the ToolMotion is not a Manufacturing Point to point, nothing is done.

**Parameters:**

` oFeedrateType`      **Legal values** : oFeedrateType can be:

`"RAPID"`     `"LOCAL"`     `"NONE"`
` oFeedrate`      Feedrate value. (expressed in MKS units : m/s if linear feedrate, or m/turn if angular feedrate)
Feedrate value has a meaning only if oFeedrateType is "LOCAL"  **Example:**     The following example gets the feedrate type of a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
dim FeedVal as double
dim FeedType as CATBSTR
FeedType=SubMotion1.GetFeedrate(FeedVal)

```

### Sub **GetGotoPtPointCoordinates**( double  `oX`,  double  `oY`,  double  `oZ`)

Retrieves coordinates on the ToolMotion.
If the type of the ToolMotion is not MfgSeqMotionPoint, nothing is done.
These coordinates are expressed in the current axis system.
Coordinates units are millimeters.

**Example:**     The following example gets coordinates on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
dim XCoord as double
dim YCoord as double
dim ZCoord as double
Call SubMotion1.GetGotoPtPointCoordinates(XCoord, YCoord, ZCoord)

```

### Func **GetPPWord**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the content of a Manufacturing PP Word ToolMotion.

**Example:**     The following example retrieves in `Message` the content of the Manufacturing PPWord Toolmotion `firstToolmotion`

```VBScript
dim Message as CATBSTR
Message = firstToolmotion.GetPPWord

```

### Func **GetType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

Retrieves the type of a Manufacturing ToolMotion.

**Parameters:**

` oType`      **Legal values** : oType can be:

`"MfgSeqMotionPoint"`     `"MfgSeqMotionPosition"`     `"MfgSeqMotionDelta"`     **Example:**     The following example retrieves in `ThisType` the type of the Manufacturing Toolmotion `firstToolMotion`

```VBScript
dim ThisType as CATBSTR
Set ThisType = firstToolMotion.GetType

```

### Sub **SetFeedrate**( double  `iFeedrate`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFeedrateType`)

Defines the feedrate of a Manufacturing Point to point ToolMotion.
If the ToolMotion is not a Manufacturing Point to point, nothing is done.

**Parameters:**

` iFeedrateType`      **Legal values** : iFeedrateType can be:

`"RAPID"`     `"LOCAL"`     `"NONE"`
` oFeedrate`      Feedrate value. (expressed in MKS units : m/s if linear feedrate, or m/turn if angular feedrate)
Feedrate value is taken into account only if iFeedrateType is "LOCAL"  **Example:**     The following example sets a local feedrate on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
dim FeedVal as double
dim FeedType as CATBSTR
FeedVal = 169.0
FeedType="LOCAL"
Call SubMotion1.SetFeedrate(FeedVal, FeedType)

```

### Sub **SetGotoPtPointCoordinates**( double  `iX`,  double  `iY`,  double  `iZ`)

Defines coordinates on the ToolMotion.
If the type of the ToolMotion is not MfgSeqMotionPoint, nothing is done.
These coordinates are expressed in the current axis system.
Coordinates units are millimeters.

**Example:**     The following example sets coordinates on a Manufacturing Point To Point Toolmotion `submotion1`

```VBScript
dim XCoord as double
dim YCoord as double
dim ZCoord as double
XCoord = 10.0
YCoord = 20.0
ZCoord = 5.0
Call SubMotion1.SetGotoPtPointCoordinates(XCoord, YCoord, ZCoord)

```

### Sub **SetPPWord**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iMessage`)

Adds a line containing iMessage to a Manufacturing PP Word ToolMotion.

**Example:**     The following example adds the line `Message` to the content of the Manufacturing PPWord Toolmotion `firstToolmotion`

```VBScript
firstToolmotion.SetPPWord("Message")

```