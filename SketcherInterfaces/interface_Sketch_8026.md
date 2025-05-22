# Sketch (Object)

**_The Sketch is a 2D based element comprising constrained 2D geometrical elements._**
The Sketch is created by giving a 2D support.

## Properties

### Property **AbsoluteAxis**( ) As [CATIAAxis2D](../SketcherInterfaces/interface_Axis2D_6614.md) (Read Only)

Returns the 2D absolute axis of the sketch. The absolute axis is used for constraining the sketch in 3D space, and its constituting horizontal and vertical directions can also be used to constrain horizontally or vertically subsequent geometrical elements in the sketch.

**Returns:**      oAxis The absolute axis of the sketch (@see CATIAAxis2D for more information).

**Example:**     The following example places in `myAxis` the absolute axis
of the sketch `mySketch`:

```VBScript
Set myAxis = mySketch.**AbsoluteAxis**

```

### Property **CenterLine**( ) As [CATIALine2D](../SketcherInterfaces/interface_Line2D_6416.md)

Returns the geometric 2D line defined as the center line of the sketch. Center lines are then used for creating shafts.

**Returns:**      oLine The center line of the sketch(@see CATIALine2D for more information).

**Example:**     The following example returns in `myCenterLine` the center line
in the sketch `mySketch`:

```VBScript
Set myCenterLine = mySketch.**CenterLine**

```

### Property **Constraints**( ) As [CATIAConstraints](../MecModInterfaces/interface_Constraints_27490.md) (Read Only)

Returns the list of constraints included in the sketch.

**Returns:**      oConstraints The list of constraints in the sketch (@see CATIAConstraints
for more information).

**Example:**     The following example returns in `colConstraint` the list of constraints
in the sketch `mySketch`:

```VBScript
Set colConstraint = mySketch.**Constraints**

```

### Property **Factory2D**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md) (Read Only)

Returns the 2D factory of the sketch. Take care that you must open edition
on a sketch before adding or modifying elements in it.

**Returns:**      oFactory The 2D geometrical factory of the sketch (@see CATIAFactory2D
for more information).

**Example:**     The following example returns in `my2DFactory` the 2D factory
of the sketch `mySketch`:

```VBScript
Set my2DFactory = mySketch.**Factory2D**

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

Returns the list of geometrical elements included in the sketch.

**Returns:**      oGeometricElements The list of geometric elements in the sketch (@see CATIAGeometricElements
for more information).

**Example:**     The following example returns in `colGeometry` the list of geometrical
elements in the sketch `mySketch`:

```VBScript
Set colGeometry = mySketch.**GeometricElements**

```

Methods

### Sub **CloseEdition**( )

Closes the Sketch Edition. Once you have finished working with the sketch, you
must close its edition before using it for sketch-based shapes.

**Example:**     The following example closes the edition of the sketch `mySketch`:

```VBScript
mySketch.**CloseEdition**

```

### Sub **Evaluate**( )

Evaluate the constraint system of the sketch  
### Sub **GetAbsoluteAxisData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAxisData`)

Returns the sketch axis coordinates in 3D space. The matrix returned comprises 9 doubles, the first 3 being the coordinates
of the axis origin, the next 3 being those of the horizontal axis, and the
last 3 those of the vertical axis.
The sketch horizontal axis is in fact computed from the first non null projection of one of the 3 3D space axes on the sketch plane.

**Returns:**      oAxisData The matrix of the axis in 3D space.

**Example:**     The following example reads the coordinates of the axis
of the sketch `mySketch`:

```VBScript
Dim myAxisCoordinate (8)
mySketch.GetAbsoluteAxisData myAxisCoordinate
Set OriginX = myAxisCoordinate(1)
Set OriginY = myAxisCoordinate(2)
Set OriginZ = myAxisCoordinate(3)
Set HorizontalX = myAxisCoordinate(4)
Set HorizontalY = myAxisCoordinate(5)
Set HorizontalZ = myAxisCoordinate(6)
Set VerticalX = myAxisCoordinate(7)
Set VerticalY = myAxisCoordinate(8)
Set VerticalZ = myAxisCoordinate(9)

```

### Sub **InverseOrientation**( )

Inverse Orientation Of Sketch  
### Func **OpenEdition**( ) As [CATIAFactory2D](../SketcherInterfaces/interface_Factory2D_15860.md)

Opens the Sketch Edition. You must open edition on a sketch before you can add
elements in it. The CATIAFactory2D returned then enables you to create 2D
geometrical elements in the sketch.

**Returns:**      oFactory Returns the 2D FACTORY.

**Example:**     The following example opens edition on the sketch `mySketch`
and places the factory in `my2DFactory`:

```VBScript
Set my2DFactory = mySketch.**OpenEdition**

```

### Sub **SetAbsoluteAxisData**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iAxisData`)

Sets the absolute axis of the sketch in 3D space.

**Parameters:**

` oAxisData`      The matrix comprises 9 doubles, the first 3 being the coordinates
of the axis origin, the next 3 being those of the horizontal axis,
and the last 3 those of the vertical axis of the absolute axis.