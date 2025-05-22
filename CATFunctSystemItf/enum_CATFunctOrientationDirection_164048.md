# CATFunctOrientationDirection (Enumeration)

**_The qualifications of Orientation and Direction of a Functional Action._**

* * When NotOriented, no distinction is made between the two Elements the Action is connected on.
Graphically,they are connected by a line without any arrow.
(but they still have to be accessed thru the "From" and "To" properties)
_Such qualification is used when the Action is in fact a relationship that points the Elements
(a Welding relationship might be used to point 2 Entities : Flange and Stiffener)_
* When Oriented, there are two possibilities :

  * When Unidirectional, the "From" and "To" Elements are connected by a simple arrow matching the direction.
_Such qualification is used when the Action is a true Subject-Action-Object relationship.
(a Welding relationship might be used to point 2 Entities : Flange and Stiffener)_
  * When Bidirectional, they are connected by a double arrow, that avoids to create two symetrical unidirectional actions with the same identification.
_Such qualification is used when the Action is a true Subject-Action-Object relationship.
(a Heating relationship might be used to point 2 Entities : DiskBrake and BrakeJaws)_