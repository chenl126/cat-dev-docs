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