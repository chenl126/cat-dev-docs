# Hole (Object)

**_Hole Feature in Part Design._**

## Properties

### Property **AnchorMode**( ) As [CatHoleAnchorMode](../PartInterfaces/enum_CatHoleAnchorMode_58938.md)

Returns the hole anchor mode.
This information is pertinent when hole type is Counterbored or Counterdrilled only.

**Returns:**      oMode The hole anchor mode (see [CatHoleAnchorMode](../PartInterfaces/enum_CatHoleAnchorMode_58938.md) for list of possible types)

**Example:**     The following example returns in `holeAnchorMode` the anchor mode of hole `firstHole`:

```VBScript
Set holeAnchorMode = firstHole.AnchorMode

```

### Property **BottomAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the hole bottom angle.
This call is valid when the hole bottom type is : VBottom.

**Returns:**      oBottomAngle An Angle object controlling the hole bottom angle (see [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) for more information)

**Example:**     The following example returns in `holeBottomAngle` the bottom angle of hole `firstHole`:

```VBScript
Set holeBottomAngle = firstHole.BottomAngle

```

### Property **BottomLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

Returns the bottom limit.
This call is valid when the hole bottom type is : BlindHole or ThruHole.

**Returns:**      oBottomLimit A Limit object controlling the hole bottom limit (see [Limit](../PartInterfaces/interface_Limit_5781.md) for more information)

**Example:**     The following example returns in `holeBottomLimit` the bottom limit of hole `firstHole`:

```VBScript
Set holeBottomLimit = firstHole.BottomLimit

```

### Property **BottomType**( ) As [CatHoleBottomType](../PartInterfaces/enum_CatHoleBottomType_61261.md)

Returns the hole bottom type.

**Returns:**      oBottomType The hole bottom type (see [CatHoleBottomType](../PartInterfaces/enum_CatHoleBottomType_61261.md) for list of possible types)

**Example:**     The following example returns in `holeBottomType` the bottom type of hole `firstHole`:

```VBScript
Set holeBottomType = firstHole.BottomType

```

### Property **CounterSunkMode**( ) As [CatCSHoleMode](../PartInterfaces/enum_CatCSHoleMode_33299.md)

Returns the mode of a countersunk hole .

**Returns:**      CSMode Value of the countersunk mode (see [CatCSHoleMode](../PartInterfaces/enum_CatCSHoleMode_33299.md) for list of possible types)

**Example:**     The following example returns in `CSMode` the CSMode of hole `firsthole`:

```VBScript
Set CSMode = firsthole.CounterSunkMode

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole diameter.

**Returns:**      oDiameter A Length object controlling the hole diameter (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeDiam` the diameter of hole `firstHole`:

```VBScript
Set holeDiam = firstHole.Diameter

```

### Property **HeadAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the hole head angle.
This call is valid when the hole type is : Tapered or Counterdrilled or Countersunk.

**Returns:**      oHeadAngle An Angle object controlling the hole head angle (see [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) for more information)

**Example:**     The following example returns in `holeHeadAngle` the head angle of hole `firstHole`:

```VBScript
Set holeHeadAngle = firstHole.HeadAngle

```

### Property **HeadDepth**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole head depth.
This call is valid when the hole type is : Counterbored or Counterdrilled or Countersunk.

