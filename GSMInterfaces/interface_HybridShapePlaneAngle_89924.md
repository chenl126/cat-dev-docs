# HybridShapePlaneAngle (Object)

**_Represents the hybrid shape plane angle feature object._**
**Role** : To access the data of the hybrid shape plane angle feature object, created with an angle to another plane. This data includes:

  * The rotation axis
  * The rotation angle
  * The reference plane

Use the CATIAHybridShapeFactory to create a HybridShapePlaneAngle object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Angle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

Returns the rotation angle.  
### Property **Orientation**( ) As long

Returns or sets the plane orientation.
**Role** : The orientation allows you to invert the plane from the reference plane.
**Legal values** : the orientation is 1 if the plane orientation is not inverted, and -1 otherwise.  
### Property **Plane**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference plane.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  
### Property **ProjectionMode**( ) As boolean

Gets or sets the projection mode status. ProjectionMode = TRUE : Rotation axis will be projected on to reference plane. = FALSE(default) : Rotation axis will be as it is. This example retrieves in `ProjMode` the projection mode status for the `PlaneAngle` hybrid shape feature.

```VBScript
Dim ProjMode As boolean
ProjMode = PlaneAngle.ProjectionMode

```

### Property **RevolAxis**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the rotation axis.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).