# CatConstraintDistConfig (Enumeration)

**_Special constraint configurations for distance constraints._**

When distance constraints involve lines or cylinders, the constrained elements can rotate around the line on which the distance is measured, while still respecting the distance constraint. This degree of freedom is in most cases not wanted.
This enum is used to further qualify the distance constraint, so that such degree of freedom can be eliminated in case of need, without requiring another distinct constraint to be defined.

**Values:**

` catCstDCUnspec`      No additional condition is set on the constraint.
` catCstDCParallel`      In addition to being positioned at a given distance, constrained elements are required to be parallel. Their orientation can be the same or opposite.
` catCstDCParallelSameOrient`      In addition to being positioned at a given distance, constrained elements are required to be parallel, and their orientations are required to be the same.
` catCstDCParallelOppOrient`      In addition to being positioned at a given distance, constrained elements are required to be parallel, and their orientations are required to be opposite.