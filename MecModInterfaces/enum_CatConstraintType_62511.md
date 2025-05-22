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