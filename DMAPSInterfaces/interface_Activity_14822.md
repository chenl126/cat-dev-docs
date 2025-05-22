# Activity (Object)

**_The object that represents an activity._**

It groups the most important methods related to an activity and enables to get the management interfaces (hierarchy management, control flow management, * ...).

## Properties

### Property **AttrCount**( ) As long (Read Only)

This property returns the number of attributes of the current activity.

**Returns:**      oNbAttr The number of attributes  
### Property **BeginningDate**( ) As double

This property returns the beginning date of the current activity.

**Returns:**      oBegin The beginning date of the current activity  
### Property **CalculatedBeginTime**( ) As double (Read Only)

This property returns and calculated time cyle on the current activity.

**Returns:**      oCBT The calculated begin time of the current activity  
### Property **CalculatedCycleTime**( ) As double (Read Only)

This property returns and sets the calculated time cyle on the current activity.

**Returns:**      oCCT The calculated time cycle of the current activity  
### Property **ChildrenActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns the interface which manages the children hierarchy on the activity.  
### Property **CycleTime**( ) As double

This property returns and set the time cyle on the current activity.

**Returns:**      oCT The time cycle of the current activity  **Parameters:**

` iCT`      The specified time cycle of the current activity

### Property **Description**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

This property returns and set the description on the current activity.

**Returns:**      oDescriptionBSTR The description of the current activity  **Parameters:**

` iDescriptionBSTR`      The specified description of the current activity

### Property **EndDate**( ) As double (Read Only)

This property returns the end date of the current activity.

**Returns:**      oEnd The end date of the current activity. Till V5R13, this method is returning S_OK even if there is no good implementation. Starting from V5R14 this method will return E_NOIMPL. Hence all the scripts that use this method would have to be updated to accomodate this change.  
### Property **Items**( ) As [CATIAItems](../DMAPSInterfaces/interface_Items_5808.md) (Read Only)

This property returns the interface which manages the items or input products/components assigned to the current activity  
### Property **NextCFActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns the interface which manages the downstream control flow hierarchy on the activity.  
### Property **NextPRFActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns the interface which manages the downstream product flow hierarchy on the activity.  
### Property **Outputs**( ) As [CATIAOutputs](../DMAPSInterfaces/interface_Outputs_11794.md) (Read Only)

This property returns the interface which manages the output products/components of the current activity  
### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

This property returns the interface which manages the knowlegde parameters of the activity.  
### Property **PossiblePrecedenceActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns list of Possible Precedence Activities defined on Current Activity.

**Parameters:**

` oActivities`      List of Activities that must precede the Current Activity

### Property **PrecedenceActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns list of Precedence Activities defined on Current Activity.

**Parameters:**

` oActivities`      List of Activities that must precede the Current Activity

### Property **PreviousCFActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns the interface which manages the upstream control flow hierarchy on the activity.  
### Property **PreviousPRFActivities**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

This property returns the interface which manages the upstream product flow hierarchy on the activity.  
### Property **ProcessID**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

This property returns process identifier on the current activity.

**Parameters:**

` oProcessID`      The process ID of the current activity

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

This property returns the interface which manages the knowlegde relations of the activity.  
### Property **Resources**( ) As [CATIAResources](../DMAPSInterfaces/interface_Resources_18351.md) (Read Only)

This property returns the interface which manages the resources hierarchy on the activity.  
### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

This method returns the type of the current activity.

**Parameters:**

` oType`      The type of the current activity
Methods

### Func **AttrName**( long  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

This method returns the name for the specified attribute.

**Parameters:**

` iIndex`      The attribute index
` oName`      The attribute name

### Func **AttrValue**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATVariant](../System/typedef_CATVariant_20656.md)

This method returns the value for the specified attribute.

**Parameters:**

` iIndex`      The attribute identifier
**Returns:**      oAttVal The attribute value  
### Func **CreateChild**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeOfChild`) As [CATIAActivity](../DMAPSInterfaces/interface_Activity_14822.md)

This method creates a new child activity of the requested type.

**Parameters:**

` iTypeOfChild`      The type of the child activity to create.
` oCreatedChild`      The new created child activity.

### Sub **CreateLink**( [CATIAActivity](../DMAPSInterfaces/interface_Activity_14822.md)  `iSecondActivity`)

This method creates a link from the current activity to another activity.

**Parameters:**

` iSecondActivity`      The activity that will be linked to the current activity.

### Func **GetTechnologicalObject**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iApplicationType`) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md)

Returns the process's applicative data which type is the given parameter. The data returned can be either a collection or a simple object.

**Parameters:**

` iApplicationType`      The type of applicative data searched.
**Example:**      This example retrieves the GraphEditor position for the `Loading1` activity.

```VBScript
Dim GEPosition
Set GEPosition = Loading1.GetTechnologicalObject("GEPosition")

```

### Func **IsSubTypeOf**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As boolean

This method allows to test the type of a specific activity.

**Parameters:**

` iName`      The name of the type to test
**Returns:**      oVal The logical value returned by the test  
### Sub **RemoveLink**( [CATIAActivity](../DMAPSInterfaces/interface_Activity_14822.md)  `iSecondActivity`)

This method removes a link existing on the current activity.

**Parameters:**

` iSecondActivity`      The activity on which the link will be removed.

### Sub **SetProcessID**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iProcessID`,  boolean  `iCheckUnique`)

Sets the process ID of the current activity

**Parameters:**

` iProcessID`      Input Process ID string
` iCheckUnique`      Option to enable uniqueness check