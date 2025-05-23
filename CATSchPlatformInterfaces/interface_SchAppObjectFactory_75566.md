# SchAppObjectFactory (Object)

**_Application factory to create application objects._**

## Methods

### Sub **AppCreateCompRef**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iAppCompClassType`,| | [CATIABase](../System/interface_AnyObject_17321.md) | `oAppComp`)

   Create an Application Component reference.

**Parameters:**

` iAppCompClassType`      Class type of the Application Component reference.
` oAppComp`      The new Application Component object created (CATISchAppComponent interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim strVar1 As String
     Dim objArg2 As AnyObject
      ...
     objThisIntf.AppCreateCompRefstrVar1,objArg2

```

### Sub **AppCreateConnection**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppCntnClassType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppConnection`)

   Create an Application Connection object.

**Parameters:**

` iAppCntnClassType`      Class type of the Application Connection object.
` oAppConnection`      The new Application Connection object created (CATISchAppConnection interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim strVar1 As String
     Dim objArg2 As AnyObject
      ...
     objThisIntf.AppCreateConnectionstrVar1,objArg2

```

### Sub **AppCreateGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppGroupClassType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppGroup`)

   Create an Application Group object.

**Parameters:**

` iAppGroupClassType`      Class type of the Application Group object.
` oAppGroup`      The new Application Group object created (CATISchAppGroup interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim strVar1 As String
     Dim objArg2 As AnyObject
      ...
     objThisIntf.AppCreateGroupstrVar1,objArg2

```

### Sub **AppCreateRoute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppRouteClassType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppRoute`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogLineID`)

   Create an Application Route object.

**Parameters:**

` iAppRouteClassType`      Class type of the Application Route object.
` oAppRoute`      The new Application Route object created (CATISchAppRoute interface pointer).
` iLogLineID`      The logical line ID that will contain the new route. This is an optional input.

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim strVar1 As String
     Dim objArg2 As AnyObject
     Dim strVar3 As String
      ...
     objThisIntf.AppCreateRoutestrVar1,objArg2,strVar3

```

### Sub **AppCreateRouteFromRef**( [CATIASchAppRoute](../CATSchPlatformInterfaces/interface_SchAppRoute_25864.md)  `iRouteReference`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppRoute`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogLineID`)

   Create an Application Route object with a specific reference.

**Parameters:**

` iAppRouteRef`      Route reference to creaet the output route from
` oAppRoute`      The new Application Route object created (CATISchAppRoute interface pointer).
` iLogLineID`      The logical line ID that will contain the new route. This is an optional input.

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim objArg1 As SchAppRoute
     Dim objArg2 As AnyObject
     Dim strVar3 As String
      ...
     objThisIntf.AppCreateRouteFromRefobjArg1,objArg2,strVar3

```

### Sub **AppCreateZone**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppZoneClassType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppZone`)

   Create an Application Zone object.

**Parameters:**

` iAppZoneClassType`      Class type of the Application Zone object.
` oAppZone`      The new Application Zone object created (CATISchAppZone interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory
     Dim strVar1 As String
     Dim objArg2 As AnyObject
      ...
     objThisIntf.AppCreateZonestrVar1,objArg2

```