# CATFunctSystemItf Framework

## Object Index

  * [FunctActionsGroup](CATFunctSystemItf/interface_FunctActionsGroup_62338.md)
  * [FunctActionsGroups](CATFunctSystemItf/interface_FunctActionsGroups_70306.md)
  * [FunctAssociation](CATFunctSystemItf/interface_FunctAssociation_55448.md)
  * [FunctAssociations](CATFunctSystemItf/interface_FunctAssociations_62974.md)
  * [FunctFacetManagers](CATFunctSystemItf/interface_FunctFacetManagers_67638.md)
  * [FunctGenScriptMgr](CATFunctSystemItf/interface_FunctGenScriptMgr_60579.md)
  * [FunctMultiRepMgr](CATFunctSystemItf/interface_FunctMultiRepMgr_53716.md)
  * [FunctNodeGraphLayout](CATFunctSystemItf/interface_FunctNodeGraphLayout_84548.md)
  * [FunctScript](CATFunctSystemItf/interface_FunctScript_26659.md)
  * [FunctScripts](CATFunctSystemItf/interface_FunctScripts_31940.md)
  * [FunctionalAction](CATFunctSystemItf/interface_FunctionalAction_54696.md)
  * [FunctionalActions](CATFunctSystemItf/interface_FunctionalActions_62210.md)
  * [FunctionalDescription](CATFunctSystemItf/interface_FunctionalDescription_95375.md)
  * [FunctionalDocument](CATFunctSystemItf/interface_FunctionalDocument_69860.md)
  * [FunctionalElement](CATFunctSystemItf/interface_FunctionalElement_61851.md)
  * [FunctionalFacet](CATFunctSystemItf/interface_FunctionalFacet_47340.md)
  * [FunctionalFacetMgr](CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)
  * [FunctionalObject](CATFunctSystemItf/interface_FunctionalObject_54328.md)
  * [FunctionalObjectProxy](CATFunctSystemItf/interface_FunctionalObjectProxy_94928.md)
  * [FunctionalObjects](CATFunctSystemItf/interface_FunctionalObjects_61835.md)
  * [FunctionalPosition](CATFunctSystemItf/interface_FunctionalPosition_70756.md)
  * [FunctionalSystemSettingAtt](CATFunctSystemItf/interface_FunctionalSystemSettingAtt_144326.md)
  * [FunctionalVariant](CATFunctSystemItf/interface_FunctionalVariant_62254.md)
  * [FunctionalVariants](CATFunctSystemItf/interface_FunctionalVariants_70232.md)

## Enumerated Types Index

  * [CATFunctOrientationDirection](CATFunctSystemItf/enum_CATFunctOrientationDirection_164048.md)

---

# CATFunctOrientationDirection (Enumeration)

**_The qualifications of Orientation and Direction of a Functional Action._**

* * When NotOriented, no distinction is made between the two Elements the Action is connected on.
Graphically,they are connected by a line without any arrow.
(but they still have to be accessed thru the "From" and "To" properties)
_Such qualification is used when the Action is in fact a relationship that points the Elements
(a Welding relationship might be used to point 2 Entities : Flange and Stiffener)_
* When Oriented, there are two possibilities :

  * When Unidirectional, the "From" and "To" Elements are connected by a simple arrow matching the direction.
_Such qualification is used when the Action is a true Subject-Action-Object relationship.
(a Welding relationship might be used to point 2 Entities : Flange and Stiffener)_
  * When Bidirectional, they are connected by a double arrow, that avoids to create two symetrical unidirectional actions with the same identification.
_Such qualification is used when the Action is a true Subject-Action-Object relationship.
(a Heating relationship might be used to point 2 Entities : DiskBrake and BrakeJaws)_

---

# FunctActionsGroup (Object)

**_The interface to access a group of functional actions in a system._**

## Properties

### Property **ActionsCount**( ) As long (Read Only)

   Get the count of actions referenced by the actions' group.  Methods

### Sub **Add**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

   Adds an action to the actions' group.  Fails if the action :

  * is already in a group
  * has "From" and "To" extremities inconsistent with the existing actions.
In case of an ordered group, the added action will be appended.
(i.e. for flows sequencing actions)

**Parameters:**

` iAction`      The action to be added to the group of actions.

