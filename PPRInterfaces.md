# PPRInterfaces Framework

## Object Index

  * [PPRActivity](PPRInterfaces/interface_PPRActivity_26061.md)
  * [PPRDocument](PPRInterfaces/interface_PPRDocument_25569.md)
  * [PPRProducts](PPRInterfaces/interface_PPRProducts_26022.md)

---

# PPRActivity (Object)

**_The interface is used to retrieve the items and resources of the current Activity._**

## Properties

### Property **PPRItems**( ) As [CATIAPPRProducts](../PPRInterfaces/interface_PPRProducts_26022.md) (Read Only)

   Retrieves the list of items as Products aggregated by the Activity.

**Returns:**      The list of items of the current Activity.  
### Property **PPRResources**( ) As [CATIAPPRProducts](../PPRInterfaces/interface_PPRProducts_26022.md) (Read Only)

   Retrieves the list of resources as Products aggregated by the Activity.

**Returns:**      The list of resources of the current Activity.

---

# PPRDocument (Object)

**_This interface is used to access Processes, Products and Resources._**

## Properties

### Property **Processes**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

   Retrieves the list of Processes as Activities contained in the current document.

**Returns:**      The list of Activities contained in the current document.  
### Property **Products**( ) As [CATIAPPRProducts](../PPRInterfaces/interface_PPRProducts_26022.md) (Read Only)

   Retrieves the list of Products contained in the current document.

**Returns:**      The list of Products contained in the current document.  
### Property **Resources**( ) As [CATIAPPRProducts](../PPRInterfaces/interface_PPRProducts_26022.md) (Read Only)

   Retrieves the list of Resources contained in the current document.

**Returns:**      The list of Resources contained in the current document.

---

# PPRProducts (Collection)

**_This interface is used to retrieve and add Products from and to the list of Products._**

## Methods

### Func **Add**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Adds the specified Product to the current list of Products.

**Parameters:**

` iProduct`      The Product to be added.

**Returns:**      The added Product.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)

   Retrieves the Product corresponding to the specified index in the list of Products.

**Parameters:**

` iIndex`      The index in the Product list.

**Returns:**      The retrieved Product corresponding to the specified index.