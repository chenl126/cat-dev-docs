# OrderedGeometricalSet (Object)

**_The object is an ordered geometrical set._**
The ordered geometrical set manages a set of hybrid shapes, a set of bodies and a set of ordered geometrical sets.
It belongs to the [OrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or [OrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md) object.

## Properties

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

Returns the ordered geometrical set's Bodies collection.

**Example:**     The following example returns in `bodyColl` the collection of bodies of the ordered geometrical set `OrderedGeometricalSet1` :

```VBScript
Set bodyColl = OrderedGeometricalSet1.Bodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

Returns the list of hybrid shapes included in the ordered geometrical set.

**Returns:**      oHybridShapes The list of hybrid shapes in the ordered geometrical set (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `HybridShapes1` the list of
hybrid shapes in the ordered geometrical set`OrderedGeometricalSet1`:

```VBScript
Dim HybridShapes1 As HybridShapes
Set HybridShapes1 = OrderedGeometricalSet1.**HybridShapes**

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

Returns the ordered geometrical set's OrderedGeometricalSets collection.

**Example:**     The following example returns in `OrderedGeometricalSetColl` the collection of ordered geometrical set of the ordered geometrical set `OrderedGeometricalSet1` :

```VBScript
Set OrderedGeometricalSetColl = OrderedGeometricalSet1.OrderedGeometricalSets

```

### Property **OrderedSketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

Returns the ordered geometrical set's Sketches collection. These sketches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `sketchesCollection` the collection of independent sketches of an ordered geometrical set :

```VBScript
Set sketchesCollection = OrderedGeometricalSet1.OrderedSketches

```

Methods

### Sub **InsertHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

Inserts a hybrid shape to the ordered geometrical set.

**Parameters:**

` iHybridShape`      The hybrid shape to insert.  **Example:**      This example inserts the hybrid shape `HybridShape1` to the ordered geometrical set `OrderedGeometricalSet1`:

```VBScript
OrderedGeometricalSet1.InsertHybridShape (HybridShape1)

```