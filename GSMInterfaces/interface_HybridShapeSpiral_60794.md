# HybridShapeSpiral (Object)

**_Represents the hybrid shape Spiral feature object._**
**Role** : Allows to access data of the Spiral feature. This data includes:

  * type
  * support
  * centre point
  * axis
  * starting radius
  * orientation
  * ending angle
  * ending radius
  * revolution
  * pitch

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Axis**( ) As [CATIAHybridShapeDirection](../GSMInterfaces/interface_HybridShapeDirection_84226.md)

Reads / Changes the Spiral axis (Reference direction).  
### Property **CenterPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Reads / Changes the center point of the Spiral.  
### Property **ClockwiseRevolution**( ) As boolean

Reads / Modifies the sense of revolutions .
FALSE means that revolutions are counter-clockwise.
TRUE means that revolutions are clockwise.  
### Property **EndingAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Reads / Changes the Ending Angle of the Spiral.  
### Property **EndingRadius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Reads / Changes the ending radius of the Spiral.  
### Property **InvertAxis**( ) As boolean

Reads / Modifies the orientation .
FALSE means that there is no invertion (natural orientation).
TRUE to invert this orientation.  
### Property **Pitch**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Reads the pitch of the Spiral.  
### Property **StartingRadius**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Reads / Changes the starting radius of the Spiral.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Reads / Changes the spiral plane support.  
### Property **Type**( ) As long

Reads / Changes the spiral type.  Methods

### Sub **SetAnglePitchParam**( double  `iEndAngle`,  double  `iRevolNumber`,  double  `iPitch`)

Sets Angle pitch parameter.  
### Sub **SetAngleRadiusParam**( double  `iEndAngle`,  double  `iRevolNumber`,  double  `iEndRadius`)

Sets Angle radius parameters.  
### Sub **SetRadiusPitchParam**( double  `iEndRadius`,  double  `iPitch`)

Sets Radius pitch parameter.