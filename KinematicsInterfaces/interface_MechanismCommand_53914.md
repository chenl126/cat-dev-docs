# MechanismCommand (Object)

**_Interface to access the Command object (in Kinematics context)._**

## Properties

### Property **CurrentValue**( ) As double (Read Only)

Returns the current value for a command.

**Parameters:**

` oCurrentValue`      The current value This property is read only because current value modification is done by solver

### Property **Orientation**( ) As short

**Deprecated:**      V5R18 Not implemented - will be deprecated Returns or sets the command orientation.  **Parameters:**

` oOrientation`      The orientation of the command; only the sign is important (+: same as relying joint/-: opposite)

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

Returns the command type.

**Parameters:**

` oType`      The type of the command
**See also:**      [Mechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)