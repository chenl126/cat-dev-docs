# MecModInterfaces Framework

## Object Index

  * [AxisSystem](MecModInterfaces/interface_AxisSystem_22406.md)
  * [AxisSystems](MecModInterfaces/interface_AxisSystems_27251.md)
  * [BiDimFeatEdge](MecModInterfaces/interface_BiDimFeatEdge_33192.md)
  * [Bodies](MecModInterfaces/interface_Bodies_7994.md)
  * [Body](MecModInterfaces/interface_Body_3736.md)
  * [Boundary](MecModInterfaces/interface_Boundary_14542.md)
  * [Constraint](MecModInterfaces/interface_Constraint_22634.md)
  * [Constraints](MecModInterfaces/interface_Constraints_27490.md)
  * [CylindricalFace](MecModInterfaces/interface_CylindricalFace_46299.md)
  * [Edge](MecModInterfaces/interface_Edge_3456.md)
  * [Face](MecModInterfaces/interface_Face_3398.md)
  * [Factory](MecModInterfaces/interface_Factory_11318.md)
  * [FixTogether](MecModInterfaces/interface_FixTogether_26387.md)
  * [FixTogethers](MecModInterfaces/interface_FixTogethers_31656.md)
  * [GeometricElements](MecModInterfaces/interface_GeometricElements_62160.md)
  * [HybridBodies](MecModInterfaces/interface_HybridBodies_30456.md)
  * [HybridBody](MecModInterfaces/interface_HybridBody_21378.md)
  * [HybridShape](MecModInterfaces/interface_HybridShape_25589.md)
  * [HybridShapeInstance](MecModInterfaces/interface_HybridShapeInstance_75602.md)
  * [HybridShapes](MecModInterfaces/interface_HybridShapes_30836.md)
  * [InstanceFactory](MecModInterfaces/interface_InstanceFactory_48601.md)
  * [MonoDimFeatEdge](MecModInterfaces/interface_MonoDimFeatEdge_44932.md)
  * [NotWireBoundaryMonoDimFeatVertex](MecModInterfaces/interface_NotWireBoundaryMonoDimFeatVertex_212840.md)
  * [OrderedGeometricalSet](MecModInterfaces/interface_OrderedGeometricalSet_92509.md)
  * [OrderedGeometricalSets](MecModInterfaces/interface_OrderedGeometricalSets_102240.md)
  * [OriginElements](MecModInterfaces/interface_OriginElements_42458.md)
  * [Part](MecModInterfaces/interface_Part_3788.md)
  * [PartDocument](MecModInterfaces/interface_PartDocument_31472.md)
  * [PartInfrastructureSettingAtt](MecModInterfaces/interface_PartInfrastructureSettingAtt_168320.md)
  * [PlanarFace](MecModInterfaces/interface_PlanarFace_20456.md)
  * [RectilinearBiDimFeatEdge](MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md)
  * [RectilinearMonoDimFeatEdge](MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md)
  * [RectilinearTriDimFeatEdge](MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md)
  * [Shape](MecModInterfaces/interface_Shape_5555.md)
  * [ShapeInstance](MecModInterfaces/interface_ShapeInstance_35910.md)
  * [Shapes](MecModInterfaces/interface_Shapes_8122.md)
  * [Sketches](MecModInterfaces/interface_Sketches_14228.md)
  * [Solid](MecModInterfaces/interface_Solid_5633.md)
  * [TriDimFeatEdge](MecModInterfaces/interface_TriDimFeatEdge_39030.md)
  * [TriDimFeatVertexOrBiDimFeatVertex](MecModInterfaces/interface_TriDimFeatVertexOrBiDimFeatVertex_221087.md)
  * [Vertex](MecModInterfaces/interface_Vertex_8466.md)
  * [ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex](MecModInterfaces/interface_ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex_474398.md)

## Enumerated Types Index

  * [CATAxisSystemAxisType](MecModInterfaces/enum_CATAxisSystemAxisType_92007.md)
  * [CATAxisSystemMainType](MecModInterfaces/enum_CATAxisSystemMainType_91147.md)
  * [CATAxisSystemOriginType](MecModInterfaces/enum_CATAxisSystemOriginType_110474.md)
  * [CatConstraintAngleSector](MecModInterfaces/enum_CatConstraintAngleSector_121214.md)
  * [CatConstraintDistConfig](MecModInterfaces/enum_CatConstraintDistConfig_110847.md)
  * [CatConstraintDistDirection](MecModInterfaces/enum_CatConstraintDistDirection_143052.md)
  * [CatConstraintMode](MecModInterfaces/enum_CatConstraintMode_61138.md)
  * [CatConstraintOrientation](MecModInterfaces/enum_CatConstraintOrientation_124280.md)
  * [CatConstraintRefAxis](MecModInterfaces/enum_CatConstraintRefAxis_83938.md)
  * [CatConstraintRefType](MecModInterfaces/enum_CatConstraintRefType_84586.md)
  * [CatConstraintSide](MecModInterfaces/enum_CatConstraintSide_61126.md)
  * [CatConstraintStatus](MecModInterfaces/enum_CatConstraintStatus_78757.md)
  * [CatConstraintType](MecModInterfaces/enum_CatConstraintType_62511.md)
  * [CatPartElementsNamingMode](MecModInterfaces/enum_CatPartElementsNamingMode_128721.md)
  * [CatPartSurfaceElementsLocation](MecModInterfaces/enum_CatPartSurfaceElementsLocation_188182.md)
  * [CatPartUpdateMode](MecModInterfaces/enum_CatPartUpdateMode_59539.md)

---

# CATAxisSystemAxisType (Enumeration)

**_Specification of the axes of the coordinate system._**

**Values:**

` catAxisSystemAxisSameDirection`      = 0 Specifies that the axis direction is defined by a point, line, or plane.
If the axis is defined by a point, the axis has the direction of the vector going from the origin of the coordinate system to the point.
If defined by a line, the axis has the same direction as the line.
If defined by a plane, the axis has the same direction as the normal vector of the plane.
` catAxisSystemAxisByCoordinates`      = 1 Specifies that the axis direction is defined by the three coordinates x,y,z of a vector.
` catAxisSystemAxisOppositeDirection`      = 2 Specifies that the axis direction is not specified or defined by a point, line, or plane.
If the axis is defined by a point, the axis has the direction of the vector going from the point to the origin of the coordinate system.
If defined by a line, the axis has the opposite direction of the line.
If defined by a plane, the axis has the opposite direction of the normal vector of the plane.

---

# CATAxisSystemMainType (Enumeration)

**_Axis System type._**

**Values:**

` catAxisSystemStandard`      = 0 Specifies that the axis system is defined by an origin point and three axes
` catAxisSystemAxisRotation`      = 1 Specifies that the axis system is defined by an origin point, and a rotation around one axis
` catAxisSystemEulerAngles`      = 2 Specifies that the axis system is defined by an origin point, and the three Euler angles
` catAxisSystemExplicit=`      30 Specifies that the axis system is a datum.

---

# CATAxisSystemOriginType (Enumeration)

**_Axis System Origin._**

**Values:**

` catAxisSystemOriginByPoint`      = 0 Specifies that the origin point is put at the position defined by a geometric point. If no point si selected, the origin will be automatically put at the intersection of the lines or planes defining the axes.
` catAxisSystemOriginByCoordinates`      = 1 Specifies that the origin point must stay at the position defined by three coordinates x,y,z.

---

# CatConstraintAngleSector (Enumeration)

**_Special constraint property for angle constraints._**

It only applies to the constraints of type Angle or PlanarAngle.
The geometric elements of an angle constraint (e.g. : 2 lines or 2 planes) divide the sketch or the space in 4 regions which are called angular sectors, numbered from 0 to 3. By default, the constraint is created in the sector number 0. One angular sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angular sector, the Dimension.Value, Side and Orientation are also modified. 1 / 0 \---/--- 2/ 3 By default, the constraint is created in the sector number 0. One angle sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angle sector, the Dimension.Value, Side and Orientation are also modified.

**Values:**

` AngleSector=0`      The default sector of a constraint. Dimension.Value = angle Orientation = catCstOrientSame Side = catCstSidePositive
` AngleSector=1`      Dimension.Value = angle-180 if angle>180 abs(angle)+180 otherwise Orientation = catCstOrientOpposite Side = catCstSidePositive
` AngleSector=2`      Dimension.Value = abs(540-angle) if angle>180 180-fabs(angle) otherwise Orientation = catCstOrientOpposite Side = catCstSideNegative
` AngleSector=3`      Dimension.Value = 360-abs(angle) Orientation = catCstOrientSame Side = catCstSideNegative

---

# CatConstraintDistConfig (Enumeration)

**_Special constraint configurations for distance constraints._**

When distance constraints involve lines or cylinders, the constrained elements can rotate around the line on which the distance is measured, while still respecting the distance constraint. This degree of freedom is in most cases not wanted.
This enum is used to further qualify the distance constraint, so that such degree of freedom can be eliminated in case of need, without requiring another distinct constraint to be defined.

**Values:**

` catCstDCUnspec`      No additional condition is set on the constraint.
` catCstDCParallel`      In addition to being positioned at a given distance, constrained elements are required to be parallel. Their orientation can be the same or opposite.
` catCstDCParallelSameOrient`      In addition to being positioned at a given distance, constrained elements are required to be parallel, and their orientations are required to be the same.
` catCstDCParallelOppOrient`      In addition to being positioned at a given distance, constrained elements are required to be parallel, and their orientations are required to be opposite.

---

# CatConstraintDistDirection (Enumeration)

**_Constraint distance direction._**

`DistanceDirection`. This enum lists the appropriate values to set this property.

**Values:**

` catCstDistDirectionNone`      No direction has been specified. The constraint is measured as usual.
` catCstDistDirection1`      2D : The constraint is measured along the horizontal axis. 3D : The constraint is measured along the X axis.
` catCstDistDirection2`      2D : The constraint is measured along the vertical axis. 3D : The constraint is measured along the Y axis.
` catCstDistDirection3`      3D : The constraint is measured along the Z axis.

---

# CatConstraintMode (Enumeration)

**_Constraint working mode
Part constraints can work in two modes: as constraints or as measurements._**

In _constraint_ mode, the value assigned to the constraint drives the actual position of the constrained geometry.
In _measurement_ mode, the constraint value only reflects what can be observed from the actual position of the constrained geometry.

**Values:**

` catCstModeDrivingDimension`      Specifies that a constraint should work as a constraint.
` catCstModeDrivenDimension`      Specifies that a constraint should work as a measurement.

---

# CatConstraintOrientation (Enumeration)

**_Constraint elements relative orientation._**

When two geometrical elements are constrained, there is often a variety of relative positions and orientations of these elements that respect the constraint. For instance, if a distance constraint is placed on two planes, the second plane can lie on both sides of first plane while maintaining the requested distance: the constraint is respected, but geometry remains unresolved. Furthermore, even if the side is fixed, second plane still can be oriented so that its normal points towards the first plane or in the opposite direction, without breaking the constraint.
Managing such indetermination requires control over two variables:

