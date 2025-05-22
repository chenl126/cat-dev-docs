# Activities (Collection)

**_The collection of activities related to the current activity._**

It respectively manages the children hierarchy, the downstream control flow, the uptream control flow, the downstream product flow or the upstream product flow.

## Methods

### Sub **Add**( [CATIAActivity](../DMAPSInterfaces/interface_Activity_14822.md)  `iActivity`)

This method adds the specified activity as a precedence constraint

**Parameters:**

` iActivity`      The activity Handle

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAActivity](../DMAPSInterfaces/interface_Activity_14822.md)

This method gets the specified activity on the current activities management.

**Parameters:**

` iIndex`      The activity identifier
**Returns:**      oActivity The activity  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

This method removes the specified activity on the current activities management.

**Parameters:**

` iIndex`      The activity identifier