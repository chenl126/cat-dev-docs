# DMAPSInterfaces Framework

## Object Index

  * [Activities](DMAPSInterfaces/interface_Activities_22374.md)
  * [Activity](DMAPSInterfaces/interface_Activity_14822.md)
  * [Item](DMAPSInterfaces/interface_Item_3684.md)
  * [Items](DMAPSInterfaces/interface_Items_5808.md)
  * [LibTabSettingAtt](DMAPSInterfaces/interface_LibTabSettingAtt_53228.md)
  * [Outputs](DMAPSInterfaces/interface_Outputs_11794.md)
  * [ProcessDocument](DMAPSInterfaces/interface_ProcessDocument_49006.md)
  * [Resource](DMAPSInterfaces/interface_Resource_14406.md)
  * [ResourceCollection](DMAPSInterfaces/interface_ResourceCollection_69820.md)
  * [Resources](DMAPSInterfaces/interface_Resources_18351.md)
  * [TreeTabSettingAtt](DMAPSInterfaces/interface_TreeTabSettingAtt_60372.md)
  * [VerifTabSettingAtt](DMAPSInterfaces/interface_VerifTabSettingAtt_67728.md)

## Enumerated Types Index

  * [ItemAssignmentType](DMAPSInterfaces/enum_ItemAssignmentType_69816.md)

---

# ItemAssignmentType (Enumeration)

**_The Analysis Level setting attribute range of values._**

**Values:**

` ProcessProcesses`      Assignment type is Process Processes Item/Product
` ProcessFirstProcesses`      Assignment type is Process First Processes Item/Product
` ProcessRemoves`      Assignment type is Process Removes Item/Product
` ProcessImplementsRequirementPartial`      Assignment type is Process Implements Requirement(Partial)with Item/Product
` ProcessImplementsRequirementComplete`      Assignment type is Process Implements Requirement(Complete)with Item/Product

---

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

---

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

---

# Item (Object)

**_The object that represents an item._**

---

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

---

# LibTabSettingAtt (Object)

**__**

## Methods

### Sub **GetIDUniqueSetting**( long  `oIsUnique`)

   Retrieves the option which enables to check ID uniqueness amongst sibling processes

**Role** : Retrieves the option which enables to check ID uniqueness amongst sibling processes

**Parameters:**

` oIsUnique`      Flag indicating whether the check should be enabled or not

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetIDUniqueSettingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Unique Check' parameter.

**Role** :Retrieves the state of the 'Unique Check' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetListOfLibraryFilePath**( ) As [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)

   Retrieves the List of Libraries that are used in the Process document

**Role** : Retrieves the List of Libraries that are used in the Process document

**Parameters:**

` ioPath`      a CATSafeArrayVariant of CATBSTR that has the list of libraries

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetListOfLibraryFilePathInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves the information about the list of libraries path that are used in the Process document

**Role** :Retrieves the information about the list of libraries path that are used in the Process document

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetProcessIDScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oPath`)

   Retrieves the path of custom VB script to generate process ID

**Role** : Retrieves the path of custom VB script to generate process ID

**Parameters:**

` oPath`      The output path of the custom VB script

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetProcessIDScriptInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves the information about the custom VB script path that are used in the Process document

**Role** :Retrieves the information about the custom VB script path that are used in the Process document

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **PutListOfLibraryFilePath**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iPath`)

   Sets a List of Libraries that are used in the Process document

**Role** : Sets the List of Libraries that are used in the Process document

**Parameters:**

` iPath`      a CATSafeArrayVariant of CATBSTR that has the list of libraries.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetIDUniqueSetting**( long  `isUnique`)

   Sets the option which enables to check ID uniqueness amongst sibling processes

**Role** : Sets the option which enables to check ID uniqueness amongst sibling processes

**Parameters:**

` isUnique`      Sets the option to enable uniqueness check or not

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetIDUniqueSettingLock**( boolean  `iLocked`)

   Locks or unlocks the "Unique Check" parameter.

**Role** : Locks or unlocks the 'Unique Check' parameter if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`1 :` to lock the parameter.
`0:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetListOfLibraryFilePathLock**( boolean  `iLocked`)

   Locks or unlocks the list of libraries to be used

**Role** :Locks or unlocks the "list of libraries" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetProcessIDScript**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

   Sets the path of custom VB script to generate process ID

**Role** : Sets the path of custom VB script to generate process ID

**Parameters:**

` iPath`      Path of the custom VB script to be set

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetProcessIDScriptLock**( boolean  `iLocked`)

   Locks or unlocks the "Custom VB Script" parameter.

**Role** : Locks or unlocks the 'Custom VB Script' parameter if the operation is allowed in the current administrated environment. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`1 :` to lock the parameter.
`0:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure

