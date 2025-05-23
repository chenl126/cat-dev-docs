# AxisSystem (Object)

**_The object Axis System A axis system has got one origin point and three orthogonal axes, crossing at the origin point._**

## Properties

### Property **AxisRotationAngle**(| ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

   Returns the rotation angle of an axis system. Succeeds only if the axis system is defined by a rotation around an axis, wich means that its type is catAxisSystemAxisRotation.  
### Property **AxisRotationReference**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the reference for the axis rotation. Succeeds only if the axis system is defined by a rotation around an axis, wich means that its type is catAxisSystemAxisRotation.  
### Property **IsCurrent**( ) As boolean

   Returns True if the axis system is the current one, else returns False. Sets the axis system as the current one or not.

**Example:**     The following example returns in `isCurrent` True if the axis system `axisSystem` is the current one :

```VBScript
     isCurrent = axisSystem.IsCurrent

```

    The following example sets the axis system `axisSystem` as the current one :

```VBScript
     axisSystem.IsCurrent = 1

```
```

    The following example sets the axis system `axisSystem` as not the current one :

```VBScript
     axisSystem.IsCurrent = 0

```

### Property **OriginPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns or sets the geometric point which defines the origin of the axis system.
OriginPoint is and must be a reference on a geometric 3D point.

**Example:**     The following example sets the point `Point.1` of the Geometrical Set `Geometrical Set.1` as the origin point of the axis system `AxisSystem0`:

```VBScript
     Dim HybridBody4 As AnyObject
     Set HybridBody4 = Body1.HybridBodies.Item  ( "Geometrical Set.1" )
     Dim HybridShapePointCoord5 As AnyObject
     Set HybridShapePointCoord5 = HybridBody4.HybridShapes.Item  ( "Point.1" )
     Dim Reference6 As Reference
     Set Reference6 = CATIA.ActiveDocument.Part.CreateReferenceFromGeometry  ( HybridShapePointCoord5 )
     AxisSystem0.OriginPoint = Reference6

```

### Property **OriginType**( ) As [CATAxisSystemOriginType](../MecModInterfaces/enum_CATAxisSystemOriginType_110474.md)

   Returns or sets the way the origin point is defined.
The origin point can be not specified, or be defined by coordinates or by a geometric point.
CATAxisSystemOriginType is the enumeration which describes how the origin point is defined :
If OriginType=0, the origin point is defined by a geometric point. If no point si selected, the origin will be automatically put at the intersection of the lines or planes defining the axes.
If OriginType=1, the origin is defined by three coordinates x,y,z. Then, the origin will allways stays at the position defined by the coordinates.

**Example:**     The following example prints the origin type :

```VBScript
     Catia.SystemService.Print " OriginType = " & axisSystem.OriginType

```

    The following example sets the origin type to 1 :

```VBScript
     axisSystem.OriginType = 1

```

### Property **Type**( ) As [CATAxisSystemMainType](../MecModInterfaces/enum_CATAxisSystemMainType_91147.md)

   Returns or sets the type of the axis system. Sets the axis system type.

**Example:**     The following example returns in `type1` the type of the axis system `axisSystem1`:

```VBScript
     type1 = axisSystem1.Type

```

    The following example sets the type of the axis system `axisSystem1` as standard:

```VBScript
     axisSystem1.Type = 0

```

    The following example sets the type of the axis system `axisSystem1` as axis rotation:

```VBScript
     axisSystem1.Type = 1

```

    The following example sets the type of the axis system `axisSystem1` as datum (explicit):

```VBScript
     axisSystem1.Type = 3

```

### Property **XAxisDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Reads or sets the geometric point, line or plane which defines the direction of the X axis.
AxisDirection is and must be a reference on a 3D point or 3D line or plane.

**Example:**     The following example sets the point `Point.1` of the Geometrical Set `Geometrical Set.1` as the direction of the X axis of the axis system `AxisSystem0`:

```VBScript
     Dim HybridBody4 As AnyObject
     Set HybridBody4 = Body1.HybridBodies.Item  ( "Geometrical Set.1" )
     Dim HybridShapePointCoord5 As AnyObject
     Set HybridShapePointCoord5 = HybridBody4.HybridShapes.Item  ( "Point.1" )
     Dim Reference6 As Reference
     Set Reference6 = CATIA.ActiveDocument.Part.CreateReferenceFromGeometry  ( HybridShapePointCoord5 )
     AxisSystem0.XAxisDirection = Reference6

```

### Property **XAxisType**( ) As [CATAxisSystemAxisType](../MecModInterfaces/enum_CATAxisSystemAxisType_92007.md)

   Reads or sets the way the X axis is specified.
An axis X,Y, or Z of the axis system can be defined by a geometric point, line or plane, or by coordinates.
AxisType = 0 : The axis is defined by a geometric point, line or plane and with the same direction.
AxisType = 1 : The axis direction is defined by the three coordinates x,y,z, of a vector, to which the axis will allways stay parallel.
AxisType = 2 : the axis is defined by a geometric point, line or plane and with the opposite direction. Notice : If the X axis is neither defined by coordinates nor by a point,line or plane, the axis will be automatically computed in order to build an orthogonal axis sytem with the other specified axes.

**Example:**     The following example prints the X axis type :

```VBScript
     Catia.SystemService.Print " XAxisType = " & axisSystem.XAxisType

