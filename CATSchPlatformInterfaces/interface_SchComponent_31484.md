# SchComponent (Object)

**_Manage a schematic component._**

## Methods

### Sub **CreateComponentInst**(| [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md) | `iGRR`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb6Axis`,| | [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md) | `oNewComponent`)

   Create a component instance. The reference component must exist **in current document**

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` iDb6Axis`      X-axis of the local axis of the new instance Y-axis of the local axis of the new instance X-Y coordinates of the orgin of the new instance. This axis defines the orientation and location of the new instance in space. Optional (could be NULL). If provided, the instance will be and orientated as defined. Else (1.0,0.0,0.0,1.0,0.0,0.0) is used
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim dbVar2(6) As CATSafeArrayVariant
     Dim objArg3 As SchComponent
      ...
     objThisIntf.CreateComponentInstobjArg1,dbVar2,objArg3

```

### Func **CreateLocalReference**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToPutCopyIn`) As [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)

   Make a local component reference in another document by copying an existing one in the current document.

**Parameters:**

` iDocumentToPutCopyIn`      Pointer to the document to make the copy in
` oSchComp`      Pointer to the copy.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As Document
     Dim objArg2 As SchComponent
      ...
     Set objArg2 = objThisIntf.CreateLocalReference(objArg1)

```

### Sub **FlipConnected**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   For component that is connected to another component or is inserted into a route. This method changes the current connections on this component and connects the component to the next compatible connector (connectors-pair in case of inserted component).

**Parameters:**

` iGRR`      Pointer to the component graphical representation object. if NULL the first insert image found will be used.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.FlipConnectedobjArg1

```

### Sub **FlipHorizontal**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   Mirror transform a component's image about the horizontal-axis centered at the local axis of the component. This component should not be connected to any other object.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.FlipHorizontalobjArg1

```

### Sub **FlipOnLine**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   Mirror the graphical object of this component. Ths mirror line is the inserted route segment. The current connections on the component is **not** changed. case of inserted component).

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.FlipOnLineobjArg1

```

### Sub **FlipVertical**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   Mirror transform a component's image about the vertical-axis centered at the local axis of the component. This component should not be connected to any other object.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.FlipVerticalobjArg1

```

### Sub **InsertIntoRouteWithInfo**( [CATIABase](../System/interface_AnyObject_17321.md)  `iInsertInfo`,  [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `oNewComponent`,  [CATIASchRoute](../CATSchPlatformInterfaces/interface_SchRoute_14100.md)  `oNewRoute`)

   Insert a component into a route. An internal structure is prerequisite to calling this method. This structure is obtained from calling CATISchCompatible::GetBestFitInsertInfo.

**Parameters:**

` iInsertInfo`      Pointer to an internal class which contains structured information of a component for placement. This is the **output** for calling CATISchCompatible::GetBestFitInsertInfo.
` oNewComponent`      Interface pointer to the new component instance placed.
` oNewRoute`      Interface pointer to the new route instance, created when the component is inserted into the route

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As AnyObject
     Dim objArg2 As SchComponent
     Dim objArg3 As SchRoute
      ...
     objThisIntf.InsertIntoRouteWithInfoobjArg1,objArg2,objArg3

```

### Sub **IsAReference**( boolean  `oBYes`)

   Query whether the component is a reference (as opposed to an instance).

**Parameters:**

` oBYes`      If TRUE, the component is a reference.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim bVar1 As boolean
      ...
     objThisIntf.IsAReferencebVar1

```

### Sub **IsInserted**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether the component is inserted into a route.

**Parameters:**

` iGRR`      Pointer to the component graphical representation.
` oBYes`      If TRUE, the component is currently inserted in a route.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.IsInsertedobjArg1,bVar2

```

### Sub **OKToFlipConnected**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether it is OK to connect the component via next compatible connectors.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, then it is OK to flip the component.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToFlipConnectedobjArg1,bVar2

```

### Sub **OKToFlipHorizontal**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether it is OK to flip the component about the horizontal axis.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, then it is OK to flip the component.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToFlipHorizontalobjArg1,bVar2

```

### Sub **OKToFlipOnLine**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`,  [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2LinePt`,  [CATIASchListOfDoubles](../CATSchPlatformInterfaces/interface_SchListOfDoubles_53392.md)  `oDb2LineVec`)

   Query whether it is OK to flip the component about the inserted route segment.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, then it is OK to flip the component.
