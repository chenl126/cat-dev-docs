# HybridShapeLineAngle (Object)

**_Line defined from a reference curve, a plane or a surface, a point and an angle._**
**Role** : Allows to access data of the the line feature created with an angle to a curve.

## Properties

### Property **Angle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

**Role** : Get the angle to the reference curve of the line.

**Parameters:**

` oAngle`      angle

### Property **BeginOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

**Role** : Get the start length of the line.

**Parameters:**

` oStart`      start length

### Property **Curve**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Get the reference curve.

**Parameters:**

` oCurve`      reference curve.

### Property **EndOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

**Role** : Get the end length of the line.

**Parameters:**

` oEnd`      end length

### Property **Geodesic**( ) As boolean

**Role** : Get geodesic mode. If geodesic, the line lies on the support surface, otherwise the surface is only used to compute the line direction.

**Parameters:**

` oGeod`      Geodesic boolean

### Property **Orientation**( ) As long

**Role** : Get the line orientation. Orientation allows to reverse the line direction from the reference point. For a line of L length, it is the same as creating this line with -L length.

**Parameters:**

` oOrientation`      orientation : can be 1 or -1

### Property **Point**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Get the starting point of the line.

**Parameters:**

` oPoint`      starting point.

### Property **Surface**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

**Role** : Get the support surface.

**Parameters:**

` oSurface`      support surface.
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