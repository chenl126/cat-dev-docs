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