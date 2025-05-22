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