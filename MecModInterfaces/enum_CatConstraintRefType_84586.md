# CatConstraintRefType (Enumeration)

**_Constraint reference type._**

In the PartDesign context, an element having a Reference constraint will not move during the update. The Assembly context allows two behaviours : Either the element will not move, or the element will move to the position where it was when the Reference type has been set to FixInSpace. `ReferenceType`. This enum lists appropriate values to set this property.

**Values:**

` catCstRefTypeRelative`      The element will not move during the update (the default mode).
` catCstRefTypeFixInSpace`      The element will move to its former position (Assembly context only).