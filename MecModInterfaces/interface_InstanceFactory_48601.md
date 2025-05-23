# InstanceFactory (Object)

**_Represents the CATIAInstanceFactory._**

**Role** : This interface is used to create a new instance of a shape reference ([ShapeInstance](../MecModInterfaces/interface_ShapeInstance_35910.md) ) or a hybrid shape reference ( [HybridShapeInstance](../MecModInterfaces/interface_HybridShapeInstance_75602.md) ) in case of the instantiation of a `User Feature`.
It is also used to instantiate a `Power Copy` reference.

This interface contains two protocols of instantiation:

  * The first protocol is dedicated to `User Feature` instantiation only.
It is defined by a single method: AddInstance . It creates a shape or hybrid shape instance depending on the result of the `User Feature`.
Use this method when you want to perform only one instantiation of the reference. Read the document containing the `User Feature` reference and instantiate it.
As the document containing the reference is released from the session at the end of the instantiation, it is not recommmended to use this method if you want to perform several instantiations of the same reference in a loop.
In that case, prefer the second protocol of instantiation.
  * The second protocol is dedicated to both `User Feature` and `Power Copy` instantiations.
It is defined by several methods that must be called in order.

    * For `User Feature` instantiation, these methods are an alternative way of the AddInstance method.
It is recommended to use the second protocol to perform several instantiations of the same reference in a loop.

    * For `Power Copy` instantiation, it is the only way of instantiating a reference.

The instantiation process is composed of three major steps:

    1. The first step BeginInstanceFactory consists in initializing the [InstanceFactory](../MecModInterfaces/interface_InstanceFactory_48601.md) with the reference and the document where it is stored.
This step must be called once at the beginning whatever the number of instantiations are done.
    2. The second step is the instantiation itself: it is composed of five methods that must be called in the order.
This set of five methods can be called in a loop in order to make several instantiations.

       1. The method BeginInstantiate is used to initialize all data of the reference.
       2. The method PutInputData is used to set a value to any input of the reference.
       3. The method GetParameter is used to retrieve any parameter of the reference in order to modify its value.
       4. The method Instantiate is used to duplicate the reference. It returns the created instance when it does exist.
       5. The method EndInstantiate is used to indicate that the instantiation is done.
    3. The third step EndInstantiateFactory consists in ending the instantiation and cleaning the [InstanceFactory](../MecModInterfaces/interface_InstanceFactory_48601.md).
When doing several instantiations in a loop, this step must be called just once at the end of all instantiations.

## Methods

### Func **AddInstance**(| [CATIABase](../System/interface_AnyObject_17321.md) | `iReference`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Creates a new instance of a shape or hybrid shape.

**Parameters:**

` iReference`      The reference shape or hybrid shape.  **Example:**      This example creates the instance `NewInstance` in the part.

```VBScript
     Set NewInstance = instanceFactory.AddInstance(reference)

```

### Sub **BeginInstanceFactory**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNameOfReference`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iNameOfDocument`)

   Initializes the instantiation process with the document containing the reference.

**Role** : Use this method to start instantiating a reference in the current document.
In that method, the document containing the reference is locked in session.
It will be unlocked in the last step EndInstanceFactory .

**Parameters:**

` iNameOfReference`      The name of the reference to be instantiated.
` iDocumentFileName`      The name of the file containing the document where to find the reference to be instantiated.  **Example:**      The following example initializes the factory with a document and a reference:

```VBScript
     InstanceFactory.BeginInstanceFactory"NameOfReference","c:\tmp\NameOfDocument.CATPart"

```

### Sub **BeginInstantiate**( )

   Initializes the data of the reference.

**Role** : This is the first method of the second step of instantiation.
It is used to initialize all data of the reference in the factory.

**Example:**      The following example shows how to initialize the factory:

```VBScript
     InstanceFactory.BeginInstantiate

```

### Sub **EndInstanceFactory**( )

   Ends the instantiation process.

**Role** : Use this method to end the instantiation process.
In that method the document containing the reference is unlocked and released from the session.

**Example:**      The following example shows how to end the instantiation:

```VBScript
     InstanceFactory.EndInstanceFactory

```

### Sub **EndInstantiate**( )

   Ends the instantiation of the reference.

**Role** : This is the fifth and last method of the second step of instantiation.
It is used to end the instantiation: after this step, all the links to the reference are broken.

**Example:**      The following example shows how to end the instantiation:

```VBScript
     InstanceFactory.EndInstantiate

```

### Func **GetParameter**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieves a parameter of the reference by its name.

**Role** : This is the third method of the second step of instantiation.
This step is optional.
It is used to retrieve a parameter of the reference in order to change its value, using the `ValuateFromString` method of the `Parameter` interface.
It has to be called on each parameter whose value has to be changed.

**Parameters:**

` iName`      The name of the parameter.  **Example:**      The following example retrieves a parameter on the reference:

```VBScript
     Set parameter = InstanceFactory.GetParameter("Parameter1")

```

### Func **Instantiate**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

   Instantiates the reference in the current document.

**Role** : This is the fourth method of the second step of instantiation.
It is used to duplicate or instantiate the data of the reference.

  * In case of `Power Copy` instantiation, the data are duplicated and there is no created instance.
  * In case of `User Feature` instantiation, the data are instantiated and an instance is created and returned.

**Example:**      The following example instantiates the reference:

```VBScript
     Set Instance = InstanceFactory.Instantiate

```

### Sub **PutInputData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)  `iInput`)

   Sets a value to an input of the reference.

**Role** : This is the second method of the second step of instantiation.
It is used to set a value to any input of the reference.
It has to be called on each input of the reference.

**Parameters:**

` iName`      The name of the input.
` iInput`      The element to set as the new value of the input.
All types of
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object are possibly supported.  **Example:**      The following example sets a value to an input of the reference: The input is a point and its name is Input1.

```VBScript
     InstanceFactory.PutInputData "Input1",point1

```