**Side**     determines, when relevant, on which side of each other constrained elements should be positionned **Orientation**     determines, when relevant, how to orient constrained elements, whith respect to each other.  This enum deals with possibles options for dealing with the **Orientation** variable (see [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for possibles options for **Side**).

This enum is based on the notion of characteristic vector. A characteristic vector is a vector which is associated with a constrained element each time it can be assimilated to a line or a plane. The vector represents the direction of the line, or the direction normal to the plane.

**Values:**

` catCstOrientSame`      specifies that characteristic vectors associated to constrained elements have same orientation.
` catCstOrientOpposite`      specifies that characteristic vectors associated to constrained elements have opposite orientation.
` catCstOrientUndefined`      specifies that the relative orientation of characteristic vectors associated to constrained elements is not specified

---

# CatConstraintRefAxis (Enumeration)

**_Constraint reference axis._**

Constraints that specify parallelism or perpendicularity to an axis in 3D are mono-element constraints. The axis to which the constraint applies is determined by the constraint property `ReferenceAxis`. This enum lists appropriate values to set this property.

**Values:**

` catCstRefAxisX`      The constraint applies to the X axis.
` catCstRefAxisY`      The constraint applies to the Y axis.
` catCstRefAxisZ`      The constraint applies to the Z axis.

---

# CatConstraintRefType (Enumeration)

**_Constraint reference type._**

In the PartDesign context, an element having a Reference constraint will not move during the update. The Assembly context allows two behaviours : Either the element will not move, or the element will move to the position where it was when the Reference type has been set to FixInSpace. `ReferenceType`. This enum lists appropriate values to set this property.

**Values:**

` catCstRefTypeRelative`      The element will not move during the update (the default mode).
` catCstRefTypeFixInSpace`      The element will move to its former position (Assembly context only).

---

# CatConstraintSide (Enumeration)

**_Constrained elements relative side._**

When two geometrical elements are constrained, there is often a variety of relative positions and orientations of these elements that respect the constraint. For instance, if a distance constraint is placed on two planes, the second plane can lie on both sides of first plane while maintaining the requested distance: the constraint is respected, but geometry remains unresolved. Furthermore, even if the side is fixed, second plane still can be oriented so that its normal points towards the first plane or in the opposite direction, without breaking the constraint.
Managing such indetermination requires control over two variables:

**Side**     determines, when relevant, on which side of each other constrained elements should be positionned **Orientation**     determines, when relevant, how to orient constrained elements, whith respect to each other.  This enum deals with possibles options for dealing with the **Side** variable (see [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for possibles options for **Orientation**).

This enum is based on the notion of characteristic vector. A characteristic vector is a vector which is associated with a constrained element each time it can be assimilated to a line or a plane. The vector represents the direction of the line, or the direction normal to the plane.

**Values:**

` catCstSidePositive`      First constrained element characteristic vector points towards second constrained element.
Arithmetic sign of constraint value is ignored, only its absolute value is taken into account.
` catCstSideNegative`      First constrained element characteristic vector points opposite to second constrained element.
Arithmetic sign of constraint value is ignored, only its absolute value is taken into account.
` catCstSideSameAsValue`      Arithmetic sign of constraint value specifies where second element lies with regard to first one: a positive value means in the direction of first constrained element characteristic vector, a negative value in the opposite direction.
` catCstSideOppositeToValue`      Arithmetic sign of constraint value specifies where second element lies with regard to first one: a negative value means in the direction of first constrained element characteristic vector, a positive value in the opposite direction.
` catCstSideUndefined`      Relative positionning of constrained elements is not defined.

---

# CatConstraintStatus (Enumeration)

**_Possible state of a constraint._**

Indicates whether a constraint is satisfied or not, along with a diagnosis when not satisfied.

**Values:**

` catCstStatusOK`      The constraint is satisfied.
` catCstStatusKOStronglyNotSatisfied`      The constraint is strongly not satisfied (e.g. distance constraint between two planes, which are not currently parallel).
` catCstStatusKOWrongOrientOrSide`      The constraint is not satisfied because of the wrong orientation or side of its geometric elements (e.g. planes are parallel and at the specified distance, but their orientation is inverted with respect to the one specified by the constraint).
` catCstStatusKOWrongValue`      The constraint is not satisfied because of its value (e.g. planes are parallel and at the specified orientation and side but not at the specified distance).
` catCstStatusKOWrongGeomEltType`      The constraint is not satisfied because of the wrong type of its geometric elements (e.g. angle between a point and a plane). It can happen in an assembly when replacing a part by another.
` catCstStatusKOBroken`      The constraint is not satisfied because a geometric element is missing. It can happen in an assembly when a part is missing.

---

# CatConstraintType (Enumeration)

**_Possible types of constraints._**
According to their type, constraint may exist in 3D space (at the part level), in 2D space (at the sketch level), or both.

The constraint type also determines the number of elements (from 1 to 3) that are necessary to define the constraint, plus the type of those elements. Also, the constraint type defines the valid combinations between those types, and the associated semantics.

These combinations plus usage notes are detailed in tables on a per-type basis below.

**Values:**

` catCstTypeReference`      **catCstTypeReference Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt |  Point, Line, Circle or Arc, Ellipse or Arc, parabola, Hyperbola, Polynomial curve, Spline
_Possible configurations (2D)_
_1rst elt type_ | _Definition_ | _Notes_
All types |  The element support is not modifiable  | \--

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Point, Line, Plane, Cylinder, Sphere, Cone
_Possible configurations (3D)_
_1rst elt type_ | _Definition_ | _Notes_
All types |  The element cannot move with respect to the bloc that contains it  | \--
` catCstTypeDistance`      **catCstTypeDistance between 2 elements Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Line, Circle or Arc, Ellipse or Arc, Parabola, Hyperbola, Polynomial curve, Spline
Valid types for 2nd elt | Same as 1rst elt
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Point | Point |  Distance between points is equal to constraint value  | \--
Point | Curve |  Constraint is measured between point and its closest projection onto curve. Constraint value is equal to that distance.  | "Curve" means every possible type except point
Curve | Curve |  Constraint is measured at points on curves that mutually project onto the other curve, and such as their distance is minimum. Constraint value is this distance.  | "Curve" means every possible type except point

**_Constraint definition in 3D space**_
Valid types for 1rst Elt | Point, Line, Plane, Cylinder, Sphere, Cone
Valid types for 2nd Elt | Same as 1rst elt
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
_...with point_
Point | Point |  Distance between points is equal to constraint value.  | \--
Point | Line |  Distance between point and its projection onto line support is equal to constraint value.  | \--
Point | Plane |  Distance between point and its projection onto plane is equal to constraint value.  |  See
[CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the relative position of constrained elements
Point | Cylinder |  Constraint is measured along the line, perpendicular to cylinder axis, that contains point. Constraint value is equal to the distance between the point and the cylinder surface, measured along this line.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the placement of point relative to the normal to the cylinder at projection point.
Point | Sphere |  Constraint is measured along the line passing through point and sphere center. Constraint value is equal to the distance between point and sphere surface, measured along this line.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the placement of point relative to the normal to the sphere at projection point.
_...with line_
Line | Line |  Constraint is measured along the common perpendicular to both lines. Constraint value is equal to the distance between both lines measures on this perpendicular.  |  See [CatConstraintDistConfig](../MecModInterfaces/enum_CatConstraintDistConfig_110847.md) for further specifying parallelism conditions on lines.
Line | Plane |  Line is parallel to plane, i.e. line lies within a plane parallel to plane. Constraint value is equal to distance between those planes.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the relative position of line and plane
Line | Cylinder |  Same as Line/Line case, but constraint value is measured between line and cylinder surface.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing on which side of measurement point on first element is second element located (relative to the direction of normal to element at that point). See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing wether the distance to second element is measured on the inside or on the outside of it: it mutually orients the normals taken at measurement points on both elements.
Line | Sphere |  Constraint is measured on the line by which sphere center projects onto line. Constraint value is equal to the distance between that projection point and the sphere surface.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the relative position of line regarding the normal to sphere at constraint measurement point.
_...with plane_
Plane | Plane |  Planes are parallel and constraint value is equal to their distance.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing on which side of measurement point on first element is second element located (relative to the direction of normal to element at that point). See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing wether the distance to second element is measured on the inside or on the outside of it: it mutually orients the normals
Plane | Cylinder |  Plane is parallel to cylinder axis (as in Plane/Line case) and constraint value is measured between plane and cylinder surface.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing on which side of measurement point on first element is second element located (relative to the direction of normal to element at that point). See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing wether the distance to second element is measured on the inside or on the outside of it: it mutually orients the normals taken at measurement points on both elements.
Plane | Sphere |  Constraint value is equal to distance between plane and sphere surface.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the relative position of plane and sphere. See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of plane normal and normal to sphere at constraint measurement point.
_...with cylinder_
Cylinder | Cylinder |  Similar to a Line/Line distance constraint applied to cylinder axis, but constraint value is measured between cylinder surfaces.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing on which side of measurement point on first element is second element located (relative to the direction of normal to element at that point). See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing wether the distance to second element is measured on the inside or on the outside of it: it mutually orients the normals taken at measurement points on both elements. See [CatConstraintDistConfig](../MecModInterfaces/enum_CatConstraintDistConfig_110847.md) for further specifying parallelism conditions on cylinders axes.
Cylinder | Sphere |  Similar to a Line/Point distance constraint applied to cylinder axis and sphere center, but constraint value is measured between cylinder and sphere surfaces.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing on which side of measurement point on first element is second element located (relative to the direction of normal to element at that point). See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing wether the distance to second element is measured on the inside or on the outside of it: it mutually orients the normals taken at measurement points on both elements.
_...with sphere_
Sphere | Sphere |  Similar to a Point/Point distance constraint applied between spheres centers, but constraint value is measured between spheres surfaces.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing where second measurement point is taken on second sphere: normals to spheres at measurement points may be or not oriented in the same direction, thus defining two possible measurement points. See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the direction of constraint measurement relative to normal vector to first sphere.
Sphere | Cone |  Similar to a Point/Cone distance constraint applied between sphere center and cone, but constraint value is measured between sphere and cone surfaces.  | \--
` catCstTypeDistance`      **catCstTypeDistance with 3 elements Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **3**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | same as catCstTypeDistance
Valid types for 2nd elt | same as catCstTypeDistance
Valid types for 3rd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Same as catCstTypeDistance | Same as catCstTypeDistance | Line |  The difference with the distance between 2 elements is that the third element is a projection direction. The distance is measured after projection on the third element.  | \--

**_Constraint definition in 3D space**_
Valid types for 1rst elt | same as catCstTypeDistance
Valid types for 2nd elt | same as catCstTypeDistance
Valid types for 3rd elt | Line, plane
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Same as catCstTypeDistance | Same as catCstTypeDistance | Line or plane |  The distance is measured after projection on the third element.  | \--
` catCstTypeOn`      **catCstTypeOn Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Line, Circle or Arc, Ellipse or Arc
Valid types for 2nd elt | Same as 1rst elt
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
All Types | All Types |  Constrained elements supports are identical.  |  Support mean the element considered without limitation (e.g. the underlying infinite line for a line segment).

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Point, Line, Plane, Cylinder, Sphere, Cone, Circle
Valid types for 2nd elt | Same as 1rst elt
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Point | Point |  Points lie at the same location.  | \--
Point | Line |  Points lie on line support.  | \--
Point | Plane |  Point lies within plane.  | \--
Point | Cylinder |  Point lies on cylinder surface.  | \--
Point | Sphere |  Point lies on sphere surface.  | \--
Line | Line |  Lines supports are identical.  |  See
[CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of lines.
Line | Plane |  Line lies within plane.  | \--
Line | Cylinder |  One of the cylinder generating lines and line supports are the same.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of line support and Cylinder axis.
Line | Sphere |  Line support contains sphere center.  | \--
Plane | Plane |  Both planes are identical.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of planes.
Sphere | Sphere |  Spheres centers and radii are identical.  | \--
Cylinder | Cylinder |  Both cylinder supports are identical.  | Cylinder are considered infinite in length.
Cone | Cone |  Both cones supports are identical.  | Cones are considered infinite in heigth.
Cone | Circle |  The circle lies on the cone.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of the plane of the circle.
` catCstTypeConcentricity`      **catCstTypeConcentricity Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Circle or Arc, Ellipse or Arc
Valid types for 2nd elt | Same as 1rst elt
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Point | Circle |  Circle center lies on point.  | \--
Circle | Circle |  Circle centers lie on each other.  | \--
Point | Ellipse |  Ellipse center lies on point.  | \--
Ellipse | Circle |  Ellipse center lies on circle center.  | \--
Ellipse | Ellipse |  Ellipse center lies on ellipse center.  | \--

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Sphere
Valid types for 2nd elt | Sphere
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Sphere | Sphere |  Both spheres centers are the same.  | \--
` catCstTypeTangency`      **catCstTypeTangency Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Line, Circle or Arc, Ellipse or Arc, Parabola, Hyperbola, Polynomial curve, Spline
Valid types for 2nd elt | Same as 1rst elt
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
All types | All types |  A point exists, where both elements supports are tangent.  |  This constraint type cannot be defined between two lines.

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line, Plane, Cylinder, Sphere, Cone
Valid types for 2nd elt | Cylinder, Sphere, Cone
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Cylinder |  Line is tangent to cylinder.  | \--
Line | Sphere |  Line is tangent to sphere.  | \--
Plane | Cylinder |  Plane is tangent to cylinder.  |  See
[CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of plane and cylinder normals.
Plane | Sphere |  Plane is tangent to Sphere.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of plane and sphere normals.
Cylinder | Cylinder |  Both cylinders are tangent.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of both cylinder normals at tangency point. See [CatConstraintDistConfig](../MecModInterfaces/enum_CatConstraintDistConfig_110847.md) for adding additional parallelism requirements on the constraint.
Cylinder | Sphere |  Cylinders is tangent to sphere.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of cylinder and sphere normals.
Sphere | Sphere |  Both spheres are tangent.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of both spheres normals.
Cone | Cone |  Both cones are tangent through on of their gererating lines.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of both generating lines.
` catCstTypeLength`      **catCstTypeLength Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Line |  Line length is equal to constraint value.  | \--
` catCstTypeAngle`      **catCstTypeAngle Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  Angle between lines supports is equal to constraint value.  |  The angle is measured in degrees, within the 0-360 range.

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line, Plane
Valid types for 2nd elt | Line, Plane
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  The common perpendicular to both lines defines the normal to the measuring plane. Both lines direction vector is projected onto that plane. The constraint value is equal to the angular difference between those two projected vectors.  |  Angle is measured in degree, in the 0-180 range.
Line | Plane |  Constraint value is equal to the angular difference between the line direction vector and its projection onto the plane.  |  Angle is measured in degree, in the 0-180 range.
Plane | Plane |  Constraint value is equal to the angular difference between the normals to both planes.  |  Angle is measured in degree, in the 0-180 range.
` catCstTypePlanarAngle`      **catCstTypePlanarAngle Definition**
---
Constraint valid in | **3D**
# of needed elements | **3**

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Plane
Valid types for 2nd elt | Plane
Valid types for 3rd elt | Line
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Plane | Plane | Line |  Line lies at the intersection of both planes. Angle is measured in the normal plane to line.  |  Angle is measured in degrees, in the 0-360 range, in the direct sense of the measuring plane deduced for the line orientation.
` catCstTypeParallelism`      **catCstTypeParallelism Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  Both lines supports are parallel.  |  See
[CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of lines.

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line, Plane
Valid types for 2nd elt | Line, Plan
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  Both lines supports are parallel.  |  See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of lines.
Line | Plane |  Lines support is parallel to plane.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) for managing the relative position of line and plane
Plane | Plane |  Planes are parallel.  |  See [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md) and [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative positioning and orientation of planes.
` catCstTypeAxisParallelism`      **catCstTypeAxisParallelism Definition**
---
Constraint valid in | **3D**
# of needed elements | **1**

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line, Plane, Cylinder
_Possible combinations(3D)_
_1rst elt type_ | _Definition_ | _Notes_
All types |  Element is parallel to one of the 3D space axes.  |  See
[CatConstraintRefAxis](../MecModInterfaces/enum_CatConstraintRefAxis_83938.md) for managing which axis the constraint applies to. See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of element and axis in the case of line and cylinder.
` catCstTypeHorizontality`      **catCstTypeHorizontality Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Line |  Line is parallel to the horizontal component of the reference axis.  | \--
` catCstTypePerpendicularity`      **catCstTypePerpendicularity Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  Lines support are perpendicular.  | \--

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line, Plane, Cylinder
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
...with line
Line | Line |  Lines support are perpendicular.  | \--
Line | Plane |  Line is perpendicular to plane.  |  See
[CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of line direction vector and normal to plane.
Line | Cylinder |  Lines support is perpendicular to cylinder axis.  | \--
` catCstTypeAxisPerpendicularity`      **catCstTypeAxisPerpendicularity Definition**
---
Constraint valid in | **3D**
# of needed elements | **1**

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Line, Plane, Cylinder
_Possible combinations(3D)_
_1rst elt type_ | _Definition_ | _Notes_
All types |  Element is perpendicular to one of the 3D space axes.  |  See
[CatConstraintRefAxis](../MecModInterfaces/enum_CatConstraintRefAxis_83938.md) for managing which axis the constraint applies to. See [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md) for managing the relative orientation of element and axis in the case of line and cylinder.
` catCstTypeVerticality`      **catCstTypeVerticality Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Line |  Line is parallel to the vertical component of the reference axis.  | \--
` catCstTypeRadius`      **catCstTypeRadius Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Circle or Arc
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Circle/Arc |  Circle or arc radius is equal to constraint value.  | \--
` catCstTypeSymmetry`      **catCstTypeSymmetry Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **3**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Line, Circle or Arc, Ellipse or Arc
Valid types for 2nd elt | Same as 1rst elt
Valid types for 3rd elt | Line
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
All types | All types | Line |  First element is symmetric to second one with respect to line.  |  Types of first and second elements are the same.

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Point, Line, Plane, Cylinder, Sphere, Cone
Valid types for 2nd elt | Same as 1rst elt
Valid types for 3rd elt | Line, Plane
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
All types | All types | Line |  First element is symmetric to second one with respect to line.  |  Types of first and second elements are the same. Characteristic vectors of symmetric elements are always opposite.
All types | All types | Plane |  First element is symmetric to second one with respect to plane.  |  Types of first and second elements are the same. Characteristic vectors of symmetric elements are always opposite.
` catCstTypeMidPoint`      **catCstTypeMidPoint Definition**
---
Constraint valid in | **2D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Point | Line |  Point is equally distant from both line extremities.  | \--
` catCstTypeEquidistance`      **catCstTypeEquidistance Definition**
---
Constraint valid in | **2D**
# of needed elements | **3**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Point, Line
Valid types for 2nd elt | Same as 1rst elt
Valid types for 3rd elt | Point
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Point | Point | Point |  Third point is equally distant from first and second one.  | \--
Line | Line | Point |  Third point is equally distant from each of its projections onto first and second line.  | \--
` catCstTypeMajorRadius`      **catCstTypeMajorRadius Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Ellipse or Arc
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Ellipse or Arc |  The length of ellipse major axis is equal to constraint value.  |  Ellipse major axis is the largest of ellipse axes at creation time
` catCstTypeMinorRadius`      **catCstTypeMinorRadius Definition**
---
Constraint valid in | **2D**
# of needed elements | **1**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Ellipse or Arc
_Possible combinations(2D)_
_1rst elt type_ | _Definition_ | _Notes_
Ellipse or Arc |  The length of ellipse minor axis is equal to constraint value.  |  Ellipse minor axis is the smallest of ellipse axes at creation time
` catCstTypeChamfer`      **catCstTypeChamfer Definition**
---
Constraint valid in | **2D & 3D**
# of needed elements | **3**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
Valid types for 3rd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Line | Line | Line |  The chamfer is defined by two lengths and two angles.  |  The first line is between the second and the third lines. The first and second lines intersect in one of their extremities. Idem with the first and third lines.

**_Constraint definition in 3D space**_
Valid types for 1rst elt | Plane, Cone
Valid types for 2nd elt | Plane
Valid types for 3rd elt | Plane, Cylinder
_Possible combinations (3D)_
_1rst elt type_ | _2nd elt type_ | _3rd elt type_ | _Definition_ | _Notes_
Plane | Plane | Plane |  The chamfer is defined by two lengths and two angles. The mode of the constraint is catCstModeDrivenDimension.  |  The first plane is between the second and the third planes. The normal vectors of the planes are in a same plane.
Cone | Plane | Cylinder |  The chamfer is defined by two lengths and two angles. |  The cone and the cylinder have the same axis. The plane is normal to that axis. The cone is between the plane and the cylinder.
` catCstTypeChamferPerpend`      | **catCstTypeChamferPerpend Definition**
---
Constraint valid in | **2D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  Chamfer is defined by one length and one angle. The mode of the constraint is catCstModeDrivenDimension.  |  The third element is implicit because it is perpendicular to the second line and it intersects the first line in one of their extremities.
` catCstTypeCylinderRadius`      **catCstTypeChamferPerpend Definition**
---
Constraint valid in | **2D**
# of needed elements | **2**

**_Constraint definition in 2D space**_
Valid types for 1rst elt | Line
Valid types for 2nd elt | Line
_Possible combinations (2D)_
_1rst elt type_ | _2nd elt type_ | _Definition_ | _Notes_
Line | Line |  The cylinder radius is defined by the distance beetween 2 the lines which results of the projection of a cylinder on a drawing sheet.  | \--

---

# CatPartElementsNamingMode (Enumeration)

**_Naming mode parameter's possible values._**

**Role** : This enumeration is used in the [PartInfrastructureSettingAtt](../MecModInterfaces/interface_PartInfrastructureSettingAtt_168320.md) interface.

**Values:**

` catNoCheck`      Naming is rule-free,
` catNamingCheckUnderSameNode`      Two elements cannot have the same name under the same node,
` catNamingCheckWithinUIActiveObject`      Two elements cannot have the same name within a defined UIActiveObject.

---

# CatPartSurfaceElementsLocation (Enumeration)

**_Wireframe and surface elements location parameter's possible values._**

**Role** : This enum is used in the [PartInfrastructureSettingAtt](../MecModInterfaces/interface_PartInfrastructureSettingAtt_168320.md) interface.

**Values:**

` catPartBodyLocation`      Wireframe and surface elements are created within a PartBody
` catXGSLocation`      Wireframe and surface elements are created within a G.S. or an O.G.S..

---

# CatPartUpdateMode (Enumeration)

**_Update mode setting parameter's possible values._**

**Role** : This enum is used in the [PartInfrastructureSettingAtt](../MecModInterfaces/interface_PartInfrastructureSettingAtt_168320.md) interface.

**Values:**

` catManualUpdate`      User has to manually launch update tasks.
` catAutomaticUpdate`      Update is automatically launched

---

# AxisSystem (Object)

**_The object Axis System A axis system has got one origin point and three orthogonal axes, crossing at the origin point._**

## Properties

### Property **AxisRotationAngle**( ) As [CATIAAngle](../KnowledgeInterfaces/interface_Angle_5497.md) (Read Only)

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

---

# AxisSystems (Collection)

**_A collection of all the AxisSystem objects contained in the part._**

## Methods

### Func **Add**( ) As [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)

   Creates a new AxisSystem and adds it to the AxisSystems collection.

**Returns:**      The created AxisSystem  **Example:**      The following example creates a AxisSystem names `NewAxisSystem` in the AxisSystem collection of the `rootPart` part in the `partDoc` part document.

```VBScript
     Set rootPart = partDoc.Part
     Set NewAxisSystem = rootPart.AxisSystems.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)

   Returns an Axis System using its index or its name from the AxisSystems collection.

**Parameters:**

` iIndex`      The index or the name of the AxisSystem to retrieve from the collection of AxisSystems. As a numerics, this index is the rank of the AxisSystem in the collection. The index of the first AxisSystem in the collection is 1, and the index of the last AxisSystem is Count. As a string, it is the name you assigned to the AxisSystem using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved AxisSystem **Example:**      This example retrieves in `ThisAxisSystem` the fifth AxisSystem in the collection and in `ThatAxisSystem` the AxisSystem named `MyAxisSystem` in the AxisSystem collection of the `partDoc` part document.

```VBScript
     Set AxisSystemColl = partDoc.Part.AxisSystems
     Set ThisAxisSystem = AxisSystemColl.Item(5)
     Set ThatAxisSystem = AxisSystemColl.Item("MyAxisSystem")

```

---

# BiDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is two dimensional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a surface obtained through the extrusion of a spline. You will create a BiDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewPointOnCurveFromDistance](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewPointOnCurveFromDistance) ). The lifetime of a BiDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select an edge, and creates a point on this edge. Here, both TriDimFeatEdge and BiDimFeatEdge objects are proposed to the user.

```VBScript
     Dim InputObjectType(1)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     Set HybridBodies = Document.Part.HybridBodies
     Set HybridBody = HybridBodies.Item("Geometrical Set.1")
     'We propose to the user that he select an edge
     InputObjectType(0)="TriDimFeatEdge"
     InputObjectType(1)="BiDimFeatEdge"
     Status=Selection.SelectElement2(InputObjectType,"Select an edge",true)
     if (Status = "cancel") then Exit Sub
     Set Curve = Selection.Item(1).Value
     Set HybridShapePointOnCurve = HybridShapeFactory.AddNewPointOnCurveFromDistance(Curve,18.0,False)
     HybridBody.AppendHybridShape HybridShapePointOnCurve
     Document.Part.InWorkObject = HybridShapePointOnCurve
     Document.Part.Update

```

---

# Bodies (Collection)

**_A collection of all the Body objects contained in the part._**

## Methods

### Func **Add**( ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

   Creates a new body and adds it to the Bodies collection. This body becomes the current one

**Returns:**      The created body  **Example:**      The following example creates a body names `NewBody` in the body collection of the `rootPart` part in the `partDoc` part document. `NewBody` becomes the current body in `partDoc`.

```VBScript
     Set rootPart = partDoc.Part
     Set NewBody = rootPart.Bodies.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

   Returns a body using its index or its name from the Bodies collection.

**Parameters:**

` iIndex`      The index or the name of the body to retrieve from the collection of bodies. As a numerics, this index is the rank of the body in the collection. The index of the first body in the collection is 1, and the index of the last body is Count. As a string, it is the name you assigned to the body using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved body **Example:**      This example retrieves in `ThisBody` the fifth body in the collection and in `ThatBody` the body named `MyBody` in the body collection of the `partDoc` part document.

```VBScript
     Set BodyColl = partDoc.Part.Bodies
     Set ThisBody = BodyColl.Item(5)
     Set ThatBody = BodyColl.Item("MyBody")

```

---

# Body (Object)

**_The object that manages a sequence of shapes, and a set of independent sketches waiting for their use in shapes; a set of hybrid bodies, a set of ordered geometrical sets and a set of hybrid shapes._**

It belongs to the [Bodies](../MecModInterfaces/interface_Bodies_7994.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or [HybridBody](../MecModInterfaces/interface_HybridBody_21378.md) object.

## Properties

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

   Returns the body's HybridBodies collection.

**Example:**     The following example returns in `hybridBodyColl` the collection of hybrid bodies of the main body of `partDoc` part document:

```VBScript
     Dim body As Body
     Set body = partDoc.Part.Bodies.MainBody
     Set hybridBodyColl = body.HybridBodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

   Returns the list of hybrid shapes included in the body.

**Returns:**      oHybridShapes The list of hybrid shapes in the body (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `HybridShapes1` the list of
hybrid shapes in the body `Body1`:

```VBScript
     Dim HybridShapes1 As HybridShapes
     Set HybridShapes1 = Body1.**HybridShapes**

```

### Property **InBooleanOperation**( ) As boolean (Read Only)

   Returns True if the body is involved in a boolean operation, else returns False.

**Example:**     The following example returns in `operated` True if the body `body1`belongs to a boolean operation.

```VBScript
     operated = body1.InBooleanOperation

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

   Returns the body's OrderedGeometricalSets collection.

ometricalSetColl = Body1.OrderedGeometricalSets
```

**Example:**     The following example returns in `OrderedGeometricalSetColl` the collection of ordered geometrical set of the body `Body1` :

```VBScript
     Set OrderedGe

### Property **Shapes**( ) As [CATIAShapes](../MecModInterfaces/interface_Shapes_8122.md)  (Read Only)

     Returns the body's Shapes collection.
     These shapes make up the sequence of shapes that will produce an
     intermediate result for the part,
     or the final result in the case of the main body.

     **Example:**
         The following example returns in shapColl the collection
     of shapes managed by the main body of the partDoc
     part document:

```VBScript
     Dim body As Body
     Set body = partDoc.Part.Bodies.MainBody
     Set shapColl = body.Shapes

```

### Property **Sketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

   Returns the body's Sketches collection. These skectches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `skColl` the collection of independent sketches of the main body of `partDoc` part document:

```VBScript
     Dim body As Body
     Set body = partDoc.Part.Bodies.MainBody
     Set skColl = body.Sketches

```

Methods

### Sub **InsertHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

   Insert a hybrid shape to the body.

**Parameters:**

` iHybriShape`      The hybrid shape to insert.  **Example:**      This example inserts the hybrid shape `HybridShape1` to the body `Body1`:

```VBScript
     Body1.InsertHybridShape (HybridShape1)

```

---

# Boundary (Object)

**_Topological cell, such as a face, an edge or a vertex._**

**Role** : The Boundary objects are basic topological objects, such as the edge of a Pad. Some of them posess a geometrical feature (_planar_ face, _rectilinear_ edge). You will create a Boundary object (such as the [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) object, which is derived, indirectly, from the Boundary object) using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewEdgeFilletWithConstantRadius](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewEdgeFilletWithConstantRadius) ). Note that, regarding V4 sub-elements, once the data of a CATIA Version 4 Model has been copied to a .CATPart, the sub-elements of the resulting .CATPart are supported by the [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. The lifetime of a Boundary object is limited. In particular, after having call [Part.Update](../MecModInterfaces/interface_Part_3788.htm#Update) , the Boundary objects are usually no more valid. **See also:**

  * [Face](../MecModInterfaces/interface_Face_3398.md) , [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md)
  * [Edge](../MecModInterfaces/interface_Edge_3456.md) , [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) , [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) , [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) , [MonoDimFeatEdge](../MecModInterfaces/interface_MonoDimFeatEdge_44932.md) , [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md)
  * [Vertex](../MecModInterfaces/interface_Vertex_8466.md) , [TriDimFeatVertexOrBiDimFeatVertex](../MecModInterfaces/interface_TriDimFeatVertexOrBiDimFeatVertex_221087.md) , [NotWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_NotWireBoundaryMonoDimFeatVertex_212840.md), [ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex_474398.md)

**Note:** [Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects cannot be selected into the specification tree.

**Note:** For a [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object, the object returned by the [AnyObject.Parent](../System/interface_AnyObject_17321.htm#Parent) property is the master shape. For example, if we have:

```VBScript
                             Pad.2
                              !
                              !
     +                        V
     !                      +---+
     !                    /   / !
     +-- Pad.1          /   /   !
     !                /   / one +------+
     !               +---+    /       /! <--- Pad.1
     !               !   !  /       /  +
     +-- Pad.2       !   !/       /   /
                     !   +------+   /
                     !          ! /
                     +----------+

```

then, for the [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) number "one", the [AnyObject.Parent](../System/interface_AnyObject_17321.htm#Parent) property returns the Pad.2 automation object (see [Pad](../PartInterfaces/interface_Pad_1979.md) ).

**Example:**      This example asks the end user to select an edge (using the [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) object), and creates an edge fillet on this edge:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select an edge
     InputObjectType(0)="TriDimFeatEdge"
     Status=Selection.SelectElement2(InputObjectType,"Select an edge",true)
     if (Status = "cancel") then Exit Sub
     Set EdgeFillet = ShapeFactory.AddNewEdgeFilletWithConstantRadius(Selection.Item(1).Value,1,5.0)
     EdgeFillet.EdgePropagation = 1
     Document.Part.Update

```

---

# Constraint (Object)

**_A geometric constraint set for geometric elements of a part, a sketch, or a product._**

## Properties

### Property **AngleSector**( ) As [CatConstraintAngleSector](../MecModInterfaces/enum_CatConstraintAngleSector_121214.md)

   Returns or sets the constraint angle (or angular) sector. The geometric elements of an angle constraint (e.g. : 2 lines or 2 planes) divide the sketch or the space in 4 regions which are called angle or angular sectors, numbered from 0 to 3. 1 / 0 \---/--- 2/ 3 By default, the constraint is created in the sector number 0. One angle sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angle sector, the Dimension.Value, Side and Orientation are also modified.

**Parameters:**

` AngleSector=0`      The default sector of a constraint. Dimension.Value = angle Orientation = catCstOrientSame Side = catCstSidePositive
` AngleSector=1`      Dimension.Value = angle-180 if angle>180 abs(angle)+180 otherwise Orientation = catCstOrientOpposite Side = catCstSidePositive
` AngleSector=2`      Dimension.Value = abs(540-angle) if angle>180 180-fabs(angle) otherwise Orientation = catCstOrientOpposite Side = catCstSideNegative
` AngleSector=3`      Dimension.Value = 360-abs(angle) Orientation = catCstOrientSame Side = catCstSideNegative

**Example:**     The following example retrieves in `angleSector` the angle sector of the `angleCst` angle constraint and then changes the angle sector

```VBScript
     angleSector = angleCst.AngleSector
     angleCst.AngleSector = 2

```

### Property **Dimension**( ) As [CATIADimension](../KnowledgeInterfaces/interface_Dimension_18130.md) (Read Only)

   Returns the constraint dimension. The dimension may be meaningless for some types of constraints such as tangency constraints, or if the constraint is not currently satisfied. Use the Status property to check whether the constraint is satisfied.

**Example:**     The following example returns in `cstDimension` the dimension of the `firstCst` constraint:

```VBScript
     Set cstDimension = firstCst.Dimension

```

### Property **DistanceConfig**( ) As [CatConstraintDistConfig](../MecModInterfaces/enum_CatConstraintDistConfig_110847.md)

   Returns or sets the distance constraint configuration. Distance constraints between lines and cylinders offer often more degrees of freedom to geometry than acually desired. This property allows to limit these degrees of freedom without having to redefine additional constraints. This property is useless for constraints whose type is not distance.

**Example:**     The following example retrieves in `distCstConfig` the configuration of the `distCst` distance constraint:

```VBScript
     distCstConfig = distCst.DistanceConfig

```

### Property **DistanceDirection**( ) As [CatConstraintDistDirection](../MecModInterfaces/enum_CatConstraintDistDirection_143052.md)

   Returns or sets the distance constraint direction. This property is useless for constraints whose type is not Distance (1). Distance constraints may be measured along a particular direction. This property will be used if the direction is a reference axis : In 2D, 1 means the horizontal axis, 2 the vertical axis. In 3D, 1 stands for the X axis, 2 for the Y axis, 3 for the Z axis. 0 means that no direction is specified and the distance is measured as usual.

**Example:**     The following example retrieves in `distCstDirection` the configuration of the `distCst` distance constraint:

```VBScript
     distCstConfig = distCst.DistanceDirection

```

### Property **Mode**( ) As [CatConstraintMode](../MecModInterfaces/enum_CatConstraintMode_61138.md)

   Returns or sets the constraint driving mode. For constraint types supporting the concept of value, such as distance constraints, the driving mode tells whether the constraint value actually drives the geometry position, or, conversely, is driven by it.

**Example:**     The following example retrieves in `currentMode` the driving mode for the `distCst` distance constraint:

```VBScript
     currentMode = distCst.Mode

```

### Property **Orientation**( ) As [CatConstraintOrientation](../MecModInterfaces/enum_CatConstraintOrientation_124280.md)

   Returns or sets the constraint orientation. This is used for constraints that involve two geometric elements and specifies the orientation for the second geometric element with regard to the first one, when several possible orientations are all satisfying the constraint.

**Example:**     The following example retrieves the in `distCstOrient` the orientation of the `distCst` distance constraint:

```VBScript
     distCstOrient = distCst.Orientation

```

### Property **ReferenceAxis**( ) As [CatConstraintRefAxis](../MecModInterfaces/enum_CatConstraintRefAxis_83938.md)

   Returns or sets the constraint reference axis. AxisParallel or AxisPerpendicular constraint types define which axis they relate to through this property, which makes no sense for constraints of another type.

**Example:**     The following example retrieves in `refAxis` the reference axis for the `axisPerpCst` AxisPerpendicular constraint:

```VBScript
     refAxis = axisPerpCst.ReferenceAxis

```

### Property **ReferenceType**( ) As [CatConstraintRefType](../MecModInterfaces/enum_CatConstraintRefType_84586.md)

   Returns or sets the constraint reference type. This property is used only for Reference constraints in the Assembly context.

**Example:**     The following example applies to the reference constraint refCst2 the reference type of the constraint refCst1.

```VBScript
     refCst2.ReferenceType = refCst1.ReferenceType

```

### Property **Side**( ) As [CatConstraintSide](../MecModInterfaces/enum_CatConstraintSide_61126.md)

   Returns or sets the constraint side. Some constraint types need to relatively position the constrained geometries, when several possible configurations are all satisfying the constraint.

**Example:**     The following example retrieves in `distCstSide` the side of the `distCst` distance constraint:

```VBScript
     distCstSide = distCst.Side

```

### Property **Status**( ) As [CatConstraintStatus](../MecModInterfaces/enum_CatConstraintStatus_78757.md) (Read Only)

   Returns the constraint status. The constraint status is a diagnosis on whether the constraint is satisfied.

**Example:**     The following example retrieves the status of the `distCst` distance constraint.

```VBScript
     distCstSts = distCst.Status

```

### Property **Type**( ) As [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md) (Read Only)

   Returns the constraint type.

**Example:**     The following example returns in `cstType` the type of the `firstCst` constraint:

```VBScript
     cstType = firstCst.Type

```

Methods

### Sub **Activate**( )

   Unsuppresses a constraint for the update process. An activated constraint is again taken into account for the calculation of the part or product. **Example:**     The following example es the `pad1` pad: **Example:**     The following example activates the `tangencyCst` constraint :

```VBScript
     tangencyCst.Activate

```

### Sub **Deactivate**( )

   Suppresses the constraint from being updated. A deactivated constraint is not taken into account for the calculation of the part or of the product.  **Example:**     The following example deactivates the `tangencyCst` constraint from being updated:

```VBScript
     tangencyCst.Deactivate

```

### Func **GetConstraintElement**( long  `iElementNumber`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Reads an element of a constraint.

**Parameters:**

` iElementNumber`      The number of the element of the constraint to be read. (1 for the first element,2 for the second, 3 for the third). Notice it must not exceed the total number of elements of the constraint. (eg : not allowed to read the third element of a tangency).
` oCurrentElement`      An element of the constraint.  **Example:**     The following example reads the first element of a constraint

```VBScript
     Dim reference1 As Reference
     reference1=tangencyCst.GetConstraintElement( 1 )

```

### Sub **GetConstraintVisuLocation**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAnchorPoint`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oAnchorVector`)

   Returns the constraint visualisation location. When displayed on screen, the constraint is visualized as a dimension positioned close to the constrained geometric element(s). This method retrieves the data used to position this representation within the 3D space.

**Parameters:**

` oAnchorPoint`      A Safe Array made up of 3 doubles: X, Y, Z, representing the coordinates in model space of the point where the constraint value is displayed.
` oAnchorVector`      A Safe Array made up of 3 doubles : X, Y, Z, representing the vector normal to the plane onto which the constraint value is displayed.  **Example:**     The following example retrieves in `anchorPt` the anchor point of the `tangencyCst` tangency constraint:

```VBScript
     Dim anchorPoint(2)
     Dim anchorVector(2)
     tangencyCst.ConstraintVisuLocation anchorPoint,vectorPoint

```

### Func **IsInactive**( ) As boolean

   Indicates whether a constraint is suppressed from the update process. A suppressed constraint is not taken into account for the calculation of part or the product. The method returns True if the constraint is not active, False if the constraint is active. **Example:**     The following example returns in `isInactive` whether the `tangencyCst` constraint is suppressed from the update process:

```VBScript
     Set isInactive = tangencyCst.IsInactive

```

### Sub **SetConstraintElement**( long  `iElementNumber`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewElement`)

   Replaces an element of a constraint.

**Parameters:**

` iElementNumber`      The number of the element of the constraint to replace. (1 for the first element,2 for the second, 3 for the third).
` iNewElement`      A new element of the constraint.  **Example:**     The following example changes the second element of a constraint

```VBScript
     Dim reference1 As Reference
     tangencyCst.SetConstraintElement ( 2, reference1)

```

### Sub **SetConstraintVisuLocation**( double  `iNewX`,  double  `iNewY`,  double  `iNewZ`)

   Sets a new location for the constraint visualization.

**Parameters:**

` iNewX`      The new value for the constraint anchor point X coordinate
` iNewY`      The new value for the constraint anchor point Y coordinate
` iNewZ`      The new value for the constraint anchor point Z coordinate  **Example:**     The following example changes the anchor point coordinates to 10,0,0

```VBScript
     tangencyCst.SetConstraintVisuLocation 10,0,0

```

---

# Constraints (Collection)

**_A collection of all geometric constraints set on a part, a sketch, or a product._**
A constraint collection is created with default values for its properties (such as value, orientation, etc.). Use the constraint properties edition services to set them to appropriate values after constraint creation.

**See also:**      [Constraint](../MecModInterfaces/interface_Constraint_22634.md)

## Properties

### Property **BrokenConstraintsCount**( ) As long (Read Only)

   Returns the number of broken constraints from the Constraints collection.

**Example:**     The following example retrieves in `BknCstNum` the number of broken constraints from the `myListofConstraints` collection of constraints:

```VBScript
     BknCstNum = myListofConstraints.BrokenConstraintsCount

```

### Property **UnUpdatedConstraintsCount**( ) As long (Read Only)

   Returns the number of unupdated constraints from the Constraints collection.

**Example:**     The following example retrieves in `UnUpdCstNum` the number of unupdated constraints from the `myListofConstraints` collection of constraints:

```VBScript
     UnUpdCstNum = myListofConstraints.UnUpdatedConstraintsCount

```

Methods

### Func **AddBiEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to two geometric elements and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iFirstElem`      The first constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iSecondElem`      The second constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example adds the `NewCst` tangency constraint in a sketch, between the two circles `c1` and `c2` using the value 4 for `catCstTypeTangency`.

```VBScript
     Set newCst = skCstList.AddBiEltCst(4, c1, c2)

```

### Func **AddMonoEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to a single geometric element and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iElem`      The constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example creates the reference constraint `NewCst` to a part, stating that the `P1` point should remain fixed with respect to the part's origin elements using the value 0 for `catCstTypeReference`, and adds it to the `cstList` collection.

```VBScript
     Set NewCst = cstList.AddMonoEltCst(0, P1)

```

### Func **AddTriEltCst**( [CatConstraintType](../MecModInterfaces/enum_CatConstraintType_62511.md)  `iCstType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFirstElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSecondElem`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iThirdElem`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Creates a new constraint applying to three geometric elements and adds it to the Constraints collection.

**Parameters:**

` iCstType`      The constraint type
` iFirstElem`      The first constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iSecondElem`      The second constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md). ` iThirdElem`      The third constrained geometric element
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Boundary](../MecModInterfaces/interface_Boundary_14542.md).  **Example:**      This example adds `symCst` symmetry constraint in a part, stating that the cylinders `cyl1` and `cyl2` are symmetric with respect to the plane `symPlane` using the value 15 for `catCstTypeSymmetry`.

```VBScript
     Set symCst = prtCstList.AddTriEltCst(15, cyl1, cyl2, symPlane)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)

   Returns a constraint using its index or its name from the Constraints collection.

**Parameters:**

` iIndex`      The index or the name of the constraint to retrieve frm the collection of constraints. As a numerics, this index is the rank of the constraint in the collection. The index of the first constraint in the collection is 1, and the index of the last constraint is Count. As a string, it is the name you assigned to the constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved constraint  **Example:**      This example retrieves in `cst1` the first constraint in the collection and in `cst2` the constraint Constraint.2.

```VBScript
     Set cst1 = cstList.Item(1)
     Set cst2 = cstList.Item("Constraint.2")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a constraint from the Constraints collection.

**Parameters:**

` iIndex`      The index or the name of the constraint to remove from the Constraints collection. As a numerics, this index is the rank of the constraint in the collection. The index of the first constraint in the collection is 1, and the index of the last constraint is Count. As a string, it is the name you assigned to the constraint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last constraint in the collection.

```VBScript
     cstList.Remove(cstList.Count)

```

---

# CylindricalFace (Object)

**_2-D boundary with a cylindrical geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the lateral face of a cylinder. You will create a CylindricalFace object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewCircPattern](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewCircPattern) ). The lifetime of a CylindricalFace object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a shape to pattern and a cylindrical face, and creates a circular pattern of the shape. The cylindrical face specifies the rotation axis.

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select the shape to pattern
     InputObjectType(0)="SketchBasedShape"
     Status=Selection.SelectElement2(InputObjectType,"Select the shape to pattern",true)
     if (Status = "cancel") then Exit Sub
     Set Shape = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the cylindrical face
     InputObjectType(0)="CylindricalFace"
     Status=Selection.SelectElement2(InputObjectType,"Select the cylindrical face",true)
     if (Status = "cancel") then Exit Sub
     Set CylindricalFace = Selection.Item(1).Value
     Set RotationCenter = Document.Part.CreateReferenceFromName("")
     Set CircPattern = ShapeFactory.AddNewCircPattern(Shape,1,4,20.0,45.0,1,4,RotationCenter,CylindricalFace,True,0.0,True)
     Document.Part.Update

```

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

   Returns the direction of the cylindrical face axis

**Parameters:**

` oDirection[0]`      The X Coordinate of the axis direction
` oDirection[1]`      The Y Coordinate of the axis direction
` oDirection[2]`      The Z Coordinate of the axis direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the cylindrical face axis.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the axis origin
` oOrigin[1]`      The Y Coordinate of the axis origin
` oOrigin[2]`      The Z Coordinate of the axis origin

---

# Edge (Object)

**_1-D boundary._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a cylinder. You will create an Edge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewPointTangent](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewPointTangent) ). The lifetime of an Edge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) , [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md) , [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md) , [MonoDimFeatEdge](../MecModInterfaces/interface_MonoDimFeatEdge_44932.md) , [RectilinearMonoDimFeatEdge](../MecModInterfaces/interface_RectilinearMonoDimFeatEdge_136236.md) .

**Example:**      This example asks the end user to select a planar curve, whose plane is parallel to the XY plane. Then, it creates a point on the tangent to the curve in the X direction:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     Set HybridBodies = Document.Part.HybridBodies
     Set HybridBody = HybridBodies.Item("Geometrical Set.1")
     'We propose to the user that he select a planar curve whose plane is parallel to the XY plane
     InputObjectType(0)="Edge"
     Status=Selection.SelectElement2(InputObjectType,"Select a planar curve whose plane is parallel to the XY plane",true)
     if (Status = "cancel") then Exit Sub
     Set PlanarCurve = Selection.Item(1).Value
     Set HybridShapeDirection = HybridShapeFactory.AddNewDirectionByCoord(1.0,0.0,0.0)
     Set HybridShapePointTangent = HybridShapeFactory.AddNewPointTangent(PlanarCurve,HybridShapeDirection)
     HybridBody.AppendHybridShape HybridShapePointTangent
     Document.Part.InWorkObject = HybridShapePointTangent
     Document.Part.Update

```

---

# Face (Object)

**_2-D boundary._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the lateral face of cylinder. You will create a Face object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewFaceFillet](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewFaceFillet) ). The lifetime of a Face object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md) .

**Example:**      This example asks the end user to select two faces, and creates a face-face fillet on these faces:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select the first face
     InputObjectType(0)="Face"
     Status=Selection.SelectElement2(InputObjectType,"Select the first face",true)
     if (Status = "cancel") then Exit Sub
     Set FirstFace = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the second face
     InputObjectType(0)="Face"
     Status=Selection.SelectElement2(InputObjectType,"Select the second face",true)
     if (Status = "cancel") then Exit Sub
     Set SecondFace = Selection.Item(1).Value
     Set FaceFillet = ShapeFactory.AddNewFaceFillet(FirstFace,SecondFace,5.0)
     Document.Part.Update

```

---

# Factory (Object)

**_Abstract object gathering behaviours of all objects being a factory._**

---

# FixTogether (Object)

**_The object that manages a sequence of products or fixTogethers._**

It belongs to the [FixTogether](../MecModInterfaces/interface_FixTogether_26387.md) collection of a [Product](../ProductStructureInterfaces/interface_Product_11223.md).

## Properties

### Property **FixTogethersCount**( ) As long (Read Only)

   Returns the number of FixTogether entities in the FixTogether.

**Example:**     The following example retrieves in `fixTogethersCount` the number of FixTogethers of the `myFixTogether` FixTogether :

```VBScript
     fixTogethersCount = myFixTogether.FixTogethersCount

```

### Property **ProductsCount**( ) As long (Read Only)

   Returns the number of products fixed together in the FixTogether.

**Example:**     The following example retrieves in `productsCount` the number of products of the `myFixTogether` FixTogether :

```VBScript
     productsCount = myFixTogether.ProductsCount

```

Methods

### Sub **AddFixTogether**( [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)  `iFixTogether`)

   Add a fixTogether to a FixTogether. The fixTogether is fixed together with the products or fixTogethers already contained in the FixTogether.  **Example:**      The following example adds a FixTogether `fixTogether` in a FixTogether `myFixTogether`.

```VBScript
     myFixTogether.AddFixTogether(fixTogether)

```

### Sub **AddProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`)

   Add a product to a FixTogether. The product is fixed together with the products and fixTogethers already contained in the FixTogether.  **Example:**      The following example adds a Product `myProduct` in a FixTogether.

```VBScript
     myFixTogether.AddProduct(myProduct)

```

### Func **GetFixTogether**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

   Returns a FixTogether using its index or its name in the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to retrieve. As a numerics, this index is the rank of the FixTogether in the FixTogethers of the FixTogether. The index of the first FixTogether is 1, and the index of the last FixTogether is FixTogethersCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved FixTogether **Example:**      This example retrieves in `thisFixTogether` the fifth FixTogether and in `thatFixTogether` the FixTogether named `myFixTogether` in the FixTogethers of the FixTogether.

```VBScript
     Dim thisFixTogether As FixTogether
     Set thisFixTogether = myFixTogether.GetFixTogether(5)
     Dim thatFixTogether As FixTogether
     Set thatFixTogether = myFixTogether.GetFixTogether("myFixTogether")

```

### Func **GetProduct**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Returns a Product using its index or its name in the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the Product to retrieve. As a numerics, this index is the rank of the Product in the products of the FixTogether. The index of the first Product is 1, and the index of the last Product is ProductsCount. As a string, it is the name you assigned to the Product using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Product **Example:**      This example retrieves in `thisProduct` the fifth Product and in `thatProduct` the Product named `myProduct` in the products of the FixTogether.

```VBScript
     Dim thisProduct As Product
     Set thisProduct = myFixTogether.GetProduct(5)
     Dim thatProduct As Product
     Set thatProduct = myFixTogether.GetProduct("myProduct")

```

### Sub **RemoveFixTogether**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a FixTogether from the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to remove from the FixTogether. As a numerics, this index is the rank of the FixTogether in the FixTogethers of the FixTogether. The index of the first FixTogether is 1, and the index of the last FixTogether is FixTogethersCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last FixTogether of the FixTogether.

```VBScript
     fixTogether.RemoveFixTogether(fixTogether.FixTogethersCount)

```

### Sub **RemoveProduct**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Product from the FixTogether.

**Parameters:**

` iIndex`      The index or the name of the Product to remove from the FixTogether. As a numerics, this index is the rank of the Product in the products of the FixTogether. The index of the first Product is 1, and the index of the last Product is ProductsCount. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last Product of the FixTogether.

```VBScript
     fixTogether.RemoveProduct(fixTogether.ProductsCount)

```

---

# FixTogethers (Collection)

**_A collection of all the FixTogether objects contained in the product._**

## Methods

### Func **Add**( ) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

   Creates a new FixTogether and adds it to the FixTogethers collection.

**Returns:**      The created FixTogether  **Example:**      The following example creates a FixTogether `newFixTogether` in the FixTogether collection.

```VBScript
     Set newFixTogether = fixTogethers.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFixTogether](../MecModInterfaces/interface_FixTogether_26387.md)

   Returns a FixTogether using its index or its name from the FixTogethers collection.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to retrieve from the collection of FixTogether. As a numerics, this index is the rank of the FixTogether in the collection. The index of the first FixTogether in the collection is 1, and the index of the last FixTogether is Count. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved FixTogether **Example:**      This example retrieves in `thisFixTogether` the fifth FixTogether in the collection and in `thatFixTogether` the FixTogether named `MyFixTogether` in the FixTogether collection of the `product` product.

```VBScript
     Set fixTogetherColl = product.FixTogethers
     Set thisFixTogether = fixTogetherColl.Item(5)
     Set thatFixTogether = fixTogetherColl.Item("MyFixTogether")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a FixTogether from the FixTogethers collection.

**Parameters:**

` iIndex`      The index or the name of the FixTogether to remove from the FixTogethers collection. As a numerics, this index is the rank of the FixTogether in the collection. The index of the first FixTogether in the collection is 1, and the index of the last FixTogether is Count. As a string, it is the name you assigned to the FixTogether using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Example:**      This example removes the last FixTogether in the collection.

```VBScript
     fixTogetherColl.Remove(fixTogetherColl.Count)

```

---

# GeometricElements (Collection)

**_A collection of all geometric elements contained in a part or a sketch._**
Geometric elements are created with the 2D factory for the sketch and with the 3D factory for the part. Geometric elements thus created are then aggregated either in the sketch or as part of the geometric element collection.

**See also:**      [Factory2D](../SketcherInterfaces/interface_Factory2D_15860.md), [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAGeometricElement](../SketcherInterfaces/interface_GeometricElement_54654.md)

   Returns a geometric element using its index or its name from the GeometricElements collection.

**Parameters:**

` iIndex`      The index or the name of the geometric element to retrieve from the collection of geometric elements. As a numerics, this index is the rank of the geometric element in the collection. The index of the first geometric element in the collection is 1, and the index of the last geometric element is Count. As a string, it is the name you assigned to the geometric element using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved geometric element  **Example:**      This example retrieves the last item in the geometric element collection.

```VBScript
     Set lastCst = cstList.Item(cstList.Count)

```

---

# HybridBodies (Collection)

**_A collection of the HybridBody objects._**

## Methods

### Func **Add**( ) As [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)

   Creates a new hybrid body and adds it to the HybridBodies collection. This body becomes the current one

**Returns:**      The created body  **Example:**      The following example creates a body named `newHybridBody` in the hybrid body collection of the `rootPart` part in the `partDoc` part document. `NewPartBody` becomes the current body in `partDoc`.

```VBScript
     Set NewPartBody = rootPart.Bodies.AddPartBody()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)

   Returns a body using its index or its name from the Bodies collection.

**Parameters:**

` iIndex`      The index or the name of the hybrid body to retrieve from the collection of hybrid bodies. As a numerics, this index is the rank of the hybrid body in the collection. The index of the first hybrid body in the collection is 1, and the index of the last hybrid body is Count. As a string, it is the name you assigned to the hybrid body using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved hybrid body **Example:**      This example retrieves in `ThisHybridBody` the fifth hybrid body in the collection and in `ThatHybridBody` the hybrid body named `MyHybridBody` in the hybrid body collection of the `partDoc` part document.

```VBScript
     Set hybridBodyColl = partDoc.Part.HybridBodies
     Set ThisHybridBody = hybridBodyColl.Item(5)
     Set ThatHybridBody = hybridBodyColl.Item("MyHybridBody")

```

---

# HybridBody (Object)

**_The object is a hybrid body._**
The hybrid body manages a set of geometric elements, a set of hybrid shapes, a set of bodies and a set of hybrid bodies.
It belongs to the [HybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or @ref CATIABody or [HybridBody](../MecModInterfaces/interface_HybridBody_21378.md) object.

## Properties

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

   Returns the hybrid body's Bodies collection.

**Example:**     The following example returns in `bodyColl` the collection of bodies of the hybrid body `hybridBody` :

```VBScript
     Set bodyColl = hybridBody.Bodies

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

   Returns the list of geometrical elements included in the hybrid body.

**Returns:**      oGeometricElements The list of geometric elements in the hybrid body (@see CATIAGeometricElements
for more information).

**Example:**     The following example returns in `geometricElements` the list of
geometrical elements in the Hybrid body `hybridBody`:

```VBScript
     Dim geometricElements As GeometricElements
     Set geometricElements = hybridBody.**GeometricElements**

```

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

   Returns the hybrid body's HybridBodies collection.

**Example:**     The following example returns in `hybridBodyColl` the collection of hybrid bodies of the hybrid body `hybridBody` :

```VBScript
     Set hybridBodyColl = hybridBody.HybridBodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

   Returns the list of hybrid shapes included in the hybrid body.

**Returns:**      oHybridShapes The list of hybrid shapes in the hybrid body (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `hybridShapes` the list of
hybrid shapes in the hybrid body `hybridBody`:

```VBScript
     Dim hybridShapes As HybridShapes
     Set hybridShapes = hybridBody.**HybridShapes**

```

### Property **HybridSketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

   Returns the hybrid body's Sketches collection. These skectches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `skColl` the collection of independent sketches of a hybrid body :

```VBScript
     Set skColl = hybridBody.HybridSketches

```

Methods

### Sub **AppendHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

   Appends a hybrid shape to the hybrid body.

**Parameters:**

` iHybriShape`      The hybrid shape to append.  **Example:**      This example appends the hybrid shape `hybridShape` to the hybrid body `hybridBody`:

```VBScript
     hybridBody.AppendHybridShape (hybridShape)

```

---

# HybridShape (Object)

**_Represents the hybrid shape object._**

## Properties

### Property **Thickness**( ) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md) (Read Only)

   Returns the thickness of the hybrid shape.
The thickness is a CATIAHybridShapeThickness.

**Example:**     The following example returns the thickness `ExtrudeThickness` of the extrude `Extrude.1` as the origin point of the axis system `AxisSystem0`:

```VBScript
     Dim Extrude1 As AnyObject
     Set Extrude1 = HybridBody1.HybridShapes.Item  ( "Extrude.1" )
     Dim Thickness1 As HybridShapeThickness
     Set Thickness1 = Extrude1.Thickness

```

Methods

### Sub **AppendHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

   Appends a hybrid shape to another hybrid shape.

**Parameters:**

` iHybridShape`      The hybrid shape to append.  **Example:**      This example appends the hybrid shape `newHybridShape` to the hybrid shape `oldHybridShape`:

```VBScript
     oldHybridShape.AppendHybridShape (newHybridShape)

```

### Sub **Compute**( )

   Computes the result of the hybrid shape.

---

# HybridShapeInstance (Object)

**_The interface to access a CATIAHybridShapeInstance._**

## Properties

### Property **InputsCount**( ) As long (Read Only)

   Returns the number of Inputs.

**Example:**     The following example retrieves in `inputsCount` the number of Inputs of `hybridShapeInstance`:

```VBScript
     inputsCount = hybridShapeInstance.InputsCount

```

### Property **OutputsCount**( ) As long (Read Only)

   Returns the number of Outputs.

**Example:**     The following example retrieves in `outputsCount` the number of Outputs of `hybridShapeInstance`:

```VBScript
     outputsCount = hybridShapeInstance.OutputsCount

```

### Property **ParametersCount**( ) As long (Read Only)

   Returns the number of Parameters.

**Example:**     The following example retrieves in `parametersCount` the number of parameters of `hybridShapeInstance`:

```VBScript
     parametersCount = hybridShapeInstance.ParametersCount

```

Methods

### Func **GetInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets an input of a hybrid shape instance by its name.

**Parameters:**

` iName`      The name of the input of the hybrid shape instance

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = hybridShapeInstance.GetInput("Input1")
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Gets an input of a shape instance by its name. Use this method if you want to retrieve a Reference.

**Parameters:**

` iName`      The name of the input of the shape instance

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = shapeInstance.GetInput("Input1")
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputDataFromPosition**( long  `iPosition`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Gets an input of a hybrid shape instance from its position. Use this method if you want to retrieve a Reference.

**Parameters:**

` iPosition`      The position

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = hybridShapeInstance.GetInputFromPosition(2)
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets an input of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = hybridShapeInstance.GetInputFromPosition(2)
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetOutput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a Ouput by its name.

**Parameters:**

` iName`      The name of the output of the shape instance

**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
     Set output = shapeInstance.GetOuput("Output1")
     If TypeName(output)="Nothing" Then
          MsgBox "Output not found"
     End If

```

### Func **GetOutputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a Ouput from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
     Set output = shapeInstance.GetOuputFromPosition(2)
     If TypeName(output)="Nothing" Then
          MsgBox "Output not found"
     End If

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a parameter of a hybrid shape instance by its name.

**Parameters:**

` iName`      The name of the parameter of the hybrid shape instance

**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
     Set parameter = hybridShapeInstance.GetParameter("Parameter1")
     If TypeName(parameter)="Nothing" Then
          MsgBox "Parameter not found"
     End If

```

### Func **GetParameterFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a parameter of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
     Set parameter = hybridShapeInstance.GetParameterFromPosition(2)
     If TypeName(input)="Nothing" Then
           MsgBox "Parameter not found"
     End If

```

### Sub **PutInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iIndex`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iInput`)

   Defines an input of a hybrid shape instance.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the hybrid shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a hybrid shape instance The input will be a point and its name will be Input1.

```VBScript
     hybridShapeInstance.PutInput "Input1",point

```

### Sub **PutInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iInput`)

   Defines an input of a shape instance. Use this method if you want to set as input a Reference.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a shape instance The input will be a point and its name will be Input1.

```VBScript
     shapeInstance.PutInput "Input1",point

```

---

# HybridShapes (Collection)

**_The collection of the HybridShapes making up a body._**

## Methods

### Func **GetBoundary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

   Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)

   Returns a HybridShape using its index or its name from the HybridShapes collection.

**Parameters:**

` iIndex`      The index or the name of the HybridShape to retrieve from the collection of HybridShapes. As a numerics, this index is the rank of the HybridShape in the collection. The index of the first HybridShape in the collection is 1, and the index of the last HybridShape is
[Collection.Count](../System/interface_Collection_22150.htm#Count). As a string, it is the name you assigned to the HybridShape using the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved HybridShape  **Example:**      This example retrieves in `ThisHybridShape` the third HybridShape, and in `ThatHybridShape` the HybridShape named `MyHybridShape` in the HybridShape collection of the active document, supposed to be a part document.

```VBScript
     Set ThisHybridShape = CATIA.ActiveDocument.HybridShapes.Item(3)
     Set ThatHybridShape = CATIA.ActiveDocument.HybridShapes.Item("MyHybridShape")

```

---

# InstanceFactory (Object)

**_Represents the CATIAInstanceFactory._**

**Role** : This interface is used to create a new instance of a shape reference ([ShapeInstance](../MecModInterfaces/interface_ShapeInstance_35910.md) ) or a hybrid shape reference ( [HybridShapeInstance](../MecModInterfaces/interface_HybridShapeInstance_75602.md) ) in case of the instantiation of a `User Feature`.
It is also used to instantiate a `Power Copy` reference.

This interface contains two protocols of instantiation:

  * The first protocol is dedicated to `User Feature` instantiation only.
It is defined by a single method: AddInstance . It creates a shape or hybrid shape instance depending on the result of the `User Feature`.
Use this method when you want to perform only one instantiation of the reference. Read the document containing the `User Feature` reference and instantiate it.
As the document containing the reference is released from the session at the end of the instantiation, it is not recommmended to use this method if you want to perform several instantiations of the same reference in a loop.
In that case, prefer the second protocol of instantiation.
  * The second protocol is dedicated to both `User Feature` and `Power Copy` instantiations.
It is defined by several methods that must be called in order.

    * For `User Feature` instantiation, these methods are an alternative way of the AddInstance method.
It is recommended to use the second protocol to perform several instantiations of the same reference in a loop.

    * For `Power Copy` instantiation, it is the only way of instantiating a reference.

The instantiation process is composed of three major steps:

    1. The first step BeginInstanceFactory consists in initializing the [InstanceFactory](../MecModInterfaces/interface_InstanceFactory_48601.md) with the reference and the document where it is stored.
This step must be called once at the beginning whatever the number of instantiations are done.
    2. The second step is the instantiation itself: it is composed of five methods that must be called in the order.
This set of five methods can be called in a loop in order to make several instantiations.

       1. The method BeginInstantiate is used to initialize all data of the reference.
       2. The method PutInputData is used to set a value to any input of the reference.
       3. The method GetParameter is used to retrieve any parameter of the reference in order to modify its value.
       4. The method Instantiate is used to duplicate the reference. It returns the created instance when it does exist.
       5. The method EndInstantiate is used to indicate that the instantiation is done.
    3. The third step EndInstantiateFactory consists in ending the instantiation and cleaning the [InstanceFactory](../MecModInterfaces/interface_InstanceFactory_48601.md).
When doing several instantiations in a loop, this step must be called just once at the end of all instantiations.

## Methods

### Func **AddInstance**( [CATIABase](../System/interface_AnyObject_17321.md)  `iReference`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Creates a new instance of a shape or hybrid shape.

**Parameters:**

` iReference`      The reference shape or hybrid shape.  **Example:**      This example creates the instance `NewInstance` in the part.

```VBScript
     Set NewInstance = instanceFactory.AddInstance(reference)

```

### Sub **BeginInstanceFactory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNameOfReference`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNameOfDocument`)

   Initializes the instantiation process with the document containing the reference.

**Role** : Use this method to start instantiating a reference in the current document.
In that method, the document containing the reference is locked in session.
It will be unlocked in the last step EndInstanceFactory .

**Parameters:**

` iNameOfReference`      The name of the reference to be instantiated.
` iDocumentFileName`      The name of the file containing the document where to find the reference to be instantiated.  **Example:**      The following example initializes the factory with a document and a reference:

```VBScript
     InstanceFactory.BeginInstanceFactory"NameOfReference","c:\tmp\NameOfDocument.CATPart"

```

### Sub **BeginInstantiate**( )

   Initializes the data of the reference.

**Role** : This is the first method of the second step of instantiation.
It is used to initialize all data of the reference in the factory.

**Example:**      The following example shows how to initialize the factory:

```VBScript
     InstanceFactory.BeginInstantiate

```

### Sub **EndInstanceFactory**( )

   Ends the instantiation process.

**Role** : Use this method to end the instantiation process.
In that method the document containing the reference is unlocked and released from the session.

**Example:**      The following example shows how to end the instantiation:

```VBScript
     InstanceFactory.EndInstanceFactory

```

### Sub **EndInstantiate**( )

   Ends the instantiation of the reference.

**Role** : This is the fifth and last method of the second step of instantiation.
It is used to end the instantiation: after this step, all the links to the reference are broken.

**Example:**      The following example shows how to end the instantiation:

```VBScript
     InstanceFactory.EndInstantiate

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves a parameter of the reference by its name.

**Role** : This is the third method of the second step of instantiation.
This step is optional.
It is used to retrieve a parameter of the reference in order to change its value, using the `ValuateFromString` method of the `Parameter` interface.
It has to be called on each parameter whose value has to be changed.

**Parameters:**

` iName`      The name of the parameter.  **Example:**      The following example retrieves a parameter on the reference:

```VBScript
     Set parameter = InstanceFactory.GetParameter("Parameter1")

```

### Func **Instantiate**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Instantiates the reference in the current document.

**Role** : This is the fourth method of the second step of instantiation.
It is used to duplicate or instantiate the data of the reference.

  * In case of `Power Copy` instantiation, the data are duplicated and there is no created instance.
  * In case of `User Feature` instantiation, the data are instantiated and an instance is created and returned.

**Example:**      The following example instantiates the reference:

```VBScript
     Set Instance = InstanceFactory.Instantiate

```

### Sub **PutInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iInput`)

   Sets a value to an input of the reference.

**Role** : This is the second method of the second step of instantiation.
It is used to set a value to any input of the reference.
It has to be called on each input of the reference.

**Parameters:**

` iName`      The name of the input.
` iInput`      The element to set as the new value of the input.
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**      The following example sets a value to an input of the reference: The input is a point and its name is Input1.

```VBScript
     InstanceFactory.PutInputData "Input1",point1

```

---

# MonoDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is one dimensional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, in a part containing a Sketch which is made up of a circle arc and a spline, the circle arc. You will create a MonoDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewPointTangent](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewPointTangent) ). The lifetime of a MonoDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

---

# NotWireBoundaryMonoDimFeatVertex (Object)

**_0-D boundary belonging to a feature whose topological result is one dimensional, the boundary not beeing the extremity of the feature._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, in a part containing a Sketch which is made up of a circle arc and a spline, the vertex between the circle arc and the spline. You will create a NotWireBoundaryMonoDimFeatVertex object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator. The lifetime of a NotWireBoundaryMonoDimFeatVertex object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

---

# OrderedGeometricalSet (Object)

**_The object is an ordered geometrical set._**
The ordered geometrical set manages a set of hybrid shapes, a set of bodies and a set of ordered geometrical sets.
It belongs to the [OrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) collection of a [Part](../MecModInterfaces/interface_Part_3788.md) or [OrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md) object.

## Properties

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

   Returns the ordered geometrical set's Bodies collection.

**Example:**     The following example returns in `bodyColl` the collection of bodies of the ordered geometrical set `OrderedGeometricalSet1` :

```VBScript
     Set bodyColl = OrderedGeometricalSet1.Bodies

```

### Property **HybridShapes**( ) As [CATIAHybridShapes](../MecModInterfaces/interface_HybridShapes_30836.md) (Read Only)

   Returns the list of hybrid shapes included in the ordered geometrical set.

**Returns:**      oHybridShapes The list of hybrid shapes in the ordered geometrical set (@see CATIAHybridShapes
for more information).

**Example:**     The following example returns in `HybridShapes1` the list of
hybrid shapes in the ordered geometrical set`OrderedGeometricalSet1`:

```VBScript
     Dim HybridShapes1 As HybridShapes
     Set HybridShapes1 = OrderedGeometricalSet1.**HybridShapes**

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

   Returns the ordered geometrical set's OrderedGeometricalSets collection.

**Example:**     The following example returns in `OrderedGeometricalSetColl` the collection of ordered geometrical set of the ordered geometrical set `OrderedGeometricalSet1` :

```VBScript
     Set OrderedGeometricalSetColl = OrderedGeometricalSet1.OrderedGeometricalSets

```

### Property **OrderedSketches**( ) As [CATIASketches](../MecModInterfaces/interface_Sketches_14228.md) (Read Only)

   Returns the ordered geometrical set's Sketches collection. These sketches are independent from any shape, since they haven't yet been used to create shapes.

**Example:**     The following example returns in `sketchesCollection` the collection of independent sketches of an ordered geometrical set :

```VBScript
     Set sketchesCollection = OrderedGeometricalSet1.OrderedSketches

```

Methods

### Sub **InsertHybridShape**( [CATIAHybridShape](../MecModInterfaces/interface_HybridShape_25589.md)  `iHybridShape`)

   Inserts a hybrid shape to the ordered geometrical set.

**Parameters:**

` iHybridShape`      The hybrid shape to insert.  **Example:**      This example inserts the hybrid shape `HybridShape1` to the ordered geometrical set `OrderedGeometricalSet1`:

```VBScript
     OrderedGeometricalSet1.InsertHybridShape (HybridShape1)

```

---

# OrderedGeometricalSets (Collection)

**_A collection of the OrderedGeometricalSet objects._**

## Methods

### Func **Add**( ) As [CATIAOrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md)

   Creates a new ordered geometrical set and adds it to the OrderedGeometricalSets collection. Thisordered geometrical set becomes the current one

**Returns:**      The created ordered geometrical set  **Example:**      The following example creates a ordered geometrical set named `newOrderedGeometricalSet` in the ordered geometrical set collection of the `rootPart` part in the `partDoc` part document. `NewPartBody` becomes the in work object of `partDoc`.

```VBScript
     Set NewPartBody = rootPart.OrderedGeometricalSets.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAOrderedGeometricalSet](../MecModInterfaces/interface_OrderedGeometricalSet_92509.md)

   Returns a ordered geometrical set using its index or its name from the ordered geometrical set collection.

**Parameters:**

` iIndex`      The index or the name of the ordered geometrical set to retrieve from the collection of ordered geometrical sets. As a numerics, this index is the rank of the ordered geometrical set in the collection. The index of the first ordered geometrical set in the collection is 1, and the index of the last ordered geometrical set is Count. As a string, it is the name you assigned to the ordered geometrical set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved ordered geometrical set **Example:**      This example retrieves in `ThisOrderedGeometricalSet` the fifth ordered geometrical set in the collection and in `ThatOrderedGeometricalSet` the ordered geometrical set named `MyOrderedGeometricalSet` in the ordered geometrical set collection of the `partDoc` part document.

```VBScript
     Set orderedGeometricalSetColl = partDoc.Part.OrderedGeometricalSets
     Set ThisOrderedGeometricalSet = orderedGeometricalSetColl.Item(5)
     Set ThatOrderedGeometricalSet = orderedGeometricalSetColl.Item("MyOrderedGeometricalSet")

```

---

# OriginElements (Object)

**_Represents the part's 3D reference axis system._**
It allows an easy access to 3D reference axis system of a Part object thru the three planes XY, YZ, and ZX.
See [Part](../MecModInterfaces/interface_Part_3788.md) for parent object.

## Properties

### Property **PlaneXY**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the XY plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnXY` the XY plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnXY = partRoot.originElements.PlaneXY

```

### Property **PlaneYZ**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the YZ plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnYZ` the YZ plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnYZ = partRoot.originElements.PlaneYZ

```

### Property **PlaneZX**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the ZX plane of the part 3D reference axis system.

**Example:**     The following example returns in `plnZX` the ZX plane of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set plnZX = partRoot.originElements.PlaneZX

```

---

# Part (Object)

**_The root level object inside a PartDocument object._**

**Role** : It aggregates all the objects making up the part document.
It provides many factories and collections. The collections list only the direct children of the part. [Selection.Search](../InfInterfaces/interface_Selection_18040.htm#Search) allows to get all objects of one type.

**See also:**      [PartDocument](../MecModInterfaces/interface_PartDocument_31472.md)

## Properties

### Property **AnnotationSets**( ) As [CATIACollection](../System/interface_Collection_22150.md) (Read Only)

   Returns the collection object containing the annotation sets. All the annotation sets that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `annotationSets` the annotation sets of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim annotationSets As AnnotationSets
     Set annotationSets = partRoot.AnnotationSets

```

### Property **AxisSystems**( ) As [CATIAAxisSystems](../MecModInterfaces/interface_AxisSystems_27251.md) (Read Only)

   Returns the collection object containing the coordinate systems. All the coordinate systems that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `axisSystems` the coordinate systems of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim axisSystems As AxisSystems
     Set axisSystems = partRoot.AxisSystems

```

### Property **Bodies**( ) As [CATIABodies](../MecModInterfaces/interface_Bodies_7994.md) (Read Only)

   Returns the collection object containing the bodies that are direct children of the part.
It does not return all the bodies of the part, particularly the bodies in a boolean operation.

**Example:**     The following example returns in `bodiesColl` the collection of the bodies of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set bodiesColl = partRoot.Bodies

```

### Property **Constraints**( ) As [CATIAConstraints](../MecModInterfaces/interface_Constraints_27490.md) (Read Only)

   Returns the collection object containing the part constraints. Only 3D constraints are concerned here, 2D constraints are managed in sketches.

**Example:**     The following example returns in `csts` the constraints of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set csts = partRoot.Constraints

```

### Property **Density**( ) As double (Read Only)

   Returns the part density.

**Example:**     The following example displays the density of the part:

```VBScript
     Set partRoot = partDoc.Part
     MsgBox "The density is " & partRoot.Density

```

### Property **GeometricElements**( ) As [CATIAGeometricElements](../MecModInterfaces/interface_GeometricElements_62160.md) (Read Only)

   Returns the collection object containing the part geometrical elements. Only 3D elements are concerned here, 2D elements are managed in sketches. The origin elements are also accessible thru that collection.

**Example:**     The following example returns in `geomElts` the 3D elements of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set geomElts = partRoot.GeometricElements

```

### Property **HybridBodies**( ) As [CATIAHybridBodies](../MecModInterfaces/interface_HybridBodies_30456.md) (Read Only)

   Returns the collection object containing the hybrid bodies that are direct children of the part.

**Example:**     The following example returns in `hybridBodiesColl` the collection of hybrid bodies of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set hybridBodiesColl = partRoot.HybridBodies

```

### Property **HybridShapeFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

   Returns the part hybrid shape factory. It allows the creation of hybrid shapes in the part.

**Example:**     The following example returns in `hybridShapeFact` the hybrid shape factory of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim hybridShapeFact As Factory
     Set hybridShapeFact = partRoot.HybridShapeFactory

```

### Property **InWorkObject**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Returns or sets the in work object of the part. The in work object is the object after which a new object is added.

**Example:**

```VBScript
     Set partRoot = partDoc.Part
     Set partRoot.InWorkObject = cylindricPad
     If ( partRoot.InWorkObject <> cylindricPad ) Then
          MsgBox "There is a big problem"
     End If

```

### Property **MainBody**( ) As [CATIABody](../MecModInterfaces/interface_Body_3736.md)

   Returns or sets the main body of the part.

**Example:**     The following example returns the main body of the part of the current document.

```VBScript
     Dim mainBody As Body
     Set mainBody=CATIA.ActiveDocument.Part.MainBody

```

### Property **OrderedGeometricalSets**( ) As [CATIAOrderedGeometricalSets](../MecModInterfaces/interface_OrderedGeometricalSets_102240.md) (Read Only)

   Returns the collection object containing the ordered geometrical sets of the part.

**Example:**     The following example returns in `ogsColl` the collection of ordered geometrical sets of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set ogsColl = partRoot.OrderedGeometricalSets

```

### Property **OriginElements**( ) As [CATIAOriginElements](../MecModInterfaces/interface_OriginElements_42458.md) (Read Only)

   Returns the object defining the part 3D reference axis system.

**Example:**     The following example returns in `originElts` the origin of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set originElts = partRoot.OriginElements

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection object containing the part parameters. All the parameters that are aggregated in the different objects of the part might be accessed thru that collection.

**Example:**     The following example returns in `params` the parameters of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim params As Parameters
     Set params = partRoot.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

   Returns the collection object containing the part relations. All the relations that are used to valuate the parameters of the part might be accessed thru that collection.

**Example:**     The following example returns in `rels` the relations of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Set rels = partRoot.Relations

```

### Property **ShapeFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

   Returns the part shape factory. It allows the creation of shapes in the part.

**Example:**     The following example returns in `shapeFact` the shape factory of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim shapeFact As Factory
     Set shapeFact = partRoot.ShapeFactory

```

### Property **SheetMetalFactory**( ) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md) (Read Only)

   Returns the sheet metal factory of the part. It allows the creation of sheet metal elements in the part.

**Example:**     The following example returns in `sheetMetalFact` the sheet metal factory of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim sheetMetalFact As Factory
     Set sheetMetalFact = partRoot.SheetMetalFactory

```

### Property **SheetMetalParameters**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the sheet metal parameters of the part.

**Example:**     The following example returns in `sheetMetalParm` the sheet metal parameters of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim sheetMetalParm As SheetMetalParameters
     Set sheetMetalFact = partRoot.SheetMetalParameters

```

### Property **UserSurfaces**( ) As [CATIACollection](../System/interface_Collection_22150.md) (Read Only)

   Returns the collection object containing the user surfaces. All the user surfaces that are aggregated in the part might be accessed thru that collection.

**Example:**     The following example returns in `userSurfaces` the user surfaces of the `partRoot` part from the `partDoc` part document:

```VBScript
     Set partRoot = partDoc.Part
     Dim userSurfaces As UserSurfaces
     Set userSurfaces = partRoot.UserSurfaces

```

Methods

### Sub **Activate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Unsuppresses an object for the update process. A unsuppressed object is again taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to unsuppress for the update process  **Example:**     The following example unsuppresses the `pad1` pad:

```VBScript
     Set partRoot = partDoc.Part
     Set pad1 = partRoot.FindObjectByName("Pad.1")
     partRoot.Activate(pad1)

```

### Func **CreateReferenceFromBRepName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iObjectContext`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from a GenericNaming label. This allows manipulation of B-Rep (Type Functinal and Relimited) that are not easy to access.

**Parameters:**

` iLabel`      The GenericNaming identification for an object. This is a cryptic form for "the edge surrounded by the face extruded from line.12 of sketch.4 and the face...")
` iObjectContext`      The Object Context of Resolution This is the feature used for label GenericNaming resolution

**Returns:**      The reference to a B-Rep sub-element such a face or an edge  
### Func **CreateReferenceFromName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from a GenericNaming label. This allows manipulation of B-Rep (type Functional Only) that are not easy to access.

**Parameters:**

` iLabel`      The GenericNaming identification for an object. This is a cryptic form for "the edge surrounded by the face extruded from line.12 of sketch.4 and the face...")

**Returns:**      The reference to a B-Rep sub-element such a face or an edge  
### Func **CreateReferenceFromObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from a operator. Use of reference allows a uniform handling of B-Rep and non B-Rep objects.

**Parameters:**

` iObject`      The geometric object to be referenced. It can be a plane, a line or a point.

**Returns:**      The reference to the object. This way, a direction can be either an edge of a pad or a 3D line.  
### Func **FindObjectByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iObjName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Finds an object that is not a collection by its name. Scan in depth among all the direct and indirect children (expensive, but hard to escape).

**Parameters:**

` iObjName`      The name to be searched

**Returns:**      The object, if found  **Example:**     The following example tests if the object was found:

```VBScript
     Set partRoot = partDoc.Part
     Set obj = partRoot.FindObjectByName("Wrong name")
     If TypeName(obj)="Nothing" Then
          MsgBox "Object not found"
     End If

```

### Func **GetCustomerFactory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFactoryIID`) As [CATIAFactory](../MecModInterfaces/interface_Factory_11318.md)

   Returns a customer factory from a code string defined by the customer. It allows a customer to define its own factory to create its own objects.

**Parameters:**

` iFactoryIID`      The code name of the factory

### Sub **Inactivate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Suppresses an object from being updated. A suppressed object is not taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to suppress from being updated  **Example:**     The following example suppresses the `pad1` pad from being updated:

```VBScript
     Set partRoot = partDoc.Part
     Set pad1 = partRoot.FindObjectByName("Pad.1")
     partRoot.Inactivate(pad1)

```

### Func **IsInactive**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As boolean

   Indicates whether an object is deactivated. A deactivated object is not taken into account for the calculation of the part.

**Parameters:**

` iObject`      The object to examine  **Example:**     The following example returns in `isInactive` whether the `pad1` pad is deactivated:

```VBScript
     Set partRoot = partDoc.Part
     Set pad1 = partRoot.FindObjectByName("Pad.1")
     isInactive = partRoot.IsInactive(pad1)

```

### Func **IsUpToDate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As boolean

   Indicates whether an object needs to be updated. An object which is not up-to-date has not be calculated with the last specifications.

**Parameters:**

` iObject`      The object to examine  **Example:**     The following example returns in `isuptodate` whether the `pad1` pad is up-to-date:

```VBScript
     Set partRoot = partDoc.Part
     Set pad1 = partRoot.FindObjectByName("Pad.1")
     isuptodate = partRoot.IsUpToDate(pad1)

```

### Sub **Update**( )

   Updates of the part result with respect to its specifications. Any composing specification that hasn't its result up-to-date will recompute it, thus propagating changes to the whole part.

**Example:**     The following example update the part:

```VBScript
     Set partRoot = partDoc.Part
     partRoot.Update

```

### Sub **UpdateObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`)

   Updates an object with respect to its specifications. Any composing specification of the object that hasn't its result up-to-date will recompute it, thus propagating changes to the object.

**Parameters:**

` iObject`      The object to be updated  **Example:**     The following example updates Pad.1:

```VBScript
     Set partRoot = partDoc.Part
     Set pad1 = partRoot.FindObjectByName("Pad.1")
     partRoot.UpdateObject(pad1)

```

---

# PartDocument (Object)

**_Represents the Document object for parts._**

**Role** : When a PartDocument object is created, a Part object is also created. This Part object is the root object of the Part structure.

A reference Product object is also created in each PartDocument. It is used to access Publications, PartNumber.

**See also:**      [Product](../ProductStructureInterfaces/interface_Product_11223.md), [Part](../MecModInterfaces/interface_Part_3788.md)

## Properties

### Property **Part**( ) As [CATIAPart](../MecModInterfaces/interface_Part_3788.md) (Read Only)

   Returns the root Part object from the current part document.

**Example:**     The following example retrieves in `RootPart` the root Part object of the active document, assumed to be a part document:

```VBScript
     Set RootPart = CATIA.ActiveDocument.Part

```

### Property **Product**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the root Product object from the current part document.

**Example:**     The following example retrieves in `RootProd` the root Product object of the active document, assumed to be a part document:

```VBScript
     Set RootProd = CATIA.ActiveDocument.Part

```

---

# PartInfrastructureSettingAtt (Object)

**_Setting controller for all the Part Infrastructure property tab pages._**

**Role** : This interface is implemented by a component representing the controller for the Part Infrastructure settings.

## Properties

### Property **AlsoDeleteExclusiveParents**( ) As boolean

   Returns or sets the "AlsoDeleteExclusiveParents" parameter.

**Role:** This parameter defines if a exclusive parents of an object will also be deleted when the object is deleted.
This option is effective only when the "Deletion warning box" is displayed.

**Parameters:**

` oDeleted`      Current "AlsoDeleteExclusiveParents" parameter's value:

  * TRUE or 1 if exclusive parents are also deleted,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **AxisSystemSize**( ) As short

   Returns or sets the "AxisSystemSize" parameter.

**Role:** This parameter determines the size of axis systems.

**Parameters:**

` oSize`      Current size of axis systems

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **BodiesUnderOperationsInTree**( ) As boolean

   Returns or sets the "BodiesUnderOperationsInTree" parameter.

**Role:** This parameter determines if a Body node is displayed when it is being aggregated under a boolean operation (Add, Assemble, Remove, Intersect, Union Trim).
Its value can be changed even after a boolean operation has been created. Simply collapse and expand the federating boolean operation node for the specification tree to be refreshed.

**Parameters:**

` oNodeDisplayed`      Current "BodiesUnderOperationsInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ColorSynchronizationEditability**( ) As boolean

   Returns or sets the "ColorSynchronizationEditability" parameter.

**Role:** This parameter determines whether color synchronization property on Part is editable or not.
Color synchronization editability defines whether the property of synchronization on Part can be interactively editable If it is valuated to 1, user will be able to interactively modify the Part property of Color management tab for synchronization. If it is defined to 0, user will not be able to interactively modify the Part property of Color management tab for synchronization. This option cannot be changed after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorSynchronizationEditability" parameter's value:

  * TRUE or 1, Part property option for synchronization is editable
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ColorSynchronizationMode**( ) As boolean

   Returns or sets the "ColorSynchronizationMode" parameter.

**Role:** This parameter determines color synchronization mode for imported features in a part.
Color synchronization mode defines whether the imported feature, created through copy/paste as result with link mechanism, copies reference feature colors on its faces or not. If it is valuated to 1, synchronization will be effective and referece feature colors will be reported. If it is defined to 0, nothing will be copied(default mode). This option cannot be changed after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorSynchronizationMode" parameter's value:

  * TRUE or 1 if reference feature colors are reported on imported feature,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ConstraintsInGeometry**( ) As boolean

   Returns or sets the "ConstraintsInGeometry" parameter.

**Role:** This parameter enables constraints to be visualized in the 3D view.

**Parameters:**

` oDisplayed`      Current "Display constraints within 3D" parameter's value:

  * TRUE or 1 if constraints are displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ConstraintsNodeInTree**( ) As boolean

   Returns or sets the "ConstraintsNodeInTree" parameter.

**Role:** This parameter determines if a node called "Constraints" is created to contain all constraints.
Its value can be changed even after constraints have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ConstraintsNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ContextualFeaturesSelectableAtCreation**( ) As boolean

   Returns or sets the "ContextualFeaturesSelectableAtCreation" parameter.

**Role:** This parameter determines if contextual features can be selected during the creation of an other feature.

**Parameters:**

` oContextualFeaturesSelectable`      Current "ContextualFeaturesSelectableAtCreation" parameter's value:

  * TRUE or 1 if contextual features can be selected,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **DeleteWarningBox**( ) As boolean

   Returns or sets the "DeleteWarningBox" parameter.

**Role:** This parameter defines if a warning box is displayed when an element is deleted.

**Parameters:**

` oDisplayed`      Current "DeleteWarningBox" parameter's value:

  * TRUE or 1 if a warning box is displayed at deletion,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **DisplayGeometryAfterCurrent**( ) As boolean

   Returns or sets the "DisplayGeometryAfterCurrent" parameter.

**Role:** This parameter enables to visualize in the 3D features after the current object in O.G.S. and "solid and surface set".

**Parameters:**

` oDisplayed`      Current "DisplayGeometryAfterCurrent" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExpandSketchBasedFeaturesNodeAtCreation**( ) As boolean

   Returns or sets the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role:** This parameter determines if specification tree nodes for sketch-based features are expanded when such elements are created. This will enable to view their sketch node.

**Parameters:**

` oNodeExpanded`      Current "ExpandSketchBasedFeaturesNodeAtCreation" parameter's value:

  * TRUE or 1 if such nodes are expanded,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesAsVisible**( ) As boolean

   Returns or sets the "ExternalReferencesAsVisible" parameter.

**Role:** This parameter defines if an external reference is visible when being created.

**Parameters:**

` oVisible`      Current "ExternalReferencesAsVisible" parameter's value:

  * TRUE or 1 if external references are visible when being created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesAssemblyRootContext**( ) As boolean

   Returns or sets the "ExternalReferencesAssemblyRootContext" parameter.

**Role:** This parameter defines if external references are created using the root context of an assembly.

**Parameters:**

` oRootContextUsed`      Current "ExternalReferencesAssemblyRootContext" parameter's value:

  * TRUE or 1 if external references are created using the root context of an assembly,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ExternalReferencesNodeInTree**( ) As boolean

   Returns or sets the "ExternalReferencesNodeInTree" parameter.

**Role:** This parameter determines if a node called "External Reference" is created to contain all linked external references.
Its value can be changed even after linked external references have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ExternalReferencesNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **HybridDesignMode**( ) As boolean

   Returns or sets the "HybridDesignMode" parameter.

**Role:** This parameter determines if hybrid design is possible inside Part Bodies and bodies.
This option can be changed even after a document has been opened.

**Parameters:**

` oHybridDesign`      Current "HybridDesignMode" parameter's value:

  * TRUE or 1 if hybrid design is enabled,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **KnowledgeInHybridDesignMode**( ) As boolean

   Returns or sets the "KnowledgeInHybridDesignMode" parameter.

**Role:** This parameter determines if knowledge features (formulas, parameters, rules, ...) can be located inside ordered sets.
This option can be changed even after a document has been opened.

**Parameters:**

` oKnowledgeInHybridDesign`      Current "KnowledgeInHybridDesignMode" parameter's value:

  * TRUE or 1 if hybrid design is enabled,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferences**( ) As boolean

   Returns or sets the "LinkedExternalReferences" parameter.

**Role:** This parameter enables creation of external references with links.

**Parameters:**

` oWithLink`      "LinkedExternalReferences" parameter's value:

  * TRUE or 1 if external references are created with links,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferencesOnlyOnPublication**( ) As boolean

   Returns or sets the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role:** This parameter restricts the creation of external references with links to only published elements.
This option is only used when external references are created with link.

**Parameters:**

` oOnlyForPublishedElements`      Current "LinkedExternalReferencesOnlyOnPublication" parameter's value:

  * TRUE or 1 if external references with link are only allowed on published elements,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **LinkedExternalReferencesWarningAtCreation**( ) As boolean

   Returns or sets the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role:** This parameter defines if a warning panel is displayed each time an external reference with llink is created. The panel enables the user to decide whether the link will be kept or not.
This option is only used when external references are created with link.

**Parameters:**

` oWarningAtCreation`      Current "LinkedExternalReferencesWarningAtCreation" parameter's value:

  * TRUE or 1 if a panel is displayed upon external references with link creation,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NamingMode**( ) As [CatPartElementsNamingMode](../MecModInterfaces/enum_CatPartElementsNamingMode_128721.md)

   Returns or sets the "NamingMode" parameter.

**Role:** This parameter determines how an element can be named through Edit/Properties or any operation creating a feature (Copy-Paste, etc.).
When this option is being changed, it only affects elements whose name is modified afterwards.

**Parameters:**

` oNamingMode`      Current "NamingMode" parameter's value:

  * `catNoCheck` when naming is rule-free,
  * `catNamingCheckUnderSameNode` when 2 elements cannot have the same name under the same node,
  * `catNamingCheckWithinUIActiveObject` when 2 elements cannot have the same name within a defined UIActiveObject.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWith3DSupport**( ) As boolean

   Returns or sets the "NewWith3DSupport" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with 3D working support.

**Parameters:**

` o3DSupportCreated`      Current "NewWith3DSupport" parameter's value:

  * TRUE or 1 if a 3D support is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithAxisSystem**( ) As boolean

   Returns or sets the "NewWithAxisSystem" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with an Axis System.

**Parameters:**

` oAxisSystemCreated`      Current "NewWithAxisSystem" parameter's value:

  * TRUE or 1 if an axis system is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithGS**( ) As boolean

   Returns or sets the "NewWithGS" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with a Geometrical Set.

**Parameters:**

` oGSCreated`      Current "NewWithGS" parameter's value:

  * TRUE or 1 if a G.S. is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithOGS**( ) As boolean

   Returns or sets the "NewWithOGS" parameter.

**Role:** This parameter determines if a new .CATPart document will be created with an Ordered Geometrical Set.

**Parameters:**

` oOGSCreated`      Current "NewWithOGS" parameter's value:

  * TRUE or 1 if an O.G.S. is created,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **NewWithPanel**( ) As boolean

   Returns or sets the "NewWithPanel" parameter.

**Role:** This parameter determines if a dedicated '_New Part_ ' panel is displayed when createing a new .CATPart document.

**Parameters:**

` oNewPartPanelDisplayed`      Current "NewWithPanel" parameter's value:

  * TRUE or 1 if the 'New Part' panel is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **OnlyCurrentOperatedSolidSetInGeometry**( ) As boolean

   Returns or sets the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role:** This parameter enables to visualize in the 3D only the current operated body's feature (operated means being aggregated in a boolean operation), as well as all other bodies and sets direcly inserted under the Part feature.

**Parameters:**

` oDisplayed`      Current "Display in 3D only current operated solid set" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **OnlyCurrentSolidSetInGeometry**( ) As boolean

   Returns or sets the "OnlyCurrentSolidSetInGeometry" parameter.

**Role:** This parameter enables to visualize in the 3D only the current operated body's feature (operated means being aggregated in a boolean operation), as well as all other bodies and sets direcly inserted under the Part feature.

**Parameters:**

` oDisplayed`      Current "Display in 3D only current operated solid set" parameter's value:

  * TRUE or 1 if such is the visualization,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ParametersNodeInTree**( ) As boolean

   Returns or sets the "ParametersNodeInTree" parameter.

**Role:** This parameter determines if a node called "Parameters" is created to contain all Knowledgeware parameters.
Its value can be changed even after parameters have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "ParametersNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **PublishTopologicalElements**( ) As boolean

   Returns or sets the "PublishTopologicalElements" parameter.

**Role:** This parameter defines if topological elements (faces, edges, vertices, axes extremities) can be published.

**Parameters:**

` oTopologyAllowed`      Current "PublishTopologicalElements" parameter's value:

  * TRUE or 1 if topological elements can be used for publication,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **RelationsNodeInTree**( ) As boolean

   Returns or sets the "RelationsNodeInTree" parameter.

**Role:** This parameter determines if a node called "Relations" is created to contain all Knowledgeware relations (for instance formulas).
Its value can be changed even after parameters have been created. The result is that the specification tree node display status will be affected.

**Parameters:**

` oNodeDisplayed`      Current "RelationsNodeInTree" parameter's value:

  * TRUE or 1 if such a node is displayed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **ReplaceOnlyAfterCurrent**( ) As boolean

   Returns or sets the "ReplaceOnlyAfterCurrent" parameter.

**Role:** This parameter defines if the replace operation can only apply to components located after the current object.

**Parameters:**

` oOnlyAfterCurrent`      Current "ReplaceOnlyAfterCurrent" parameter's value:

  * TRUE or 1 if the replace operation can only apply to components located after the current object,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **SurfaceElementsLocation**( ) As [CatPartSurfaceElementsLocation](../MecModInterfaces/enum_CatPartSurfaceElementsLocation_188182.md)

   Returns or sets the "SurfaceElementsLocation" parameter.

**Role:** This parameter determines where wireframe and surface elements are created when hybrid design is active.
This option can be changed when hybrid design mode is not active (but useless then), and also even after a document has been opened.

**Parameters:**

` oLocation`      Current "SurfaceElementsLocation" parameter's value:

  * `catPartBodyLocation` when elements are created within a PartBody,
  * `catXGSLocation` when elements are created within a G.S. or an O.G.S..

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **TrueColorMode**( ) As boolean

   Returns or sets the "ColorInheritanceMode" parameter.

**Role:** This parameter determines color inheritance mode for absorbing features in a part.
Color inheritance mode defines which mode of propagation will be used to set color on an absorbing feature. If it is valuated to 1, absorbing feature will inherit colors from all their input. If it is defined to 0, absorbing features will inherit colors from their main input only (default mode). This option can be changed even after a document has been opened.

**Parameters:**

` oActivated`      Current "ColorInheritanceMode" parameter's value:

  * TRUE or 1 if absorbing features inherit from all their inputs,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateElementsRefreshed**( ) As boolean

   Returns or sets the "UpdateElementsRefreshed" parameter.

**Role:** This parameter determines if elements visualization has to be refreshed individually during update tasks.

**Parameters:**

` oElementsRefreshed`      Current "UpdateElementsRefreshed" parameter's value:

  * TRUE or 1 if elements visualization is refreshed,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateLinkedExternalReferences**( ) As boolean

   Returns or sets the "UpdateLinkedExternalReferences" parameter.

**Role:** This parameter determines if update tasks also apply to linked external references.

**Parameters:**

` oExternalReferencesUpdated`      Current "UpdateLinkedExternalReferences" parameter's value:

  * TRUE or 1 if the update tasks apply to linked external references,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateMode**( ) As [CatPartUpdateMode](../MecModInterfaces/enum_CatPartUpdateMode_59539.md)

   Returns or sets the "UpdateMode" parameter.

**Role:** This parameter determines how the update of a .CATPart document is conducted.

**Parameters:**

` oUpdateMode`      Current update mode:

  * `catAutomaticUpdate` when update is automatically launched,
  * `catManualUpdate` when update has to be launched manually.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  
### Property **UpdateStoppedOnError**( ) As boolean

   Returns or sets the "UpdateStoppedOnError" parameter.

**Role:** This parameter determines if update tasks stop on the first detected error.

**Parameters:**

` oStoppedOnError`      Current "UpdateStoppedOnError" parameter's value:

  * TRUE or 1 if update tasks stop,
  * FALSE or 0 otherwise.

**Returns:**      S_OK if the parameter is correctly retrieved, E_FAIL otherwise.  Methods

### Func **GetAlsoDeleteExclusiveParentsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "AlsoDeleteExclusiveParents" parameter.

**Role** :Retrieves the state of the "AlsoDeleteExclusiveParents" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAxisSystemSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "AxisSystemSize" parameter.

**Role** :Retrieves the state of the "AxisSystemSize" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetBodiesUnderOperationsInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "BodiesUnderOperationsInTree" parameter.

**Role** :Retrieves the state of the "BodiesUnderOperationsInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetColorSynchronizationEditabilityInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorSynchronizationEditability" parameter.

**Role** :Retrieves the state of the "ColorSynchronizationEditability" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetColorSynchronizationModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorSynchronizationMode" parameter.

**Role** :Retrieves the state of the "ColorSynchronizationMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetConstraintsInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ConstraintsInGeometry" parameter.

**Role** :Retrieves the state of the "ConstraintsInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetConstraintsNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ConstraintsNodeInTree" parameter.

**Role** :Retrieves the state of the "ConstraintsNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetContextualFeaturesSelectableAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ContextualFeaturesSelectableAtCreation" parameter.

**Role** :Retrieves the state of the "ContextualFeaturesSelectableAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDeleteWarningBoxInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "DeleteWarningBox" parameter.

**Role** :Retrieves the state of the "DeleteWarningBox" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayGeometryAfterCurrentInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "DisplayGeometryAfterCurrent" parameter.

**Role** :Retrieves the state of the "DisplayGeometryAfterCurrent" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExpandSketchBasedFeaturesNodeAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role** :Retrieves the state of the "ExpandSketchBasedFeaturesNodeAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesAsVisibleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesAsVisible" parameter.

**Role** :Retrieves the state of the "ExternalReferencesAsVisible" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesAssemblyRootContextInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesAssemblyRootContext" parameter.

**Role** :Retrieves the state of the "ExternalReferencesAssemblyRootContext" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetExternalReferencesNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ExternalReferencesNodeInTree" parameter.

**Role** :Retrieves the state of the "ExternalReferencesNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHybridDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "HybridDesignMode" parameter.

**Role** :Retrieves the state of the "HybridDesignMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetKnowledgeInHybridDesignModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "KnowledgeInHybridDesignMode" parameter.

**Role** :Retrieves the state of the "KnowledgeInHybridDesignMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferences" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferences" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesOnlyOnPublicationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferencesOnlyOnPublication" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLinkedExternalReferencesWarningAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role** :Retrieves the state of the "LinkedExternalReferencesWarningAtCreation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNamingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NamingMode" parameter.

**Role** :Retrieves the state of the "NamingMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWith3DSupportInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWith3DSupport" parameter.

**Role** :Retrieves the state of the "NewWith3DSupport" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithAxisSystemInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithAxisSystem" parameter.

**Role** :Retrieves the state of the "NewWithAxisSystem" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithGSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithGS" parameter.

**Role** :Retrieves the state of the "NewWithGS" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithOGSInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithOGS" parameter.

**Role** :Retrieves the state of the "NewWithOGS" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetNewWithPanelInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "NewWithPanel" parameter.

**Role** :Retrieves the state of the "NewWithPanel" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOnlyCurrentOperatedSolidSetInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role** :Retrieves the state of the "OnlyCurrentOperatedSolidSetInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOnlyCurrentSolidSetInGeometryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "OnlyCurrentSolidSetInGeometry" parameter.

**Role** :Retrieves the state of the "OnlyCurrentSolidSetInGeometry" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetParametersNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ParametersNodeInTree" parameter.

**Role** :Retrieves the state of the "ParametersNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPublishTopologicalElementsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "PublishTopologicalElements" parameter.

**Role** :Retrieves the state of the "PublishTopologicalElements" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRelationsNodeInTreeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "RelationsNodeInTree" parameter.

**Role** :Retrieves the state of the "RelationsNodeInTree" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetReplaceOnlyAfterCurrentInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ReplaceOnlyAfterCurrent" parameter.

**Role** :Retrieves the state of the "ReplaceOnlyAfterCurrent" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSurfaceElementsLocationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "SurfaceElementsLocation" parameter.

**Role** :Retrieves the state of the "SurfaceElementsLocation" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTrueColorModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "ColorInheritanceMode" parameter.

**Role** :Retrieves the state of the "ColorInheritanceMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateElementsRefreshedInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateElementsRefreshed" parameter.

**Role** :Retrieves the state of the "UpdateElementsRefreshed" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateLinkedExternalReferencesInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateLinkedExternalReferences" parameter.

**Role** :Retrieves the state of the "UpdateLinkedExternalReferences" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateMode" parameter.

**Role** :Retrieves the state of the "UpdateMode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateStoppedOnErrorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "UpdateStoppedOnError" parameter.

**Role** :Retrieves the state of the "UpdateStoppedOnError" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAlsoDeleteExclusiveParentsLock**( boolean  `iLocked`)

   Locks or unlocks the "AlsoDeleteExclusiveParents" parameter.

**Role** :Locks or unlocks the "AlsoDeleteExclusiveParents" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAxisSystemSizeLock**( boolean  `iLocked`)

   Locks or unlocks the "AxisSystemSize" parameter.

**Role** :Locks or unlocks the "AxisSystemSize" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetBodiesUnderOperationsInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "BodiesUnderOperationsInTree" parameter.

**Role** :Locks or unlocks the "BodiesUnderOperationsInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetColorSynchronizationEditabilityLock**( boolean  `iLocked`)

   Locks or unlocks the "ColorSynchronizationEditability" parameter.

**Role** :Locks or unlocks the "ColorSynchronizationEditability" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetColorSynchronizationModeLock**( boolean  `iLocked`)

   Locks or unlocks the "ColorSynchronizationMode" parameter.

**Role** :Locks or unlocks the "ColorSynchronizationMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetConstraintsInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "ConstraintsInGeometry" parameter.

**Role** :Locks or unlocks the "ConstraintsInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetConstraintsNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ConstraintsNodeInTree" parameter.

**Role** :Locks or unlocks the "ConstraintsNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetContextualFeaturesSelectableAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "ContextualFeaturesSelectableAtCreation" parameter.

**Role** :Locks or unlocks the "ContextualFeaturesSelectableAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDeleteWarningBoxLock**( boolean  `iLocked`)

   Locks or unlocks the "DeleteWarningBox" parameter.

**Role** :Locks or unlocks the "DeleteWarningBox" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayGeometryAfterCurrentLock**( boolean  `iLocked`)

   Locks or unlocks the "DisplayGeometryAfterCurrent" parameter.

**Role** :Locks or unlocks the "DisplayGeometryAfterCurrent" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExpandSketchBasedFeaturesNodeAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "ExpandSketchBasedFeaturesNodeAtCreation" parameter.

**Role** :Locks or unlocks the "ExpandSketchBasedFeaturesNodeAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesAsVisibleLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesAsVisible" parameter.

**Role** :Locks or unlocks the "ExternalReferencesAsVisible" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesAssemblyRootContextLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesAssemblyRootContext" parameter.

**Role** :Locks or unlocks the "ExternalReferencesAssemblyRootContext" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetExternalReferencesNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ExternalReferencesNodeInTree" parameter.

**Role** :Locks or unlocks the "ExternalReferencesNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHybridDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the "HybridDesignMode" parameter.

**Role** :Locks or unlocks the "HybridDesignMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetKnowledgeInHybridDesignModeLock**( boolean  `iLocked`)

   Locks or unlocks the "KnowledgeInHybridDesignMode" parameter.

**Role** :Locks or unlocks the "KnowledgeInHybridDesignMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferences" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferences" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesOnlyOnPublicationLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferencesOnlyOnPublication" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferencesOnlyOnPublication" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLinkedExternalReferencesWarningAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the "LinkedExternalReferencesWarningAtCreation" parameter.

**Role** :Locks or unlocks the "LinkedExternalReferencesWarningAtCreation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNamingModeLock**( boolean  `iLocked`)

   Locks or unlocks the "NamingMode" parameter.

**Role** :Locks or unlocks the "NamingMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWith3DSupportLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWith3DSupport" parameter.

**Role** :Locks or unlocks the "NewWith3DSupport" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithAxisSystemLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithAxisSystem" parameter.

**Role** :Locks or unlocks the "NewWithAxisSystem" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithGSLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithGS" parameter.

**Role** :Locks or unlocks the "NewWithGS" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithOGSLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithOGS" parameter.

**Role** :Locks or unlocks the "NewWithOGS" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetNewWithPanelLock**( boolean  `iLocked`)

   Locks or unlocks the "NewWithPanel" parameter.

**Role** :Locks or unlocks the "NewWithPanel" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOnlyCurrentOperatedSolidSetInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "OnlyCurrentOperatedSolidSetInGeometry" parameter.

**Role** :Locks or unlocks the "OnlyCurrentOperatedSolidSetInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOnlyCurrentSolidSetInGeometryLock**( boolean  `iLocked`)

   Locks or unlocks the "OnlyCurrentSolidSetInGeometry" parameter.

**Role** :Locks or unlocks the "OnlyCurrentSolidSetInGeometry" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetParametersNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "ParametersNodeInTree" parameter.

**Role** :Locks or unlocks the "ParametersNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPublishTopologicalElementsLock**( boolean  `iLocked`)

   Locks or unlocks the "PublishTopologicalElements" parameter.

**Role** :Locks or unlocks the "PublishTopologicalElements" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRelationsNodeInTreeLock**( boolean  `iLocked`)

   Locks or unlocks the "RelationsNodeInTree" parameter.

**Role** :Locks or unlocks the "RelationsNodeInTree" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetReplaceOnlyAfterCurrentLock**( boolean  `iLocked`)

   Locks or unlocks the "ReplaceOnlyAfterCurrent" parameter.

**Role** :Locks or unlocks the "ReplaceOnlyAfterCurrent" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSurfaceElementsLocationLock**( boolean  `iLocked`)

   Locks or unlocks the "SurfaceElementsLocation" parameter.

**Role** :Locks or unlocks the "SurfaceElementsLocation" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateElementsRefreshedLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateElementsRefreshed" parameter.

**Role** :Locks or unlocks the "UpdateElementsRefreshed" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateLinkedExternalReferencesLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateLinkedExternalReferences" parameter.

**Role** :Locks or unlocks the "UpdateLinkedExternalReferences" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateModeLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateMode" parameter.

**Role** :Locks or unlocks the "UpdateMode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateStoppedOnErrorLock**( boolean  `iLocked`)

   Locks or unlocks the "UpdateStoppedOnError" parameter.

**Role** :Locks or unlocks the "UpdateStoppedOnError" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# PlanarFace (Object)

**_2-D boundary with a planar geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the face of a cube. You will create a PlanarFace object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewDraft](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewDraft) ). The lifetime of a PlanarFace object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a face and two planar faces, and creates a draft on these faces:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select the face to draft
     InputObjectType(0)="Face"
     Status=Selection.SelectElement2(InputObjectType,"Select the face to draft",true)
     if (Status = "cancel") then Exit Sub
     Set FaceToDraft = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the neutral face
     InputObjectType(0)="PlanarFace"
     Status=Selection.SelectElement2(InputObjectType,"Select the neutral face",true)
     if (Status = "cancel") then Exit Sub
     Set NeutralFace = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the parting element
     InputObjectType(0)="PlanarFace"
     Status=Selection.SelectElement2(InputObjectType,"Select the parting element",true)
     if (Status = "cancel") then Exit Sub
     Set PartingElement = Selection.Item(1).Value
     Set Draft = ShapeFactory.AddNewDraft(FaceToDraft,NeutralFace,0,PartingElement,0.0,0.0,1.0,0,5.0,0)
     Set DraftDomains = Draft.DraftDomains
     Set DraftDomain = DraftDomains.Item(1)
     DraftDomain.SetPullingDirection 0.0, 0.0,1.0
     Document.Part.Update

```

## Methods

### Sub **GetFirstAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oFirstAxis`)

   Returns the planar face first axis

**Parameters:**

` oFirstAxis[0]`      The X Coordinate of the planar face first axis
` oFirstAxis[1]`      The Y Coordinate of the planar face first axis
` oFirstAxis[2]`      The Z Coordinate of the planar face first axis

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the planar face.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the planar face origin
` oOrigin[1]`      The Y Coordinate of the planar face origin
` oOrigin[2]`      The Z Coordinate of the planar face origin

### Sub **GetSecondAxis**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oSecondAxis`)

   Returns the planar face second axis.

**Parameters:**

` oSecondAxis[0]`      The X Coordinate of the planar face second axis
` oSecondAxis[1]`      The Y Coordinate of the planar face second axis
` oSecondAxis[2]`      The Z Coordinate of the planar face second axis

---

# RectilinearBiDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is two dimensional, the boundary having a rectilinear geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a surface obtained through the extrusion of a line. You will create a RectilinearBiDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [Hole.SetDirection](../PartInterfaces/interface_Hole_3612.htm#SetDirection) ). The lifetime of a RectilinearBiDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:** see the [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) example

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

   Returns the direction of the rectilinear edge.

**Parameters:**

` oDirection[0]`      The X Coordinate of the direction
` oDirection[1]`      The Y Coordinate of the direction
` oDirection[2]`      The Z Coordinate of the direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the the rectilinear edge.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the rectilinear edge origin
` oOrigin[1]`      The Y Coordinate of the rectilinear edge origin
` oOrigin[2]`      The Z Coordinate of the rectilinear edge origin

---

# RectilinearMonoDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is one dimensional, the boundary having a rectilinear geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, in a part containing a Sketch which is made up of a line segment and a spline, the line segment. You will create a RectilinearMonoDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [Hole.SetDirection](../PartInterfaces/interface_Hole_3612.htm#SetDirection) ). The lifetime of a RectilinearMonoDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:** see the [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) example

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

   Returns the direction of the rectilinear edge

**Parameters:**

` oDirection[0]`      The X Coordinate of the direction
` oDirection[1]`      The Y Coordinate of the direction
` oDirection[2]`      The Z Coordinate of the direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the the rectilinear edge.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the rectilinear edge origin
` oOrigin[1]`      The Y Coordinate of the rectilinear edge origin
` oOrigin[2]`      The Z Coordinate of the rectilinear edge origin

---

# RectilinearTriDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is three dimensional, the boundary having a rectilinear geometry._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a Pad resulting from the extrusion of a square. You will create a RectilinearTriDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [Hole.SetDirection](../PartInterfaces/interface_Hole_3612.htm#SetDirection) ). The lifetime of a RectilinearTriDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select a face, a rectilinear edge, and creates a hole. The rectilinear edge specifies the hole direction. It may be a RectilinearTriDimFeatEdge, a RectilinearBiDimFeatEdge or a RectilinearMonoDimFeatEdge.

```VBScript
     Dim EnabledObjectSelection1(0)
     Dim EnabledObjectSelection2(2)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select a face
     EnabledObjectSelection1(0)="Face"
     Status=Selection.SelectElement2(EnabledObjectSelection1,"Select a face",true)
     if (Status = "cancel") then Exit Sub
     Set Face = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the hole direction
     EnabledObjectSelection2(0)="RectilinearTriDimFeatEdge"
     EnabledObjectSelection2(1)="RectilinearBiDimFeatEdge"
     EnabledObjectSelection2(2)="RectilinearMonoDimFeatEdge"
     Status=Selection.SelectElement2(EnabledObjectSelection2,"Select the hole direction",true)
     if (Status = "cancel") then Exit Sub
     Set Hole = ShapeFactory.AddNewHoleFromPoint(20.0,-5.5, 1.07,Face,10.0)
     Hole.ThreadingMode = 1
     Hole.ThreadSide = 0
     Hole.SetDirection Selection.Item(1).Value
     Document.Part.Update

```

## Methods

### Sub **GetDirection**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oDirection`)

   Returns the direction of the rectilinear edge

**Parameters:**

` oDirection[0]`      The X Coordinate of the direction
` oDirection[1]`      The Y Coordinate of the direction
` oDirection[2]`      The Z Coordinate of the direction

### Sub **GetOrigin**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oOrigin`)

   Returns the origin of the the rectilinear edge.

**Parameters:**

` oOrigin[0]`      The X Coordinate of the rectilinear edge origin
` oOrigin[1]`      The Y Coordinate of the rectilinear edge origin
` oOrigin[2]`      The Z Coordinate of the rectilinear edge origin

---

# Shape (Object)

**_Represents the Shape object._**
It is an abstract object which is not intended to be created as such, from which all objects having a shape representation derive.

**See also:**      [SketchBasedShape](../PartInterfaces/interface_SketchBasedShape_52512.md), [BooleanShape](../PartInterfaces/interface_BooleanShape_30260.md), [DressUpShape](../PartInterfaces/interface_DressUpShape_30368.md), [TransformationShape](../PartInterfaces/interface_TransformationShape_77612.md)

---

# ShapeInstance (Object)

**_The interface to access a CATIAShapeInstance._**

## Properties

### Property **InputsCount**( ) As long (Read Only)

   Returns the number of Inputs.

**Example:**     The following example retrieves in `inputsCount` the number of Inputs of `hybridShapeInstance`:

```VBScript
     inputsCount = hybridShapeInstance.InputsCount

```

### Property **OutputsCount**( ) As long (Read Only)

   Returns the number of Outputs.

**Example:**     The following example retrieves in `outputsCount` the number of Outputs of `hybridShapeInstance`:

```VBScript
     outputsCount = hybridShapeInstance.OutputsCount

```

### Property **ParametersCount**( ) As long (Read Only)

   Returns the number of Parameters.

**Example:**     The following example retrieves in `parametersCount` the number of parameters of `hybridShapeInstance`:

```VBScript
     parametersCount = hybridShapeInstance.ParametersCount

```

Methods

### Func **GetInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets an input of a shape instance by its name.

**Parameters:**

` iName`      The name of the input of the shape instance

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = shapeInstance.GetInput("Input1")
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Gets an input of a shape instance by its name. Use this method if you want to retrieve a Reference.

**Parameters:**

` iName`      The name of the input of the shape instance

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = shapeInstance.GetInput("Input1")
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputDataFromPosition**( long  `iPosition`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

   Gets an input of a hybrid shape instance from its position. Use this method if you want to retrieve a Reference.

**Parameters:**

` iPosition`      The position

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = hybridShapeInstance.GetInputFromPosition(2)
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetInputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets an input of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The input, if found  **Example:**     The following example tests if the input was found:

```VBScript
     Set input = hybridShapeInstance.GetInputFromPosition(2)
     If TypeName(input)="Nothing" Then
          MsgBox "Input not found"
     End If

```

### Func **GetOutput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a Ouput by its name.

**Parameters:**

` iName`      The name of the output of the shape instance

**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
     Set output = shapeInstance.GetOuput("Output1")
     If TypeName(output)="Nothing" Then
          MsgBox "Output not found"
     End If

```

### Func **GetOutputFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a Ouput from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The output, if found  **Example:**     The following example tests if the output was found:

```VBScript
     Set output = shapeInstance.GetOuputFromPosition(2)
     If TypeName(output)="Nothing" Then
          MsgBox "Output not found"
     End If

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a parameter of a shape instance by its name.

**Parameters:**

` iName`      The name of the parameter of the shape instance

**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
     Set parameter = shapeInstance.GetParameter("Parameter1")
     If TypeName(parameter)="Nothing" Then
          MsgBox "Parameter not found"
     End If

```

### Func **GetParameterFromPosition**( long  `iPosition`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Gets a parameter of a hybrid shape instance from its position.

**Parameters:**

` iPosition`      The position

**Returns:**      The parameter, if found  **Example:**     The following example tests if the parameter was found:

```VBScript
     Set parameter = hybridShapeInstance.GetParameterFromPosition(2)
     If TypeName(input)="Nothing" Then
           MsgBox "Parameter not found"
     End If

```

### Sub **PutInput**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iInput`)

   Defines an input of a shape instance.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a shape instance The input will be a point and its name will be Input1.

```VBScript
     shapeInstance.PutInput "Input1",point

```

### Sub **PutInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iInput`)

   Defines an input of a shape instance. Use this method if you want to set as input a Reference.

**Parameters:**

` iName`      The input name
` iInput`      The element wich will be input of the shape instance
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**     The following example defines the input of a shape instance The input will be a point and its name will be Input1.

```VBScript
     shapeInstance.PutInput "Input1",point

```

---

# Shapes (Collection)

**_The collection of the shapes making up a body._**

## Methods

### Func **GetBoundary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

   Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAShape](../MecModInterfaces/interface_Shape_5555.md)

   Returns a shape using its index or its name from the Shapes collection.

