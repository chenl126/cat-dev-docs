# OptimizationConstraint (Object)

**_Represents an optimization constraint._**

**See also:**      [OptimizationConstraints](../KnowledgeInterfaces/interface_OptimizationConstraints_116449.md)

## Properties

### Property **DistanceToSatisfaction**( ) As [CATIARealParam](../KnowledgeInterfaces/interface_RealParam_17053.md) (Read Only)

Returns the parameter containing the distance to constraint satisfaction.  
### Property **Precision**( ) As double

Returns or sets the constraint precision. Only for equality constraints.
The constraint precision allows the system to know when an equality constraint can be declared as satisfied (when : distance to satisfaction < precision).  
### Property **Satisfaction**( ) As boolean (Read Only)

Returns the constraint satisfaction.