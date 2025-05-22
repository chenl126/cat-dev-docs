# HybridShapeDevelop (Object)

**_Represents the hybrid shape develop feature object._**
**Role** : To access the data of the hybrid shape develop feature object. This data includes:

  * The developing mode
  * The positining mode used for the 2D wire
  * The 2D wire to be developed
  * The positioning transformation
  * The support revolution surface on which the development is operated
  * The point designated as the origin of the planar 2D wire
  * The direction corresponding to the first axis of the planar axis system related to the planar 2D wire
  * The development origin on the support surface

Use the CATIAHybridShapeFactory to create a HybridShapeDevelop object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Mode**( ) As long

Returns or sets the developing mode.
**Legal values** :

CATGSMDevelopMethod_DevDev
    Develop / develop algorithm
CATGSMDevelopMethod_DevProj
    Develop / project algorithm

### Property **ModePos**( ) As long

Returns or sets the positioning mode used for the 2D wire.
**Legal values** :

CATGSMPositionMode_NoneOrPositioned
    No positioning CATGSMPositionMode_ExplicitSweep     **=== DO NOT USE IN THIS CASE ===** CATGSMPositionMode_Develop     The 2D wire is to be moved from its initial position

### Property **PlaneAxisDirection**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the direction corresponding to the first axis of the planar axis system related to the planar 2D wire.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).  
### Property **PlaneAxisOrigin**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the point designated as the origin of the planar 2D wire.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Property **PointOnSupport**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the development origin on the support surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Property **PositionedWire**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the positioning transformation.
**Role** : To retrieve or set the positioning transformation associated to the develop feature and which result corresponds to the positioned 2D wire.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support revolution surface on which the development is operated.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Property **WireToDevelop**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the 2D wire to be developed.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  Methods

### Func **GetPlaneAxisAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md)

Retrieves the rotation angle.
**Role** : The rotation angle is expressed in the planar coordinate system related to the 2D planar wire from its default position.

**Returns:**      The rotation value  
### Func **GetPlaneAxisCoord**( long  `iCoorIdx`) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md)

Retrieves the translation coordinates.
**Role** : The translation coordinates are expressed with respect to the planar coordinate system related to the 2D planar wire from its default position. `GetPlaneAxisCoord` retrieves one coordinate at a time.

**Parameters:**

` iCoorIdx`      The coordinate index
**Legal values : 1 for X and 2 for Y
**Returns:**      The coordinate value  
### Func **GetPlaneAxisSwapAxes**( long  `ii`) As long

Retrieves the inversion axes from their previous definitions.

**Parameters:**

` iI`      == NOT USED YET == Must always be set to 0
**Returns:**      The inversion value
**Legal values** :

CATGSMAxisInversionMode_None
    No axis inverted CATGSMAxisInversionMode_X
    Only the X axis is inverted
CATGSMAxisInversionMode_Y
    Only the Y axis is inverted
CATGSMAxisInversionMode_Both
    Both axes are inverted

### Sub **SetPlaneAxisAngle**( double  `iAngle`)

Sets the rotation angle.
**Role** : The rotation angle is expressed in the planar coordinate system related to the 2D planar wire from its default position.

**Parameters:**

` iAngle`      The rotation angle value.

### Sub **SetPlaneAxisCoord**( long  `iCoorIdx`,  double  `iCoordValue`)

Sets the translation coordinates.
**Role** : The translation coordinates are expressed with respect to the planar coordinate system related to the 2D planar wire from its default position. `SetPlaneAxisCoord` sets one coordinate at a time.

**Parameters:**

` iCoorIdx`      The coordinate index
**Legal values : 1 for X and 2 for Y
` iCoordValue`      The coordinate value

### Sub **SetPlaneAxisSwapAxes**( long  `iIdx`,  long  `iInversionValue`)

Sets the inversion axes from their previous definitions.

**Parameters:**

` iIdx`      == NOT USED YET == Must always be set to 0
` iInversionValue`      The inversion value
**Legal values** :

CATGSMAxisInversionMode_None
    No axis inverted CATGSMAxisInversionMode_X
    Only the X axis is inverted
CATGSMAxisInversionMode_Y
    Only the Y axis is inverted
CATGSMAxisInversionMode_Both
    Both axes are inverted