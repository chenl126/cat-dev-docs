# KinematicsInterfaces Framework

## Object Index

  * [Dressup](KinematicsInterfaces/interface_Dressup_11434.md)
  * [Dressups](KinematicsInterfaces/interface_Dressups_14936.md)
  * [Joint](KinematicsInterfaces/interface_Joint_5842.md)
  * [Joints](KinematicsInterfaces/interface_Joints_8428.md)
  * [KinematicsWorkbench](KinematicsInterfaces/interface_KinematicsWorkbench_76941.md)
  * [Mechanism](KinematicsInterfaces/interface_Mechanism_17799.md)
  * [MechanismCommand](KinematicsInterfaces/interface_MechanismCommand_53914.md)
  * [MechanismCommands](KinematicsInterfaces/interface_MechanismCommands_61399.md)
  * [Mechanisms](KinematicsInterfaces/interface_Mechanisms_22166.md)

---

# Dressup (Object)

**_Interface to access the Dressup object._**

## Properties

### Property **Context**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the context product on which the mechanism is defined. This property is read only.

**Returns:**      The dressup mechanism's context  **Example:**      This example sets in `MecaContext` the context product of `MyDressup`.

```VBScript
        Dim MecaContext As Product
        Set MecaContext = MyDressup.Context

```

### Property **Mechanism**( ) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md) (Read Only)

   Returns the mechanism on which a dressup is applied. This property is read only.

**Returns:**      The dressup's mechanism  **Example:**      This example sets in `Meca` the mechanism of `MyDressup`.

```VBScript
      Dim Meca As Mechanism
      Set Meca = MyDressup.Mechanism

```

Methods

### Sub **Attach**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLink`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iAttachedProd`)

   Attaches a given product to a link of the mechanism pointed by the dressup.

**Parameters:**

` iLink`      The link (Product) on which the attachment should be done. It should be a product that belongs to the mechanism pointed by the dressup, otherwise the method will fail.
` iAttachedProd`      The Product that will be attached to the link. This product should not be a product that is already attached by another link, otherwise the method will fail.

**Returns:**      Nothing  **Example:**      This example attaches inside `MyDressup`, `Link1` as mechanism's part to `Product1`.

```VBScript
        Dim Link1 As Product
        Dim Product1 As Product
        ...
        MyDressup.Attach(Link1,Product1)

```

### Sub **Detach**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iAttachedProd`)

   Detaches an attached product from its link.

**Parameters:**

` iAttachedProd`      The Product that will be detached. It should be a product that is currently attached in the dressup, otherwise the method will fail.

**Returns:**      Nothing  **Example:**      This example detaches `Product1` previously attached to a mechanism's part inside `MyDressup`.

```VBScript
        Dim Product1 As Product
        ...
        MyDressup.Detach(Product1)

```

### Func **ListAttached**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iLink`) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns the list of products attached to a given link.

**Parameters:**

` iLink`      The Product on which the returned product list is attached to.

**Returns:**      The Product list that is attached to iLink.  **Example:**      The following example loops for all the products attached to `Link1`.

```VBScript
        Dim ListAttached1 as Product
        ListAttached1 = MyDressup.ListAttached(Link1)
        Dim Maxi as Integer
        Set Maxi = ubound(ListAttached1)
        Dim Prod_i as Product
        For i = 0  To  Maxi
           Set Prod_i = ListAttached1(i)
           ..
        Next

```

---

# Dressups (Collection)

**_A collection of all Dressup entities currently managed by the application._**

## Methods

### Func **Add**( [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)  `iMechanism`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iContext`) As [CATIADressup](../KinematicsInterfaces/interface_Dressup_11434.md)

   Creates a new Dressup and adds it to the Dressups collection.

**Parameters:**

` iMechanism`      The mechanism on which the dressup will apply.
` iContext`      The Context product on which the mechanism is defined

**Returns:**      The created Dressup  **Example:**      This example creates a new Dressup in the `TheDressups` collection.

```VBScript
        Dim NewDressup As Dressup
        Set NewDressup = TheDressups.Add(Mechanism)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADressup](../KinematicsInterfaces/interface_Dressup_11434.md)

   Returns a Dressup using its index or its name from the Dressups collection.

**Parameters:**

` iIndex`      The index or the name of the Dressup to retrieve from the collection of Dressups. As a numerics, this index is the rank of the Dressup in the collection. The index of the first Dressup in the collection is 1, and the index of the last Dressup is Count. As a string, it is the name you assigned to the Dressup using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Dressup  **Example:**      This example returns in `ThisDressup` the third Dressup in the collection, and in `ThatDressup` the Dressup named `MyDressup`.

```VBScript
     Dim ThisDressup As Dressup
     Set ThisDressup = TheDressups.Item(3)
     Dim ThatDressup As Dressup
     Set ThatDressup = CATIA.Dressups.Item("MyDressup")

