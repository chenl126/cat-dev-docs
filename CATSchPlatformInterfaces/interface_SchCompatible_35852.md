# SchCompatible (Object)

**_Provides connecting rule to schematic objects._**

## Methods

### Sub **GetBestCntrForRoute**(| [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb2PlacementPt`,| | [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md) | `iGRR`,| | [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md) | `iLOKCntrs`,| | [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md) | `oDb2CntrPt`,| | [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md) | `oBestCntr`)

   Find the best-fit connector to be used to connect a route to.

**Parameters:**

` iDb2PlacementPt`      X-Y coordinates of the target (component or route) graphic selection point.
` iGRR`      Pointer to the graphical image of a component or to the primitive of a route
` iLOKCntrs`      A list of compatible and available connectors on the component. Members are CATISchAppConnector interface pointers. This is an **Output** of IsTargetOKForRoute
` oDb2CntrPt`      X-Y coordinates of the best-fit connector point.
` oBestCntr`      Best-fit connector

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim dbVar1(2) As CATSafeArrayVariant
     Dim objArg2 As SchGRR
     Dim objArg3 As SchListOfObjects
     Dim objArg4 As SchListOfDoubles
     Dim objArg5 As SchAppConnector
      ...
     objThisIntf.GetBestCntrForRoutedbVar1,objArg2,objArg3,objArg4,objArg5

```

### Sub **GetBestFitInsertInfo**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2PlacementPt`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iInsertCompatInfo`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ioInsertInfo`,  boolean  `iBYesCycleAllSolns`)

   Find the best-fit connector(s) to be used for inserting a component into a route.

**Parameters:**

` iDb2PlacementPt`      X-Y coordinates of the target component graphical selection point.
` iInsertCompatInfo`      Pointer to an internal class which contains structured information This is an **output** of IsTargetOKForInsert
` ioInsertInfo`      Pointer to an internal class which contains structured information for how to inesrt a component into a route. Caller must initialize this pointer to NULL when calling this code the **first** time. This is used as an **input** to CATISchComponent::InsertIntoRouteWithInfo
` iBYesCycleAllSolns`      default is FALSE, and ioInsertInfo is an output for the best fit solution. When there are more than one internal flows that can be used for insertion, this routine will choose the best solution in the following order:

   linear internal flow parallel to x-axis
   linear internal flow parallel to y-axis
   corner internal flow
   others
If iBYesCycleAllSolns =TRUE, then the implementation will calculate all possible solutions and allow the caller to recall this code with the same ioInsertInfo. **if and only if current input iDB2PlacementPt is the the same as the previous one**. Otherwise, the insertion position of the component on the route is different and the previously calculated solutions are all invalid for the current call. If the iDB2PlacementPt is the same as the previous one and iBYesCycleAllSolns is TRUE, this code will set the internal data ioInsertInfo accordingly, so that when used in InsertIntoRouteWithInfo, the next solution will be used. For example, say there are 3 possible solutions and we call them solution1, solution2 and solution3. Call this code the first time and InsertIntoComponentWithInfo will use solution1. Call this code the second time (provided that CntrTgt remains the same) and solution2 will be used. The third time, solution3. The fourth time, solution1 and so one.

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim dbVar1(2) As CATSafeArrayVariant
     Dim objArg2 As AnyObject
     Dim objArg3 As AnyObject
     Dim bVar4 As boolean
      ...
     objThisIntf.GetBestFitInsertInfodbVar1,objArg2,objArg3,bVar4

