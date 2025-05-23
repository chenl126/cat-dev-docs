# Draft (Object)

**_Represents the draft shape._**
A draft shape is made up of draft domains (at least one) and of a parting element.

## Properties

### Property **DraftDomains**(| ) As [CATIADraftDomains](../PartInterfaces/interface_DraftDomains_30834.md) (Read Only)

   Returns the collection of draft domains.

**Example:**     The following example returns in `list` the collection of draft domains of the `firstDraft` draft:

```VBScript
     Set list = firstDraft.DraftDomains

```

### Property **Mode**( ) As [CatDraftMode](../PartInterfaces/enum_CatDraftMode_29572.md)

   Returns or sets the draft mode.

**Example:**     The following example returns in `mode` the draft mode of the `firstDraft` draft, and then sets it to `CatReflectKeepFaceDraftMode`:

```VBScript
     Set mode = firstDraft.Mode
     Set firstDraft.Mode = CatReflectKeepFaceDraftMode

```

### Property **PartingElement**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the draft parting element.
To set the property, you can use the following [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).

**Example:**     The following example returns in `element` the parting element of the `firstDraft` draft, and then sets it to the `element2` geometrical element:

```VBScript
     Set element = firstDraft.PartingElement
     Set firstDraft.PartingElement = element2

```