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