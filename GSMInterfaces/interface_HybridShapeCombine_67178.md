# HybridShapeCombine (Object)

**_Represents the hybrid shape combined curve object._**
**Role** : To access the data of the hybrid shape combined curve object. This data includes:

  * The three curves to which the circle is tangent
  * The surface that supports the circle
  * The orientation of each curve.

Use the [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md) object to create a HybridShapeCombine object.

## Properties

### Property **Direction1**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the first direction used to create the combined curve. The first direction is the direction along which the first curve is extruded.

**Example:**      This example sets `firstDir` as the first direction to create the combined curve `hybCombCurve`.

```VBScript
hybCombCurve.Direction1 = firstDir

```

### Property **Direction2**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns or sets the second direction used to create the combined curve.

**Example:**      This example retrieves in `secondDir` the second direction used to create the combined curve `hybCombCurve`.

```VBScript
Dim secondDir As CATIAHybridShapeDirection
Set secondDir = hybCombCurve.Direction2

```

### Property **Elem1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first curve used to create the combined curve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example:**      This example sets `firstCurve` as the first curve to create the combined curve `hybCombCurve`.

```VBScript
hybCombCurve.Elem1 = firstCurve

```

### Property **Elem2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the second curve used to create the combined curve.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).

**Example:**      This example retrieves in `secondCurve` the second curve used to create the combined curve `hybCombCurve`.

```VBScript
Dim secondCurve As CATIAReference
Set secondCurve = hybCombCurve.Elem2

```

### Property **NearestSolution**( ) As long

Returns or sets whether the combined curve is or should be created as the curve closest to the first curve.
**Role** : The nearest solution indicates whether the created combined curve is the one closest to the first curve if there are several possible combined curves, or if all these possible combined curves are created..
**Legal values** : 0 for the nearest solution and 1 for all possible solutions.

**Example:**      This example sets the nearest solution mode to create the combined curve `hybCombCurve` closest to the first curve.

```VBScript
hybCombCurve.NearestSolution = 1

```

### Property **SolutionTypeCombine**( ) As long

Returns or sets whether the curves that create the combined curve are or should be extruded along normals to the curve planes or along given directions.
**Role** : The curves that make up the combined curve are each extruded along a direction. This direction can be the normal to the curve plane, or can be set to a given direction. This is valid for the two curves altogether.
**Legal values** : 0 for the normal to the curve planes (default mode), 1 for given directions

**Example:**      This example sets that the combined curve `hybCombCurve` should be created by extruding the two curves along the normals to their planes.

```VBScript
hybCombCurve.SolutionTypeCombine = 0

```