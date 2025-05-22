# Joint (Object)

**_Interface to manage the Joint object._**
Depending on their type, joints have parameters or not, representing length or angle:  **Joint type** | **Parameter1** | **Parameter2**
---|---|---
Revolute | Angle |
Prismatic | Length |
Cylindrical | Length | Angle
Screw | Length | Angle
Gear | Angle | Angle
Rack | Length | Angle
Cable | Length | Length
PointOnCurve | Length |
RollCurve | Length |

Each parameter can have a lower and/or an upper limit.

Methods are provided to set, unset and return the limits for each parameter.

## Properties

### Property **CurrentValue1**( ) As double (Read Only)

Gets the joint current value for first parameter.

**Parameters:**

` oCurrentValue`      This property is read only because current value modification is done by solver

### Property **CurrentValue2**( ) As double (Read Only)

Gets the joint current value for second parameter.

**Parameters:**

` oCurrentValue`      This property is read only because current value modification is done by solver

### Property **LowerLimit1**( ) As double

Gets or returns the lower limit of the joint, for the first parameter.

**Parameters:**

` iLimitValue`      The value for the limit When reading, an error is returned if the joint type has no such parameter, or if the limit is unset.

### Property **LowerLimit2**( ) As double

Gets or returns the lower limit of the joint, for the second parameter.

**Parameters:**

` iLimitValue`      The value for the limit When reading, an error is returned if the joint type has no such parameter, or if the limit is unset.

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the joint type.

**Parameters:**

` oType`      The type of the joint This property is read only because the construction of the object depends on the type.

### Property **UpperLimit1**( ) As double

Gets or returns the upper limit of the joint, for the first parameter.

**Parameters:**

` iLimitValue`      The value for the limit When reading, an error is returned if the joint type has no such parameter, or if the limit is unset.

### Property **UpperLimit2**( ) As double

Gets or returns the upper limit of the joint, for the second parameter.

**Parameters:**

` iLimitValue`      The value for the limit When reading, an error is returned if the joint type has no such parameter, or if the limit is unset.
Methods

### Sub **UnsetLowerLimit1**( )

Unsets the lower limit of the joint, for the first parameter.

**Parameters:**

` iLimitValue`      The value for the limit When reading, an error is returned if the joint type has no such parameter, or if the limit is unset.

### Sub **UnsetLowerLimit2**( )

Unsets the lower limit of the joint, for the second parameter.

**Parameters:**

` iLimitValue`      The value for the limit

### Sub **UnsetUpperLimit1**( )

Unsets the upper limit of the joint, for the first parameter.

**Parameters:**

` iLimitValue`      The value for the limit

### Sub **UnsetUpperLimit2**( )

Unsets the upper limit of the joint, for the second parameter.

**Parameters:**

` iLimitValue`      The value for the limit