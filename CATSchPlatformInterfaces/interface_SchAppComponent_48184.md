# SchAppComponent (Object)

**_Represents an application component object._**

## Methods

### Func **AppCreateComponentInst**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Create a component instance.

**Parameters:**

` oNewAppCompInst`      Interface pointer (CATISchAppComponent) to the new **application** component instance placed.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As AnyObject
 ...
Set objArg1 = objThisIntf.AppCreateComponentInst

```

### Func **AppCreateLocalReference**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocToCopyTo`) As [CATIABase](../System/interface_AnyObject_17321.md)

Create Local Reference object. Given a reference object (the "this"), This method make a copy of the reference into another document.

**Parameters:**

` iDocToCopyTo`      Pointer to a document to copy the reference to,
` oNewAppCompRef`      Interface pointer (CATISchAppComponent) to the new **application** component Reference copied.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As Document
Dim objArg2 As AnyObject
 ...
Set objArg2 = objThisIntf.AppCreateLocalReference(objArg1)

```

### Sub **AppGetDefaultGRRName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oGRRDefaultName`)

Get the default graphical representation names of an application component.

**Parameters:**

` oGRRDefaultName`      The default name to be used for the graphical representation of a component
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim strVar1 As String
 ...
objThisIntf.AppGetDefaultGRRNamestrVar1

```

### Func **AppListGRRNames**( ) As [CATIASchListOfBSTRs](../CATSchPlatformInterfaces/interface_SchListOfBSTRs_37788.md)

Find all the valid graphical representation names of an application component.

**Parameters:**

` oLGRRNames`      A list of all the valid graphical representation names with this connector for connections.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As SchListOfBSTRs
 ...
Set objArg1 = objThisIntf.AppListGRRNames

```

### Sub **AppOKToFlipConnected**( boolean  `oBYes`)

Query whether it is OK to reconnect a component to a different compatible configuration.

**Parameters:**

` oBYes`      If TRUE, then it is OK to flip the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToFlipConnectedbVar1

```

### Sub **AppOKToFlipHorizontal**( boolean  `oBYes`)

Query whether it is OK to flip the application component about Y.

**Parameters:**

` oBYes`      If TRUE, then it is OK to flip the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToFlipHorizontalbVar1

```

### Sub **AppOKToFlipOnLine**( boolean  `oBYes`)

Query whether it is OK to flip a component about its inserted line.

**Parameters:**

` oBYes`      If TRUE, then it is OK to flip the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToFlipOnLinebVar1

```

### Sub **AppOKToFlipVertical**( boolean  `oBYes`)

Query whether it is OK to flip the application component about X.

**Parameters:**

` oBYes`      If TRUE, then it is OK to flip the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToFlipVerticalbVar1

```

### Sub **AppOKToPlaceInSpace**( boolean  `oBYes`)

Query whether the application component can be placed in free space.

**Parameters:**

` oBYes`      If TRUE, the component can be slided.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToPlaceInSpacebVar1

```

### Sub **AppOKToScale**( boolean  `oBYes`)

Query whether it is OK to scale the application component.

**Parameters:**

` oBYes`      If TRUE, then it is OK to scale the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToScalebVar1

```

### Sub **AppOKToSlide**( boolean  `oBYes`)

Query whether the application component can be slided.

**Parameters:**

` oBYes`      If TRUE, the component can be slided.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToSlidebVar1

```

### Sub **AppOKToUninsert**( boolean  `oBYes`)

Query whether it is OK to uninsert the application component.

**Parameters:**

` oBYes`      If TRUE, then it is OK to uninsert the component.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim bVar1 As boolean
 ...
objThisIntf.AppOKToUninsertbVar1

```

### Sub **AppPostFlipConnectedProcess**( )

Post process after reconnecting a component to a different compatible configuration.

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
 ...
objThisIntf.AppPostFlipConnectedProcess

```

### Sub **AppPostFlipHorizontalProcess**( )

Post process after flipping a component in "x".

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
 ...
objThisIntf.AppPostFlipHorizontalProcess

```

### Sub **AppPostFlipOnLineProcess**( )

Post process after flipping an inserted component about the inserted line segment of the route.

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
 ...
objThisIntf.AppPostFlipOnLineProcess

```

### Sub **AppPostFlipVerticalProcess**( )

Post process after flipping a component in "y".

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
 ...
objThisIntf.AppPostFlipVerticalProcess

```

### Sub **AppPostPlaceProcess**( [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `iNewCompInst`,  [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iCntblConnectedTo`)

Post process after placing an application component instance.

**Parameters:**

` iNewCompInst`      The newly placed component instance (CATISchComponent interface pointer).
` iCntbleConnectedTo`      The connectable that the placed component is connected to or placed onto
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As SchComponent
Dim objArg2 As SchAppConnectable
 ...
objThisIntf.AppPostPlaceProcessobjArg1,objArg2

```

### Sub **AppPostSlideProcess**( )

Post process after sliding a component.

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
 ...
objThisIntf.AppPostSlideProcess

```

### Sub **AppPostSwitchGraphicProcess**( [CATIASchGRR](../CATSchPlatformInterfaces/interface_SchGRR_6684.md)  `iGRR`)

Post process after switching a component's graphic representation.

**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As SchGRR
 ...
objThisIntf.AppPostSwitchGraphicProcessobjArg1

```

### Sub **AppPostUninsertProcess**( [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iOldAppRoute1`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iOldAppRoute2`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `iNewAppRoute`)

Post process after uninserting a component, disconnecting it from a route.

**Parameters:**

` iOldAppRoute1`      One of the route that was connected to one connector of the inserted component before the operation.
` iOldAppRoute2`      The other route that was connected to the other connector of the inserted component before the operation. This would be NULL if the component was connected at extremity.
` iNewAppRoute`      The new route created after the operation. This would be NULL if the component was connected at extremity.
**Example:**

```VBScript
Dim objThisIntf As SchAppComponent
Dim objArg1 As SchRoute
Dim objArg2 As SchRoute
Dim objArg3 As SchRoute
 ...
objThisIntf.AppPostUninsertProcessobjArg1,objArg2,objArg3

```