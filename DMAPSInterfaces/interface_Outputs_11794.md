# Outputs (Collection)

**_The collection of outputs related to the current activity._**

## Methods

### Func **Add**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iOutput`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method can be used to assign a given product as an output

**Parameters:**

` iOutput`      The output to add
**Returns:**      oProduct The assigned product  
### Func **Count**( ) As long

This method returns the no. of products / features that are assigned to a process as output.

**Returns:**      oNbOutputs No. of Outputss that are assigned to the activity.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method can be used to get the associated output product.

**Parameters:**

` iIndex`      The item identifier (can be the index or the name)
**Returns:**      oProduct The indexed product/MA that is assigned to the process.  
### Func **Remove**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iOutput`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method can be used to unassign an output product from a process

**Parameters:**

` iProduct`      The product to remove
**Returns:**      oProduct The item