---

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

---

# ProcessDocument (Object)

**_This interface is used to access the PPRDocument and to add a new library._**

## Properties

### Property **PPRDocument**( ) As [CATBaseDispatch](../System/interface_CATBaseDispatch_45333.md) (Read Only)

   Retrieves the interface which manages the PPRDocument.

**Returns:**      The PPRDocument corresponding to the current Process document.  Methods

### Sub **AddLibrary**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`)

   Adds a new library to the current Process document.

**Parameters:**

` iFileName`      The name of the library to be added.

---

# Resource (Object)

**_The object that represents a resource._**

It also allows to get the real resource object.

## Properties

### Property **ChildrenTSAs**( ) As [CATIAActivities](../DMAPSInterfaces/interface_Activities_22374.md) (Read Only)

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

---

# ResourceCollection (Collection)

**_Interface representing collection of Resources._**

**Role** : Components that implement CATIAResourceCollection are ...

Do not use the CATIAResourceCollection interface for such and such ClassReference, Class#MethodReference, #InternalMethod...

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAResource](../DMAPSInterfaces/interface_Resource_14406.md)

   This method gets the specified resource from the given resource collection management.

**Parameters:**

` iIndex`      The resource identifier

**Returns:**      oResource The resource

---

# Resources (Collection)

**_The collection of resources related to the current activity._**

## Methods

### Func **Add**( [CATIAResource](../DMAPSInterfaces/interface_Resource_14406.md)  `iResource`) As [CATIAResource](../DMAPSInterfaces/interface_Resource_14406.md)

   This method add the specified item in the current list

**Parameters:**

` iItem`      The item to add

**Returns:**      oitem The item  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAResource](../DMAPSInterfaces/interface_Resource_14406.md)

   This method returns the idl object Resource for the specified resource identifier.

**Parameters:**

` iIndex`      The resource identifier

**Returns:**      oResource The idl resource

---

# TreeTabSettingAtt (Object)

**__**

## Properties

### Property **ApplicativeDataFilter**( ) As long

   Returns of sets the value to signify Whether "Applicative Data" created by an application is visible in the PPR tree

**Role** : Returns or sets the value of "Applicative Data" option to signify whether the applicative containers are visualized in the PPR tree  
### Property **AssignedViewer**( ) As long

   Returns or sets the value to signify whether the 3D Assigned Viewer is default viewer or not

**Role** : Returns or sets the value to signify whether 3D Assigned Viewer is default viewer or not  
### Property **AttributesFilter**( ) As long

   Returns or sets the value for "Attributes" option

**Role** : Returns or sets the value of "Attributes" option to signify whether the 'User Attributes' of an Activity is visualized in the PPR tree  
### Property **CollapseExpandFilter**( ) As long

   Returns or sets the value to signify Whether the double clicking on an activity expands/collapses a given activity in the PPR tree

**Role** : Returns or sets the value to signify Whether the double clicking on an activity expands/collapses a given activity in the PPR tree  
### Property **DisplayNameMode**( ) As long

   Returns or sets the value to signify whether the E5 Configured Name is to be displayed

**Role** : Returns or sets the value to signify whether the E5 Configured Name is to be displayed  
### Property **DisplayOrder**( ) As long

   Returns or sets the value for 'Display Order'

**Role** : Returns or sets the value of 'Display Order' to signify which order the product/resource list are in the PPR tree  
### Property **ItemsFilter**( ) As long

   Returns or sets the value for 'Items Folder'

**Role** : Returns or sets the value of 'Items Folder' to signify whether the 'Assigned Items' are visualized in the PPR tree  
### Property **ItemsPerRelationFilter**( ) As long

   Returns or sets the value for 'Items Folder (Per Relation Type)'

**Role** : Returns or sets the value of 'Items Folder(Per Relation Type)' to signify whether the 'Assigned Items'with proper relations ( like First Processes Product) are visualized in the PPR tree  
### Property **LogicalActFilter**( ) As long

   Returns or sets the value to signify Whether the logical activites are visible in the PPR tree

**Role** : Returns or sets the value of "Logical Activities" option to signify whether the logical activites are visible in the PPR tree  
### Property **OutputProductFilter**( ) As long

   Returns of sets the value to signify Whether "Output Products" assigned to a given activity is visible in the PPR tree

**Role** : Returns or sets the value of "Output Products Folder" option to signify whether the output products associated with an activity are visualized in the PPR tree  
### Property **RenderStyle**( ) As long

   Returns or sets the value to signify whether the 3D Render Style is Parallel or Perspective

**Role** : Returns or sets the value to signify whether the 3D Render Style is Parallel or Perspective  
### Property **ResourceFilter**( ) As long

   Returns or sets the value for 'Resources Folder'