` oDb2LinePt`      Absolute X-Y coordinates of a point on the segment.
` oDb2LineVec`      Absolute X-Y component vector along the segment.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
     Dim objArg3 As SchListOfDoubles
     Dim objArg4 As SchListOfDoubles
      ...
     objThisIntf.OKToFlipOnLineobjArg1,bVar2,objArg3,objArg4

```

### Sub **OKToFlipVertical**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether it is OK to flip the component about vertical axis.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, then it is OK to flip the component.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToFlipVerticalobjArg1,bVar2

```

### Sub **OKToPlaceInSpace**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether the component can be placed in free space.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, the component can be slided.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToPlaceInSpaceobjArg1,bVar2

```

### Sub **OKToScale**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether it is OK to scale the component.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first image found will be used.
` oBYes`      If TRUE, then it is OK to scale the component.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToScaleobjArg1,bVar2

```

### Sub **OKToSlide**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether the component can be slided.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, the component can be slided.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToSlideobjArg1,bVar2

```

### Sub **OKToUninsert**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  boolean  `oBYes`)

   Query whether it is OK to uninsert the component.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` oBYes`      If TRUE, then it is OK to uninsert the component.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim bVar2 As boolean
      ...
     objThisIntf.OKToUninsertobjArg1,bVar2

```

### Sub **PlaceInSpace**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb6Axis`,  [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `oNewComponent`)

   Place a component in space, unconnected to other objects. It will create local reference (from a catalog referenced document) if necessary.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` iDb6Axis[6]`      X-axis of the local axis of the new instance Y-axis of the local axis of the new instance X-Y coordinates of the orgin of the new instance. This axis defines the orientation and location of the new instance in space.
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim dbVar2(6) As CATSafeArrayVariant
     Dim objArg3 As SchComponent
      ...
     objThisIntf.PlaceInSpaceobjArg1,dbVar2,objArg3

```

### Func **PlaceOnComponentWithInfo**( [CATIABase](../System/interface_AnyObject_17321.md)  `iPlaceInfo`) As [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)

   Place a component connected to another component. An internal structure is prerequisite to calling this method. This structure is obtained from calling CATISchCompatible::GetBestFitPlaceInfo.

**Parameters:**

` iPlaceInfo`      Pointer to an internal class which contains structured information of a component for placement. This is the **output** for calling CATISchCompatible::GetBestFitPlaceInfo.
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As AnyObject
     Dim objArg2 As SchComponent
      ...
     Set objArg2 = objThisIntf.PlaceOnComponentWithInfo(objArg1)

```

### Sub **PlaceOnObject**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb6Axis`,  [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iObjectToConnect`,  [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `oNewComponent`)

   Place a component connected to another component or insert into a route.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` iDb6Axis[6]`      X-axis of the local axis of the new instance Y-axis of the local axis of the new instance X-Y coordinates of the orgin of the new instance. This axis defines the orientation and location of the new instance in space.
` iObjectToConnect`      Pointer to a component to connect the new instance to or a route object to insert new component into.
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim dbVar2(6) As CATSafeArrayVariant
     Dim objArg3 As SchAppConnectable
     Dim objArg4 As SchComponent
      ...
     objThisIntf.PlaceOnObjectobjArg1,dbVar2,objArg3,objArg4

```

### Func **QueryConnectAbility**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Find the Schematic component information for placement.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` oPlaceInfo`      Pointer to an internal class which contains structured information of a component for placement. This is the **input** for calling CATISchCompatible::IsComponentCompatible

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim objArg2 As AnyObject
      ...
     Set objArg2 = objThisIntf.QueryConnectAbility(objArg1)

```

### Sub **Slide**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2PtToSlideTo`)

   Slide a component (applicable to inserted component only). The component is moved along the route and remain inserted.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.
` iDb2PtToSlideTo[2]`      X-Y coordinates of the point to slide the component to.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
     Dim dbVar2(2) As CATSafeArrayVariant
      ...
     objThisIntf.SlideobjArg1,dbVar2

```

### Sub **Uninsert**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`)

   Remove all connections of a component with a route. (applicable to inserted component only).

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the first insert image found will be used.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent
     Dim objArg1 As SchGRRComp
      ...
     objThisIntf.UninsertobjArg1

```