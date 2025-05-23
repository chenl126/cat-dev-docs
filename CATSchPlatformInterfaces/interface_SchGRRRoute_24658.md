# SchGRRRoute (Object)

**_Manage the graphical representations of a schematic route._**

## Methods

### Sub **AddPoints**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iLDb2PtPathToAdd`,| | long | `iAfterWhichPtNum`)

   Add a list of point to a route.

**Parameters:**

` iLDbPtPathToAdd`      A list of X-Y coordinates of the points to be added. 2 doubles per point.
` iAfterWhichPtNum`      The point number to add the points after. Use 0 to indicate adding before the first point.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(x) As CATSafeArrayVariant
     Dim intVar3 As Integer
      ...
     objThisIntf.AddPointsdbVar1,intVar3

```

### Sub **Break**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Pt1`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2Pt2`,  [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `oNewGRRRoute`)

   Break a route graphic into 2 pieces. The old graphic is shortened and a new graphic is created.

**Parameters:**

` iDb2Pt1`      X-Y coordinates of point 1 to break the route at (this point is **mandatory**).
` iDb2Pt2`      X-Y coordinates of point 2 to break the route at (this point is **optional**). If provided the points in between point 1 and this point will be eliminated. Point 1 is the last point of the shortened old route and point 2 is the first point of the new route. If this point is not provided (i.e. sends in a NULL). point 1 and point 2 are the same.
` oNewGRRRoute`      The new line string graphic created (CATISchGRRRoute interface pointer)

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(2) As CATSafeArrayVariant
     Dim dbVar2(2) As CATSafeArrayVariant
     Dim objArg3 As SchGRRRoute
      ...
     objThisIntf.BreakdbVar1,dbVar2,objArg3

```

### Sub **Compress**( )

   Compress a the defining points of a route graphic, removing coincident points.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
      ...
     objThisIntf.Compress

```

### Sub **Compress2**( [CatSchIDLRouteUnsetGapsMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteUnsetGapsMode_146155.md)  `iUnsetGaps`)

   Compress the defining points of a route graphic, removing coincident points.

**Parameters:**

` iUnsetGaps`      Whether to unset gaps (in all the effected routes: this route and other routes intersecting it) or not = SchUnsetGapsOn : unset gaps = SchUnsetGapsOff : don't unset gaps

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute

      ...
     objThisIntf.Compress2CatSchIDLRouteUnsetGapsMode_Enum

```

### Sub **Concatenate**( long  `iWhichEnd1`,  [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRRRoute2`,  long  `iWhichEnd2`)

   Concatenate 2 route graphic objects into one. The first route graphic is elongated and the second object is deleted.

**Parameters:**

` iWhichEnd1`      =1 at start point; =2 at end point
` iGRRRoute2`      Second route graphic object (CATISchGRRRoute interface pointer) to be concatenated to the first. This route graphic will be deleted.
` iWhichEnd2`      =1 at start point; =2 at end point

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim intVar1 As Integer
     Dim objArg2 As SchGRRRoute
     Dim intVar3 As Integer
      ...
     objThisIntf.ConcatenateintVar1,objArg2,intVar3

```

### Sub **ConcatenateKeepGRR2**( long  `iWhichEnd1`,  [CATIASchGRRRoute](../CATSchPlatformInterfaces/interface_SchGRRRoute_24658.md)  `iGRRRoute2`,  long  `iWhichEnd2`)

   Concatenate 2 route graphic objects into one. The first route graphic is elongated and the second object is unchanged.

**Parameters:**

` iWhichEnd1`      =1 at start point; =2 at end point
` iGRRRoute2`      Second route graphic object (CATISchGRRRoute interface pointer) to be concatenated to the first. This route graphic will be unchanged.
` iWhichEnd2`      =1 at start point; =2 at end point

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim intVar1 As Integer
     Dim objArg2 As SchGRRRoute
     Dim intVar3 As Integer
      ...
     objThisIntf.ConcatenateKeepGRR2intVar1,objArg2,intVar3

```

### Sub **CreateRouteSymbol**( long  `iSegNum`,  double  `iSegParm`,  [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRRSymbol`,  [CATIASchRouteSymbol](../CATSchPlatformInterfaces/interface_SchRouteSymbol_42372.md)  `oRouteSymbol`)

   Place a symbol on the route.

**Parameters:**

` iSegNum`      The route segment number to place the symbol on.
` iSegParm`      The parameter along the segment used to place the symbol on (0.<=iSegParm<=1.).
` iGRRSymbol`      The graphical primitive (detail) to be used for the symbol.
` oRouteSymbol`      The created route symbol (ditto).

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim intVar1 As Integer
     Dim dbVar2 As Double;
     Dim objArg3 As SchGRR
     Dim objArg4 As SchRouteSymbol
      ...
     objThisIntf.CreateRouteSymbolintVar1,dbVar2,objArg3,objArg4

```

### Sub **GetEndPoint**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2EndPt`)

   Get the end point of the route graphic.

**Parameters:**

` oDb2EndPt`      X-Y coordinates of the end point of the route graphic object.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetEndPointobjArg1

