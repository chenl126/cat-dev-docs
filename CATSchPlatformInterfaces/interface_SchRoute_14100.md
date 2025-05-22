# SchRoute (Object)

**_Manage a schematic route data._**

## Methods

### Sub **AddPoints**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPathToAdd`,  long  `iAfterWhichPtNum`)

Add a list of point to a route. Modify the route according to the route mode

**Parameters:**

` iGRR`      graphical primitive of the route to add points to (if NULL, assume there is only one graphical primitive)
` iLDbPtPathToAdd`      A list of X-Y coordinates of points to be added. 2 doubles per point.
` iAfterWhichPtNum`      The point number to add the points after. Use 0 to indicate adding before the first point.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim dbVar2(x) As CATSafeArrayVariant
Dim intVar4 As Integer
 ...
objThisIntf.AddPointsobjArg1,dbVar2,intVar4

```

### Sub **Branch**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRRMain`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iSchBranchRoute`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchBranchRouteCntr`,  [CATIASchAppConnection](../CATSchPlatformInterfaces/interface_SchAppConnection_54308.md)  `oBranchCntn`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `oNewBranchCntr`)

Create a branch from this route.

**Parameters:**

` iGRRMain`      graphical primitive of the "this" route to branch from (if NULL, assume there is only one graphical primitive)
` iSchBranchRoute`      The route to create a branch connection to (from this route)
` iSchBranchRouteCntr`      The extremity connector of the branch
` oBranchCntn`      The branch connection created
` oNewBranchCntr`      The new branch connector created on "this" route
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim objArg2 As SchRoute
Dim objArg3 As SchAppConnector
Dim objArg4 As SchAppConnection
Dim objArg5 As SchAppConnector
 ...
objThisIntf.BranchobjArg1,objArg2,objArg3,objArg4,objArg5

```

### Sub **Break**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Pt1`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Pt2`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `oNewSchRoute`)

Break a route into 2 pieces. The old route is shortened and a new route is created.

**Parameters:**

` iGRR`      graphical primitive of the route to be broken (if NULL, assume there is only one graphical primitive)
` iDb2Pt1`      X-Y coordinates of point 1 to break the route at (this point is **mandatory**).
` iDb2Pt2`      X-Y coordinates of point 2 to break the route at (this point is **optional**). If provided the points in between point 1 and this point will be eliminated. Point 1 is the last point of the shortened old route and point 2 is the first point of the new route. If this point is not provided (sends in a NULL). point 1 and point 2 are the same.
` oNewSchRoute`      The new Schematic route object
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim dbVar2(2) As CATSafeArrayVariant
Dim dbVar3(2) As CATSafeArrayVariant
Dim objArg4 As SchRoute
 ...
objThisIntf.BreakobjArg1,dbVar2,dbVar3,objArg4

```

### Sub **Compress**( )

Compress a the defining points of a route, removing coincident points.

**Example:**

```VBScript
Dim objThisIntf As SchRoute
 ...
objThisIntf.Compress

```

### Sub **Concatenate**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchRoute1Cntr`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iSchRoute2`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchRoute2Cntr`)

Concatenate 2 routes into one. Only works for those that have only one line graphic object. The first route is elongated and is modified. The second route is deleted.

**Parameters:**

` iSchRoute1Cntr`      Connector of this route to concatenate with the second route.
` iSchRoute2`      Second route to be concatenate to the first. iSchRoute2 will be deleted.
` iSchRoute2Cntr`      Connector of second route to concatenate with the first route.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchAppConnector
Dim objArg2 As SchRoute
Dim objArg3 As SchAppConnector
 ...
objThisIntf.ConcatenateobjArg1,objArg2,objArg3

```

### Sub **ConcatenateKeepRoute2**( [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchRoute1Cntr`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iSchRoute2`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iSchRoute2Cntr`)

Concatenate 2 routes into one. Only works for those that have only one line graphic object. The first route is elongated and is modified. The second route is unchanged.

**Parameters:**

` iSchRoute1Cntr`      Connector of this route to concatenate with the second route.
` iSchRoute2`      Second route to be concatenate to the first. iSchRoute2 will be unchanged.
` iSchRoute2Cntr`      Connector of second route to concatenate with the first route.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchAppConnector
Dim objArg2 As SchRoute
Dim objArg3 As SchAppConnector
 ...
objThisIntf.ConcatenateKeepRoute2objArg1,objArg2,objArg3

```

### Sub **GetExtremityCntrs**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `oRouteCntr1`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `oRouteCntr2`)

Get extremity connectors of the route.

**Parameters:**

` iGRR`      graphical primitive of the route to query. (if NULL, assume there is only one graphical primitive)
` oRouteCntr1`      Route connector at first extremity
` oRouteCntr2`      Route connector at second extremity
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim objArg2 As SchAppConnector
Dim objArg3 As SchAppConnector
 ...
objThisIntf.GetExtremityCntrsobjArg1,objArg2,objArg3

```

