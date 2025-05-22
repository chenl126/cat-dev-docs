# SchReplace (Object)

**_Manage existing schematic component instances._**

## Methods

### Func **Replace**( [CATIASchGRRComp](../CATSchPlatformInterfaces/interface_SchGRRComp_19674.md)  `iGRRToBePlaced`,  [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)  `iSchCompToBeRemoved`) As [CATIASchComponent](../CATSchPlatformInterfaces/interface_SchComponent_31484.md)

Replace an existing component with this component.

**Parameters:**

` iGRRToBePlaced`      Pointer to the component graphical representation of this component to be placed. if NULL the first representation found will be used.
` iSchCompToBeRemoved`      Pointer to the existing component to be replaced by this component.
` oNewComponent`      Interface pointer to the new component instance placed.
**Example:**

```VBScript
Dim objThisIntf As SchReplace
Dim objArg1 As SchGRRComp
Dim objArg2 As SchComponent
Dim objArg3 As SchComponent
 ...
Set objArg3 = objThisIntf.Replace(objArg1,objArg2)

```