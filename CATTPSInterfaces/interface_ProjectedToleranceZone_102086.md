# ProjectedToleranceZone (Object)

**_Interface for accessing projected tolerance zone informations of a TPS._**
========| Position Length / |<\----------->|<\----------->| Toleranced | | | Surface - - - +-------> +=============+ \ |\ \ \ \ | Origin Direction Projected Tolerance Zone ========|

## Properties

### Property **Length**(| ) As double (Read Only)

   Retrieves length of the projected tolerance zone (in millimeters). The length defines the ending point of the tolerance zone. This point can be computed by using Origin and Direction of the axis.  
### Property **Position**( ) As double (Read Only)

   Retrieves position of the projected tolerance zone (in millimeters). The position defines the starting point of the tolerance zone. This point can be computed by using Origin and Direction of the axis.