# HybridShapeHelix (Object)

**_Represents the hybrid shape helix feature object._**
**Role** : Allows to access data of the Helix feature. This data includes:

  * axis
  * a starting point
  * a pitch
  * a height
  * 2 angle values

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Axis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Reads / Changes the Helix axis.

**Parameters:**

` Axis`      Helix axis.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): CATIARectlinearTriDimFeatEdge or [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  
### Property **ClockwiseRevolution**( ) As boolean

Reads / Modifies the sense of revolutions .

**Parameters:**

` Clockwise`      FALSE means that revolutions are counter-clockwise. TRUE means that revolutions are clockwise.

### Property **Height**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Reads the height of the Helix.

**Parameters:**

` oHeight`      Height.

### Property **InvertAxis**( ) As boolean

Reads / Modifies the orientation .

**Parameters:**

` Invert`      FALSE means that there is no invertion (natural orientation). TRUE to invert this orientation.

### Property **Pitch**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Reads the pitch of the Helix.

**Parameters:**

` oPitch`      Pitch.

### Property **Pitch2**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Reads the Helix pitch2.

**Parameters:**

` Pitch2`      Pitch2 for Helix.

### Property **PitchLawType**( ) As long

Reads / Changes the Helix pitch law type.

**Parameters:**

` LawType`      LawType for Helix.

### Property **Profile**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Reads / Changes the Helix profile.

**Parameters:**

` Profile`      Profile for Helix.

### Property **StartingAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Reads the helix starting angle.

**Parameters:**

` oStartingAngle`      Starting angle.

### Property **StartingPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Reads / Changes the starting point of the Helix. The starting point must not be on the Helix axis.

**Parameters:**

` StartingPoint`      Starting point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Property **TaperAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Reads the helix taper angle.

**Parameters:**

` oTaperAngle`      Taper angle.

### Property **TaperOutward**( ) As boolean

Reads / Modifies the taper angle sense of variation.

**Parameters:**

` TaperOutward`      FALSE means that helix radius decreases. TRUE means that helix radius increases.
Methods

### Sub **SetHeight**( double  `iHeight`)

Sets the helix height.

**Parameters:**

` iHeight`      Height.

### Sub **SetPitch**( double  `iPitch`)

Sets the helix pitch.

**Parameters:**

` iPitch`      Pitch.

### Sub **SetPitch2**( double  `iPitch2`)

Changes the Helix pitch2 .

**Parameters:**

` Pitch2`      Pitch2 for Helix.

### Sub **SetRevolutionNumber**( double  `iNbRevol`)

Changes the Revolution Numbers.

**Parameters:**

` NbRevol`      Number of revolutions for Helix.

### Sub **SetStartingAngle**( double  `iStartingAngle`)

Sets the helix starting angle.

**Parameters:**

` oTaperAngle`      Starting angle.

### Sub **SetTaperAngle**( double  `iTaperAngle`)

Sets the helix taper angle.

**Parameters:**

` iTaperAngle`      Taper angle.