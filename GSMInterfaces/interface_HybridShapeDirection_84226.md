# HybridShapeDirection (Object)

**_Represents the hybrid shape direction feature object._**
**Role** : To access the data of the hybrid shape direction feature object. A direction can be specified using:

  * A line: the direction is tangent to the line
  * A plane: the direction is normal to the plane
  * Its components

Use the CATIAHybridShapeFactory to create a HybridShapeDirection object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Object**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the object that specifies the direction.
This object can be a line or a plane.

**Parameters:**

` oObject`      The object (a line or a plane) that specifies the direction

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) or [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md).  
### Property **RefAxisSystem**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or Sets the reference Axis System for Direction feature.
This data is not mandatory, if element is null, the absolute axis system is taken.
When an element is given, X, Y and Z are considered in this Axis system. Example
:      This example retrieves in `oRefAxis` the reference Axis System for `Direction` feature.

```VBScript
Dim oRefAxis As CATIAReference
Set oRefAxis  = Direction.RefAxisSystem

```

### Property **Type**( ) As long (Read Only)

Returns the direction type.
**Legal value** : The direction type can be:

0
    The direction is specified using an object (a line or a plane). In the case of a plane, the direction is the normal to the plane
1
    The direction is specified using its components
Methods

### Func **DirectionSpecification**( ) As long

Queries the direction specification status.

**Parameters:**

` oDir`      direction specification = 0 : Direction is not specified. = 1 : Direction is specified and is valid. = -1 : Direction is specified but is not valid.

### Func **GetX**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

Returns the direction X component. This method succeeds only when direction is specified using components. It fails when direction is specified using a geometrical element i.e Line, Plane. In such cases use GetXVal method instead.

**Parameters:**

` oCoordinates`      The direction X component

### Func **GetXVal**( ) As double

Returns the direction X component as Double. This method succeeds irrespective of the way direction is specified.

**Parameters:**

` oX`      The direction X component

### Func **GetY**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

Returns the direction Y component. This method succeeds only when direction is specified using components. It fails when direction is specified using a geometrical element i.e Line, Plane. In such cases use GetYVal method instead.

**Parameters:**

` oCoordinates`      The direction Y component

### Func **GetYVal**( ) As double

Returns the direction Y component as Double.This method succeeds irrespective of the way direction is specified.

**Parameters:**

` oY`      The direction Y component

### Func **GetZ**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md)

Returns the direction Z component. This method succeeds only when direction is specified using components. It fails when direction is specified using a geometrical element i.e Line, Plane. In such cases use GetZVal method instead.

**Parameters:**

` oCoordinates`      The direction Z component

### Func **GetZVal**( ) As double

Returns the direction Z component as Double.This method succeeds irrespective of the way direction is specified.

**Parameters:**

` oZ`      The direction Z component