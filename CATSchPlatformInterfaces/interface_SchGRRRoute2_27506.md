# SchGRRRoute2 (Object)

**_Manage the graphical representation of a schematic route._**

## Methods

### Sub **GetReshapeMode**( [CatSchIDLGRRRouteReshapeMode](../CATSchPlatformInterfaces/enum_CatSchIDLGRRRouteReshapeMode_153478.md)  `oReshapeMode`)

Get the reshape mode.

**Parameters:**

` oReshapeMode`      Whether or not the route shape is fixed for the purpose of reshaping the route. = SchFixedShapeOff : no restriction on how to reshape the route. = SchFixedShapeOn : reshape only the route's extremity (the segment directly connected to the object that's being moved).
**Example:**

```VBScript
Dim objThisIntf As SchGRRRoute2

 ...
objThisIntf.GetReshapeModeCatSchIDLGRRRouteReshapeMode_Enum

```

### Sub **SetReshapeMode**( [CatSchIDLGRRRouteReshapeMode](../CATSchPlatformInterfaces/enum_CatSchIDLGRRRouteReshapeMode_153478.md)  `iReshapeMode`)

Set the reshape mode.

**Parameters:**

` iReshapeMode`      Whether or not the route shape is fixed for the purpose of reshaping the route. = SchFixedShapeOff : no restriction on how to reshape the route. = SchFixedShapeOn : reshape only the route's extremity (the segment directly connected to the object that's being moved).
**Example:**

```VBScript
Dim objThisIntf As SchGRRRoute2

 ...
objThisIntf.SetReshapeModeCatSchIDLGRRRouteReshapeMode_Enum

```