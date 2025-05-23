# SchAppObjectFactory2 (Object)

**_Application factory to create application objects._**

## Methods

### Sub **AppCreateCompRef**(| [CATBSTR](../System/typedef_CATBSTR_8129.md) | `iAppCompClassType`,| | [CATIADocument](../InfInterfaces/interface_Document_14456.md) | `iDoc`,| | [CATIABase](../System/interface_AnyObject_17321.md) | `oAppComp`)

   Create an Application Component reference.

**Parameters:**

` iAppCompClassType`      Class type of the Application Component reference.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oAppComp`      The new Application Component object created (CATISchAppComponent interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As Document
     Dim objArg3 As AnyObject
      ...
     objThisIntf.AppCreateCompRefstrVar1,objArg2,objArg3

```

### Sub **AppCreateConnection**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppCntnClassType`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppConnection`)

   Create an Application Connection object.

**Parameters:**

` iAppCntnClassType`      Class type of the Application Connection object.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oAppConnection`      The new Application Connection object created (CATISchAppConnection interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As Document
     Dim objArg3 As AnyObject
      ...
     objThisIntf.AppCreateConnectionstrVar1,objArg2,objArg3

```

### Sub **AppCreateGroup**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppGroupClassType`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppGroup`)

   Create an Application Group object.

**Parameters:**

` iAppGroupClassType`      Class type of the Application Group object.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oAppGroup`      The new Application Group object created (CATISchAppGroup interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As Document
     Dim objArg3 As AnyObject
      ...
     objThisIntf.AppCreateGroupstrVar1,objArg2,objArg3

```

### Sub **AppCreateRoute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppRouteClassType`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogLineID`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppRoute`)

   Create an Application Route object.

**Parameters:**

` iAppRouteClassType`      Class type of the Application Route object.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` iLogLineID`      The logical line ID that will contain the new route. This is an optional input. If could be NULL.
` oAppRoute`      The new Application Route object created (CATISchAppRoute interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As Document
     Dim strVar3 As String
     Dim objArg4 As AnyObject
      ...
     objThisIntf.AppCreateRoutestrVar1,objArg2,strVar3,objArg4

```

### Sub **AppCreateRouteFromRef**( [CATIASchAppRoute](../CATSchPlatformInterfaces/interface_SchAppRoute_25864.md)  `iRouteReference`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLogLineID`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppRoute`)

   Create an Application Route object with a specific reference.

**Parameters:**

` iAppRouteRef`      Route reference to creaet the output route from
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` iLogLineID`      The logical line ID that will contain the new route. This is an optional input. If could be NULL.
` oAppRoute`      The new Application Route object created (CATISchAppRoute interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim objArg1 As SchAppRoute
     Dim objArg2 As Document
     Dim strVar3 As String
     Dim objArg4 As AnyObject
      ...
     objThisIntf.AppCreateRouteFromRefobjArg1,objArg2,strVar3,objArg4

```

### Sub **AppCreateRouteWithInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppRouteClassType`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAppInfo`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppRoute`)

   Create an Application Route object with application information.

**Parameters:**

` iAppRouteClassType`      Class type of the Application Route object.
` iAppInfo`      Application data pointer
` oAppRoute`      The new Application Route object created (CATISchAppRoute interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As AnyObject
     Dim objArg3 As AnyObject
      ...
     objThisIntf.AppCreateRouteWithInfostrVar1,objArg2,objArg3

```

### Sub **AppCreateZone**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iAppZoneClassType`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oAppZone`)

   Create an Application Zone object.

**Parameters:**

` iAppZoneClassType`      Class type of the Application Zone object.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oAppZone`      The new Application Zone object created (CATISchAppZone interface pointer).

**Example:**

```VBScript
     Dim objThisIntf As SchAppObjectFactory2
     Dim strVar1 As String
     Dim objArg2 As Document
     Dim objArg3 As AnyObject
      ...
     objThisIntf.AppCreateZonestrVar1,objArg2,objArg3

```