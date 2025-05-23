# SchComponent2 (Object)

**_Manage a schematic component._**

## Methods

### Sub **PlaceInSpace**(| [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md) | `iGRR`,| | [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md) | `iDb6Axis`,| | [CATIADocument](../InfInterfaces/interface_Document_14456.md) | `iDoc`,| | [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md) | `oNewComponent`)

   Place a component in space, unconnected to other objects. It will create local reference (from a catalog referenced document) if necessary.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` iDb6Axis[6]`      X-axis of the local axis of the new instance Y-axis of the local axis of the new instance X-Y coordinates of the orgin of the new instance. This axis defines the orientation and location of the new instance in space.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent2
     Dim objArg1 As SchGRRComp
     Dim dbVar2(6) As CATSafeArrayVariant
     Dim objArg3 As Document
     Dim objArg4 As SchComponent
      ...
     objThisIntf.PlaceInSpaceobjArg1,dbVar2,objArg3,objArg4

```

### Sub **PlaceOnObject**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRR`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb6Axis`,  [CATIASchAppConnectable](../CATSchPlatformInterfaces/interface_SchAppConnectable_60005.md)  `iObjectToConnect`,  [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDoc`,  [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `oNewComponent`)

   Place a component connected to another component or insert into a route.

**Parameters:**

` iGRR`      Pointer to the component graphical representation. if NULL the "Primary" graphical representation will be used.
` iDb6Axis[6]`      X-axis of the local axis of the new instance Y-axis of the local axis of the new instance X-Y coordinates of the orgin of the new instance. This axis defines the orientation and location of the new instance in space.
` iObjectToConnect`      Pointer to a component to connect the new instance to or a route object to insert new component into.
` iDoc`      Pointer to a document to create the object in. If NULL, the document associated with the current Editor will be used.
` oNewComponent`      Interface pointer to the new component instance placed.

**Example:**

```VBScript
     Dim objThisIntf As SchComponent2
     Dim objArg1 As SchGRRComp
     Dim dbVar2(6) As CATSafeArrayVariant
     Dim objArg3 As SchAppConnectable
     Dim objArg4 As Document
     Dim objArg5 As SchComponent
      ...
     objThisIntf.PlaceOnObjectobjArg1,dbVar2,objArg3,objArg4,objArg5

```