### Sub **GetExtremities**( double  `oInputX`,  double  `oInputY`,  double  `oOutputX`,  double  `oOutputY`)

   Get coordinates of Input and Output extremities.  
### Sub **Remove**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

   Removes an action from the actions' group.

**Parameters:**

` iAction`      The action to be removed from the group of actions.

### Sub **RemovePosition**( long  `iPosition`)

   Removes an action from the actions' group.

**Parameters:**

` iPosition`      The position of the action to be removed from the group of actions.

### Func **Retrieve**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

   Returns an action using its index or its name from the actions group.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the group of actions. As a numerics, this index is the rank of the action in the group. The index of the first action in the group is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth action in the group and in `Obj2` the action named `Valve`.

```VBScript
     Dim Act1 As FunctionalAction
     Set Act1 = ActionsGrp.Retrieve(5)
     Dim Act2 As FunctionalAction
     Set Act2 = ActionsGrp.Retrieve("Reduces noise")

```

### Sub **SetExtremities**( double  `iInputX`,  double  `iInputY`,  double  `iOutputX`,  double  `iOutputY`)

   Set coordinates of Input and Output extremities.

---

# FunctActionsGroups (Collection)

**_The interface to access the groups of functional actions in a system._**

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  double  `iInputX`,  double  `iInputY`,  double  `iOutputX`,  double  `iOutputY`) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)

   Create a Group of Actions.  
### Sub **Delete**( [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)  `iActGrp`)

   Delete a Group of Actions.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md)

   Returns an actions'group using its index or its name from the actions' groups collection.

**Parameters:**

` iIndex`      The index or the name of the actions'group to retrieve from the collection of actions' groups. As a numerics, this index is the rank of the actions' group in the collection. The index of the first actions' group in the collection is 1, and the index of the last actions' group is Count. As a string, it is the name you assigned to the actions' group using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `AG1` the fifth actions' group in the collection and in `AG2` the actions' group named `Transmission`.

```VBScript
     Dim AG1 As FunctActionsGroup
     Set AG1 = ActionsGroups.Elem(5)
     Dim AG2 As FunctActionsGroup
     Set AG2 = ActionsGroups.Elem("Transmission")

```

---

# FunctAssociation (Object)

**_The interface to access a Functional Association._**

It is managed on a Functional Element, thru the MultiRep Facet Manager (MRM).

## Properties

### Property **LinkedCount**( ) As long (Read Only)

   Get count of linked objects.  Methods

### Sub **DetachFrom**( [CATIABase](../System/interface_AnyObject_17321.md)  `iLinked`)

   Delete a link to a linked object.  
### Sub **LinkTo**( [CATIABase](../System/interface_AnyObject_17321.md)  `iLinked`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iKind`)

   Create a link to another object.  
### Func **RetrieveKindOfLinked**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieve the kind of linked object.  
### Func **RetrieveLinked**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

   Retrieve a linked object.

---

# FunctAssociations (Collection)

**_The interface to access a set of Functional Associations._**

It is managed on a Functional Element, thru the MultiRep Facet Manager (MRM).

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)

   Create a FunctAssociation.  
### Sub **Delete**( [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)  `iAssociation`)

   Delete a FunctAssociation.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctAssociation](../CATFunctSystemItf/interface_FunctAssociation_55448.md)

   Returns an association using its index or its name from the associations collection.

**Parameters:**

` iIndex`      The index or the name of the association to retrieve from the collection of associations. As a numerics, this index is the rank of the association in the collection. The index of the first association in the collection is 1, and the index of the last association is Count. As a string, it is the name you assigned to the association using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved association **Example:**      This example retrieves in `Act1` the fifth association in the collection and in `Act2` the association named `Moves`.

```VBScript
     Dim FunctElem As FunctionalObject
     Set FunctElem = FunctDoc.CurrentDescription.Objects.Elem("Valve")
     Dim FacetMRM As FunctionalMultiRepMgr
     Set FacetMRM = FunctElem.GetFacetByName("MRM")
     Dim Assoc1 As FunctAssociation
     Set Assoc1 = FacetMRM.Associations.Elem(5)
     Dim Assoc2 As FunctAssociation
     Set Assoc2 = FacetMRM.Associations.Elem("Skeleton 2D")

```

---

# FunctFacetManagers (Collection)

**_Represents the Functional Facet's Managers._**

