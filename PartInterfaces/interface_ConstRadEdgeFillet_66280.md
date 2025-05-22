# ConstRadEdgeFillet (Object)

**_Represents the edge fillet shape with a constant radius._**
The resulting shape is made up of edge fillets built with a constant radius.

## Properties

### Property **ObjectsToFillet**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

Returns the collection of reference elements to be filleted.

**Example:**     The following example returns in `elements` the reference elements to be filleted of the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
Set elements = firstCstEdgeFillet.ObjectsToFillet

```

### Property **Radius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the edge fillet constant radius.

**Example:**     The following example returns in `radius` the radius of the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
Set radius = firstCstEdgeFillet.Radius

```

Methods

### Sub **AddObjectToFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToFillet`)

Adds a new sub-element to be filleted. This sub-element is usually an edge.

**Parameters:**

` iObjectToFillet`      The sub-element to be filleted
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example adds a new geometrical element `element` to be filleted by the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
firstCstEdgeFillet.AddObjectToFillet(element)

```

### Sub **WithdrawObjectToFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToWithdraw`)

Withdraws a sub-element from those to be filleted. This sub-element is usually an edge.

**Parameters:**

` iObjectToWithdraw`      The sub-element to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example withdraws the geometrical element `element` from those to be filleted by the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
firstCstEdgeFillet.WithdrawObjectToFillet(element)

```