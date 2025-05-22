# SchDropOffView (Object)

**_Manage the drop off views in a schematic viewer._**

## Methods

### Sub **AddDropOffView**( [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)  `iView`,  [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)  `oView`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iDb2PosXY`,  double  `iDb1Scale`,  double  `iDb1Angl`)

Adds a drafting view to the schematics diagram.

**Parameters:**

` iView`      pointer to drafting view to add
` oView`      pointer to newly added drafting in this document
` iDb2PosXY`      pointer to XY coordinate for placement, if NULL, the position is the same as that of the input view.
` iDb1Scale`      scale of view added, if NULL, scale is assumed to be that of the input view.
` iDb1Angle`      The view orientation, if NULL, orientation is assumed to be that of the input view.
**Example:**

```VBScript
Dim objThisIntf As SchDropOffView
Dim objArg1 As DrawingView
Dim objArg2 As DrawingView
Dim dbVar3(2) As CATSafeArrayVariant

 ...
objThisIntf.AddDropOffViewobjArg1,objArg2,dbVar3,dbVar3,dbVar3

```

### Func **ListDropOffViews**( ) As [CATIASchListOfObjects](../CATSchPlatformInterfaces/interface_SchListOfObjects_53274.md)

Lists drafting views in this schematics diagram.

**Parameters:**

` oLDropOffViews`      A list of drafting views
**Example:**

```VBScript
Dim objThisIntf As SchDropOffView
Dim objArg1 As SchListOfObjects
 ...
Set objArg1 = objThisIntf.ListDropOffViews

```

### Sub **RemoveDropOffView**( [CATIADrawingView](../DraftingInterfaces/interface_DrawingView_26239.md)  `iViewToRemove`)

Removes a drafting view from the schematics diagram.

**Parameters:**

` iViewToRemove`      pointer to drafting view to remove
**Example:**

```VBScript
Dim objThisIntf As SchDropOffView
Dim objArg1 As DrawingView
 ...
objThisIntf.RemoveDropOffViewobjArg1

```