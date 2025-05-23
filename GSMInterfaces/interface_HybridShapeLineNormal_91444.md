# HybridShapeLineNormal (Object)

**_Line defined by a point and a direction normal to a surface._**

**Role** : To access data of the line feature created by using the normal direction of a surface

Use the CATIAHybridShapeFactory to create a HybridShapeLineNormal object.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) **See also:**      [Length](../KnowledgeInterfaces/interface_Length_8108.md) **See also:**      [HybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md) **See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BeginOffset**(| ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the start length of the line.
Start length : extension of the line, beginning at the starting point

**Example** :      This example retrieves in `oStart` the beginning offset length for the `LineNormal` hybrid shape feature.

```VBScript
     Dim oStart As  CATIALength
     Set oStart = LineNormal.BeginOffset

```

### Property **EndOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

   Returns the end length of the line.
End length : extension of the line, beginning at the ending point

**Example** :      This example retrieves in `oEnd` the starting length for the `LineNormal` hybrid shape feature.

```VBScript
     Dim oEnd As  CATIALength
     Set oEnd = LineNormal.EndOffset

```

### Property **Orientation**( ) As long

   Returns or Sets the line orientation.
Orientation allows to reverse the line direction from the reference point.
For a line of L length, it is the same as creating this line with -L length : Orientation : can be 1 or -1

**Example** :      This example retrieves in `oOrientation` the starting length for the `LineNormal` hybrid shape feature.

```VBScript
     Dim oOrientation As long
     Set oOrientation = LineNormal.Orientation

```

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the starting point of the line.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).

**Example** :      This example retrieves in `oPoint` the starting point for the `LineNormal` hybrid shape feature.

```VBScript
     Dim oPoint As Reference
     Set oPoint = LineNormal.Point

```

### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or Sets the surface to which the line will be normal.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).

**Example** :      This example retrieves in `oSurface` the surface for the `LineNormal` hybrid shape feature.

```VBScript
     Dim oSurface As Reference
     Set oSurface = LineNormal.Surface

```

Methods

### Func **GetLengthType**( ) As long

   Gets the length type Default is 0.

**Parameters:**

` oType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Func **GetSymmetricalExtension**( ) As boolean

   Gets whether the symmetrical extension of the line is active.

**Parameters:**

` oSym`      Symetry flag

### Sub **SetLengthType**( long  `iType`)

   Sets the length type Default is 0.

**Parameters:**

` iType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Sub **SetSymmetricalExtension**( boolean  `iSym`)

   Sets the symmetrical extension of the line (start = -end).

**Parameters:**

` iSym`      Symetry flag