```

### Func **ListMechanismsContext**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Each mechanism of the list given by ListPossibleMechanisms has a context product on which it is defined.

**Parameters:**

` Nothing`

**Returns:**      The list of mechanisms' contexts on which a dressup can be created. The context of oMechanismList(i) is oContextList(i).  **Example:**      The following example returns the first and the last element of the list of mechanisms' contexts. We assume that this list contains at least two values.

```VBScript
        Dim ContextList As Product
        ContextList = MyDressups.ListMechanismsContext()
        Dim FirstContext As Product
        Set FirstContext = ContextList(0)
        Dim LastContext As Product
        Set LastContext = ContextList(ubound(ContextList))

```

### Func **ListPossibleMechanisms**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Returns information about all possible mechanisms on which a dressup can be created.

**Parameters:**

` Nothing`

**Returns:**      The list of possible mechanisms on which a dressup can be created.  **Example:**      The following example returns the first and the last element of the list of possible mechanisms. We assume that this list contains at least two values.

```VBScript
        Dim PossibleMecList As Mechanism
        PossibleMecList = MyDressups.ListPossibleMechanisms()
        Dim FirstMeca As Mechanism
        Set Meca  = PossibleMecList(0)
        Dim LastMeca As Mechanism
        Set Meca  = PossibleMecList(ubound(PossibleMecList))

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Dressup from the Dressups collection.

**Parameters:**

` iIndex`      The index or the name of the Dressup to retrieve from the collection of Dressups. As a numerics, this index is the rank of the Dressup in the collection. The index of the first Dressup in the collection is 1, and the index of the last Dressup is Count. As a string, it is the name you assigned to the Dressup.

**Returns:**      Nothing  **Example:**      The following example removes the tenth Dressup and the Dressup named `DressupTwo` from the `TheDressups` collection.

```VBScript
        TheDressups.Remove(10)
        TheDressups.Remove("DressupTwo")

```

---

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

---

# Joints (Collection)

**_A collection of all Joint entities currently managed by the application._**

## Methods

### Func **Add**( ) As [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)

   Create a new Joint and adds it to the Joints collection.

**Returns:**      The created Joint  **Example:**      This example creates a new Joint in the `TheJoints` collection.

```VBScript
        Dim NewJoint As Joint
        Set NewJoint = TheJoints.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAJoint](../KinematicsInterfaces/interface_Joint_5842.md)

   Returns a Joint using its index or its name from the Joints collection.

**Parameters:**

` iIndex`      The index or the name of the Joint to retrieve from the collection of Joints. As a numerics, this index is the rank of the Joint in the collection. The index of the first Joint in the collection is 1, and the index of the last Joint is Count. As a string, it is the name you assigned to the Joint using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Joint  **Example:**      This example returns in `ThisJoint` the third Joint in the collection, and in `ThatJoint` the Joint named `MyJoint`.

```VBScript
     Dim ThisJoint As Joint
     Set ThisJoint = TheJoints.Item(3)
     Dim ThatJoint As Joint
     Set ThatJoint = CATIA.Joints.Item("MyJoint")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Remove a Joint from the Joints collection.

**Parameters:**

` iIndex`      The index or the name of the Joint to retrieve from the collection of Joints. As a numerics, this index is the rank of the Joint in the collection. The index of the first Joint in the collection is 1, and the index of the last Joint is Count. As a string, it is the name you assigned to the Joint.

**Returns:**      Nothing  **Example:**      The following example removes the tenth Joint and the Joint named `JointTwo` from the `TheJoints` collection.

```VBScript
        TheJoints.Remove(10)
        TheJoints.Remove("JointTwo")

```

---

# KinematicsWorkbench (Object)

**_Interface to access all Kinematics entities._**

## Properties

### Property **Mechanisms**( ) As [CATIAMechanisms](../KinematicsInterfaces/interface_Mechanisms_22166.md) (Read Only)

   Returns the Mechanisms collection.

**Returns:**      The Mechanisms collection  **Example:**      This example retrieves the Mechanisms collection of the active document.