```

    The following example sets the X axis type to 1 :

```VBScript
     axisSystem.XAxisType = 1

```

### Property **YAxisDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Reads or sets the geometric point, line or plane which defines the direction of the Y axis.
AxisDirection is and must be a reference on a 3D point or 3D line or plane.

**Example:**     The following example sets the point `Point.1` of the Geometrical Set `Geometrical Set.1` as the direction of the Y axis of the axis system `AxisSystem0`:

```VBScript
     Dim HybridBody4 As AnyObject
     Set HybridBody4 = Body1.HybridBodies.Item  ( "Geometrical Set.1" )
     Dim HybridShapePointCoord5 As AnyObject
     Set HybridShapePointCoord5 = HybridBody4.HybridShapes.Item  ( "Point.1" )
     Dim Reference6 As Reference
     Set Reference6 = CATIA.ActiveDocument.Part.CreateReferenceFromGeometry  ( HybridShapePointCoord5 )
     AxisSystem0.YAxisDirection = Reference6

```

### Property **YAxisType**( ) As [CATAxisSystemAxisType](../MecModInterfaces/enum_CATAxisSystemAxisType_92007.md)

   Reads or sets the way the Y axis is specified.
An axis X,Y, or Z of the axis system can be defined by a geometric point, line or plane, or by coordinates.
AxisType = 0 : The axis is defined by a geometric point, line or plane and with the same direction.
AxisType = 1 : The axis direction is defined by the three coordinates x,y,z, of a vector, to which the axis will allways stay parallel.
AxisType = 2 : the axis is defined by a geometric point, line or plane and with the opposite direction. Notice : If the Y axis is neither defined by coordinates nor by a point,line or plane, the axis will be automatically computed in order to build an orthogonal axis sytem with the other specified axes.

**Example:**     The following example prints the Y axis type :

```VBScript
     Catia.SystemService.Print " YAxisType = " & axisSystem.YAxisType

```

    The following example sets the Y axis type to 1 :

```VBScript
     axisSystem.YAxisType = 1

```

### Property **ZAxisDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Reads or sets the geometric point, line or plane which defines the direction of the Z axis.
AxisDirection is and must be a reference on a 3D point or 3D line or plane.

**Example:**     The following example sets the point `Point.1` of the Geometrical Set `Geometrical Set.1` as the direction of the Z axis of the axis system `AxisSystem0`:

```VBScript
     Dim HybridBody4 As AnyObject
     Set HybridBody4 = Body1.HybridBodies.Item  ( "Geometrical Set.1" )
     Dim HybridShapePointCoord5 As AnyObject
     Set HybridShapePointCoord5 = HybridBody4.HybridShapes.Item  ( "Point.1" )
     Dim Reference6 As Reference
     Set Reference6 = CATIA.ActiveDocument.Part.CreateReferenceFromGeometry  ( HybridShapePointCoord5 )
     AxisSystem0.ZAxisDirection = Reference6

```

### Property **ZAxisType**( ) As [CATAxisSystemAxisType](../MecModInterfaces/enum_CATAxisSystemAxisType_92007.md)

   Reads or sets the way the Z axis is specified.
An axis X,Y, or Z of the axis system can be defined by a geometric point, line or plane, or by coordinates.
AxisType = 0 : The axis is defined by a geometric point, line or plane and with the same direction.
AxisType = 1 : The axis direction is defined by the three coordinates x,y,z, of a vector, to which the axis will allways stay parallel.
AxisType = 2 : the axis is defined by a geometric point, line or plane and with the opposite direction. Notice : If the Z axis is neither defined by coordinates nor by a point,line or plane, the axis will be automatically computed in order to build an orthogonal axis sytem with the other specified axes.

**Example:**     The following example prints the Z axis type :

```VBScript
     Catia.SystemService.Print " ZAxisType = " & axisSystem.ZAxisType

```

    The following example sets the Z axis type to 1 :

```VBScript
     axisSystem.ZAxisType = 1

```

Methods

### Sub **GetEulerAngles**( [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oFirstAngle`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `oSecondAngle`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `ThirdAngle`)

   Returns the Euler Angles of an axis system. Succeeds only if the axis system is defined by Euler angles, wich means its type is catAxisSystemEulerAngles.  
### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the coordinates X,Y,Z of the origin point of the axis system.

**Parameters:**

` oOrigin`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the origin point of the axis system.  **Example:**     The following example retrieves in `originCoord` the coordinates of the origin point of the `axisSystem` axis system:

