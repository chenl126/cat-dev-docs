# Mechanism (Object)

**_Interface to access the Mechanism object._**

## Properties

### Property **Commands**( ) As [CATIAMechanismCommands](../KinematicsInterfaces/interface_MechanismCommands_61399.md) (Read Only)

Returns the collection of commands in the mechanism.

**Parameters:**

` oCommands`      The collection of commands. This property is read only because because list is aggregated in the Mechanism

### Property **FixedPart**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Returns or sets the fixed part of the mechanism.

**Parameters:**

` oFixedPart`      The fixed part.

### Property **Joints**( ) As [CATIAJoints](../KinematicsInterfaces/interface_Joints_8428.md) (Read Only)

Returns the collection of joints in the mechanism.

**Parameters:**

` oJoints`      The collection of joints. This property is read only because because list is aggregated in the Mechanism

### Property **NbCommands**( ) As long (Read Only)

Returns the number of commands in the mechanism.

**Parameters:**

` oNbCommands`      The number of commands. This property is read only because number depends on commands creation/destruction

### Property **NbDof**( ) As long (Read Only)

Returns the degree of freedom of the mechanism.

**Parameters:**

` oNbDof`      The degree of freedom. This property is read only because because it depends on joints and commands

### Property **NbJoints**( ) As long (Read Only)

Returns the number of joints in the mechanism.

**Parameters:**

` oNbJoints`      The number of joints. This property is read only because number depends on joints creation/destruction

### Property **NbProducts**( ) As long (Read Only)

Returns the number of products (i.e. bodies) involved in the mechanism.

**Parameters:**

` oNbProducts`      The number of products. This property is read only because number depends on joints creation/destruction
Methods

### Func **AddCommand**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iCmdType`,  [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)  `iJoint`) As [CATIAMechanismCommand](../KinematicsInterfaces/interface_MechanismCommand_53914.md)

Adds a command in the mechanism, on a joint.

**Parameters:**

` iCmdType`      The command type.
` iJoint`      The joint to be driven.
` oNewCommand`      The newly created command.

### Func **AddJoint**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iJointType`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iListElem`) As [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)

Adds a joint in the mechanism.

**Parameters:**

` iJointType`      The joint type.
` iListElem`      The list of elements expected to locate the joint, depending on the type.
` oNewJoint`      The newly created joint.

### Sub **GetCommandValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioCmdValues`)

Allows to retrieve current state of the mechanism.

**Parameters:**

` ioCmdValues`      current command values

### Func **GetProduct**( long  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

Returns an item from the list of the products involved in the mechanism.

**Parameters:**

` iIndex`      The index for the product.
` oProduct`      The product at that index.
**Returns:**      HRESULT  
### Sub **GetProductMotion**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `ioMotion`)

Retrieves motion from initial state to current state for a part of the mechanism.

**Parameters:**

` iProduct`      The moving product
` ioMotion`      The motion matrix (12 real values, compatible with the Move object)
**See also:**      [Move](../InfInterfaces/interface_Move_3742.md) 
### Sub **PutCommandValues**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iCmdValues`)

Triggers immediate mechanism solving (motion is NOT applied to the model).

**Parameters:**

` iCmdValues`      command values to be solved for

### Sub **Update**( )

Reassembles the mechanism after dimension changes in the parts.