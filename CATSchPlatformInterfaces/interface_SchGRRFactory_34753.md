# SchGRRFactory (Object)

**_Factory to create graphical representations of schematic objects._**

## Methods

### Func **CreateGRRCntr**(| ) As [CATIASchGRRCntr](../CATSchPlatformInterfaces/interface_SchGRRCntr_19904.md)

   Create the graphical representation of a Schematic Connector.

**Parameters:**

` oGRRCntr`      The graphical representation of the connector

**Example:**

```VBScript
     Dim objThisIntf As SchGRRFactory
     Dim objArg1 As SchGRRCntr
      ...
     Set objArg1 = objThisIntf.CreateGRRCntr

```

### Func **CreateGRRGroup**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLPrimitive`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Create the graphical representation of a Schematic Group.

**Parameters:**

` iLPrimitives`      A list of 2D drafting detail pointers Members are CATI2DDetail interface poiners.
` oGRRGroup`      The graphical representation of the Group

**Example:**

```VBScript
     Dim objThisIntf As SchGRRFactory
     Dim objArg1 As SchListOfObjects
     Dim objArg2 As AnyObject
      ...
     Set objArg2 = objThisIntf.CreateGRRGroup(objArg1)

```

### Sub **CreateGRRRoute**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDbLinePath`,  [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `oGRRRoute`)

   Create the graphical representation of a Schematic Route.

**Parameters:**

` iLDbPtPath`      A list of X-Y coordinates of points defining the Route. 2 doubles per point.
` oGRRRoute`      The graphical representation of the Route

**Example:**

```VBScript
     Dim objThisIntf As SchGRRFactory
     Dim dbVar1(x) As CATSafeArrayVariant
     Dim objArg3 As SchGRRRoute
      ...
     objThisIntf.CreateGRRRoutedbVar1,objArg3

```

### Sub **CreateGRRRouteEllipse**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDbXYSeedPt`,  [CATIASchGRRRouteEllipse](../CATSchPlatformInterfaces/interface_SchGRRRouteEllipse_66686.md)  `oGRRRouteEllipse`)

   Create the graphical representation of a Schematic Route Ellipse.

**Parameters:**

` iDbXYSeedPt`      X-Y coordinate of the seed point for the ellipse. If NULL, the seed point will not be set.
` oGRRRouteEllipse`      The graphical representation of the Route Ellipse

**Example:**

```VBScript
     Dim objThisIntf As SchGRRFactory
     Dim dbVar1(X) As CATSafeArrayVariant
     Dim objArg2 As SchGRRRouteEllipse
      ...
     objThisIntf.CreateGRRRouteEllipsedbVar1,objArg2

```

### Func **CreateGRRZone**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLPrimitive`) As [CATIASchGRRZone](../CATSchPlatformInterfaces/interface_SchGRRZone_19924.md)

   Create the graphical representation of a Schematic Zone.

**Parameters:**

` iLPrimitives`      A list of 2D drafting object pointers defining the zone boundaries.
` oGRRZone`      The graphical representation of the Zone

**Example:**

```VBScript
     Dim objThisIntf As SchGRRFactory
     Dim objArg1 As SchListOfObjects
     Dim objArg2 As SchGRRZone
      ...
     Set objArg2 = objThisIntf.CreateGRRZone(objArg1)

```