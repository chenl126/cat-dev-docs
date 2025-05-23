# AssemblyHole (Object)

**_Represents the AssemblyHole object._**

## Properties

### Property **AnchorMode**(| ) As [CatHoleAnchorMode](../PartInterfaces/enum_CatHoleAnchorMode_58938.md)

   Returns or sets the hole anchor mode.
This property is valid when the hole type is Counterbored or Counterdrilled.

**Example:**     The following example saves in `holeAnchorMode` the anchor mode of the hole `assemblyHole` and sets it so that the anchor mode will now be set to the middle of its head.

```VBScript
     Dim holeAnchorMode
     Set holeAnchorMode = assemblyHole.AnchorMode
     assemblyHole.AnchorMode = catMiddlePointHoleAnchor

```

### Property **BottomAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the hole bottom angle.
This property is valid when the hole bottom type is VBottom. The hole bottom angle is returned as a [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) object.

**Example:**     The following example retrieves in `holeBottomAngle` the bottom angle of the hole `assemblyHole`.

```VBScript
     Dim holeBottomAngle As Angle
     Set holeBottomAngle = assemblyHole.BottomAngle

```

### Property **BottomLimit**( ) As [CATIALimit](../PartInterfaces/interface_Limit_5781.md) (Read Only)

   Returns the hole bottom limit.
This limit manages the way the hole is ended. It is returned as a [Limit](../PartInterfaces/interface_Limit_5781.md) object.

**Example:**     The following example retrieves in `limit` the bottom limit of the hole `assemblyHole`.

```VBScript
     Dim limit As Limit
     Set limit = assemblyHole.BottomLimit

```

### Property **BottomType**( ) As [CatHoleBottomType](../PartInterfaces/enum_CatHoleBottomType_61261.md)

   Returns or sets the hole bottom type.

**Example:**     The following example saves in `holeBottomType` the bottom type of the hole `assemblyHole` and sets it so that the bottom will now be a V-like one.

```VBScript
     Dim holeBottomType
     Set holeBottomType = assemblyHole.BottomType
     assemblyHole.BottomType = catVHoleBottom

```

### Property **Diameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole diameter.
It is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeDiam` the diameter of the hole `assemblyHole`.

```VBScript
     Dim holeDiam As Length
     Set holeDiam = assemblyHole.Diameter

```

### Property **HeadAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the hole head angle.
This property is valid when the hole type is Tapered, Counterdrilled or Countersunk. The hole head angle is returned as a [Angle](../KnowledgeInterfaces/interface_Angle_5497.md) object.

**Example:**     The following example retrieves in `holeHeadAngle` the head angle of the hole `assemblyHole`.

```VBScript
     Dim holeHeadAngle As Angle
     Set holeHeadAngle = assemblyHole.HeadAngle

```

### Property **HeadDepth**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole head depth.
This property is valid when the hole type is Counterbored, Counterdrilled or Countersunk. The hole head depth is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeHeadDepth` the head depth of the hole `assemblyHole`.

```VBScript
     Dim holeHeadDepth As Length
     Set holeHeadDepth = assemblyHole.HeadDepth

```

### Property **HeadDiameter**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the hole head diameter.
This property is valid when the hole type is Counterbored or Counterdrilled. The hole head diameter is returned as a [Length](../KnowledgeInterfaces/interface_Length_8108.md) object.

**Example:**     The following example retrieves in `holeHeadDiam` the head diameter of the hole `assemblyHole`.

```VBScript
     Dim holeHeadDiam As Length
     Set holeHeadDiam = assemblyHole.HeadDiameter

```

### Property **Sketch**( ) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md) (Read Only)

   Returns the hole positioning sketch.

**Example:**     The following example retrieves in `sketch` the positioning sketch of the hole `assemblyHole`.

```VBScript
     Dim sketch As Sketch
     Set sketch = assemblyHole.Sketch

```

### Property **SketchComponent**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the component containing the hole positioning sketch.

**Example:**     The following example retrieves in `skComp` the component that contains the positioning sketch of the hole `assemblyHole`.

```VBScript
     Dim skComp As Product
     Set skComp = assemblyHole.SketchComponent

```

### Property **Type**( ) As [CatHoleType](../PartInterfaces/enum_CatHoleType_25588.md)

   Returns or sets the hole type.

**Example:**     The following example saves in `holeType` the type of the hole `assemblyHole`, and then sets it so that it will now be a tapered hole.

```VBScript
     Set holeType = assemblyHole.Type
     assemblyHole.Type = catTaperedHole

```

Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioDirection`)

   Retrieves the hole direction vector components.
These components are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioDirection`      The direction vector components, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example returns in `dirArray` the direction vector components of the hole `assemblyHole`.

```VBScript
     Dim dirArray(2)
     Call assemblyHole.GetDirection(dirArray)
     Set x = dirArray[0]
     Set y = dirArray[1]
     Set z = dirArray[2]

```

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioOrigin`)

   Retrieves the origin point to which the hole is anchored.
This point belongs to a plane tangent to the hole. The coordinates are expressed in millimeter according to the absolute coordinate system.

**Parameters:**

` ioOrigin`      The hole origin point coordinates, as a safe array made up of three doubles: X, Y, Z
The array must be previously initialized.  **Example:**     The following example returns in `coordArray` the coordinates of the hole `assemblyHole`.

```VBScript
     Dim coordArray(2)
     Call assemblyHole.GetOrigin coordArray
     Set x = coordArray[0]
     Set y = coordArray[1]
     Set z = coordArray[2]

```

### Sub **SetDirection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLine`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLineComp`)

   Sets the hole axis direction.

**Parameters:**

` iLine`      The hole axis direction, as a reference to a line or an edge.
` iLineComp`      The component containing the axis direction  **Example:**     The following example sets the axis direction of the hole `assemblyHole` with the `dirRef` line of the component `dirComp`.

```VBScript
     assemblyHole.SetDirection dirRef, dirComp

```