## Methods

### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)

   Returns a facet manager using its index or its name from the facet managers collection.

**Parameters:**

` iIndex`      The index or the name of the facet manager to retrieve from the collection of facet managers. As a numerics, this index is the rank of the facet manager in the collection. The index of the first facet manager in the collection is 1, and the index of the last facet manager is Count. As a string, it is the name you assigned to the facet manager using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth facet manager in the collection and in `Obj2` the facet manager named `IMC`.

```VBScript
     Dim Obj1 As FunctFacetManager
     Set Obj1 = Desc.FacetManagers.Elem(5)
     Dim Obj2 As FunctFacetManager
     Set Obj2 = Desc.FacetManagers.Elem("IMC")

```

---

# FunctGenScriptMgr (Object)

**_The interface to access a Functional GenerativeScripts manager._**

## Properties

### Property **CurrentScript**( ) As long

   Get the CurrentScript.  
### Property **Scripts**( ) As [CATIAFunctScripts](../CATFunctSystemItf/interface_FunctScripts_31940.md) (Read Only)

   Get the Generative Scripts collection.

---

# FunctionalAction (Object)

**_The interface to access a Functional Action._**

## Properties

### Property **From**( ) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

   Get the From object.  
### Property **Group**( ) As [CATIAFunctActionsGroup](../CATFunctSystemItf/interface_FunctActionsGroup_62338.md) (Read Only)

   Get the Group property.  Vary when adding/removing the action to/from a group.  
### Property **OrientationDirection**( ) As [CATFunctOrientationDirection](../CATFunctSystemItf/enum_CATFunctOrientationDirection_164048.md)

   Get the OrientationDirection property.

**See also:**      [CATFunctOrientationDirection](../CATFunctSystemItf/enum_CATFunctOrientationDirection_164048.md) 
### Property **To**( ) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

   Get the To object.  Methods

### Func **GetFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Func **GetFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Sub **InvertDirection**( )

   Invert the action's Direction.  Fails if the action is included in a group.  
### Func **SearchFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.  
### Func **SearchFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.

---

# FunctionalActions (Collection)

**_The interface to access a collection of FunctionalActions._**

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)  `iFrom`,  [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)  `iTo`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

   Create a FunctionalAction.  
### Sub **Delete**( [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)  `iAction`)

   Delete a FunctionalAction.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalAction](../CATFunctSystemItf/interface_FunctionalAction_54696.md)

   Returns an action using its index or its name from the actions collection.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the collection of actions. As a numerics, this index is the rank of the action in the collection. The index of the first action in the collection is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Act1` the fifth action in the collection and in `Act2` the action named `Moves`.

```VBScript
     Dim Act1 As FunctionalAction
     Set Act1 = Desc.Action(5)
     Dim Act2 As FunctionalAction
     Set Act2 = Desc.Action("Moves")

