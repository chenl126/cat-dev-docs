# VarRadEdgeFillet (Object)

**_Represents the edge fillet shape with a variable radius._**
The resulting shape is made up of edges fillets controlled by couples of radius/vertex.

## Properties

### Property **BitangencyType**(| ) As [CatFilletBitangencyType](../PartInterfaces/enum_CatFilletBitangencyType_111278.md)

   Returns or set the fillet bitangency type.

**Parameters:**

` iType`      The type used to perform the fillet : catSphereBitangencyType or catCircleBitangencyType

### Property **EdgesToFillet**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the collection of edges to be filleted.

**Example:**     The following example returns in `edges` the edges to fillet of variable radius edge fillet`firstVarEdgeFillet`:

```VBScript
     Set edges = firstVarEdgeFillet.EdgesToFillet

```

### Property **FilletSpine**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or set the spine for circle bitangency fillet.

**Parameters:**

` iSpin`      The spine to be used for a circle bitangency fillet

### Property **FilletVariation**( ) As [CatFilletVariation](../PartInterfaces/enum_CatFilletVariation_68872.md)

   Returns or sets the edge fillet radius variation mode.

**Example:**     The following example returns in `mode` the radius variation mode of the variable radius edge fillet`firstVarEdgeFillet`, and then sets it to `CATLinearFilletVariation` so that the radius variation is linear between two control vertices:

```VBScript
     mode = firstVarEdgeFillet.FilletVariation
     firstVarEdgeFillet.FilletVariation = CATLinearFilletVariation

```

### Property **ImposedVertices**( ) As [CATIAReferences](../InfInterfaces/interface_References_21842.md) (Read Only)

   Returns the collection of vertices where a radius has been imposed.

**Example:**     The following example returns in `vertices` the collection of imposed vertices of the variable radius edge fillet`firstVarEdgeFillet`:

```VBScript
     Set vertices = firstVarEdgeFillet.ImposedVertices

```

Methods

### Sub **AddEdgeToFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge`,  double  `iRadius`)

   Adds a new edge to the variable radius edge fillet.

**Parameters:**

` iEdge`      The edge to be filleted
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iRadius`      The radius to impose along the edge. This radius is imposed at both end points of the edge.  **Example:**     The following example adds the new edge `edge` to be filleted to the variable radius edge fillet `firstVarEdgeFillet`:

```VBScript
     call firstVarEdgeFillet.AddEdgeToFillet(edge, 5.)

```

### Sub **AddImposedVertex**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVertex`,  double  `iRadius`)

   Adds a new control couple. A control couple is made up of a vertex and a radius.

**Parameters:**

` iVertex`      The vertex where to impose the radius
` iRadius`      The radius to impose at the given vertex  **Example:**     The following example adds a new control couple (vertex, radius) to the variable radius edge fillet `firstVarEdgeFillet` set with the vertex `vertex` and a radius of 50.

```VBScript
     call firstVarEdgeFillet.AddImposedVertex(vertex, 50.)

```

### Func **ImposedVertexRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iImposedVertex`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

   Returns the fillet radius on an imposed vertex.

**Parameters:**

` iImposedVertex`      The vertex where to retrieve the fillet radius

**Returns:**      The fillet radius  **Example:**     The following example returns in `radius` the fillet radius of the variable radius edge fillet `firstVarEdgeFillet` at the vertex `vertex`:

```VBScript
     Set radius = firstVarEdgeFillet.ImposedVertexRadius(vertex)

```

### Sub **WithdrawEdgeToFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge`)

   Withdraws an edge from the variable radius edge fillet.

**Parameters:**

` iEdge`      The edge to be withdrawn
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Example:**     The following example withdraws the edge `edge` from those to be filleted of the variable radius edge fillet `firstVarEdgeFillet`:

```VBScript
     call firstVarEdgeFillet.WithdrawEdgeToFillet(edge)

```

### Sub **WithdrawImposedVertex**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVertex`)

   Withdraws a control couple.

**Parameters:**

` iVertex`      The vertex where the radius is imposed  **Example:**     The following example withdraws the imposed radius on the vertex `vertex` for the variable radius edge fillet `firstVarEdgeFillet`:

```VBScript
     call firstVarEdgeFillet.WithdrawImposedVertex(vertex)

```