### Sub **GetPath**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oLDb2PtPath`)

Get the defining points of a route.

**Parameters:**

` iGRR`      graphical primitive of the route get the path from (if NULL, assume there is only one graphical primitive)
` oLDbPtPath`      A list of X-Y coordinates of points. 2 doubles per point.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim objArg2 As SchListOfDoubles
 ...
objThisIntf.GetPathobjArg1,objArg2

```

### Sub **OKToBranch**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iBranchClassType`,  boolean  `oBYes`)

Query whether it is OK to create a branch.

**Parameters:**

` iGRR`      graphical primitive of the route to query. (if NULL, assume there is only one graphical primitive)
` iBranchClassType`      Class type of the branch to create.
` oBYes`      If TRUE, then it is OK to create a branch from a route
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim strVar2 As String
Dim bVar3 As boolean
 ...
objThisIntf.OKToBranchobjArg1,strVar2,bVar3

```

### Sub **OKToBreak**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  boolean  `oBYes`)

Query whether it is OK to break.

**Parameters:**

` iGRR`      graphical primitive of the route to query. (if NULL, assume there is only one graphical primitive)
` oBYes`      If TRUE, then it is OK to break the route
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim bVar2 As boolean
 ...
objThisIntf.OKToBreakobjArg1,bVar2

```

### Sub **OKToConcatenate**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  boolean  `oBYes`)

Query whether it is OK to concatenate.

**Parameters:**

` iGRR`      graphical primitive of the route to query. (if NULL, assume there is only one graphical primitive)
` oBYes`      If TRUE, then it is OK to concatenate the route with another
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim bVar2 As boolean
 ...
objThisIntf.OKToConcatenateobjArg1,bVar2

```

### Sub **OKToModifyPoints**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  boolean  `oBYes`)

Query whether it is OK to modify (add or remove) the points.

**Parameters:**

` iGRR`      graphical primitive of the route to query. (if NULL, assume there is only one graphical primitive).
` oBYes`      If TRUE, then it is OK to add or remove the points from the route
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim bVar2 As boolean
 ...
objThisIntf.OKToModifyPointsobjArg1,bVar2

```

### Sub **RemovePoints**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  long  `iNumOfPtsToRemove`,  long  `iAfterWhichPtNum`)

Remove points from route. Modify the route according to the route mode.

**Parameters:**

` iGRR`      graphical primitive of the route to remove the points from (if NULL, assume there is only one graphical primitive)
` iNumOfPtsToRemove`      The number of points to be removed
` iAfterWhichPtNum`      The point number at which to start removing the point.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim intVar2 As Integer
Dim intVar3 As Integer
 ...
objThisIntf.RemovePointsobjArg1,intVar2,intVar3

```

### Sub **ReshapeExtremity**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iRouteCntr`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2DeltaXY`)

Change the position of the extremity of the route.

**Parameters:**

` iGRR`      graphical primitive of the route to reshape (if NULL, assume there is only one graphical primitive)
` iRouteCntr`      Route connector whose position is to be modified (CATISchAppConnector interface pointer).
` iDb2DeltaXY`      Delta X-Y coordinates of the extremity move
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim objArg2 As SchAppConnector
Dim dbVar3(2) As CATSafeArrayVariant
 ...
objThisIntf.ReshapeExtremityobjArg1,objArg2,dbVar3

```

### Sub **ReshapeExtremity2**( [CatSchIDLRouteMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteMode_63812.md)  `iERouteMode`,  [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iRouteCntr`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2PtToMoveCntrTo`)

Change the position of the extremity of the route. Modify the route according to the route mode.

**Parameters:**

` iERouteMode`      Routing mode.
` iGRR`      graphical primitive of the route to reshape (if NULL, assume there is only one graphical primitive)
` iRouteCntr`      Route connector whose position is to be modified (CATISchConnector interface pointer).
` iDb2PtToMoveCntrTo`      X-Y coordinates of the point to move the connector to.
**Example:**

```VBScript
Dim objThisIntf As SchRoute

Dim objArg2 As SchGRRRoute
Dim objArg3 As SchAppConnector
Dim dbVar4(2) As CATSafeArrayVariant
 ...
objThisIntf.ReshapeExtremity2CatSchIDLRouteMode_Enum,objArg2,objArg3,dbVar4

```

### Sub **SetPath**( [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPath`)

Set the defining points of a route.

**Parameters:**

` iGRR`      graphical primitive of the route to set the path on (if NULL, assume there is only one graphical primitive)
` iLDbPtPath`      A list of X-Y coordinates of points to be set. 2 doubles per point.
**Example:**

```VBScript
Dim objThisIntf As SchRoute
Dim objArg1 As SchGRRRoute
Dim dbVar2(x) As CATSafeArrayVariant
 ...
objThisIntf.SetPathobjArg1,dbVar2

```