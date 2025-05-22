# HybridShapePlaneOffset (Object)

**_Offset plane._**
**Role** : Allows to access data of the plane feature created with an offset to another plane.

## Properties

### Property **Offset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the offset value.  
### Property **Orientation**( ) As long

Returns or sets the plane orientation.
**Role** : The orientation allows you to invert the plane from the reference plane.
**Legal values** : the orientation is 1 if the plane orientation is not inverted, and -1 otherwise.  
### Property **Plane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).