**Returns:**      oHeadDepth A Length object controlling the hole head depth (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeHeadDepth` the head depth of hole `firstHole`:

```VBScript
Set holeHeadDepth = firstHole.HeadDepth

```

### Property **HeadDiameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole head diameter.
This call is valid when the hole type is : Counterbored or Counterdrilled.

**Returns:**      oHeadDiameter A Length object controlling the hole head diameter (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeHeadDiam` the head diameter of hole `firstHole`:

```VBScript
Set holeHeadDiam = firstHole.HeadDiameter

```

### Property **HoleThreadDescription**( ) As [CATIAStrParam](../KnowledgeInterfaces/interface_StrParam_13874.md) (Read Only)

Returns the hole thread description parameter. This call is valid when the hole threading mode is : CATThreadedHoleThreading.
This call is valid only when a standard/user design table exists

**Returns:**      oThreadDescParam A Parameter object controlling the hole thread description (see [StrParam](../KnowledgeInterfaces/interface_StrParam_13874.md) for more information)

**Example:**     The following example returns in `holeThreadDescription` the thread description (M12 etc) of hole `firstHole`:

```VBScript
Set holeThreadDescription = firstHole.HoleThreadDescription

```

### Property **ThreadDepth**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole thread depth.
This call is valid when the hole threading mode is : CATThreadedHoleThreading.

**Returns:**      oThreadDepth A Length object controlling the hole thread depth (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeThreadDepth` the thread depth of hole `firstHole`:

```VBScript
Set holeThreadDepth = firstHole.ThreadDepth

```

### Property **ThreadDiameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole thread diameter.
This call is valid when the hole threading mode is : CATThreadedHoleThreading.

**Returns:**      oThreadDiameter A Length object controlling the hole thread diameter (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeThreadDiameter` the thread diameter of hole `firstHole`:

```VBScript
Set holeThreadDiameter = firstHole.ThreadDiameter

```

### Property **ThreadPitch**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the hole thread pitch.
This call is valid when the hole threading mode is : CATThreadedHoleThreading.

**Returns:**      oThreadPitch A Length object controlling the hole thread pitch (see [Length](../KnowledgeInterfaces/interface_Length_8108.md) for more information)

**Example:**     The following example returns in `holeThreadPitch` the thread pitch of hole `firstHole`:

```VBScript
Set holeThreadPitch = firstHole.ThreadPitch

```

### Property **ThreadSide**( ) As [CatHoleThreadSide](../PartInterfaces/enum_CatHoleThreadSide_58605.md)

Returns the hole thread side.

**Returns:**      oThreadSide The hole thread side (see [CatHoleThreadSide](../PartInterfaces/enum_CatHoleThreadSide_58605.md) for list of possible sides)

**Example:**     The following example returns in `holeThreadSide` the thread side of hole `firstHole`:

```VBScript
Set holeThreadSide = firstHole.ThreadSide

```

### Property **ThreadingMode**( ) As [CatHoleThreadingMode](../PartInterfaces/enum_CatHoleThreadingMode_81830.md)

Returns the hole threading mode.

**Returns:**      oThreadingMode The hole threading mode (see [CatHoleThreadingMode](../PartInterfaces/enum_CatHoleThreadingMode_81830.md) for list of possible types)

**Example:**     The following example returns in `holeThreadingMode` the threading mode of hole `firstHole`:

```VBScript
Set holeThreadingMode = firstHole.ThreadingMode

```

### Property **Type**( ) As [CatHoleType](../PartInterfaces/enum_CatHoleType_25588.md)

Returns the hole type.

**Returns:**      oType The hole type (see [CatHoleType](../PartInterfaces/enum_CatHoleType_25588.md) for list of possible types)

**Example:**     The following example returns in `holeType` the type of hole `firstHole`:

```VBScript
Set holeType = firstHole.Type

```

Methods

### Sub **CreateStandardThreadDesignTable**( [CatHoleThreadStandard](../PartInterfaces/enum_CatHoleThreadStandard_90823.md)  `iStandardType`)

Creates a Standard Thread design table .
This call is valid when the hole threading mode is : CATThreadedHoleThreading.

**Parameters:**

` iStandardType`      Standard type for thread (see
[CatHoleThreadStandard](../PartInterfaces/enum_CatHoleThreadStandard_90823.md) for list of possible types)

**Example:**     The following example creates a standard table for MetricThinPitch for hole `firstHole`:

```VBScript
firstHole.CreateStandardThreadDesignTable catHoleMetricThinPitch

```

### Sub **CreateUserStandardDesignTable**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iStandardName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Creates a UserStandard Thread design table .
This call is valid when the hole threading mode is : CATThreadedHoleThreading.

**Parameters:**

` iStandardName`      Name of the UserStandard thread. iStandardName should be empty if filepath is to be defined.
` iPath`      Path of the UserStandard file. iPath is empty if the filepath is already defined through CATReffilesPath.

**Example1:**     The following example creates a standard table for UserStandard for hole `firstHole`. The file path is already defined thru CATReffilesPath:

```VBScript
firstHole.CreateUserStandardDesignTable "UserStandard",""

```

**Example2:**     The following example creates a standard table for UserStandard for hole `firstHole` when file path is not defined thru CATReffilesPath:

```VBScript
firstHole.CreateUserStandardDesignTable "","E:\user\standard\UserStandard.txt"

```

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

Returns the hole direction with absolute coordinates.
It provides a safe array with 3 elements : X, Y, Z direction coordinates

**Returns:**      oDirection The direction coordinates

**Example:**     The following example returns in `dirArray` the direction coordinates of hole `firstHole`:

```VBScript
Call firstHole.GetDirection dirArray
Set x = dirArray[1]
Set y = dirArray[2]
Set z = dirArray[3]

```

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioOrigin`)

Returns the origin point which the hole is anchored to.
This point belongs to a tangent plane.

**Returns:**      oOrigin A Safe Array made up of 3 doubles : X, Y, Z - Hole origin point coordinates

**Example:**     The following example returns in `coordArray` the coordinates of hole `firstHole`:

```VBScript
Call firstHole.GetOrigin coordArray
Set x = coordArray[1]
Set y = coordArray[2]
Set z = coordArray[3]

```

### Sub **Reverse**( )

Reverses the hole direction .

**Example:**     The following example reverses the current direction of hole `firstHole`:

```VBScript
firstHole.Reverse()

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDirection`)

Sets the hole associative direction.

**Parameters:**

` iDirection`      A Reference object to an edge or a line (see
[Reference](../InfInterfaces/interface_Reference_17481.md) for more information)
The following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) and [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).

**Example:**     The following example sets the support direction of hole `firstHole` with `holeDirRef` direction reference :

```VBScript
firstHole.SetDirection holeDirref

```

### Sub **SetOrigin**( double  `iX`,  double  `iY`,  double  `iZ`)

Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.

**Parameters:**

` iX`      Origin point x absolute coordinate
` iY`      Origin point y absolute coordinate
` iZ`      Origin point z absolute coordinate

**Example:**     The following example sets the coordinates of hole `firstHole` to 10., 20., -5. :

```VBScript
firstHole.SetOrigin 10., 20., 5.

```