```

---

# FunctionalDescription (Object)

**_The interface to access a Functional Description._**

## Properties

### Property **Actions**( ) As [CATIAFunctionalActions](../CATFunctSystemItf/interface_FunctionalActions_62210.md) (Read Only)

   Get the Actions collection.  
### Property **ActionsGroups**( ) As [CATIAFunctActionsGroups](../CATFunctSystemItf/interface_FunctActionsGroups_70306.md) (Read Only)

   Get the ActionsGroups collection.  
### Property **Objects**( ) As [CATIAFunctionalObjects](../CATFunctSystemItf/interface_FunctionalObjects_61835.md) (Read Only)

   Get the Objects collection.  
### Property **Variants**( ) As [CATIAFunctionalVariants](../CATFunctSystemItf/interface_FunctionalVariants_70232.md) (Read Only)

   Get the Variants collection.  (gives a NULL pointer if the description is a itself variant)  Methods

### Func **CreatePosition**( double  `iX`,  double  `iY`) As [CATIAFunctionalPosition](../CATFunctSystemItf/interface_FunctionalPosition_70756.md)

   Create a Position.  To create actions pointing to NULL  
### Func **GetFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Func **GetFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Func **SearchFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.  
### Func **SearchFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.  
### Sub **Unlock**( )

   Unlock.  To remove the protection against modifications.

---

# FunctionalDocument (Object)

**_Represents a Functional Document._**

## Properties

### Property **CurrentDescription**( ) As [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md) (Read Only)

   Returns the Current Description.  
### Property **FacetManagers**( ) As [CATIAFunctFacetManagers](../CATFunctSystemItf/interface_FunctFacetManagers_67638.md) (Read Only)

   Returns the Facet Managers.  
### Property **OriginalDescription**( ) As [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md) (Read Only)

   Returns the Original Description.

---

# FunctionalElement (Object)

**_Represents a Functional Element._**

## Properties

### Property **Document**( ) As [CATIAFunctionalDocument](../CATFunctSystemItf/interface_FunctionalDocument_69860.md) (Read Only)

   Returns the Document.  
### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the parameters collection.

---

# FunctionalFacet (Object)

**_The interface to access a Functional Facet._**

## Properties

### Property **FunctionalElement**( ) As [CATIAFunctionalElement](../CATFunctSystemItf/interface_FunctionalElement_61851.md) (Read Only)

   Get the Functional Element owning the Facet.  Methods

### Sub **Free**( )

   Free the resources allocated by the Facet.  
### Sub **Init**( )

   Init resources for the Facet.

---

# FunctionalFacetMgr (Object)

**_The interface to access a Functional Facet Manager._**

---

# FunctionalObject (Object)

**_The interface to access a Functional Object._**

## Methods

### Func **GetFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Func **GetFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Returns the Facet.  
### Func **SearchFacet**( [CATIAFunctionalFacetMgr](../CATFunctSystemItf/interface_FunctionalFacetMgr_67280.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.  
### Func **SearchFacetByName**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFM`,  boolean  `iCreateIfNecessary`) As [CATIAFunctionalFacet](../CATFunctSystemItf/interface_FunctionalFacet_47340.md)

   Searches the Facet.

---

# FunctionalObjectProxy (Object)

**_The interface to access a Functional ObjectProxy._**

## Properties

### Property **Description**( ) As [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md) (Read Only)

   Get the description attached to the proxi.  Methods

### Sub **set_Description**( [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md)  `iDesc`)

   set the description attached to the proxi.

---

# FunctionalObjects (Collection)

**_Interface to access a collection of FunctionalObjects._**

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)

   Creates a FunctionalObject.  
### Func **CreateProxy**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md)  `iDesc`) As [CATIAFunctionalObjectProxy](../CATFunctSystemItf/interface_FunctionalObjectProxy_94928.md)

   Creates a FunctionalObjectProxi.  
### Sub **Delete**( [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)  `iObject`)

   Deletes a FunctionalObject.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalObject](../CATFunctSystemItf/interface_FunctionalObject_54328.md)

   Returns an action using its index or its name from the actions collection.

**Parameters:**

` iIndex`      The index or the name of the action to retrieve from the collection of actions. As a numerics, this index is the rank of the action in the collection. The index of the first action in the collection is 1, and the index of the last action is Count. As a string, it is the name you assigned to the action using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved action **Example:**      This example retrieves in `Obj1` the fifth object in the collection and in `Obj2` the action named `Valve`.

```VBScript
     Dim Obj1 As FunctionalObject
     Set Obj1 = Desc.Object(5)
     Dim Obj2 As FunctionalObject
     Set Obj2 = Desc.Object("Valve")

```

---

# FunctionalPosition (Object)

**_Represents a Functional Position._**

## Properties

### Property **X**( ) As double (Read Only)

   Returns the X coordinate.  
### Property **Y**( ) As double (Read Only)

   Returns the Y coordinate.  Methods

### Sub **SetCoords**( double  `iX`,  double  `iY`)

   Sets the coordinates.

**Parameters:**

` iX`      the x coordinate.
` iY`      the y coordinate

---

# FunctionalSystemSettingAtt (Object)

**_Enables attribute access to PFD options._**

## Properties

### Property **DocumentContentAtCreation**( ) As long

   Returns or sets the DocumentContentAtCreation parameter.

**Parameters:**

` iDocumentContentAtCreation`      oDocumentContentAtCreation Document Content At Creation Attribute **Legal values** :
`0 :` Sample elements
`1:` empty

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **FunctionalActionPresentation**( ) As long

   Returns or sets the FunctionalActionPresentation parameter.

**Parameters:**

