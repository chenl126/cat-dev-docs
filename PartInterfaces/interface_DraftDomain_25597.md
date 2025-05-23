# DraftDomain (Object)

**_Represents the draft domain._**
A draft domain is a basic object used by a draft shape. It contains objects such as an angle, a pulling direction, and a collection of faces to be drafted.

## Properties

### Property **DraftAngle**(| ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the draft angle.

**Example:**     The following example returns in `angle` the draft angle of the draft domain `firstDraftDomain`:

```VBScript
     Set angle = firstDraftDomain.DraftAngle

```

### Property **FacesToDraft**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the faces to be drafted. They are returned as a collection of reference geometric elements.

**Example:**     The following example returns the collection of faces to be drafted of the draft domain `firstDraftDomain` in `list`:

```VBScript
     Set list = firstDraftDomain.FacesToDraft

```

### Property **MultiselectionMode**( ) As [CatDraftMultiselectionMode](../PartInterfaces/enum_CatDraftMultiselectionMode_141932.md)

   Changes the multiselection mode.

**Parameters:**

` iMultiselectionMode.`      The elements to be drafted can be selected explicitly (CATNoneDraftMultiselectionMode) or can implicitly selected as neighbors of the neutral face (CATMultiselectionByNeutralMode)

**Example:**     The following example returns in `MultiselMode` the multiselection mode of the draft domain `firstDraftDomain`, and then sets it to `CATMultiselectionByNeutralMode`

```VBScript
     Set MultiselMode = firstDraftDomain.MultiselectionMode
     firstDraftDomain.MultiselectionMode = CATMultiselectionByNeutralMode

```

### Property **NeutralElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the draft neutral element.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

**Example:**     The following example returns in `neutral` the neutral element of the draft domain `firstDraftDomain`, and then sets it to `newNeutral`:

```VBScript
     Set neutral = firstDraftDomain.NeutralElement
     firstDraftDomain.NeutralElement = newNeutral

```

### Property **NeutralPropagationMode**( ) As [CatDraftNeutralPropagationMode](../PartInterfaces/enum_CatDraftNeutralPropagationMode_187684.md)

   Returns or sets the neutral element propagation mode. This mode is used when computing the needed neutral elements.

**Example:**     The following example returns in `propMode` the neutral propagation mode of the draft domain `firstDraftDomain`, and then sets it to `CATSmoothDraftNeutralPropagationMode` so that the neutral propagation will now be smooth:

```VBScript
     Set propMode = firstDraftDomain.NeutralPropagationMode
     firstDraftDomain.NeutralPropagationMode = CATSmoothDraftNeutralPropagationMode

```

### Property **PullingDirectionElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the draft pulling direction element.
To set the property, you can use one of the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) or [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md).

**Example:**     The following example returns in `pullingdirection` the pulling direction element of the draft domain `firstDraftDomain`, and then sets it to `newPullingDirection`:

```VBScript
     Set pullingdirection = firstDraftDomain.NeutralElement
     firstDraftDomain.PullingDirectionElement = newPullingDirection

```

Methods

### Sub **AddFaceToDraft**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

   Adds a face to those to be drafted.

**Parameters:**

` iFace`      The face to add to those to be drafted
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: ScFace.  **Example:**     The following example adds the face `NewFaceToDraft` to the draft domain `CurrentDraftDomain`:

```VBScript
     CurrentDraftDomain.AddFaceToDraft(NewFaceToDraft)

```

### Sub **GetPullingDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioPullingDirection`)

   Returns the draft pulling direction. The pulling direction is returned as an array containing the pulling direction vector components. Assume this array is `PullDir`. It contains:

`PullDir[0],PullDir[1],PullDir[2]`     The X, Y, and Z pulling direction vector components

**Example:**     The following example returns in `PullDir` the pulling direction vector components of the draft domain `firstDraftDomain`:

```VBScript
     Set PullDir = firstDraftDomain.PullingDirection
     Set x = PullDir[0]
     Set y = PullDir[1]
     Set z = PullDir[2]

```

### Sub **RemoveFaceToDraft**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

   Removes a face from those to be drafted.

**Parameters:**

` iFace`      The face to be removed from those to be drafted
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md).  **Example:**     The following example removes the face `FaceToRemove` from the draft domain `CurrentDraftDomain`:

```VBScript
     CurrentDraftDomain.RemoveFaceToDraft(FaceToRemove)

```

### Sub **SetPullingDirection**( double  `iX`,  double  `iY`,  double  `iZ`)

   Sets the draft pulling direction.

**Parameters:**

` iX,iY,iZ`      The X, Y, and Z pulling direction vector components  **Example:**     The following example sets the draft pulling direction of the draft domain `firstDraftDomain` to the direction with the vector components 10, -5, 10:

```VBScript
     firstDraftDomain.PullingDirection 10, -5, 10

```

### Sub **SetVolumeSupport**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`)

   Value the support of draft.

**Parameters:**

` iVolumeSupport`