```VBScript
     Dim originCoord(2)
     axisSystem.GetOrigin originCoord

```

### Sub **GetVectors**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oVectorX`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oVectorY`)

   Returns the coordinates X,Y,Z of the axes X and Y of the axis system.

**Parameters:**

` oVectorX`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the X axis vector of the axis system.
` oVectorY`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Y axis vector of the axis system.  **Example:**     The following example retrieves in `vectorXCoord` and `vectorYCoord` the coordinates of the vectors of the `axisSystem` axis system:

```VBScript
     Dim vectorXCoord(2)
     Dim vectorYCoord(2)
     axisSystem.GetVectors vectorXCoord, vectorYCoord

```

### Sub **GetXAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oXAxis`)

   Returns the coordinates X,Y,Z of the X axis of the axis system.

**Parameters:**

` oXAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the X axis of the axis system.  **Example:**     The following example retrieves in `XAxisCoord` the coordinates of the X axis of the `axisSystem` axis system:

```VBScript
     Dim XAxisCoord(2)
     axisSystem.GetXAxis XAxisCoord

```

### Sub **GetYAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oYAxis`)

   Returns the coordinates X,Y,Z of the Y axis of the axis system.

**Parameters:**

` oYAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Y axis of the axis system.  **Example:**     The following example retrieves in `YAxisCoord` the coordinates of the Y axis of the `axisSystem` axis system:

```VBScript
     Dim YAxisCoord(2)
     axisSystem.GetYAxis XAxisCoord

```

### Sub **GetZAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oZAxis`)

   Returns the coordinates X,Y,Z of the Z axis of the axis system.

**Parameters:**

` oZAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Z axis of the axis system.  **Example:**     The following example retrieves in `ZAxisCoord` the coordinates of the Z axis of the `axisSystem` axis system:

```VBScript
     Dim ZAxisCoord(2)
     axisSystem.GetZAxis ZAxisCoord

```

### Sub **PutOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`)

   Defines the coordinates X,Y,Z of the origin point of the axis system.

**Parameters:**

` iOrigin`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the origin point of the axis system.  **Example:**     The following example puts in `originCoord` the new coordinates of the origin point of the `axisSystem` axis system:

```VBScript
     Dim originCoord(2)
     originCoord ( 0 )  = 100.000000
     originCoord ( 1 )  = 200.000000
     originCoord ( 2 )  = 10.000000
     axisSystem.PutOrigin originCoord

```

### Sub **PutVectors**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iVectorX`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iVectorY`)

   Defines the coordinates X,Y,Z of the axes X and Y of the axis system.

**Parameters:**

` iVectorX`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the X axis vector of the axis system.
` iVectorY`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Y axis vector of the axis system.  **Example:**     The following example modifies in `vectorXCoord` and `vectorYCoord` the coordinates of the vectors of the `axisSystem` axis system:

```VBScript
     Dim vectorXCoord(2)
     vectorYCoord ( 0 )  = 1.000000
     vectorYCoord ( 1 )  = -1.000000
     vectorYCoord ( 2 )  = 0.000000
     Dim vectorYCoord(2)
     vectorYCoord ( 0 )  = 0.000000
     vectorYCoord ( 1 )  = 0.000000
     vectorYCoord ( 2 )  = 1.000000
     axisSystem.PutVectors vectorXCoord, vectorYCoord

```

### Sub **PutXAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iXAxis`)

   Defines the coordinates X,Y,Z of the X axis of the axis system.

**Parameters:**

` iXAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the X axis of the axis system.  **Example:**     The following example puts in `XAxisCoord` the new coordinates of the X axis of the `axisSystem` axis system:

```VBScript
     Dim XAxis(2)
     XAxis ( 0 )  = 100.000000
     XAxis ( 1 )  = 200.000000
     XAxis ( 2 )  = 10.000000
     axisSystem.PutXAxis XAxis

```

### Sub **PutYAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iYAxis`)

   Defines the coordinates X,Y,Z of the Y axis of the axis system.

**Parameters:**

` iYAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Y axis of the axis system.  **Example:**     The following example puts in `XAxisCoord` the new coordinates of the Y axis of the `axisSystem` axis system:

```VBScript
     Dim YAxis(2)
     YAxis ( 0 )  = 100.000000
     YAxis ( 1 )  = 200.000000
     YAxis ( 2 )  = 10.000000
     axisSystem.PutYAxis YAxis

```

### Sub **PutZAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iZAxis`)

   Defines the coordinates X,Y,Z of the Z axis of the axis system.

**Parameters:**

` iZAxis`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the Z axis of the axis system.  **Example:**     The following example puts in `ZAxisCoord` the new coordinates of the Z axis of the `axisSystem` axis system:

```VBScript
     Dim ZAxis(2)
     ZAxis ( 0 )  = 100.000000
     ZAxis ( 1 )  = 200.000000
     ZAxis ( 2 )  = 10.000000
     axisSystem.PutZAxis ZAxis

```