**Parameters:**

` iIndex`      The index or the name of the shape to retrieve from the collection of shapes. As a numerics, this index is the rank of the shape in the collection. The index of the first shape in the collection is 1, and the index of the last shape is
[Collection.Count](../System/interface_Collection_22150.htm#Count). As a string, it is the name you assigned to the shape using the [AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved shape  **Example:**      This example retrieves in `ThisShape` the third shape, and in `ThatShape` the shape named `MyShape` in the shape collection of the active document, supposed to be a part document.

```VBScript
     Set ThisShape = CATIA.ActiveDocument.Shapes.Item(3)
     Set ThatShape = CATIA.ActiveDocument.Shapes.Item("MyShape")

```

---

# Sketches (Collection)

**_The body's collection of sketches not yet used by any shape._**

## Methods

### Func **Add**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPlane`) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)

   Creates a new sketch and adds it to the sketch collection. The sketch creation implies to specify a supporting plane. Once created, the sketch exists, but is empty. You must use the [Sketch.OpenEdition](../SketcherInterfaces/interface_Sketch_8026.htm#OpenEdition) method to begin to edit it.

**Parameters:**

` iPlane`      The sketch supporting plane
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  **Returns:**      oNewSketch The created sketch  **Example:**      This example creates the `newSketch` sketch on the XY plane of the `myPart` part:

```VBScript
     Set XYPlane = myPart.OriginElements.PlaneXY()
     Set newSketch = myPart.Sketches.Add(XYPlane)

```

### Func **GetBoundary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIABoundary](../MecModInterfaces/interface_Boundary_14542.md)

   Returns a boundary using its label.

**Parameters:**

` iLabel`      Identification of the
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object. See [Reference.DisplayName](../InfInterfaces/interface_Reference_17481.htm#DisplayName).  **Returns:**      The retrieved boundary  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)

   Returns a sketch using its index or its name from the Sketches collection.

**Parameters:**

` iIndex`      The index or the name of the sketch to retrieve from the collection of sketches. As a numerics, this index is the rank of the sketch in the collection. The index of the first sketch in the collection is 1, and the index of the last sketch is Count. As a string, it is the name you assigned to the sketch using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved sketch  **Example:**      This example retrieves the last item in the collection sketches.

```VBScript
     Set lastSketch = sketchList.Item(sketchList.Count)

```

---

# Solid (Object)

**_Represents an imported solid object._**

**Role** : the imported solid is a solid obtained from copy/paste with link or design in context.
The solid object has a link to a source element obtained from SourceElement and a source product obtained from SourceProduct .

## Properties

### Property **Move**( ) As [CATIAMove](../InfInterfaces/interface_Move_3742.md) (Read Only)

   Returns the move object of the solid.

**Role** : The move object is aggregated by the solid object and itself aggregates a movable object to which you can apply a move transformation by means of an isometry matrix. It moves the solid according to this isometry.

**Example:**      This example retrieves the move object `EngineMoveObject` for the `Engine` product.

```VBScript
     Dim EngineMoveObject As Move
     Set EngineMoveObject = Engine.Move

```

**See also:**      [Move](../InfInterfaces/interface_Move_3742.md) 
### Property **SourceElement**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the source element of the imported solid.

**Role** : returns the linked element in the source part.

**Example:**     The following example returns in `element` the source element of the imported solid `importedSolid`:

```VBScript
     Set element = importedSolid.SourceElement

```

### Property **SourceProduct**( ) As [CATIABase](../System/interface_AnyObject_17321.md) (Read Only)

   Returns the source product instance of the imported solid.

**Role** : returns the product instance which was selected when the import was created.

**Example:**     The following example returns in `prod1` the source product instance of the imported solid `importedSolid`:

```VBScript
     Set prod1 = importedSolid.SourceProduct

```

---

# TriDimFeatEdge (Object)

**_1-D boundary belonging to a feature whose topological result is three dimensional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the edge of a Pad. You will create a TriDimFeatEdge object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [ShapeFactory.AddNewEdgeFilletWithConstantRadius](../PartInterfaces/interface_ShapeFactory_31272.htm#AddNewEdgeFilletWithConstantRadius) ). The lifetime of a TriDimFeatEdge object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

**Example:**      This example asks the end user to select an edge, and creates an edge fillet on this edge:

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     'We propose to the user that he select an edge
     InputObjectType(0)="TriDimFeatEdge"
     Status=Selection.SelectElement2(InputObjectType,"Select an edge",true)
     if (Status = "cancel") then Exit Sub
     Set EdgeFillet = ShapeFactory.AddNewEdgeFilletWithConstantRadius(Selection.Item(1).Value,1,5.0)
     EdgeFillet.EdgePropagation = 1
     Document.Part.Update

```

---

# TriDimFeatVertexOrBiDimFeatVertex (Object)

**_0-D boundary belonging to a feature whose topological result is three dimensional or two dimentional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the corner of a Pad resulting from the extrusion of a square. You will create a TriDimFeatVertexOrBiDimFeatVertex object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator. The lifetime of a TriDimFeatVertexOrBiDimFeatVertex object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).

---

# Vertex (Object)

**_0-D boundary._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the corner of a Pad resulting from the extrusion of a square. You will create an Vertex object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator (such as [HybridShapeFactory.AddNewLinePtPt](../GSMInterfaces/interface_HybridShapeFactory_68680.htm#AddNewLinePtPt) ). The lifetime of a Vertex object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md). **See also:**
[TriDimFeatVertexOrBiDimFeatVertex](../MecModInterfaces/interface_TriDimFeatVertexOrBiDimFeatVertex_221087.md) , [NotWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_NotWireBoundaryMonoDimFeatVertex_212840.md) , [ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex](../MecModInterfaces/interface_ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex_474398.md) .

**Example:**      This example asks the end user to select successively two vertices. Then, it creates a line between these two vertices.

```VBScript
     Dim InputObjectType(0)
     Set Document = CATIA.ActiveDocument
     Set Selection = Document.Selection
     Set HybridBodies = Document.Part.HybridBodies
     Set HybridBody = HybridBodies.Item("Geometrical Set.1")
     'We propose to the user that he select the first vertex
     InputObjectType(0)="Vertex"
     Status=Selection.SelectElement2(InputObjectType,"Select the first vertex",true)
     if (Status = "cancel") then Exit Sub
     Set FirstVertex = Selection.Item(1).Value
     Selection.Clear
     'We propose to the user that he select the second vertex
     InputObjectType(0)="Vertex"
     Status=Selection.SelectElement2(InputObjectType,"Select the second vertex",true)
     if (Status = "cancel") then Exit Sub
     Set SecondVertex = Selection.Item(1).Value
     Set hybridShapeLinePtPt = HybridShapeFactory.AddNewLinePtPt(FirstVertex,SecondVertex)
     HybridBody.AppendHybridShape hybridShapeLinePtPt
     Document.Part.InWorkObject = hybridShapeLinePtPt
     Document.Part.Update

```

---

# ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex (Object)

**_0-D boundary beeing either an isolated point or the extremity of a feature whose topological result is one dimensional._**

**Role** : This [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object may be, for example, the extremity of a line segment. You will create a ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex object using the [Shapes.GetBoundary](../MecModInterfaces/interface_Shapes_8122.htm#GetBoundary) , [HybridShapes.GetBoundary](../MecModInterfaces/interface_HybridShapes_30836.htm#GetBoundary) , [Sketches.GetBoundary](../MecModInterfaces/interface_Sketches_14228.htm#GetBoundary) or [Selection.SelectElement2](../InfInterfaces/interface_Selection_18040.htm#SelectElement2) method. Then, you pass it to the operator. The lifetime of a ZeroDimFeatVertexOrWireBoundaryMonoDimFeatVertex object is limited, see [Boundary](../MecModInterfaces/interface_Boundary_14542.md).