```

### Sub **GetPath**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oLDb2PtPath`)

   Get the defining points of a route graphic.

**Parameters:**

` oLDbPtPath`      A list of X-Y coordinates of the points. 2 doubles per point.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim objArg1 As SchListOfDoubles
     Dim intVar2 As Integer
      ...
     objThisIntf.GetPathobjArg1

```

### Sub **GetStartPoint**( [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2StartPt`)

   Get the start point of the route graphic.

**Parameters:**

` oDb2StartPt`      X-Y coordinates of the start point of the route graphic object.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim objArg1 As SchListOfDoubles
      ...
     objThisIntf.GetStartPointobjArg1

```

### Func **ListRouteSymbols**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

   List route symbols on the route.

**Parameters:**

` oLRouteSymbol`      A list of route symbols. (members are CATIASchRouteSymbol objects).

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim objArg1 As SchListOfObjects
      ...
     Set objArg1 = objThisIntf.ListRouteSymbols

```

### Sub **RemovePoints**( long  `iNumOfPtsToRemove`,  long  `iAfterWhichPtNum`)

   Remove points from route graphic.

**Parameters:**

` iNumOfPtsToRemove`      The number of points to be removed
` iAfterWhichPtNum`      The point number at which to start removing the point.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim intVar1 As Integer
     Dim intVar2 As Integer
      ...
     objThisIntf.RemovePointsintVar1,intVar2

```

### Sub **SetEndPoint**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2EndPt`)

   Set the end point of the route graphic.

**Parameters:**

` iDb2EndPt`      X-Y coordinates of the end point of the route graphic object to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetEndPointdbVar1

```

### Sub **SetPath**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPath`,  [CatSchIDLRouteCompressMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteCompressMode_137134.md)  `iCompress`)

   Set the defining points of a route graphic.

**Parameters:**

` iLDbPtPath`      A list of X-Y coordinates of the points to be set. 2 doubles per point.
` iCompress`      Whether to compress the route (i.e., remove duplicate pts, colinear segments, etc.) or not = SchCompressOn : compress = SchCompressOff : don't compress

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(x) As CATSafeArrayVariant

      ...
     objThisIntf.SetPathdbVar1,CatSchIDLRouteCompressMode_Enum

```

### Sub **SetPath2**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPath`,  [CatSchIDLRouteCompressMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteCompressMode_137134.md)  `iCompress`,  [CatSchIDLRouteUnsetGapsMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteUnsetGapsMode_146155.md)  `iUnsetGaps`)

   Set the defining points of a route graphic.

**Parameters:**

` iLDbPtPath`      A list of X-Y coordinates of the points to be set. 2 doubles per point.
` iCompress`      Whether to compress the route (i.e., remove duplicate pts, colinear segments, etc.) or not = SchCompressOn : compress = SchCompressOff : don't compress
` iUnsetGaps`      Whether to unset gaps (in all the effected routes: this route and other routes intersecting it) or not = SchUnsetGapsOn : unset gaps = SchUnsetGapsOff : don't unset gaps

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(x) As CATSafeArrayVariant

      ...
     objThisIntf.SetPath2dbVar1,CatSchIDLRouteCompressMode_Enum,CatSchIDLRouteUnsetGapsMode_Enum

```

### Sub **SetPath3**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPath`,  [CatSchIDLRouteCompressMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteCompressMode_137134.md)  `iCompress`,  [CatSchIDLRouteUnsetGapsMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteUnsetGapsMode_146155.md)  `iUnsetGaps`,  [CatSchIDLRouteSymbolUpdateMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteSymbolUpdateMode_181706.md)  `iRouteUpdateSymbols`)

   Set the defining points of a route graphic.

**Parameters:**

` iLDb2PtPath`      A list of X-Y coordinates of the points to be set. 2 doubles per point.
` iCompress`      Whether to compress the route (i.e., remove duplicate pts, colinear segments, etc.) or not = catSchIDLCompressOn : compress = catSchIDLCompressOff : don't compress
` iUnsetGaps`      Whether to unset gaps (in all the effected routes: this route and other routes intersecting it) or not = catSchIDLUnsetGapsOn : unset gaps = catSchIDLUnsetGapsOff : don't unset gaps
` iRouteSymbolUpdate`      Whether to update route symbols' positions = catSchIDLSymbolUpdateOff : don't update route symbols = catSchIDLSymbolUpdateOn : update route symbols

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(x) As CATSafeArrayVariant

      ...
     objThisIntf.SetPath3dbVar1,CatSchIDLRouteCompressMode_Enum,CatSchIDLRouteUnsetGapsMode_Enum,CatSchIDLRouteSymbolUpdateMode_Enum

```

### Sub **SetStartPoint**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2StartPt`)

   Set the start point of the route graphic.

**Parameters:**

` iDb2StartPt`      X-Y coordinates of the start point of the route graphic object to be set.

**Example:**

```VBScript
     Dim objThisIntf As SchGRRRoute
     Dim dbVar1(2) As CATSafeArrayVariant
      ...
     objThisIntf.SetStartPointdbVar1

```