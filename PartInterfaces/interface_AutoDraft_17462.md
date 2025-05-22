# AutoDraft (Object)

**_Represents the AutoDraft shape._**

## Properties

### Property **FunctionalFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`) (Write Only)

### Property **FunctionalFaces**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns or sets the functional faces.

**Example:**     The following example returns in `FunctionalFaces` the list functional faces of the AutoDraft `AutoDraft`, and then sets `NewFunctionalFace` as a functional face:

```VBScript
Set FunctionalFaces = AutoDraft.FunctionalFace
AutoDraft.FunctionalFace = NewFunctionalFace

```

### Property **MainDraftAngle**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the main draft angle.

**Example:**     The following example returns in `MainDraftAngle` the main draft angle of the AutoDraft `AutoDraft`, and then sets it to `NewMainDraftAngle.`:

```VBScript
Set MainDraftAngle = AutoDraft.MainDraftAngle
AutoDraft.MainDraftAngle = NewMainDraftAngle

```

### Property **Mode**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the draft mode.

**Example:**     The following example returns in `Mode` the mode of the draft AutoDraft `AutoDraft`, and then sets it to `NewMode`:

```VBScript
Set Mode = AutoDraft.Mode
AutoDraft.Mode = NewMode

```

### Property **PartingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the parting element.

**Example:**     The following example returns in `PartingElement` the parting element of the AutoDraft `AutoDraft`, and then sets it to `NewpartingElement`:

```VBScript
Set PartingElement = AutoDraft.PartingElement
AutoDraft.PartingElement = NewPartingElement

```

### Property **PullingDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the pulling direction.

**Example:**     The following example returns in `PullingDirection` the pulling direction of the AutoDraft `AutoDraft`, and then sets it to `NewPullingDirection.`:

```VBScript
Set PullingDirection = AutoDraft.PullingDirection
AutoDraft.PullingDirection = NewPullingDirection

```