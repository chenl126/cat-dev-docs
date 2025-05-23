# Resource (Object)

**_The object that represents a resource._**

It also allows to get the real resource object.

## Properties

### Property **ChildrenTSAs**(| ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

   This property returns the interface which manages the children TSA of the given resource/system.  
### Property **InputProducts**( ) As [CATIAItems](../DMAPSInterfaces/interface_Items_5808.md) (Read Only)

   This property returns the interface which manages the items or input products/components assigned to the given resource/system  
### Property **NextResources**( ) As [CATIAResourceCollection](../DMAPSInterfaces/interface_ResourceCollection_69820.md) (Read Only)

   This property returns the interface which manages the downstream product flow hierarchy on the given resource. This returns the collection of resources which are "Next" to the given resource in the resource product flow links  
### Property **OutputProducts**( ) As [CATIAOutputs](../DMAPSInterfaces/interface_Outputs_11794.md) (Read Only)

   This property returns the interface which manages the output products/components of the given resource/system  
### Property **PreviousResources**( ) As [CATIAResourceCollection](../DMAPSInterfaces/interface_ResourceCollection_69820.md) (Read Only)

   This property returns the interface which manages the upstream product flow hierarchy on the given resource. This returns the collection of resources which are "Previous" to the given resource in the resource product flow links  Methods

### Func **GetObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iInterfaceName`) As [CATIABase](../System/interface_AnyObject_17321.md)

   This method returns the IDL Interface for the specified interface identifier.

**Parameters:**

` iInterfaceName`      The name of the interface to query.
` oObject`      The pointer to the queried interface.