```VBScript
        Dim TheKinWorkbench As Workbench
        Set TheKinWorkbench = CATIA.ActiveDocument.GetWorkbench ( "KinematicsWorkbench" )
        Dim TheMechanismsList As Mechanisms
        Set TheMechanismsList = TheKinWorkbench.Mechanisms

```

---

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

---

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

---

# MechanismCommands (Collection)

**_A collection of all MechanismCommand entities currently managed by the application._**

## Methods

### Func **Add**( ) As [CATIAMechanismCommand](../KinematicsInterfaces/interface_MechanismCommand_53914.md)

   Creates a new MechanismCommand and adds it to the MechanismCommands collection.

**Returns:**      The created MechanismCommand  **Example:**      This example creates a new MechanismCommand in the `TheCommands` collection.

```VBScript
        Dim NewCommand As MechanismCommand
        Set NewCommand = TheCommands.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMechanismCommand](../KinematicsInterfaces/interface_MechanismCommand_53914.md)

   Returns a MechanismCommand using its index or its name from the Commands collection.

**Parameters:**

` iIndex`      The index or the name of the MechanismCommand to retrieve from the collection of Commands. As a numerics, this index is the rank of the MechanismCommand in the collection. The index of the first MechanismCommand in the collection is 1, and the index of the last MechanismCommand is Count. As a string, it is the name you assigned to the MechanismCommand using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved MechanismCommand  **Example:**      This example returns in `ThisCommand` the third MechanismCommand in the collection, and in `ThatCommand` the MechanismCommand named `MyCommand`.

```VBScript
     Dim ThisCommand As MechanismCommand
     Set ThisCommand = TheCommands.Item(3)
     Dim ThatCommand As MechanismCommand
     Set ThatCommand = CATIA.MechanismCommands.Item("MyCommand")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Remove a MechanismCommand from the MechanismCommands collection.

**Parameters:**

` iIndex`      The index or the name of the MechanismCommand to retrieve from the collection of MechanismCommands. As a numerics, this index is the rank of the MechanismCommand in the collection. The index of the first MechanismCommand in the collection is 1, and the index of the last MechanismCommand is Count. As a string, it is the name you assigned to the MechanismCommand.

**Returns:**      Nothing  **Example:**      The following example removes the tenth MechanismCommand and the MechanismCommand named `CommandTwo` from the `TheCommands` collection.

```VBScript
        TheCommands.Remove(10)
        TheCommands.Remove("CommandTwo")

```

---

# Mechanisms (Collection)

**_A collection of all Mechanism entities currently managed by the application._**

## Methods

### Func **Add**( ) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)

   Creates a new Mechanism and adds it to the Mechanisms collection.

**Returns:**      The created Mechanism  **Example:**      This example creates a new Mechanism in the `TheMechanisms` collection.

```VBScript
        Dim NewMechanism As Mechanism
        Set NewMechanism = TheMechanisms.Add()

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMechanism](../KinematicsInterfaces/interface_Mechanism_17799.md)

   Returns a Mechanism using its index or its name from the Mechanisms collection.

**Parameters:**

` iIndex`      The index or the name of the Mechanism to retrieve from the collection of Mechanisms. As a numerics, this index is the rank of the Mechanism in the collection. The index of the first Mechanism in the collection is 1, and the index of the last Mechanism is Count. As a string, it is the name you assigned to the Mechanism using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Mechanism  **Example:**      This example returns in `ThisMechanism` the third Mechanism in the collection, and in `ThatMechanism` the Mechanism named `MyMechanism`.

```VBScript
     Dim ThisMechanism As Mechanism
     Set ThisMechanism = TheMechanisms.Item(3)
     Dim ThatMechanism As Mechanism
     Set ThatMechanism = CATIA.Mechanisms.Item("MyMechanism")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Mechanism from the Mechanisms collection.

**Parameters:**

` iIndex`      The index or the name of the Mechanism to retrieve from the collection of mechanisms. As a numerics, this index is the rank of the Mechanism in the collection. The index of the first Mechanism in the collection is 1, and the index of the last Mechanism is Count. As a string, it is the name you assigned to the Mechanism.

**Returns:**      Nothing  **Example:**      The following example removes the tenth Mechanism and the Mechanism named `MechanismTwo` from the `TheMechanisms` collection.

```VBScript
        TheMechanisms.Remove(10)
        TheMechanisms.Remove("MechanismTwo")

```