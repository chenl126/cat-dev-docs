# Body (Object)

**_The object that manages a sequence of shapes, and a set of independent sketches waiting for their use in shapes; a set of hybrid bodies, a set of ordered geometrical sets and a set of hybrid shapes._**

It belongs to the [Bodies](../MecModInterfaces/interface_Bodies_7994.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or [HybridBody](../MecModInterfaces/interface_HybridBody_21378.md) object.

## Properties

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

Returns the body's HybridBodies collection.

**Example:**     The following example returns in `hybridBodyColl` the collection of hybrid bodies of the main body of `partDoc` part document:

```VBScript
Dim body As Body
Set body = partDoc.Part.Bodies.MainBody
Set hybridBodyColl = body.HybridBodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

Returns the list of hybrid shapes included in the body.

**Returns:**      oHybridShapes The list of hybrid shapes in the body (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `HybridShapes1` the list of
hybrid shapes in the body `Body1`:

```VBScript
Dim HybridShapes1 As HybridShapes
Set HybridShapes1 = Body1.**HybridShapes**

```

### Property **InBooleanOperation**( ) As boolean (Read Only)

Returns True if the body is involved in a boolean operation, else returns False.

**Example:**     The following example returns in `operated` True if the body `body1`belongs to a boolean operation.

```VBScript
operated = body1.InBooleanOperation

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

Returns the body's OrderedGeometricalSets collection.

ometricalSetColl = Body1.OrderedGeometricalSets
```

**Example:**     The following example returns in `OrderedGeometricalSetColl` the collection of ordered geometrical set of the body `Body1` :

```VBScript
Set OrderedGe

### Property **Shapes**( ) As [CATIAShapes](../MecModInterfaces/interface_Shapes_8122.md)  (Read Only)

Returns the body's Shapes collection.
These shapes make up the sequence of shapes that will produce an
intermediate result for the part,
or the final result in the case of the main body.

**Example:**
    The following example returns in shapColl the collection
of shapes managed by the main body of the partDoc
part document:

```VBScript
Dim body As Body
Set body = partDoc.Part.Bodies.MainBody
Set shapColl = body.Shapes

```

### Property **Sketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

Returns the body's Sketches collection. These skectches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `skColl` the collection of independent sketches of the main body of `partDoc` part document:

```VBScript
Dim body As Body
Set body = partDoc.Part.Bodies.MainBody
Set skColl = body.Sketches

```

Methods

### Sub **InsertHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

Insert a hybrid shape to the body.

**Parameters:**

` iHybriShape`      The hybrid shape to insert.  **Example:**      This example inserts the hybrid shape `HybridShape1` to the body `Body1`:

```VBScript
Body1.InsertHybridShape (HybridShape1)

```