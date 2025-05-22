# CatConstraintAngleSector (Enumeration)

**_Special constraint property for angle constraints._**

It only applies to the constraints of type Angle or PlanarAngle.
The geometric elements of an angle constraint (e.g. : 2 lines or 2 planes) divide the sketch or the space in 4 regions which are called angular sectors, numbered from 0 to 3. By default, the constraint is created in the sector number 0. One angular sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angular sector, the Dimension.Value, Side and Orientation are also modified. 1 / 0 \---/--- 2/ 3 By default, the constraint is created in the sector number 0. One angle sector corresponds exactly to particular values of the Dimension.Value, the Side and the Orientation. When changing the angle sector, the Dimension.Value, Side and Orientation are also modified.

**Values:**

` AngleSector=0`      The default sector of a constraint. Dimension.Value = angle Orientation = catCstOrientSame Side = catCstSidePositive
` AngleSector=1`      Dimension.Value = angle-180 if angle>180 abs(angle)+180 otherwise Orientation = catCstOrientOpposite Side = catCstSidePositive
` AngleSector=2`      Dimension.Value = abs(540-angle) if angle>180 180-fabs(angle) otherwise Orientation = catCstOrientOpposite Side = catCstSideNegative
` AngleSector=3`      Dimension.Value = 360-abs(angle) Orientation = catCstOrientSame Side = catCstSideNegative