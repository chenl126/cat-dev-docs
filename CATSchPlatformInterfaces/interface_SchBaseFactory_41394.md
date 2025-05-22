# SchBaseFactory (Object)

**_Factory to create basic schematic objects._**

## Methods

### Func **CreateNetwork**( [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLCntbls`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLGRRs`) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

Create schematic networks for query. These are volatile objects and will not be saved in the model.

**Parameters:**

` iLCntbl`      A list of related objects that belong to the network (CATISchAppConnectable pointers). These objects do not need to be connected. This method will do the analysis and returns the network(s) containing these objects.
` iLCntbl`      A list of graphical images interface (CATISchGRR) pointers. Each member corresponds to the members in iLCntbl.
` oNetwork`      [out, IUnknown#Release] Pointer to the network analysis interface pointers.
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As SchListOfObjects
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchListOfObjects
 ...
Set objArg3 = objThisIntf.CreateNetwork(objArg1,objArg2)

```

### Sub **CreateRouteAndConnectToObjects**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppRoute`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrCompFrom`,  [CATIASchAppConnector](../CATSchPlatformInterfaces/interface_SchAppConnector_47916.md)  `iCntrCompTo`,  [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRCompFrom`,  [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRCompTo`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDb2PtPath`,  [CatSchIDLRouteMode](../CATSchPlatformInterfaces/enum_CatSchIDLRouteMode_63812.md)  `iERouteMode`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `oSchRoute`)

Create a route and connect its extremity connectors to input objects.

**Parameters:**

` iAppRoute`      Application route (at least a feature)
` iCntrCompFrom`      Pointer to component connector to connect starting end of the route to If NULL, no connection is made at this end.
` iCntrCompTo`      Pointer to component connector to connect end of the route to If NULL, no connection is made at this end.
` iGRRCompFrom`      Pointer to first component graphical image, if NULL, the PRIMARY image associated with component will be used
` iGRRCompTo`      Pointer to second component graphical image, if NULL, the PRIMARY image associated with component will be used
` iLDb2PtPath`      A list of X-Y coordinates of points to be used for the route image. 2 doubles per point. Not used if iERouteMode=SchRouteMode_AroundObject input a NULL for this case
` iERouteMode`      Route mode to use. Only used when iLDb2PtPath is NULL.
` oSchRoute`      Pointer to the new route
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim objArg2 As SchAppConnector
Dim objArg3 As SchAppConnector
Dim objArg4 As SchGRRComp
Dim objArg5 As SchGRRComp
Dim dbVar6(x) As CATSafeArrayVariant

Dim objArg9 As SchRoute
 ...
objThisIntf.CreateRouteAndConnectToObjectsobjArg1,objArg2,objArg3,objArg4,objArg5,dbVar6,CatSchIDLRouteMode_Enum,objArg9

```

### Func **CreateSchCompGroup**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppGroup`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLGRR`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLMember`) As [CATIASchCompGroupExt](../CATSchPlatformInterfaces/interface_SchCompGroupExt_47737.md)

Create a Schematic Component Group object.

**Parameters:**

` iAppGroup`      Application group object (at least a feature) Optional, it could be NULL. If NULL, one will be created by the platform
` iLGRR`      A list of graphical representation. Optional, it could be NULL.
` iLMembers`      A list of initial members. Optional, it could be NULL.
` oSchGroup`      Pointer to the new group.
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchListOfObjects
Dim objArg4 As SchCompGroupExt
 ...
Set objArg4 = objThisIntf.CreateSchCompGroup(objArg1,objArg2,objArg3)

```

### Func **CreateSchComponent**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppComponentRef`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLGRR`) As [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)

Create a Schematic Component reference.

**Parameters:**

` iAppComponentRef`      Application component reference (at least a feature)
` iLGRR`      A list of graphical representations.
` oSchComp`      Pointer to the new component.
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchComponent
 ...
Set objArg3 = objThisIntf.CreateSchComponent(objArg1,objArg2)

```

### Sub **CreateSchRouteByPoints**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppRoute`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iLDbPt`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `oSchRoute`)

Create a Schematic Route object with a list of points.

**Parameters:**

` iAppRoute`      Application route (at least a feature)
` iLDbPt`      A list of X-Y coordinates of points. 2 doubles per point.
` oSchRoute`      Pointer to the new route
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim dbVar2(x) As CATSafeArrayVariant
Dim objArg4 As SchRoute
 ...
objThisIntf.CreateSchRouteByPointsobjArg1,dbVar2,objArg4

```

### Func **CreateSchRouteByPrim**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppRoute`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLGRR`) As [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)

Create a Schematic Route object with primitives.

**Parameters:**

` iAppRoute`      Application route (at least a feature)
` iLGRR`      A list of graphical primitives. pointer).
` oSchRoute`      Pointer to the new route
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchRoute
 ...
Set objArg3 = objThisIntf.CreateSchRouteByPrim(objArg1,objArg2)

```

### Func **CreateSchZone**( [CATIABase](../System/interface_AnyObject_17321.md)  `iAppZone`,  [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)  `iLGRR`) As [CATIASchZone](../CATSchPlatformInterfaces/interface_SchZone_10636.md)

Create a Schematic Zone object.

**Parameters:**

` iAppZone`      Application zone object (at least a feature)
` iLGRR`      A list of graphical representation.
` oSchZone`      Pointer to the new zone.
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
Dim objArg2 As SchListOfObjects
Dim objArg3 As SchZone
 ...
Set objArg3 = objThisIntf.CreateSchZone(objArg1,objArg2)

```

### Sub **DeleteObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

Delete a schematic object.

**Parameters:**

` iObject`      interface pointer to the object to be deleted
**Example:**

```VBScript
Dim objThisIntf As SchBaseFactory
Dim objArg1 As AnyObject
 ...
objThisIntf.DeleteObjectobjArg1

```