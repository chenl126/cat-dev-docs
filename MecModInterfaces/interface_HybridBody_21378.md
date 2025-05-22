# HybridBody (Object)

**_The object is a hybrid body._**
The hybrid body manages a set of geometric elements, a set of hybrid shapes, a set of bodies and a set of hybrid bodies.
It belongs to the [HybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or @ref CATIABody or [HybridBody](../MecModInterfaces/interface_HybridBody_21378.md) object.

## Properties

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

Returns the hybrid body's Bodies collection.

**Example:**     The following example returns in `bodyColl` the collection of bodies of the hybrid body `hybridBody` :

```VBScript
Set bodyColl = hybridBody.Bodies

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

Returns the list of geometrical elements included in the hybrid body.

**Returns:**      oGeometricElements The list of geometric elements in the hybrid body (@see CATIAGeometricElements
for more information).

**Example:**     The following example returns in `geometricElements` the list of
geometrical elements in the Hybrid body `hybridBody`:

```VBScript
Dim geometricElements As GeometricElements
Set geometricElements = hybridBody.**GeometricElements**

```

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

Returns the hybrid body's HybridBodies collection.

**Example:**     The following example returns in `hybridBodyColl` the collection of hybrid bodies of the hybrid body `hybridBody` :

```VBScript
Set hybridBodyColl = hybridBody.HybridBodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

Returns the list of hybrid shapes included in the hybrid body.

**Returns:**      oHybridShapes The list of hybrid shapes in the hybrid body (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `hybridShapes` the list of
hybrid shapes in the hybrid body `hybridBody`:

```VBScript
Dim hybridShapes As HybridShapes
Set hybridShapes = hybridBody.**HybridShapes**

```

### Property **HybridSketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

Returns the hybrid body's Sketches collection. These skectches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `skColl` the collection of independent sketches of a hybrid body :

```VBScript
Set skColl = hybridBody.HybridSketches

```

Methods

### Sub **AppendHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

Appends a hybrid shape to the hybrid body.

**Parameters:**

` iHybriShape`      The hybrid shape to append.  **Example:**      This example appends the hybrid shape `hybridShape` to the hybrid body `hybridBody`:

```VBScript
hybridBody.AppendHybridShape (hybridShape)

```