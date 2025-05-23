# EdgeFillet (Object)

**_Represents the edges-based fillet shape._**
It is the base object for constant radius edge fillets and variable radius edge fillets.

**See also:**      [ConstRadEdgeFillet](../PartInterfaces/interface_ConstRadEdgeFillet_66280.md), [VarRadEdgeFillet](../PartInterfaces/interface_VarRadEdgeFillet_52056.md)

## Properties

### Property **EdgePropagation**(| ) As [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)

   Returns or sets the edge fillet propagation mode. This propagation mode is used when computing the edges to be filleted.

**Example:**     The following example returns in `mode` the edge fillet propagation mode of the `firstEdgeFillet` edge fillet, and then sets it to `CATMinimalFilletEdgePropagation`, so that a minimum numbers of edges will be filleted:

```VBScript
     Set mode = firstEdgeFillet.EdgePropagation
     Set firstEdgeFillet.EdgePropagation = CATMinimalFilletEdgePropagation

```

### Property **EdgesToKeep**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the collection of edges to keep by the edge fillet.

**Example:**     The following example returns in `edges` the edges to keep of the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
     Set edges = firstCstEdgeFillet.EdgesToKeep

```

Methods

### Sub **AddEdgeToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToKeep`)

   Adds a new edge to keep by the filleting operation. The edge to keep is not modified by the fillet.

**Parameters:**

` iEdgeToKeep`      The edge to keep by the filleting operation
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example adds the new `edge` edge to be kept from filleting by the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
     firstCstEdgeFillet.AddEdgeToKeep(edge)

```

### Sub **WithdrawEdgeToKeep**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToWithdraw`)

   Withdraws an edge from those kept by a filleting operation.

**Parameters:**

` iEdgeToWithdraw`      The edge to withdraw
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example withdraws the `edge` edge from those kept from filleting by the constant radius edge fillet `firstCstEdgeFillet`:

```VBScript
     firstCstEdgeFillet.WithdrawEdgeToKeep(edge)

```