` iDocumentContentAtCreation`      or oDocumentContentAtCreation Functional Action Presentation **Legal values** :
`0 :` A : Action
`1:` SAO : Subject Action Object
`2:` ASO : Action Subject Object

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **ShowParameters**( ) As long

   Returns or sets the ShowParameters parameter.

**Parameters:**

` iShowParameters`      or oShowParameters Show Parameters **Legal values** :
`False :`
`True:`

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **ShowRelations**( ) As long

   Returns or sets the ShowRelations parameter.

**Parameters:**

` iShowRelations`      or oShowRelations Show Relations **Legal values** :
`False :`
`True:`

### Property **ShowSynchroStatusOfLocalParamCache**( ) As long

   Returns or sets the ShowSynchroStatusOfLocalParamCache parameter.

**Parameters:**

` iShowSynchroStatusOfLocalParamCache`      or oShowSynchroStatusOfLocalParamCache Show Synchronisation Status OfLocal Parameter Cache **Legal values** :
`False :`
`True :`

### Property **SplitFunctionalObjectName**( ) As long

   Returns or sets the SplitFunctionalObjectName parameter.

**Parameters:**

` iSplitFunctionalObjectName`      or oSplitFunctionalObjectName **Legal values** :
`False :` don't split functional object name
`True :` split Functional object name

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **StringUsedAsCarriageReturn**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the StringUsedAsCarriageReturn parameter.

**Parameters:**

` iStringUsedAsCarriageReturn`      or oStringUsedAsCarriageReturn String Used As Carriage Return

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Property **TypeOfIconOnFunctionalElement**( ) As long

   Returns or sets the TypeOfIconOnFunctionalElement parameter.

**Parameters:**

` iTypeOfIconOnFunctionalElement`      or oTypeOfIconOnFunctionalElement Type Of Icon On Functional Elements **Legal values** :
`0 :` indicate a current association with PPR links.
`1:` indicate a current generative script.
Methods

### Func **GetDocumentContentAtCreationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DocumentContentAtCreation parameter.

**Role** :Retrieves the state of the DocumentContentAtCreation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetFunctionalActionPresentationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the FunctionalActionPresentation parameter.

**Role** :Retrieves the state of the FunctionalActionPresentation parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowParametersInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowParameters parameter.

**Role** :Retrieves the state of the ShowParameters parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowRelationsInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowRelations parameter.

**Role** :Retrieves the state of the ShowRelations parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetShowSynchroStatusOfLocalParamCacheInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ShowSynchroStatusOfLocalParamCache parameter.

**Role** :Retrieves the state of the ShowSynchroStatusOfLocalParamCache parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSplitFunctionalObjectNameInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SplitFunctionalObjectName parameter.

**Role** :Retrieves the state of the SplitFunctionalObjectName parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetStringUsedAsCarriageReturnInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the StringUsedAsCarriageReturn parameter.

**Role** :Retrieves the state of the StringUsedAsCarriageReturn parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTypeOfIconOnFunctionalElementInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TypeOfIconOnFunctionalElement parameter.

**Role** :Retrieves the state of the TypeOfIconOnFunctionalElement parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetDocumentContentAtCreationLock**( boolean  `iLocked`)

   Locks or unlocks the DocumentContentAtCreation parameter.

**Role** :Locks or unlocks the DocumentContentAtCreation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetFunctionalActionPresentationLock**( boolean  `iLocked`)

   Locks or unlocks the FunctionalActionPresentation parameter.

**Role** :Locks or unlocks the FunctionalActionPresentation parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowParametersLock**( boolean  `iLocked`)

   Locks or unlocks the ShowParameters parameter.

**Role** :Locks or unlocks the ShowParameters parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowRelationsLock**( boolean  `iLocked`)

   Locks or unlocks the ShowRelations parameter.

**Role** :Locks or unlocks the ShowRelations parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetShowSynchroStatusOfLocalParamCacheLock**( boolean  `iLocked`)

   Locks or unlocks the ShowSynchroStatusOfLocalParamCache parameter.

**Role** :Locks or unlocks the ShowSynchroStatusOfLocalParamCache parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetSplitFunctionalObjectNameLock**( boolean  `iLocked`)

   Locks or unlocks the SplitFunctionalObjectName parameter.

**Role** :Locks or unlocks the SplitFunctionalObjectName parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetStringUsedAsCarriageReturnLock**( boolean  `iLocked`)

   Locks or unlocks the StringUsedAsCarriageReturn parameter.

