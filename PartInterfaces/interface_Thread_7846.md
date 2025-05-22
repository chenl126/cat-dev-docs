# Thread (Object)

**_Represents the Thread feature._**
It threads or taps cylindrical surface .

## Properties

### Property **Depth**( ) As double

Returns the thread/tap depth.

**Returns:**      oDepth Value of the thread/tap depth

**Example:**     The following example returns in `Depth` the depth of thread `firstthread`:

```VBScript
Set Depth = firstthread.Depth

```

### Property **Diameter**( ) As double

Returns the thread/tap diameter.

**Returns:**      oDiameter Value of the thread/tap diameter

**Example:**     The following example returns in `ThreadDiameter` the diameter of thread `firstthread`:

```VBScript
Set ThreadDiameter = firstthread.Diameter

```

### Property **LateralFaceElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the lateral face (must be cylindrical) .
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [Face](../MecModInterfaces/interface_Face_3398.md).  
### Property **LimitFaceElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the limit face (must be planar ) .
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  
### Property **Pitch**( ) As double

Returns the thread/tap pitch.

**Returns:**      oPitch Value of the thread/tap pitch

**Example:**     The following example returns in `ThreadPitch` the thread pitch of thread `firstthread`:

```VBScript
Set ThreadPitch = firstthread.ThreadPitch

```

### Property **Side**( ) As [CatThreadSide](../PartInterfaces/enum_CatThreadSide_34557.md)

Returns the thread or tap side.

**Returns:**      oThreadSide The thread/tap side (see [CatThreadSide](../PartInterfaces/enum_CatThreadSide_34557.md) for list of possible sides)

**Example:**     The following example returns in `ThreadSide` the thread/tap side of thread `firstthread`:

```VBScript
Set ThreadSide = firstthreadoThreadSide

```

### Property **ThreadDescription**( ) As [CATIAStrParam](../KnowledgeInterfaces/interface_StrParam_13874.md) (Read Only)

Returns the thread/tap description parameter. This call is valid only when a standard/user design table created

**Returns:**      oThreadDescParam A Parameter object controlling the thread/tap description (see [StrParam](../KnowledgeInterfaces/interface_StrParam_13874.md) for more information)

**Example:**     The following example returns in `threadDescription` the thread description (M12 etc) of thread `firstthread`:

```VBScript
Set threadDescription = firstthread.ThreadDescription

```

Methods

### Sub **CreateStandardThreadDesignTable**( [CatThreadStandard](../PartInterfaces/enum_CatThreadStandard_60071.md)  `iStandardType`)

Creates a Standard Thread design table .

**Parameters:**

` iStandardType`      Standard type for thread (see
[CatThreadStandard](../PartInterfaces/enum_CatThreadStandard_60071.md) for list of possible types)

**Example:**     The following example creates a standard table for MetricThinPitch for thread `firstthread`:

```VBScript
firstthread.CreateStandardThreadDesignTable catMetricThinPitch

```

### Sub **CreateUserStandardDesignTable**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iStandardName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Creates a UserStandard Thread design table .

**Parameters:**

` iStandardName`      Name of the UserStandard thread. iStandardName should be empty if filepath is to be defined.
` iPath`      Path of the UserStandard file. iPath is empty if the filepath is already defined through CATReffilesPath.

**Example1:**     The following example creates a standard table for UserStandard for thread `firstThread`. The file path is already defined thru CATReffilesPath:

```VBScript
firstThread.CreateUserStandardDesignTable "UserStandard",""

```

**Example2:**     The following example creates a standard table for UserStandard for thread `firstThread` when file path is not defined thru CATReffilesPath:

```VBScript
firstThread.CreateUserStandardDesignTable "","E:\user\standard\UserStandard.txt"

```

### Sub **ReverseDirection**( )

Swap the direction of the thread or the tap.  
### Sub **SetExplicitPolarity**( [CatThreadPolarity](../PartInterfaces/enum_CatThreadPolarity_61832.md)  `iThreadPolarity`)

Sets the thread polarity explicit. Thread polarity is no more evaluated implicitly on basis of support face polarity

**Parameters:**

` iThreadPolarity`      Standard type for thread (see
[CatThreadPolarity](../PartInterfaces/enum_CatThreadPolarity_61832.md) for list of possible types)

**Example:**     The following example sets the thread polarity to Tap explicitly thread `firstthread`:

```VBScript
firstthread.SetExplicitPolarity catTap

```