# CATBaseDispatch (Object)

**_Base class for Automation interfaces._**

**Role** : All Automation interfaces must inherit from the `CATBaseDispatch` interface. They usually do not inherit directly from `CATBaseDispatch`, but rather from one of its subclasses: [AnyObject](../System/interface_AnyObject_17321.md) for individual objects or [Collection](../System/interface_Collection_22150.md) for collection objects. Some methods may however have arguments of type `CATBaseDispatch` when they accept both individual objects or collection objects. The interface provides no functionalities per se.