**Role** : Returns or sets the value of 'Resources Folder' to signify whether the 'Assigned Resources' are visualized in the PPR tree  Methods

### Func **GetApplicativeDataFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Applicative Data" parameter.

**Role** :Retrieves the state of the "Applicative Data" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAssignedViewerInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Assigned Viewer" parameter.

**Role** :Retrieves the state of the "Assigned Viewer" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAttributesFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Attributes" parameter.

**Role** :Retrieves the state of the "Attributes" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCollapseExpandFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Disable Collapse/Expand" parameter.

**Role** :Retrieves the state of the "Disable Collapse/Expand" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayNameModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Display Name Mode" parameter.

**Role** :Retrieves the state of the "Display Name Mode" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayOrderInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Display Order' parameter.

**Role** :Retrieves the state of the 'Display Order' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetItemsFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Items Folder' parameter.

**Role** :Retrieves the state of the 'Items Folder' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetItemsPerRelationFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Items Folder(Per Relation Type)' parameter.

**Role** :Retrieves the state of the 'Items Folder(Per Relation Type)' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLogicalActFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Logical Activities" parameter.

**Role** :Retrieves the state of the "Logical Activities" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetOutputProductFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Output Products Folder" parameter.

**Role** :Retrieves the state of the "Output Products Folder" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetRenderStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Render Style" parameter.

**Role** :Retrieves the state of the "Render Style" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the 'Resource Folder' parameter.

**Role** :Retrieves the state of the 'Resource Folder' parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetApplicativeDataFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Applicative Data" parameter.

**Role** :Locks or unlocks the "Attributes" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAssignedViewerLock**( boolean  `iLocked`)

   Locks or unlocks the "Assigned Viewer" parameter.

**Role** :Locks or unlocks the "Assigned Viewer" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAttributesFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Attributes" parameter.

**Role** :Locks or unlocks the "Attributes" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCollapseExpandFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Disable Collapse/Expand" parameter.

**Role** :Locks or unlocks the "Disable Collapse/Expand" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayNameModeLock**( boolean  `iLocked`)

   Locks or unlocks the "Display Name Mode" parameter.

**Role** :Locks or unlocks the "Display Name Mode" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayOrderLock**( boolean  `iLocked`)

   Locks or unlocks the 'Display Order' parameter.

**Role** :Locks or unlocks the 'Display Order' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetItemsFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Items Folder' parameter.

**Role** :Locks or unlocks the 'Items Folder' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetItemsPerRelationFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Items Folde(Per Relation Type)r' parameter.

**Role** :Locks or unlocks the 'Items Folder(Per Relation Type)' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLogicalActFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Logical Activities" parameter.

**Role** :Locks or unlocks the "Logical Activities" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetOutputProductFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Output Products Folder" parameter.

**Role** :Locks or unlocks the "Output Products Folder" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetRenderStyleLock**( boolean  `iLocked`)

   Locks or unlocks the "Render Style" parameter.

**Role** :Locks or unlocks the "Render Style" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the 'Resource Folder' parameter.

**Role** :Locks or unlocks the 'Resource Folder' parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# VerifTabSettingAtt (Object)

**__**

## Properties

### Property **AllResourceFilter**( ) As long

   Returns or sets the value to signify Whether all the resources will appear during Process Navigation

**Role** : Returns or sets the value to signify Whether all the resources will appear during Process Navigation  
### Property **AutoReframeFilter**( ) As long

   Returns or sets the value to signify Whether the 'Auto Reframe' will happen during Process navigation

**Role** : Returns or sets the value to signify Whether all the items/resources will be reframed during Process Navigation  
### Property **ImpliedResourceFilter**( ) As long

   Returns or sets the value to signify Whether the Assigned resource will appear during Process Navigation

**Role** : Returns or sets the value to signify Whether all the Assigned resource will appear during Process Navigation  Methods

### Func **GetAllResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "View All Resources" parameter.

**Role** :Retrieves the state of the "View All Resources" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetAutoReframeFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "Auto Reframe" parameter.

**Role** :Retrieves the state of the "Auto Reframe" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImpliedResourceFilterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the "View Implied Resource" parameter.

**Role** :Retrieves the state of the "View Implied Resource" parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAllResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "View All Resources" parameter.

**Role** :Locks or unlocks the "View All Resources" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetAutoReframeFilterLock**( boolean  `iLocked`)

   Locks or unlocks the "Auto Reframe" parameter.

**Role** :Locks or unlocks the "Auto Reframe" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImpliedResourceFilterLock**( boolean  `iLocked`)

   Locks or unlocks the Xxx parameter.

**Role** :Locks or unlocks the "View Implied Resource" parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.