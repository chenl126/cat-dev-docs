# Items (Collection)

**_The collection of items related to the current activity._**

## Methods

### Func **Add**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iProduct`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method adds the specified item in the current list

**Parameters:**

` iItem`      The item to add
**Returns:**      oitem The item  
### Func **AddByAssignmentType**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iItem`,  [ItemAssignmentType](../DMAPSInterfaces/enum_ItemAssignmentType_69816.md)  `iAssignmentType`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method Assigns the specified item with the specified assignment type

**Parameters:**

` iItem`      The item to be assigned
` iAssignmentType`      Type of the Assignment (Item to the Process)
**Returns:**      oitem The item  
### Func **CountByAssignmentType**( [ItemAssignmentType](../DMAPSInterfaces/enum_ItemAssignmentType_69816.md)  `iAssignmentType`) As long

This method returns the Number of items that assocated with the activity with given Assignment Type.

**Parameters:**

` iAssignmentType`      Type of the Assignment between items & the activity
**Returns:**      oNbItems No. of Items that are assigned to the activity with the given assignment type.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method returns the idl object Item for the specified item identifier.

**Parameters:**

` iIndex`      The item identifier
**Returns:**      oItem The idl item  
### Func **ItemByAssignmentType**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [ItemAssignmentType](../DMAPSInterfaces/enum_ItemAssignmentType_69816.md)  `iAssignmentType`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method returns the item assocated with the activity with given Assignment Type.

**Parameters:**

` iAssignmentType`      Type of the Assignment between item & the activity
**Returns:**      oItem idl item to be returned  
### Func **RemoveByAssignmentType**( [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)  `iItem`,  [ItemAssignmentType](../DMAPSInterfaces/enum_ItemAssignmentType_69816.md)  `iAssignmentType`) As [CATIAItem](../DMAPSInterfaces/interface_Item_3684.md)

This method used to unassign the specified item (with the given assignment type)

**Parameters:**

` iItem`      The item to be Unassigned
` iAssignmentType`      Type of the Assignment (Item to the Process) to be removed
**Returns:**      oitem The item