```

### Sub **GetBestFitPlaceInfo**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2PlacementPt`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iPlaceCompatInfo`,  [CATIABase](../System/interface_AnyObject_17321.md)  `ioPlaceInfo`,  boolean  `iBYesCycleAllSolns`)

   Find the best-fit connector(s) to be used for placing a component and connecting it to another.

**Parameters:**

` iDb2PlacementPt`      X-Y coordinates of the target component graphical selection point.
` iPlaceCompatInfo`      Pointer to an internal class which contains structured information This is an **output** of IsTargetOKForPlace
` ioPlaceInfo`      Pointer to an internal class which contains structured information for how to place a component. Caller must initialize this pointer to NULL when calling this code the **first** time. This is used as an **input** to CATISchComponent::PlaceOnComponentWithInfo
` iBYesCycleAllSolns`      default is FALSE, and ioPlaceInfo is an output for the best fit solution. This solution will connect the compatible Target connector closest to the iDb2PlacementPt (call this CntrTgt) and the source connector that is closest to the origin (in position relative to ditto axis). If iBYesCycleAllSolns =TRUE, then the implementation will calculate all possible solutions and allow the caller to recall this code with the same ioPlaceInfo, **if and only if the compatible Target connector closest to the iDb2PlacementPt is the same as the previous one**. By doing this, this code will set the internal data ioPlaceInfo accordingly, so that when used in PlaceOnComponentWithInfo, the next solution will be used. For example, say there are 3 possible solutions and we call them solution1, solution2 and solution3. Call this code the first time and PlaceOnComponentWithInfo will use solution1. Call this code the second time (provided that CntrTgt remains the same) and solution2 will be used. The third time, solution3. The fourth time, solution1 and so one.

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim dbVar1(2) As CATSafeArrayVariant
     Dim objArg2 As AnyObject
     Dim objArg3 As AnyObject
     Dim bVar4 As boolean
      ...
     objThisIntf.GetBestFitPlaceInfodbVar1,objArg2,objArg3,bVar4

```

### Sub **IsTargetOKForInsert**( [CATIABase](../System/interface_AnyObject_17321.md)  `iCompInfo`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oInsertCompatInfo`,  boolean  `oBYes`)

   Query whether an object is compatible to be inserted into a route This method is used when placing a component.

**Parameters:**

` iCompInfo`      Pointer to an internal class which contains structured information of "this" component for placement. This is an **output** of CATISchComponent::QueryPlaceAbility
` oInsertCompatInfo`      Pointer to an internal class which contains structured information for "this" component **and** target route (the one in question) This is used as an **input** to GetBestFitInsertInfo
` oBYes`      If TRUE, the component is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim objArg1 As AnyObject
     Dim objArg2 As AnyObject
     Dim bVar3 As boolean
      ...
     objThisIntf.IsTargetOKForInsertobjArg1,objArg2,bVar3

```

### Sub **IsTargetOKForPlace**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRTarget`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iCompInfo`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oPlaceCompatInfo`,  boolean  `oBYes`)

   Query whether an object is compatible to be connected to another component This method is used when placing a component.

**Parameters:**

` iGRRTarget`      Pointer to the graphical image of the component in question (the target component to be connected to)
` iCompInfo`      Pointer to an internal class which contains structured information of "this" component for placement. This is an **output** of CATISchComponent::QueryPlaceAbility
` oPlaceCompatInfo`      Pointer to an internal class which contains structured information for "this" component **and** target component (the one in question) This is used as an **input** to GetBestFitPlaceInfo
` oBYes`      If TRUE, the component is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim objArg1 As SchGRRComp
     Dim objArg2 As AnyObject
     Dim objArg3 As AnyObject
     Dim bVar4 As boolean
      ...
     objThisIntf.IsTargetOKForPlaceobjArg1,objArg2,objArg3,bVar4

```

### Sub **IsTargetOKForRoute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iRouteCntrClassType`,  [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRRTarget`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `oLOKCntrs`,  boolean  `oBYes`)

   Query whether an object is compatible to be connected to a route. This method is used when routing a route.

**Parameters:**

` iRouteCntrClassType`      Class type of a schematic route connector.
` iGRRTarget`      Pointer to the graphical image of a target component or to the primitive of a target route
` oLOKCntrs`      A list of compatible and available connectors on the component or route (members are CATISchAppConnector interface pointers) This is used as an **input** to GetBestCntrForRoute
` oBYes`      If TRUE, the component is OK to be connected to a route.

**Example:**

```VBScript
     Dim objThisIntf As SchCompatible
     Dim strVar1 As String
     Dim objArg2 As SchGRR
     Dim objArg3 As SchListOfObjects
     Dim bVar4 As boolean
      ...
     objThisIntf.IsTargetOKForRoutestrVar1,objArg2,objArg3,bVar4

```