# AssemblyPocket (Object)

**_Represents the AssemblyPocket object._**

## Properties

### Property **DirectionOrientation**( ) As [CatPrismOrientation](../PartInterfaces/enum_CatPrismOrientation_77897.md)

Returns or sets the pocket direction orientation.

**Example:**     The following example saves in `dirOrientation` the direction orientation of the pocket `assemblyPocket`, and then sets it so that the direction will be now inversed.

```VBScript
Dim dirOrientation
Set dirOrientation = assemblyPocket.DirectionOrientation
assemblyPocket.DirectionOrientation = catInverseOrientation

```

### Property **DirectionType**( ) As [CatPrismExtrusionDirection](../PartInterfaces/enum_CatPrismExtrusionDirection_144922.md)

Returns or sets the pocket direction type.

**Example:**     The following example saves in `dirType` the direction type of the pocket `assemblyPocket`, and then sets it so that the direction will be now normal to the sketch.

```VBScript
Dim dirType
Set dirType = assemblyPocket.DirectionType
assemblyPocket.DirectionType = catNormalToSketchDirection

```

### Property **FirstLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

Returns the first pocket limit.
A pocket has two limits that manage the way the pocket is ended.

**Example:**     The following example returns in `firstLimit` the first limit of the pocket `assemblyPocket`.

```VBScript
Dim firstLimit As Limit
Set firstLimit = assemblyPocket.FirstLimit

```

### Property **IsSymmetric**( ) As boolean

Returns or sets the pocket symmetry flag.
**TRUE** if the pocket is symmetric with respect to the base sketch, and **FALSE** otherwise.

**Example:**     The following example saves in `symFlag` the symmetry flag of the pocket `assemblyPocket`, and then sets it so that it will be now symmetric with respect to the base sketch.

```VBScript
Dim symFlag As boolean
Set symFlag = assemblyPocket.IsSymmetric
assemblyPocket.IsSymmetric = TRUE

```

### Property **SecondLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

Returns the second pocket limit.
A pocket has two limits that manage the way the pocket is ended.

**Example:**     The following example returns in `secondLimit` the second limit of the pocket `assemblyPocket`.

```VBScript
Dim secondLimit As Limit
Set secondLimit = assemblyPocket.SecondLimit

```

### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

Returns the pocket sketch.

**Example:**     The following example retrieves in `sketch` the sketch on which the pocket `assemblyPocket` is built.

```VBScript
Dim sketch As Sketch
Set sketch = assemblyPocket.Sketch

```

### Property **SketchComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

Returns the component containing the pocket sketch.

**Example:**     The following example retrieves in `skComp` the component that contains the sketch of the pocket `assemblyPocket` is built.

```VBScript
Dim skComp As Product
Set skComp = assemblyPocket.SketchComponent

```

Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

Retrieves the pocket direction vector components.
These components are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioDirection`      The pocket direction vector components, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example retrieves in `dirArray` the direction vector components of the pocket `assemblyPocket`.

```VBScript
Dim dirArray(2)
Call assemblyPocket.GetDirection(dirArray)
Set x = dirArray[0]
Set y = dirArray[1]
Set z = dirArray[2]

```

### Sub **ReverseInnerSide**( )

Reverses the pocket inner side when the profile is open.
This is useful for finding the shape to reach.

**Example:**     The following example reverses the current inner side of the pocket `assemblyPocket`.

```VBScript
assemblyPocket.ReverseInnerSide

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLineComp`)

Sets the pocket associated direction.

**Parameters:**

` iLine`      The pocket associated direction, as a reference to a line or an edge.
` iLineComp`      The component containing the associated direction reference

**Example:**     The following example sets the associated direction of the pocket `assemblyPocket` using the `dirRef` line of the component `dirComp`.

```VBScript
assemblyPocket.SetDirection dirRef, dirComp

```