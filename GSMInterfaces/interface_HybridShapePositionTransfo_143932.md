# HybridShapePositionTransfo (Object)

**_Represents the hybrid shape position transformation feature object._**
**Role** : To access the data of the hybrid shape position transformation feature object. This data includes:

  * The positioning mode
  * The profile to be positioned
  * The initila and target planes

Use the CATIAHybridShapeFactory to create a HybridShapePositionTransfo object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **InitialDirectionComputationMode**( ) As long

Gets or sets the computation mode of the X axis (or direction) of the initial axis system.

**Parameters:**

` oDirCompMode`      computation mode = 0 : no X axis specified = 1 : the X axis is implicitly the tangent of the profile at the origin(the origin then HAS to be on the profile). = 2 : the X axis is specified by a direction by SetPositionDirection(1,UserInputDirection).

### Property **Mode**( ) As long

Returns or sets the positioning mode.
**Legal values** :

CATGSMPositionMode_NoneOrPositioned
    No positioning
CATGSMPositionMode_ExplicitSweep
    The explicit profile is to be moved from its initial plane to the first sweep plane
CATGSMPositionMode_Develop
    === DO NOT USE IN THIS VERSION === planar wire is to be positioned in its initial plane; target origin corresponds to the zero-deformation point on the support surface (target axes are defined by the parameterization of the support surface)

### Property **Profile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the profile to be positioned.  Methods

### Func **GetNbPosAngle**( ) As long

Gets the number of numerical positioning parameters : first axis direction angles.

**Parameters:**

` oI`      Number of parameters

### Func **GetNbPosCoord**( ) As long

Gets the number of numerical positioning parameters : origin planar coordinates.

**Parameters:**

` oI`      Number of parameters

### Func **GetPosAngle**( long  `iI`) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Returns angles of both initial and target coordinate systems from default positions.

**Parameters:**

` iI`      The index of numerical positioning angles in initial (value 1) or target (value 2) axis system.
` oAngle`      The angle value.

### Func **GetPosCoord**( long  `ii`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Returns translation coordinates if both initial and target coordinate systems from default positions.

**Parameters:**

` iI`      The iIndex of numerical positioning coordinates in initial (value 1 or 2) or target (value 3 or 4) coordinate system.
` oCoordinate`      The coordinate value

### Func **GetPosPoint**( long  `ii`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns the points designated as the origins of the initial and target planes.

**Parameters:**

` iI`      The plane index: 1 for initial one, 2 for target one
` oElem`      The origin point

### Func **GetPosSwapAxes**( long  `ii`) As long

Returns axis inversion from previous definitions for both initial and target planes.

**Parameters:**

` iI`      The coordinate system index: 1 for initial one, 2 for target one
` oInversion`      The inversion value:

CATGSMAxisInversionMode_None
    No axis inverted
CATGSMAxisInversionMode_X
    Only the X axis iq inverted
CATGSMAxisInversionMode_Y
    Only the Y axis is inverted
CATGSMAxisInversionMode_Both
    Both axes inverted

### Func **GetPositionDirection**( long  `iI`) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Returns the positioning directions.
The positioning direction can be initial or target plane X-axis direction.

**Parameters:**

` iI`      The plane index: 1 for initial one, 2 for target one
` oElem`      The direction element

### Sub **RemoveAllPosAngle**( )

Removes all numerical positioning parameters : first axis direction angles.  
### Sub **RemoveAllPosCoord**( )

Removes all numerical positioning parameters : origin planar coordinates.  
### Sub **SetPosAngle**( long  `iI`,  [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)  `iAngle`)

Sets angles of both initial and target coordinate systems.

**Parameters:**

` iI`      The index of numerical positioning angles in initial (value 1) or target (value 2) axis system.
` iAngle`      The angle value.

### Sub **SetPosCoord**( long  `iI`,  [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)  `iCoordinate`)

Sets translation coordinates of both initial and target coordinate systems.

**Parameters:**

` iI`      The iIndex of numerical positioning coordinates in initial (value 1 or 2) or target (value 3 or 4) coordinate system.
` iCoordinate`      The coordinate value

### Sub **SetPosPoint**( long  `iI`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`)

Sets the points designated as the origins of the initial and target planes.

**Parameters:**

` iI`      The plane index: 1 for initial one, 2 for target one
` iElem`      The origin point

### Sub **SetPosSwapAxes**( long  `ii`,  long  `iInversion`)

Sets axis inversion from previous definitions for both initial and target planes.

**Parameters:**

` iI`      The coordinate system index: 1 for initial one, 2 for target one
` iInversion`      The inversion value:

CATGSMAxisInversionMode_None
    No axis inverted
CATGSMAxisInversionMode_X
    Only the X axis iq inverted
CATGSMAxisInversionMode_Y
    Only the Y axis is inverted
CATGSMAxisInversionMode_Both
    Both axes inverted

### Sub **SetPositionDirection**( long  `iI`,  [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)  `iElem`)

Sets the positioning directions.
The positioning direction can be initial or target plane X-axis direction.

**Parameters:**

` iI`      The plane index: 1 for initial one, 2 for target one
` iElem`      The direction element