**Role** :Locks or unlocks the StringUsedAsCarriageReturn parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTypeOfIconOnFunctionalElementLock**( boolean  `iLocked`)

   Locks or unlocks the TypeOfIconOnFunctionalElement parameter.

**Role** :Locks or unlocks the TypeOfIconOnFunctionalElement parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure

---

# FunctionalVariant (Object)

**_The interface to access a Functional Variant._**

## Properties

### Property **OriginalDescription**( ) As [CATIAFunctionalDescription](../CATFunctSystemItf/interface_FunctionalDescription_95375.md) (Read Only)

   Returns the Original Description the Variant comes from.

---

# FunctionalVariants (Collection)

**_The interface to access a collection of FunctionalVariants._**

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)

   Create a FunctionalVariant.  
### Sub **Delete**( [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)  `iVariant`)

   Delete a FunctionalVariant.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctionalVariant](../CATFunctSystemItf/interface_FunctionalVariant_62254.md)

   Returns a Variant using its index or its name from the Variants collection.

**Parameters:**

` iIndex`      The index or the name of the Variant to retrieve from the collection of Variants. As a numerics, this index is the rank of the Variant in the collection. The index of the first Variant in the collection is 1, and the index of the last Variant is Count. As a string, it is the name you assigned to the Variant using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Variant **Example:**      This example retrieves in `Act1` the fifth Variant in the collection and in `Act2` the Variant named `Moves`.

```VBScript
     Dim Act1 As FunctionalVariant
     Set Act1 = Desc.Variant(5)
     Dim Act2 As FunctionalVariant
     Set Act2 = Desc.Variant("Adding new substance")

```

---

# FunctMultiRepMgr (Object)

**_The interface to access a Functional Multi-Rep manager._**

## Properties

### Property **Associations**( ) As [CATIAFunctAssociations](../CATFunctSystemItf/interface_FunctAssociations_62974.md) (Read Only)

   Get the Associations collection.  
### Property **CurrentAssoc**( ) As long

   Get the CurrentAssoc.

---

# FunctNodeGraphLayout (Object)

**_Represents a CATIAFunctNodeGraphLayout._**

## Properties

### Property **Height**( ) As double (Read Only)

   Returns the Height coordinate.  
### Property **Width**( ) As double (Read Only)

   Returns the Width coordinate.  Methods

### Sub **SetHeightAndWidth**( double  `iHeight`,  double  `iWidth`)

   Sets the height and width.

**Parameters:**

` iHeight`      the height value.
` iWidth`      the width value.

---

# FunctScript (Object)

**_The interface to access a Functional Script._**

It is managed on a Functional Element, thru the GenerativeKnowledge Facet Manager (GKW).

## Properties

### Property **ScriptText**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Get the ScriptText.

---

# FunctScripts (Collection)

**_The interface to access a set of Functional Scripts._**

It is managed on a Functional Element, thru the GenerativeKnowledge Facet Manager (GKW).

## Methods

### Func **Create**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`) As [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)

   Create a FunctScript.  
### Sub **Delete**( [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)  `iScript`)

   Delete a FunctScript.  
### Func **Elem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAFunctScript](../CATFunctSystemItf/interface_FunctScript_26659.md)

   Returns an association using its index or its name from the Scripts collection.

**Parameters:**

` iIndex`      The index or the name of the Script to retrieve from the collection of Scripts. As a numerics, this index is the rank of the Script in the collection. The index of the first Script in the collection is 1, and the index of the last Script is Count. As a string, it is the name you assigned to the Script using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Script **Example:**      This example retrieves in `Act1` the fifth Script in the collection and in `Act2` the Script named `Moves`.

```VBScript
     Dim FunctElem As FunctionalObject
     Set FunctElem = FunctDoc.CurrentDescription.Objects.Elem("Valve")
     Dim FacetGKW As FunctionalGenScriptMgr
     Set FacetGKW = FunctElem.GetFacetByName("GKW")
     Dim Assoc1 As FunctScript
     Set Assoc1 = FacetGKW.Scripts.Elem(5)
     Dim Assoc2 As FunctScript
     Set Assoc2 = FacetGKW.Scripts.Elem("Producing the Skeleton 2D")

```