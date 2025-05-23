# CATAnalysisInterfaces Framework

## Object Index

  * [AnalysisAdaptivityManager](CATAnalysisInterfaces/interface_AnalysisAdaptivityManager_132794.md)
  * [AnalysisCase](CATAnalysisInterfaces/interface_AnalysisCase_30608.md)
  * [AnalysisCases](CATAnalysisInterfaces/interface_AnalysisCases_36309.md)
  * [AnalysisDocument](CATAnalysisInterfaces/interface_AnalysisDocument_55692.md)
  * [AnalysisEntities](CATAnalysisInterfaces/interface_AnalysisEntities_55864.md)
  * [AnalysisEntity](CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)
  * [AnalysisExport](CATAnalysisInterfaces/interface_AnalysisExport_43590.md)
  * [AnalysisGeneralSettingAtt](CATAnalysisInterfaces/interface_AnalysisGeneralSettingAtt_131587.md)
  * [AnalysisGlobalSensor](CATAnalysisInterfaces/interface_AnalysisGlobalSensor_85334.md)
  * [AnalysisImage](CATAnalysisInterfaces/interface_AnalysisImage_35789.md)
  * [AnalysisImages](CATAnalysisInterfaces/interface_AnalysisImages_41938.md)
  * [AnalysisImport](CATAnalysisInterfaces/interface_AnalysisImport_43344.md)
  * [AnalysisLinkedDocuments](CATAnalysisInterfaces/interface_AnalysisLinkedDocuments_112927.md)
  * [AnalysisLocalEntities](CATAnalysisInterfaces/interface_AnalysisLocalEntities_93812.md)
  * [AnalysisLocalEntity](CATAnalysisInterfaces/interface_AnalysisLocalEntity_77422.md)
  * [AnalysisLocalSensor](CATAnalysisInterfaces/interface_AnalysisLocalSensor_77189.md)
  * [AnalysisManager](CATAnalysisInterfaces/interface_AnalysisManager_47941.md)
  * [AnalysisMeshLocalSpecification](CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecification_188218.md)
  * [AnalysisMeshLocalSpecifications](CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecifications_201982.md)
  * [AnalysisMeshManager](CATAnalysisInterfaces/interface_AnalysisMeshManager_75648.md)
  * [AnalysisMeshPart](CATAnalysisInterfaces/interface_AnalysisMeshPart_54516.md)
  * [AnalysisMeshParts](CATAnalysisInterfaces/interface_AnalysisMeshParts_62021.md)
  * [AnalysisModel](CATAnalysisInterfaces/interface_AnalysisModel_36283.md)
  * [AnalysisModels](CATAnalysisInterfaces/interface_AnalysisModels_42446.md)
  * [AnalysisOutputEntities](CATAnalysisInterfaces/interface_AnalysisOutputEntities_105692.md)
  * [AnalysisPostManager](CATAnalysisInterfaces/interface_AnalysisPostManager_76665.md)
  * [AnalysisPostProSettingAtt](CATAnalysisInterfaces/interface_AnalysisPostProSettingAtt_132726.md)
  * [AnalysisReportingSettingAtt](CATAnalysisInterfaces/interface_AnalysisReportingSettingAtt_155599.md)
  * [AnalysisSensor](CATAnalysisInterfaces/interface_AnalysisSensor_43268.md)
  * [AnalysisSet](CATAnalysisInterfaces/interface_AnalysisSet_26478.md)
  * [AnalysisSets](CATAnalysisInterfaces/interface_AnalysisSets_31754.md)
  * [AnalysisSupports](CATAnalysisInterfaces/interface_AnalysisSupports_57596.md)
  * [BasicComponent](CATAnalysisInterfaces/interface_BasicComponent_42336.md)
  * [BasicComponents](CATAnalysisInterfaces/interface_BasicComponents_48940.md)

## Enumerated Types Index

  * [CATAnalysisSetSearchType](CATAnalysisInterfaces/enum_CATAnalysisSetSearchType_118426.md)
  * [CATAnalysisSetType](CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.md)
  * [CATAxisOrientationType](CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)

---

# CATAnalysisSetSearchType (Enumeration)

**_Search type for analysis sets._**

**Role:** CATAnalysisSetSearchType defines the criterion for searching sets.

**Values:**

` catAnalysisSetSearchIn`      The required sets are the input one for update.
` catAnalysisSetSearchOut`      The required sets are the output one for update.
` catAnalysisSetSearchNeutral`      The required sets are the neutral one for update.
` catAnalysisSetSearchAll`      All the sets are required.

---

# CATAnalysisSetType (Enumeration)

**_Update type for analysis sets._**

**Role:** CATAnalysisSetType defines the Category for Set behavior for update.

**Values:**

` catAnalysisSetIn`      The set will be an input for update.
` catAnalysisSetOut`      The set will be an output for update.
` catAnalysisSetNeutral`      The set will be have no impact for update.

---

# CATAxisOrientationType (Enumeration)

**_Orientation of coordinate system._**

**Role:** CATAxisOrientationType defines the orientation type

**Values:**

` catSamCoordinateSystem_Undefined`      The Orientation is not defined.
` catSamCoordinateSystem_Cartesian`      The Orientation is of cartesian type.
` catSamCoordinateSystem_Cylindrical`      The Orientation is of Cylindrical type.
` catSamCoordinateSystem_Spherical`      The Orientation is of Spherical type.

---

# AnalysisAdaptivityManager (Object)

**_The interface to access a CATIAAnalysisAdaptivityManager._**

## Methods

### Sub **Run**( )

   Run the adaptivity process.

---

# AnalysisCase (Object)

**_Represent the analysis case object._**

**Role:** Interface designed to manage **Analysis Case behavior**.
In the Analysis document, an **Analysis Case** is the object dedicated to define and manage the environment data necessary to run a computation. This environment is made of sets.

## Properties

### Property **AnalysisSets**( ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

   Returns the analysis sets collection associated to the analysis case.

**Returns:**      The collection of analysis sets.  **Example:**      The following example retrieves the analysis sets collection ` ListSets`

```VBScript
     Dim MyCase As AnalysisCase
     Dim ListSets As AnalysisSets
     Set ListSets = MyCase.AnalysisSets

```

Methods

### Func **AddSolution**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSolutionType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

   Creates a Solution set defined by its type in the Case.

**Parameters:**

` iSolutionType`      The feature type of the solution set.
This is a user defined type corresponding to the kind of computation. For example "StaticSet"

**Returns:**      oSolution The analysis set created.  **Example:**      The following example create a solution set ` ListSets`

```VBScript
     Dim MyCase As AnalysisCase
     Dim Newsol As AnalysisSet
     Set Newsol = MyCase.AddSolution("StaticSet")

```

### Sub **Compute**( )

   Launch the computation (Update) of an analysis case. This step corresponds to the "Case Solution" option of the interactive command.  **Example:**      The following example launches the update of ` MyCase`

```VBScript
     Dim MyCase As AnalysisCase
     MyCase.Compute

```

### Sub **ComputeMeshOnly**( )

   Launch the computation (Update) of an analysis case. This method corresponds to the "Mesh Only" option of the interactive command.  **Example:**      The following example launches the update of ` MyCase`

```VBScript
     Dim MyCase As AnalysisCase
     MyCase.ComputeMeshOnly

```

---

# AnalysisCases (Collection)

**_The collection of analysis case making an Analysis._**

## Methods

### Func **Add**( ) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

   Creates a new case and adds it to the case collection. This case will be plugged under the analysis model.

**Returns:**      The created case  **Example:**      The following example creates a case `NewCase` in the case collection of the `ModelAnalysis` Analysis model .

```VBScript
     Dim ModelAnalysis As AnalysisModel
     Dim NewCase As AnalysisCase
     Set NewCase = ModelAnalysis.AnalysisCases.Add()

```

### Sub **AddExistingCase**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iCase`)

   Adds an existing analysis case to the analysis cases collection.

**Parameters:**

` iCase`      The Existing Analysis Case.  **Example:**      This example adds `ThisAnalysisCase` in the `analysisCases` analysis cases collection.

```VBScript
     Dim ThisAnalysisCase As AnalysisCase
     Dim analysisCases As AnalysisCases
     ...
     analysisCases.AddExistingCase(ThisAnalysisCase)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

   Returns a case using its index or its name from the case collection.

**Parameters:**

` iIndex`      The index or the name of the case to retrieve from the collection of cases. As a numeric, this index is the rank of the case in the collection. The index of the first case in the collection is 1, and the index of the last case is Count. As a string, it is the name you assigned to the case using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved case. **Example:**      This example retrieves in ` ThisCase` the fifth case in the collection and in ` ThatCase` the case named `"MyCase` in the case collection of the `AnalysisModel` Analysis model.

```VBScript
     Set CaseColl = AnalysisModel.AnalysisCases
     Set ThisCase = CaseColl.Item(5)
     Set ThatCase = CaseColl.Item("MyCase")

```

### Func **NewCase**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)

   Creates a new case and adds it to the case collection. This case will be plugged under the analysis model.

**Returns:**      The created case  **Example:**      The following example creates a case `NewCase` in the case collection of the `ModelAnalysis` Analysis model .

```VBScript
     Dim ModelAnalysis As AnalysisModel
     Dim NewCase As AnalysisCase
     Set NewCase = ModelAnalysis.AnalysisCases.NewCase("AnalysisPreproCase")()

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a case using its index or its name from the case collection.

**Parameters:**

` iIndex`      The index or the name of the case to retrieve from the collection of cases. As a numeric, this index is the rank of the case in the collection. The index of the first case in the collection is 1, and the index of the last case is Count. As a string, it is the name you assigned to the case using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property. **Example:**      This example removes the fifth case in the collection.

```VBScript
     AnalysisModel.AnalysisCases.Remove (5)

```

---

# AnalysisDocument (Object)

**_Represents the document object for analysis._**
This objects is used for all CAE applications to defines specifications and managed associated results.
The document for analysis data is typed as ".CATAnalysis".
When an analysis document object is created, an analysis manager is also created.
This analysis manager is the root object at the top of the structure of the Analysis document.

**See also:**      [Document](../InfInterfaces/interface_Document_14456.md)

## Properties

### Property **Analysis**( ) As [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md) (Read Only)

   Returns the root analysis object from the current analysis document.

**Example:**     The following example returns in `RootAnalysis` the root analysis object of the active document, assumed to be an analysis document:

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis

```

---

# AnalysisEntities (Collection)

**_The collection of analysis entities._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

   Creates a new analysis entity and adds it to the analysis entities collection.
This collection may be extracted from an analysis set.The Analysis entity will be created on the Analysis Model.

**Parameters:**

` iType`      The type of the entity to create.

**Returns:**      The created analysis entity  **Example:**      This example create `ThisAnalysisEntity` in the `analysisEntities` collection
The entity to create is supposed to be a pressure defined in a load set.

```VBScript
     Dim analysisEntities As CATIAAnalysisEntities
     Dim ThisAnalysisEntity As AnalysisEntity
     Set ThisAnalysisEntity = analysisEntities.Add("SAMPressure")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

   Returns an analysis entity using its index or its name from the analysis entities collection.

**Parameters:**

` iIndex`      The index or the name of the analysis entity to retrieve from the collection of analysis entities. As a numerics, this index is the rank of the analysis entity in the collection. The index of the first analysis entity in the collection is 1, and the index of the last analysis entity is Count. As a string, it is the name you assigned to the analysis entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved analysis entity  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a entity using its index or its name from the entity collection.

**Parameters:**

` iIndex`      The index or the name of the entity to retrieve from the collection of entities. As a numeric, this index is the rank of the entity in the collection. The index of the first entity in the collection is 1, and the index of the last entity is Count. As a string, it is the name you assigned to the entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# AnalysisEntity (Object)

**_Represent the analysis entity object._**
This class provides services to describe a analysis entity. It represents some preprocessing activities.
It agregates descriptive sub-entities named Basic Components, and Analysis Supports.
The basic component represent the physical data and the support the localisation.

## Properties

### Property **AnalysisImages**( ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

   Returns the analysis images collection associated with an analysis entity.

**Example:**     This example retrieves `analysisimages` collection .

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim analysisimages As AnalysisImages
     Set analysisimages = MyEntity.AnalysisImages

```

### Property **AnalysisLocalEntities**( ) As [CATIAAnalysisLocalEntities](../CATAnalysisInterfaces/interface_AnalysisLocalEntities_93812.md) (Read Only)

   Returns the analysis local entity collection associated with an analysis entity.

**Example:**     This example retrieves `analysislocalEntity` collection .

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim analysislocalEntity As AnalysisLocalEntities
     Set analysislocalEntity = MyEntity.AnalysisLocalEntities

```

### Property **AnalysisSupports**( ) As [CATIAAnalysisSupports](../CATAnalysisInterfaces/interface_AnalysisSupports_57596.md) (Read Only)

   Returns the list of Analysis Supports. The support defines the area on which the analysis is applied on.  
### Property **BasicComponents**( ) As [CATIABasicComponents](../CATAnalysisInterfaces/interface_BasicComponents_48940.md) (Read Only)

   Returns the basic components collection associated with an analysis entity.

**Example:**     This example retrieves ` basiccomponents` collection .

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim basiccomponents As BasicComponents
     Set basiccomponents = MyEntity.BasicComponents

```

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the analysis entity.

**Example:**     The following example returns `TypeofEntity` of `MyEntity`.

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim TypeofEntity As CATBSTR
     Set TypeofEntity = MyEntity.Type

```

Methods

### Sub **AddSupportFromConstraint**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iConstraintProduct`,  [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)  `iConstraint`)

   Creates a new support and add it to the description of the Analysis Entity.

**Parameters:**

` iConstraintProduct`      the CATIA Product of the Constraint.

` iConstraint`      the CATIA Constraint that represent the object to linked.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Part](../MecModInterfaces/interface_Part_3788.md) 
### Sub **AddSupportFromPart**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iPartProduct`,  [CATIAPart](../MecModInterfaces/interface_Part_3788.md)  `iPart`)

   Creates a new support and add it to the description of the Analysis Entity.

**Parameters:**

` iPartProduct`      the CATIA Product of the part.

` iPart`      the CATIA Part that represent the object to linked.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Part](../MecModInterfaces/interface_Part_3788.md) 
### Sub **AddSupportFromProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Creates a new support and add it to the description of the Analysis Entity.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iSupport`      the CATIA Reference that represent the object to linked.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromPublication**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iPublication`)

   Creates a new support and add it to the description of the Analysis Entity.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iPublication`      the CATIA Publication that represent the object to linked.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Creates a new support and add it to the description of the Analysis Entity.

**Parameters:**

` iReference`      the CATIA Reference that represent the object to linked. This identification, may locate the instance of the object

` iSupport`      the CATIA Reference that represent the object to linked.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md) 
### Func **GetReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  long  `iLineIndex`,  long  `iColumnIndex`,  long  `iLayerIndex`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Returns the reference corresponding to the given component.

**Parameters:**

` iComponent`      The identifier if the basic component.

` iLabel`      The label of the block containing the value.

` iLineIndex`      The line index of the value.

` iColumnIndex`      The column index of the value.

` iLayerIndex`      The layer index of the value.

### Func **GetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  long  `iLineIndex`,  long  `iColumnIndex`,  long  `iLayerIndex`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Returns the value corresponding to the given component.

**Parameters:**

` iComponent`      The identifier if the basic component.

` iLabel`      The label of the block containing the value.

` iLineIndex`      The line index of the value.

` iColumnIndex`      The column index of the value.

` iLayerIndex`      The layer index of the value.

### Sub **SetReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  long  `iLineIndex`,  long  `iColumnIndex`,  long  `iLayerIndex`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iValue`)

   Sets the reference corresponding to the given component.

**Parameters:**

` iComponent`      The identifier if the basic component.

` iLabel`      The label of the block containing the value.

` iLineIndex`      The line index of the value.

` iColumnIndex`      The column index of the value.

` iLayerIndex`      The layer index of the value.
If the the component has a single value, assign 0 to the 3 parameters.

### Sub **SetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iComponent`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  long  `iLineIndex`,  long  `iColumnIndex`,  long  `iLayerIndex`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets the value corresponding to the given component.

**Parameters:**

` iComponent`      The identifier if the basic component.

` iLabel`      The label of the block containing the value.

` iLineIndex`      The line index of the value.

` iColumnIndex`      The column index of the value.

` iLayerIndex`      The layer index of the value.
If the the component has a single value, assign 0 to the 3 parameters.  This example create `ThisAnalysisEntity` in the `analysisEntities` collection
The entity to create is supposed to be a pressure defined in a load set. We
will valuate the basic component that contain the pressure data "SAMPressureMag".

```VBScript
     Dim analysisEntities As CATIAAnalysisEntities
     Dim ThisAnalysisEntity As AnalysisEntity
     Set ThisAnalysisEntity = analysisEntities.Add("SAMPressure")
     ThisAnalysisEntity.SetValue("SAMPressureMag"," ",0,0,0,100)

```

---

# AnalysisGeneralSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "GeneralSetting"._**

## Properties

### Property **AnalysisCacheMode**( ) As long

   Tells if Product Structure Cache Mode will be handled.  
### Property **AnalysisLoadMode**( ) As long

   Retrieves if pointed document will be loaded.  
### Property **AnalysisNamingAuto**( ) As long

   Tells if Automatic naming will be activated.  
### Property **DefaultAnalysisFlag**( ) As long

   Retrieves if a default analysis Case will be created.  
### Property **DefaultAnalysisTemplate**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Retrieves the name of the default analysis Case that will be created.  
### Property **ViewAnalysisParameter**( ) As long

   Retrieves if the Parameter set is visible in the feature tree of the analysis document.  
### Property **ViewAnalysisRelation**( ) As long

   Retrieves if the Relation set is visible in the feature tree of the analysis document.  Methods

### Func **GetAnalysisCacheModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnalysisLoadModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetAnalysisNamingAutoInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDefaultAnalysisFlagInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the default flag.

**Role** :Retrieves the state of the default flag in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetDefaultAnalysisTemplateInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the default template.

**Role** :Retrieves the state of the default template in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetViewAnalysisParameterInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Func **GetViewAnalysisRelationInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the parameter.

**Role** :Retrieves the state of the parameter in the current environment.

**Parameters:**

` AdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` oLocked`      Indicates if the parameter has been locked.
` oModified`      Indicates if the parameter has been explicitly modified or remain to the administrated value.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisCacheModeLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisLoadModeLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetAnalysisNamingAutoLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultAnalysisFlagLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetDefaultAnalysisTemplateLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetViewAnalysisParameterLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure  
### Sub **SetViewAnalysisRelationLock**( boolean  `iLocked`)

   Locks or unlocks the flag.

**Role** :Locks or unlocks the parameter if it is possible in the current administrated. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      The locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

**Returns:**      **Legal values** :
`S_OK :` on Success
`E_FAIL:` on failure

---

# AnalysisGlobalSensor (Object)

**_Represent the analysis global sensor._**

This object is a kind of AnalysisSensor based on analysis feature global results. For example, extract the Energy value of a solution.

## Methods

### Sub **GetIdentifier**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oTypeBSTR`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `oSubTypeBSTR`)

   Retreives the Physical type and sub physical type that will be computed by the sensor.

**Parameters:**

` oTypeBSTR`      The physical type identifier.
` oSubTypeBSTR`      The "sub" physical type identifier.

### Sub **SetIdentifier**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeBSTR`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iSubTypeBSTR`)

   Sets the Physical type and sub physical type that will be computed by the sensor.

**Parameters:**

` iTypeBSTR`      The physical type identifier.
` iSubTypeBSTR`      The "sub" physical type identifier.

---

# AnalysisImage (Object)

**_Represents the analysis image object._**

## Properties

### Property **AnalysisImages**( ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

   Returns the analysis images collection associated with an analysis image.  Methods

### Sub **ExportData**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportDataWithMeshPartId

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

### Sub **ExportDataInGlobalAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataInManualAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iOrigin`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iXDirection`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iYDirection`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iZDirection`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iOrigin`      Origin of Location axis system
` iXDirection`      co-ordinates of a point on X- axis of Location axis system
` iYDirection`      co-ordinates of a point on Y- axis of Location axis system
` iZDirection`      co-ordinates of a point on Z- axis of Location axis system
` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataInUserAxis**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`,  [CATIAAxisSystem](../MecModInterfaces/interface_AxisSystem_22406.md)  `iAxisSystem`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATAxisOrientationType](../CATAnalysisInterfaces/enum_CATAxisOrientationType_101718.md)  `iAxisOrientationType`,  boolean  `iExportMeshPartID`)

   Extracts image results.
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: node, element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportDataWithMeshPartId

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

` iAxisSystem`      Reference to the axis system to be used for location transformation.
` iProduct`      Reference to the product, where the above axis system is defined.
` iAxisOrientationType`      Coordinate system type of location axis system
` iExportMeshPartID`      Flag for exporting with meshpartid or not

### Sub **ExportDataWithMeshPartId**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFileName`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iExtensionType`)

   Extracts image results and location with mesh part name (as identifier).
The export is done related to an existing image and will be stored in a CATIA Folder as a Text file or as an Excel file.

**Limitations** :

  * The allowed output positions are: element, center of element, and node of element
  * The allowed values are: integer, real or double
  * The allowed value types are: average or discontinuous iso, symbol, fringe or text

To export data with mesh-part identification use ExportData

**Parameters:**

` iFolder`      The folder to store the file to create
` iFileName`      The name of the file to create
` iExtensionType`      The extension of the file

**Legal values** :

  * "xls" for a Microsoft Excel workbook
  * "txt" for a text file.

### Sub **ResetSelection**( )

   Resets all selections in an image.
This is done related to an existing image  
### Sub **SetActivationStatus**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iActivationStatus`)

   Activates oe deactivates an image.
This is done related to an existing image

**Parameters:**

` iActivationStatus`      To activate or not the current image.

### Sub **SetCurrentOccurrence**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iOccurrenceNumber`)

   Sets occurrence number for an image.
This is done related to an existing image

**Parameters:**

` iOccurrenceNumber`      The number to select

**Legal value** : 1 ≤ iOccurrenceNumber ≤ nbOccurrence

### Sub **SetSelection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iReplaceMode`)

   Adds a selection to an image.
This is done related to an existing image

**Parameters:**

` iReference`      The selectionGroup to add
` iReplaceMode`      To replace or not the current selections.

### Sub **Update**( )

   Updates an image.
This is done related to an existing image

---

# AnalysisImages (Collection)

**_The collection of analysis images._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iImageName`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iHideExistingImages`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iShowMesh`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iDuplicate`) As [CATIAAnalysisImage](../CATAnalysisInterfaces/interface_AnalysisImage_35789.md)

   Creates a new image and adds it to the analysis image collection.

**Parameters:**

` iImageName`      The name of the image to create.
` iHideExistingImages`      To deactivate or not all the activated images before create the new image.
` iShowMesh`      To show or not the mesh image.
` iDuplicate`      To duplicate or not the new image, if same image already exists in collection of images.

**Returns:**      The created Analysis Image  **Example:**      This example create `ThisAnalysisImage` in the `analysisImages`analysis
images collection. The image to create is supposed to be a mesh deformed image.

```VBScript
     Dim ThisAnalysisImage As AnalysisImage
     Set ThisAnalysisImage = analysisImages.Add("Mesh_Deformed", True, False, False)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisImage](../CATAnalysisInterfaces/interface_AnalysisImage_35789.md)

   Returns an analysis image using its index or its name from the analysis images collection.

**Parameters:**

` iIndex`      The index or the name of the analysis image to retrieve from the collection of analysis images. This index is the rank of the analysis image in the collection. The index of the first analysis image in the collection is 1, and the index of the last analysis image is Count.

**Returns:**      The retrieved analysis image  **Example:**      This example retrieves in `ThisAnalysisImage` the third analysis image.

```VBScript
     Dim ThisAnalysisImage As AnalysisImage
     Set ThisAnalysisImage = analysisImages.Item(3)

```

---

# AnalysisImport (Object)

**_The interface to access a CATIAAnalysisExport_**

## Methods

### Sub **AddSupport**( [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProductSupport`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iSupport`)

   AddSupport for loads import if needed.
)

**Parameters:**

` iManager`      The Analysis manager.
)
` iProductSupport`      Product of the geometrical support.
)
` iSupports`      Geometrical support.
)

### Sub **ImportDisp**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iFatherCase`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFullPath`,  [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAxis`)

   Import displacements from a CATAnalysisExport file.
)

**Parameters:**

` iFatherCase`      case where Displacements will be exported.
)
` iFullPath`      The full path of the file.
)
` iManager`      analysis manager where the disp is exported.
)
` iAxis`      The user axis system to be taken into account.
)

### Sub **ImportForce**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iFatherCase`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFullPath`,  [CATIAAnalysisManager](../CATAnalysisInterfaces/interface_AnalysisManager_47941.md)  `iManager`,  [CATIABase](../System/interface_AnyObject_17321.md)  `iAxis`)

   Import loads from a CATAnalysisExport file.
)

**Parameters:**

` iFatherCase`      case where loads will be exported.
)
` iFullPath`      The full path of the file.
)
` iManager`      analysis manager where the disp is exported.
)
` iAxis`      The user axis system to be taken into account.
)

---

# AnalysisLinkedDocuments (Collection)

**_The collection of Documents linked by Analysis._**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Returns a Document by its index or its name from the linked Documents collection.

**Parameters:**

` iIndex`      The index or the name of the linked Document to retrieve from the collection of linked Documents. As a numerics, this index is the rank of the linked Document in the collection. The index of the first linked Document in the collection is 1, and the index of the last linked Document is Count. As a string, it is the name you assigned to the collection by using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved linked Document

---

# AnalysisLocalEntities (Collection)

**_The collection of local analysis entities._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisLocalEntity](../CATAnalysisInterfaces/interface_AnalysisLocalEntity_77422.md)

   Creates a new analysis local entity and adds it to the analysis entities collection.
This collection may be extracted from an analysis entity.The Analysis local entity will be created on the Analysis entity.

**Parameters:**

` iType`      The type of the entity to create.

**Returns:**      The created analysis entity  **Example:**      This example create `ThisAnalysisEntity` in the `analysisEntities` collection
The entity to create is supposed to be a pressure defined in a load set.

```VBScript
     Dim analysisEntities As CATIAAnalysisLocalEntities
     Dim ThisAnalysisEntity As AnalysisEntity
     Set ThisAnalysisEntity = analysisEntities.Add("SAMShellLocal")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisLocalEntity](../CATAnalysisInterfaces/interface_AnalysisLocalEntity_77422.md)

   Returns an analysis entity using its index or its name from the analysis entities collection.

**Parameters:**

` iIndex`      The index or the name of the analysis entity to retrieve from the collection of analysis entities. As a numerics, this index is the rank of the analysis entity in the collection. The index of the first analysis entity in the collection is 1, and the index of the last analysis entity is Count. As a string, it is the name you assigned to the analysis entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved analysis entity  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Returns an analysis local entity.

**Parameters:**

` iIndex`      The index or the name of the analysis entity to retrieve from the collection of analysis entities. As a numerics, this index is the rank of the analysis entity in the collection. The index of the first analysis entity in the collection is 1, and the index of the last analysis entity is Count. As a string, it is the name you assigned to the analysis entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.

---

# AnalysisLocalEntity (Object)

**_Represent the analysis local entity object._**
This class provides services to describe a analysis entity. It represents some local preprocessing activities.

## Properties

### Property **AnalysisImages**( ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

   Returns the analysis images collection associated with an analysis entity.

**Returns:**      a collection of CATIAAnalysisImages.  **Example:**      This example retrieves `analysis images` collection

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim myAnalysisImages As AnalysisImages
     Set myAnalysisImages = MyEntity.AnalysisImages

### Property **AnalysisSupports**( ) As [CATIAAnalysisSupports](../CATAnalysisInterfaces/interface_AnalysisSupports_57596.md)  (Read Only)

     Returns the list of Analysis Supports (Selection of geometrical or mesh
     entities) which define the area on which the analysis is applied on.

### Property **BasicComponents**( ) As [CATIABasicComponents](../CATAnalysisInterfaces/interface_BasicComponents_48940.md)  (Read Only)

     Returns the basic components collection associated with an analysis entity.

       **Returns:**
            a collection of  CATIABasicComponents.

       **Example:**
            This example retrieves Basic components collection

```VBScript
     Dim MyEntity As AnalysisEntity
     Dim myBasicComponents As BasicComponents
     Set myBasicComponents = MyEntity.BasicComponents

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)  (Read Only)

     Returns the type of the analysis Entity.

       **Returns:**
            The string that represent the analysis entity type.

     Methods

### Sub **AddSupportFromConstraint**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  iConstraintProduct,  [CATIAConstraint](../MecModInterfaces/interface_Constraint_22634.md)  iConstraint)

     Creates a new support and add it to the description of the Analysis Entity.

       **Parameters:**

         iConstraintProduct
             the CATIA Product of the Constraint.

         iConstraint
            the CATIA Constraint that represent the object to linked.

       **See also:**
           [Reference](../InfInterfaces/interface_Reference_17481.md), [Part](../MecModInterfaces/interface_Part_3788.md)

### Sub **AddSupportFromProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  iProduct,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iSupport)

     Creates a new support and add it to the description of the Analysis Entity.

       **Parameters:**

         iProduct
             the CATIA Product that represent the object to linked.

         iSupport
             the CATIA Reference that represent the object to linked.

       **See also:**
           [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md)

### Sub **AddSupportFromPublication**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  iProduct,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  iPublication)

     Creates a new support and add it to the description of the Analysis Entity.

       **Parameters:**

         iProduct
             the CATIA Product that represent the object to linked.

         iPublication
             the CATIA Publication that represent the object to linked.

       **See also:**
           [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md)

### Sub **AddSupportFromReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iReference,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iSupport)

     Creates a new support and add it to the description of the Analysis Entity.

       **Parameters:**

         iReference
             the CATIA Reference that represent the object to linked. This identification,  may locate the instance of the object

         iSupport
             the CATIA Reference that represent the object to linked.

       **See also:**
           [Reference](../InfInterfaces/interface_Reference_17481.md)

### Func **GetReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iComponent,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

     Returns the reference corresponding to the given component.

       **Parameters:**

         iComponent
             The identifier if the basic component.

         iLabel
             The label of the block containing the value.

         iLineIndex
             The line index of the value.

         iColumnIndex
             The column index of the value.

         iLayerIndex
             The layer index of the value.

### Func **GetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iComponent,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex) As [CATVariant](../System/typedef_CATVariant_20656.md)

     Returns the value corresponding to the given component.

       **Parameters:**

         iComponent
             The identifier if the basic component.

         iLabel
             The label of the block containing the value.

         iLineIndex
             The line index of the value.

         iColumnIndex
             The column index of the value.

         iLayerIndex
             The layer index of the value.

### Sub **SetReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iComponent,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iValue)

     Sets the reference corresponding to the given component.

       **Parameters:**

         iComponent
             The identifier if the basic component.

         iLabel
             The label of the block containing the value.

         iLineIndex
             The line index of the value.

         iColumnIndex
             The column index of the value.

         iLayerIndex
             The layer index of the value.
     If the the component has a single value, assign 0 to the 3 parameters.

### Sub **SetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iComponent,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex,  [CATVariant](../System/typedef_CATVariant_20656.md)  iValue)

     Sets the value corresponding to the given component.

       **Parameters:**

         iComponent
             The identifier if the basic component.

         iLabel
             The label of the block containing the value.

         iLineIndex
             The line index of the value.

         iColumnIndex
             The column index of the value.

         iLayerIndex
             The layer index of the value.
     If the the component has a single value, assign 0 to the 3 parameters.

       **Example:**
            This example create ThisAnalysisEntity in the analysisEntities collection

     The entity to create is supposed to be a pressure defined in a load set. We

     will valuate the basic component that contain the pressure data "SAMPressureMag".

```VBScript
     Dim analysisEntities As CATIAAnalysisEntities
     Dim ThisAnalysisEntity As AnalysisEntity
     Set ThisAnalysisEntity = analysisEntities.Add("SAMPressure")
     ThisAnalysisEntity.SetValue("SAMPressureMag"," ",0,0,0,100)

```

---

# AnalysisLocalSensor (Object)

**_Represent the analysis local sensor._**

This object is a kind of AnalysisSensor based on analysis feature results
based on a finite element selection. This sensor definition is based on an XML file
stored in the CATIARuntimeView.

## Properties

### Property **XMLName**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the Identifier of the sensor as defined in the XML file.

**Example:**      This example retrieves in `MyXMLName` the identifier of the `AnalysisSensor1` object.

```VBScript
     MyObjectName = AnalysisSensor1.XMLName

```

---

# AnalysisManager (Object)

**_Represents the root object inside an analysis document._**
It aggregates all the objects making up an analysis document.

## Properties

### Property **AnalysisModels**( ) As [CATIAAnalysisModels](../CATAnalysisInterfaces/interface_AnalysisModels_42446.md) (Read Only)

   Returns the analysis model collection from the current analysis manager.

**Example:**     The following example returns from `RootAnalysis` the root analysis object of the active document, assumed to be an Analysis document, the collection of analysis models.

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     Dim analysisModels As AnalysisModels
     Set analysisModels = RootAnalysis.AnalysisModels

```

### Property **AnalysisSets**( ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

   Returns the analysis sets collection associated with an analysis manager. This collection allows to access the Analysis Connection Manager that aggregates the Analysis Connection features.

**Returns:**      a collection of CATIAAnalysisSets.  
### Property **LinkedDocuments**( ) As [CATIAAnalysisLinkedDocuments](../CATAnalysisInterfaces/interface_AnalysisLinkedDocuments_112927.md) (Read Only)

   Returns the collection containing the documents linked to analysis document. All the CATIA documents that are linked to the different objects (like AnalysisMeshPart of Analysis Entity) might be accessed thru that collection.

**Example:**     The following example returns in `documents` the linked documents of the `AnalysisDocument` :

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     Dim Documents As AnalysisLinkedDocuments
     Set Documents = RootAnalysis.LinkedDocuments

```

### Property **Parameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection object containing the analysis parameters. All the parameters that are defined in analysis objects might be accessed thru that collection.

**Example:**     The following example returns in `params` the parameters of the `RootAnalysis` from the `AnalysisDocument` document:

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     Dim params As CATIAParameters
     Set params = RootAnalysis.Parameters

```

### Property **Relations**( ) As [CATIARelations](../KnowledgeInterfaces/interface_Relations_18301.md) (Read Only)

   Returns the collection object containing the analysis relations. All the relations that are defined in analysis objects might be accessed thru that collection.

**Example:**     The following example returns in `relation` the relations of the `RootAnalysis` from the `AnalysisDocument` document:

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     Dim relation As CATIARelations
     Set relation = RootAnalysis.Relations

```

Methods

### Func **CreateReferenceFromGeometry**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGeometry`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from a geometry. This geometry must in defined in a document rerecened in the CATIAAnalysisLinkedDocuments collection.

**Parameters:**

` iProduct`      The product of the geometry to be referenced that defines the instance of the geometry.
` iGeometry`      The geometry to be referenced. As a reference, it can be an CATIABoundary object of a mechanical feature.

**Returns:**      a reference of the couple (iProduct, iGeometry).  
### Func **CreateReferenceFromObject**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Creates a reference from an analysis object. Use of reference allows a uniform handling of anay objects.

**Parameters:**

` iObject`      The analysis object to be referenced. It can be an `AnalysisEntity` or an `AnalysisSet`

**Returns:**      The reference to the object.  
### Sub **Import**( [CATIADocument](../InfInterfaces/interface_Document_14456.md)  `iDocumentToImport`)

   Import an existing document in an analysis document . This document can of any type that implement the CATIADocument interface. This is implemented for internal document formats. (like Part or Product documents).

**Example:**     The following example imports an opened CATPart document

```VBScript
     Dim AnalysisDocument As Document
     Dim PartDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     RootAnalysis.Import(PartDocument)

```

### Sub **ImportDefineFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentPath`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTypeLate`,  [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iValues`)

   Import an existing document in an analysis document. This document can of any type that is managed by the CATISamImportDefine interface.

**Example:**     The following example imports an CATPart document stored as FileToOpen file. This example is also use the CATAnalysisImport Object. This object allow to import Part, Product or Analysis documents. As of today no parameters are mandatory for this object.

```VBScript
     Dim arrayOfVariant(0)
     FileToOpen = "e:\users\Parts\ThisIsANicePart.CATPart"
     ObjectForImport = "CATAnalysisImport"
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     RootAnalysis.ImportDefineFile(FileToOpen,CATAnalysisImport,arrayOfVariant)

```

### Sub **ImportFile**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iDocumentPath`)

   Import an existing document in an analysis document.

**Deprecated:**      V5R15 use ImportDefineFile instead. This document can of any type that implement the CATISamImportDefine interface.

**Example:**     The following example imports an CATPart document stored as FileToOpen file.

```VBScript
     FileToOpen = "e:\users\Parts\ThisIsANicePart.CATPart"
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     RootAnalysis.ImportFile(FileToOpen)

```

---

# AnalysisMeshLocalSpecification (Object)

**_The interface to access a CATIAAnalysisMeshLocalSpecification._**

## Properties

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the local specification.

**Returns:**      The string that represent the type of local specification.  Methods

### Sub **AddSupportFromPublication**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`)

   Defines the support of the local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iProduct`      the CATIA Product that represent the object to linked.
` iPublication`      the CATIA Publication that represent the geometry.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Defines the support of the local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iProduct`      the CATIA Product that represent the object to linked.
` iSupport`      the CATIA Reference that represent the geometry.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **SetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets the value corresponding to the given local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iValue`      The value of the local specification.

---

# AnalysisMeshLocalSpecifications (Collection)

**_The interface to access a AnalysisMeshLocalSpecifications._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisMeshLocalSpecification](../CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecification_188218.md)

   Creates a new local specification and adds it to the local specification collection.
The local specification will be created linked to the AnalysisMeshManager object.

**Parameters:**

` iType`      The type of mesh part to create.

**Returns:**      The created local specification  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a local specification using its index or its name from the local specification collection.

**Parameters:**

` iIndex`      The index or the name of the local specification to retrieve from the collection of local specification . As a numeric, this index is the rank of the local specification in the collection. The index of the first local specification in the collection is 1, and the index of the last local specification is Count. As a string, it is the name you assigned to the local specification using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# AnalysisMeshManager (Object)

**_The interface to access a CATIAAnalysisMeshManager._**

## Properties

### Property **AnalysisMeshParts**( ) As [CATIAAnalysisMeshParts](../CATAnalysisInterfaces/interface_AnalysisMeshParts_62021.md) (Read Only)

   Returns the meshpart collection from the current analysis mesh manager.

---

# AnalysisMeshPart (Object)

**_The interface to access a CATIAAnalysisMeshPart._**

## Properties

### Property **Activity**( ) As boolean

   Returns the activity of an meshpart.

**Parameters:**

` oActivity`

**Legal values** :

FALSE

    **Mesh Part** is not active. TRUE

    **Mesh Part** is active.

### Property **AnalysisMeshLocalSpecifications**( ) As [CATIAAnalysisMeshLocalSpecifications](../CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecifications_201982.md) (Read Only)

   Returns the local specification collection from the meshpart analysis.  Methods

### Sub **AddSupportFromPublication**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`)

   Creates a new support and add it to the support description of the mesh part.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iPublication`      the CATIA Publication that represent the the geometry to meshed.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromReference**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Creates a new support and add it to the support description of the mesh part.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iSupport`      the CATIA Reference that represent the geometry to meshed.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **SetGlobalSpecification**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets the value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iValue`      The value of the global specification.

### Sub **SetSpecificationFromPublication**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`,  long  `iMode`)

   Adds the geometric value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iProduct`      the CATIA Product that represent the object to linked.

` iPublication`      the CATIA Publication that represent the the geometry to meshed.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) ` iMode`      The mode used to valuate the publication global specification.

**Legal values** :

0
    the global specification is defined as a single reference. 1
    the global specification is added to exising references.

### Sub **SetSpecificationFromReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iMode`)

   Set the geometric value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iProduct`      the CATIA Product that represent the object to linked.

` iSupport`      the CATIA Reference that represent the geometry to meshed.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) ` iMode`      The mode used to valuate the reference global specification.

**Legal values** :

0
    the global specification is defined as a single reference. 1
    the global specification is added to exising references.

---

# AnalysisMeshParts (Collection)

**_The collection of analysis meshparts._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisMeshPart](../CATAnalysisInterfaces/interface_AnalysisMeshPart_54516.md)

   Creates a new meshpart and adds it to the meshpart collection.
The meshpart will be created linked to the AnalysisMeshManager object.

**Parameters:**

` iType`      The type of mesh part to create.

**Returns:**      The created meshpart  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisMeshPart](../CATAnalysisInterfaces/interface_AnalysisMeshPart_54516.md)

   Returns a meshpart using its index or its name from the meshpart collection.

**Parameters:**

` iIndex`      The index or the name of the meshpart to retrieve from the collection of meshparts. As a numeric, this index is the rank of the meshpart in the collection. The index of the first meshpart in the collection is 1, and the index of the last meshpart is Count. As a string, it is the name you assigned to the meshpart using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved meshpart.

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a meshpart using its index or its name from the meshpart collection.

**Parameters:**

` iIndex`      The index or the name of the meshpart to retrieve from the collection of meshpart. As a numeric, this index is the rank of the meshpart in the collection. The index of the first meshpart in the collection is 1, and the index of the last meshpart is Count. As a string, it is the name you assigned to the meshpart using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# AnalysisModel (Object)

**_Represent the analysis model object._**

**Role** : In the analysis document, an analysis model is the object dedicated to set and manage all the required data for the discretization and idealization of a Finite Element model.
This object gives access to:

  * A collection of AnalysisCase.
  * A collection of AnalysisSets (All the input sets like properties, groups).
  * A AnalysisPostManager object for reporting.

## Properties

### Property **AdaptivityManager**( ) As [CATIAAnalysisAdaptivityManager](../CATAnalysisInterfaces/interface_AnalysisAdaptivityManager_132794.md) (Read Only)

   Returns the AdaptivityManager defined on the analysis model.

**Returns:**      a CATIAAnalysisAdaptivityManager.  
### Property **AnalysisCases**( ) As [CATIAAnalysisCases](../CATAnalysisInterfaces/interface_AnalysisCases_36309.md) (Read Only)

   Returns the collection of analysis cases defined on the analysis model.

**Returns:**      oAnalysisCases Collection of cases.  
### Property **AnalysisSets**( ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

   Returns the analysis sets collection associated with a analysis model.

**Returns:**      a collection of CATIAAnalysisSets.  
### Property **MeshManager**( ) As [CATIAAnalysisMeshManager](../CATAnalysisInterfaces/interface_AnalysisMeshManager_75648.md) (Read Only)

   Returns the MeshManager defined on the analysis model.

**Returns:**      a CATIAAnalysisMeshManager.  
### Property **PostManager**( ) As [CATIAAnalysisPostManager](../CATAnalysisInterfaces/interface_AnalysisPostManager_76665.md) (Read Only)

   Returns the Postprocessing manager defined on the analysis model.

**Returns:**      oPostManager the AnalysisPostManager Object.  Methods

### Sub **RunTransition**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTransitionName`)

   Apply a transition to the analysis model.

**Parameters:**

` Transition`      name.

---

# AnalysisModels (Collection)

**_The collection of analysis models making an analysis document._**
As of today this collection is made of a single analysis model.

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisModel](../CATAnalysisInterfaces/interface_AnalysisModel_36283.md)

   Returns an analysis model using its index or its name from the analysis model collection.

**Parameters:**

` iIndex`      The index or the name of the analysis model to retrieve from the collection of analysis model. As a numerics, this index is the rank of the analysis model in the collection. The index of the first analysis model in the collection is 1, and the index of the last analysis model is Count. As a string, it is the name you assigned to the analysis model using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved analysis model  **Example:**      The following example retrieves the first analysis model in the analysis model collection of the ` AnalysisManager` object.

```VBScript
     Dim AnalysisDocument As Document
     Set AnalysisDocument = CATIA.ActiveDocument
     Dim RootAnalysis As AnalysisManager
     Set RootAnalysis = AnalysisDocument.Analysis
     Dim analysisModels As AnalysisModels
     Set analysisModels = RootAnalysis.AnalysisModels
     Dim analysisModel As AnalysisModel
     Set AnalysisModel = analysisModel.Item(1)

```

---

# AnalysisOutputEntities (Collection)

**_The collection of analysis entities results of a set._**
This collection is implemented only for analysis sets. with analysis entities as Output (regarding to the update mechanism).

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

   Creates a new analysis entity and adds it to the analysis entities collection.
This collection may be extracted from an analysis set.The Analysis entity will be created on the Analysis Model.

**Parameters:**

` iType`      The type of the entity to create.

**Returns:**      The created analysis entity  **Example:**      This example create `ThisAnalysisEntity` in the `AnalysisOutputEntities` collection

```VBScript
     Dim AnalysisOutputEntities As CATIAAnalysisOutputEntities
     Dim ThisAnalysisEntity As AnalysisEntity
     Set ThisAnalysisEntity = AnalysisOutputEntities.Add("MyEntity")

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAAnalysisEntity](../CATAnalysisInterfaces/interface_AnalysisEntity_43456.md)

   Returns an analysis entity using its index or its name from the analysis entities collection.

**Parameters:**

` iIndex`      The index or the name of the analysis entity to retrieve from the collection of analysis entities. As a numerics, this index is the rank of the analysis entity in the collection. The index of the first analysis entity in the collection is 1, and the index of the last analysis entity is Count. As a string, it is the name you assigned to the analysis entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method.  **Returns:**      The retrieved analysis entity  
### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a entity using its index or its name from the entity collection.

**Parameters:**

` iIndex`      The index or the name of the entity to retrieve from the collection of entities. As a numeric, this index is the rank of the entity in the collection. The index of the first entity in the collection is 1, and the index of the last entity is Count. As a string, it is the name you assigned to the entity using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# AnalysisPostManager (Object)

**_Interface to define the Post Processing Manager._**

**Role** : In the analysis document, an Post Processing is dedicated to Visualization and reporting.

## Methods

### Sub **AddExistingCaseForReport**( [CATIAAnalysisCase](../CATAnalysisInterfaces/interface_AnalysisCase_30608.md)  `iCase`)

   Adds an existing analysis case to manager. To declare Case which will be taken into account for the HTML report.

**Parameters:**

` iCase`      The Existing Analysis Case.

### Sub **BuildReport**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTitle`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iAddCreatedImages`)

   Extract the HTML Report. The Report is defined related to Analysis cases, using AddExistingCaseForReport and will be stored in a CATIA Folder.

**Parameters:**

` iFolder`      Folder to store the HTML file.
` iTitle`      Title of the report.
` iAddCreatedImages`      To add created images under analysis case in the report.

### Sub **ExtractHTMLReport**( [CATIAFolder](../InfInterfaces/interface_Folder_8034.md)  `iFolder`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iTitle`)

**Deprecated:**      V5R14 use BuildReport instead. Extract the HTML Report. The Report is defined related to Analysis cases, using AddExistingCaseForReport and will be stored in a CATIA Folder.  **Parameters:**

` iFolder`      Folder to store the HTML file.
` iTitle`      Title of the report.

---

# AnalysisPostProSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "PostProcessingSetting"._**

## Properties

### Property **AutoPreviewMode**( ) As boolean

   Returns or sets the AutoPreviewMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageTextSize**( ) As float

   Returns or sets the ImageTextSize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageTextStacking**( ) As long

   Returns or sets the ImageTextStacking parameter.

**Parameters:**

` iImageTextStacking`      **Legal values** :
`0 :` Text stacking is Horizontal
`1 :` Text stacking is Vertical Ensure consistency with the C++ interface to which the work is delegated.

### Property **ModeImageTextSize**( ) As boolean

   Returns or sets the ModeImageTextSize parameter.

**Parameters:**

` iModeImageTextSize`      **Legal values** :
`TRUE :` Enables the setting of image text size
`FALSE:` Disables the setting of image text size Ensure consistency with the C++ interface to which the work is delegated.

### Property **SaveAsNewTemplateDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the SaveAsNewTemplateDirectory parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetAutoPreviewModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the AutoPreviewMode parameter.

**Role** :Retrieves the state of the AutoPreviewMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageTextSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ImageTextSize parameter.

**Role** :Retrieves the state of the ImageTextSize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageTextStackingInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ImageTextStacking parameter.

**Role** :Retrieves the state of the ImageTextStacking parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetModeImageTextSizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ModeImageTextSize parameter.

**Role** :Retrieves the state of the ModeImageTextSize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSaveAsNewTemplateDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SaveAsNewTemplateDirectory parameter.

**Role** :Retrieves the state of the SaveAsNewTemplateDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetAutoPreviewModeLock**( boolean  `iLocked`)

   Locks or unlocks the AutoPreviewMode parameter.

**Role** :Locks or unlocks the AutoPreviewMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageTextSizeLock**( boolean  `iLocked`)

   Locks or unlocks the ImageTextSize parameter.

**Role** :Locks or unlocks the ImageTextSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageTextStackingLock**( boolean  `iLocked`)

   Locks or unlocks the ImageTextStacking parameter.

**Role** :Locks or unlocks the ImageTextStacking parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetModeImageTextSizeLock**( boolean  `iLocked`)

   Locks or unlocks the ModeImageTextSize parameter.

**Role** :Locks or unlocks the ModeImageTextSize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSaveAsNewTemplateDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the SaveAsNewTemplateDirectory parameter.

**Role** :Locks or unlocks the Xxx parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# AnalysisReportingSettingAtt (Object)

**_Interface to handle the Analysis & Simulation "ReportingSetting"._**

## Properties

### Property **BackgroundImageMode**( ) As boolean

   Returns or sets the BackgroundImageMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomBackgroundImage**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the CustomBackgroundImage parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageFormat**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the CustomImageFormat parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageHeight**( ) As long

   Returns or sets the CustomImageHeight parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **CustomImageWidth**( ) As long

   Returns or sets the CustomImageWidth parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ImageQualityMode**( ) As boolean

   Returns or sets the ImageQualityMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **TempOutputDirectory**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the TempOutputDirectory parameter.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetBackgroundImageModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the BackgroundImageMode parameter.

**Role** :Retrieves the state of the BackgroundImageMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomBackgroundImageInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CustomBackgroundImage parameter.

**Role** :Retrieves the state of the CustomBackgroundImage parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageFormatInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CustomImageFormat parameter.

**Role** :Retrieves the state of the CustomImageFormat parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageHeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CustomImageHeight parameter.

**Role** :Retrieves the state of the CustomImageHeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetCustomImageWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the CustomImageWidth parameter.

**Role** :Retrieves the state of the CustomImageWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetImageQualityModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ImageQualityMode parameter.

**Role** :Retrieves the state of the ImageQualityMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTempOutputDirectoryInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TempOutputDirectory parameter.

**Role** :Retrieves the state of the TempOutputDirectory parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetBackgroundImageModeLock**( boolean  `iLocked`)

   Locks or unlocks the BackgroundImageMode parameter.

**Role** :Locks or unlocks the BackgroundImageMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomBackgroundImageLock**( boolean  `iLocked`)

   Locks or unlocks the CustomBackgroundImage parameter.

**Role** :Locks or unlocks the CustomBackgroundImage parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageFormatLock**( boolean  `iLocked`)

   Locks or unlocks the CustomImageFormat parameter.

**Role** :Locks or unlocks the CustomImageFormat parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageHeightLock**( boolean  `iLocked`)

   Locks or unlocks the CustomImageHeight parameter.

**Role** :Locks or unlocks the ImageHeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetCustomImageWidthLock**( boolean  `iLocked`)

   Locks or unlocks the ImageWidth parameter.

**Role** :Locks or unlocks the ImageWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetImageQualityModeLock**( boolean  `iLocked`)

   Locks or unlocks the ImageQualityMode parameter.

**Role** :Locks or unlocks the DefaultImageQuality parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTempOutputDirectoryLock**( boolean  `iLocked`)

   Locks or unlocks the TempOutputDirectory parameter.

**Role** :Locks or unlocks the TempOutputDirectory parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# AnalysisSensor (Object)

**_Represent the analysis sensor._**

## Properties

### Property **OutPutParameters**( ) As [CATIAParameters](../KnowledgeInterfaces/interface_Parameters_22342.md) (Read Only)

   Returns the collection object containing the sensor parameters.

**Example:**     The following example returns in `params` the parameters computed by the sensor:

```VBScript
     Dim AnalysisSensor1 As AnalysisSensor
     Dim params As CATIAParameters
     Set params = AnalysisSensor1.OutPutParameters

```

Methods

### Sub **Update**( )

   Update the sensor. Computation of OutPutParameters if needed.

**Example:**     The following example computes the sensor:

```VBScript
     Dim AnalysisSensor1 As AnalysisSensor
     AnalysisSensor1.Update

```

---

# AnalysisSet (Object)

**_Represent the analysis set object._**
In the Analysis Model, an **Analysis Set** is the data dedicated to manage the **Analysis Entities** for specific preprocessing data.
For example, LoadSet will manage loading conditions...

## Properties

### Property **AnalysisEntities**( ) As [CATIAAnalysisEntities](../CATAnalysisInterfaces/interface_AnalysisEntities_55864.md) (Read Only)

   Returns the analysis entities collection associated to a set. The corresponding entities are default preprocessing objects.

**Example :**     This example retrieves `analysis entities` collection .

```VBScript
     Dim MySet As AnalysisSet
     Dim analysisEntities As AnalysisEntities
     Set analysisEntities = MySet.AnalysisEntities

```

### Property **AnalysisImages**( ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

   Returns the analysis images collection associated with an analysis set.

**Example:**     This example retrieves `analysisimages` collection .

```VBScript
     Dim MySet As AnalysisSet
     Dim analysisimages As AnalysisImages
     Set analysisimages = MySet.AnalysisImages

```

### Property **AnalysisOutputEntities**( ) As [CATIAAnalysisOutputEntities](../CATAnalysisInterfaces/interface_AnalysisOutputEntities_105692.md) (Read Only)

   Returns the analysis entities collection associated to a set. The corresponding entities are not preprocessing features but can be used, for example to manage error features.

**Example:**     This example retrieves `analysisEntities` collection .

```VBScript
     Dim MySet As AnalysisSet
     Dim analysisEntities As AnalysisOutputEntities
     Set analysisEntities = MySet.AnalysisOutputEntities

```

### Property **AnalysisSets**( ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

   Returns the analysis sets collection associated with an analysis set. This method will return a collection only if the set is made of other sets.

**Example:**     This example retrieves `analysisSets` collection .

```VBScript
     Dim MySet As AnalysisSet
     Dim analysisSets As AnalysisSets
     Set analysisSets = MySet.AnalysisSets

```

### Property **BasicComponents**( ) As [CATIABasicComponents](../CATAnalysisInterfaces/interface_BasicComponents_48940.md) (Read Only)

   Returns the basic components collection associated with an analysis set.

**Example:**     This example retrieves ` basiccomponents` collection .

```VBScript
     Dim MySet As AnalysisSet
     Dim basiccomponents As BasicComponents
     Set basiccomponents = MySet.BasicComponents

```

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the analysis Set.

**Example:**     The following example returns `TypeofSet` of `MySet`.

```VBScript
     Dim MySet As AnalysisSet
     Dim TypeofSet As CATBSTR
     Set TypeofSet = MySet.Type

```

Methods

### Sub **Update**( )

   Launch the update (computation if needed) of an AnalysisSet.

---

# AnalysisSets (Collection)

**_The collection of analysis sets._**

## Methods

### Func **Add**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`,  [CATAnalysisSetType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.md)  `iSetType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

   Creates a new analysis set and adds it to the analysis sets collection.
The analysis set will be aggregated on the Analysis Model

**Parameters:**

` iType`      The type of the set to create.
` iSetType`      The category of the set for update.

**Returns:**      The created Analysis Set  **Example:**      This example create `ThisAnalysisSet` in the `analysisSets`analysis
sets collection. The set to create is supposed to be a load set defined as an input of
the case for the update.

```VBScript
     Dim ThisAnalysisSet As AnalysisSet
     Set ThisAnalysisSet = analysisSets.Add("LoadSet", 0)

```

### Sub **AddExistingSet**( [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)  `iSet`,  [CATAnalysisSetType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.md)  `iSetType`)

   Adds an existing analysis set to the analysis sets collection.

**Parameters:**

` iSet`      The Existing Analysis Set.
` iSetType`      The category of the set for update.

**Example:**      This example adds `ThisAnalysisSet` in the `analysisSets`analysis
sets collection. The set to add is supposed to be a restrain set defined as an input of
the case for the update.

```VBScript
     Dim ThisAnalysisSet As AnalysisSet
     ...
     analysisSets.AddExistingSet(ThisAnalysisSet, 0)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  [CATAnalysisSetSearchType](../CATAnalysisInterfaces/enum_CATAnalysisSetSearchType_118426.md)  `iSerachType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

   Returns an analysis set using its index or its name from the analysis sets collection.

**Parameters:**

` iIndex`      The index or the name of the analysis set to retrieve from the collection of analysis sets. As a numerics, this index is the rank of the analysis set in the collection. The index of the first analysis set in the collection is 1, and the index of the last analysis set is Count. As a string, it is the name you assigned to the analysis set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property or when creating it using the Add method. ` iSerachType`      The criterion of searching the set.
[CATAnalysisSetType.CATAnalysisSetSearchType](../CATAnalysisInterfaces/enum_CATAnalysisSetType_67392.htm#CATAnalysisSetSearchType) **Returns:**      The retrieved analysis set  **Example:**      This example retrieves in `ThisAnalysisSet` the third analysis set, and in `ThatAnalysisSet` the analysis set named `MySet` in the analysis set collection of an Analysis Case of analysis model.

```VBScript
     Dim ThisAnalysisSet As AnalysisSet
     Set ThisAnalysisSet = analysisCase.AnalysisSets.Item(3,1)
     Dim ThatAnalysisSet As AnalysisSet
     Set ThatAnalysisSet = analysisCase.AnalysisSets.Item("MySet")

```

### Func **ItemByType**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iType`) As [CATIAAnalysisSet](../CATAnalysisInterfaces/interface_AnalysisSet_26478.md)

   Returns an analysis set using its type from the analysis sets collection.

**Parameters:**

` iType`      The type of the set required for the search

**Returns:**      The retrieved analysis set  **Example:**      This example retrieves in `ThisAnalysisSet` the "LoadSet" analysis set in the analysis set collection.

```VBScript
     Dim ThisAnalysisSet As AnalysisSet
     Set ThisAnalysisSet = analysisCase.AnalysisSets.ItemByType("LoadSet")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a set using its index or its name from the set collection.

**Parameters:**

` iIndex`      The index or the name of the set to retrieve from the collection of sets. As a numeric, this index is the rank of the set in the collection. The index of the first set in the collection is 1, and the index of the last set is Count. As a string, it is the name you assigned to the set using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.

---

# AnalysisSupports (Collection)

**_The collection of analysis case making an Analysis._**

## Methods

### Sub **Item**( long  `iIndex`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oPositionning`,  [CATIABase](../System/interface_AnyObject_17321.md)  `oPointed`)

   Returns analysis support object information using its index in the collection.

**Parameters:**

` iIndex`      The numeric index is the rank in the collection. The index of the first case in the collection is 1, and the index of the last is Count.
` oPositionning`      The positionning feature is exists.
` oPointed`      The pointed object.

---

# BasicComponent (Object)

**_Interface designed to manage**Analysis Basic Components**._**

A **Basic Component** is the low level of physical descriptive data. It is a "brick" dedicated to build the **Analysis Entity** or an **Analysis Set** .

A **Basic Components** can contain several **Blocks**. A **Block** is identified by a label. It contains entity data of the same type, organized in superimposed tables.

To create **Analysis Entities** with a complex structure, we have also created a particular **Basic Component** dedicated to encapsulate other **Basic Components**.

## Properties

### Property **BasicComponents**( ) As [CATIABasicComponents](../CATAnalysisInterfaces/interface_BasicComponents_48940.md) (Read Only)

   Returns the collection of Basic Components agregated by the basic component. It can be (scalar value, vector, tensor,...). Depending on the type of the Basic component, the collection can be empty.

**Example:**      This example retrieves `Basic components` collection

```VBScript
     Dim MyBasicComp As BasicComponent
     Dim myBasicComponents As BasicComponents
     Set myBasicComponents = MyBasicComp.BasicComponents

### Property **Entities**( ) As [CATIAAnalysisEntities](../CATAnalysisInterfaces/interface_AnalysisEntities_55864.md)  (Read Only)

     Returns the collection of Entities agregated by the basic component.
     Depending on the type of the Basic component,the collection can be empty.

       **Example:**
            This example retrieves Basic components collection

```VBScript
     Dim MyBasicComp As BasicComponent
     Dim myEntities AnalysisEntities
     Set myEntities = MyBasicComp.AnalysisEntities

### Property **Type**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)  (Read Only)

     Returns the type of the Basic Component.

       **Returns:**
            The string that represent the Basic Component type.

     Methods

### Sub **AddSupportFromProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  iProduct,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iSupport)

     Creates a new support and add it to the description of the basic component.

       **Parameters:**

         iProduct
             the CATIA Product that represent the object to linked.

         iSupport
             the CATIA Reference that represent the object to linked.

       **See also:**
           [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md)

### Sub **AddSupportFromPublication**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  iProduct,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  iPublication)

     Creates a new support and add it to the description of the Basic Component.

       **Parameters:**

         iProduct
             the CATIA Product that represent the object to linked.

         iPublication
             the CATIA Publication that represent the object to linked.

       **See also:**
           [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md)

### Sub **AddSupportFromReference**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iReference,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iSupport)

     Creates a new support and add it to the description of the basic component.

       **Parameters:**

         iReference
            the CATIA Reference that represent the object to linked.

         iSupport
             the CATIA Reference that represent the object to linked.

       **See also:**
           [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md)

### Func **GetColumnsNumber**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel) As long

     Return one of the dimensions information of the Basic Component structure.

       **Parameters:**

         oColumnsNumber
            = Number of Columns.

### Func **GetLayersNumber**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel) As long

     Return one of the dimensions information of the Basic Component structure.

       **Parameters:**

         oLayersNumber
            = Number of Layers.

### Func **GetLinesNumber**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel) As long

     Return one of the dimensions information of the Basic Component structure.

       **Parameters:**

         oLinesNumber
            = Number of lines.

### Func **GetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex) As [CATVariant](../System/typedef_CATVariant_20656.md)

     Return the value corresponding to the given coordinates.

       **Parameters:**

         iLabel
            = Label of the block containing the value.

         iLineIndex
            = line index of the value.

         iColumnIndex
            = column index of the value.

         iLayerIndex
            = layer index of the value.
     If the the component has a single value, set these 3 parameters
     to 0.

### Sub **SetDimensions**( long  iLineCount,  long  iColumnCount,  long  iLayerCount)

     Sets the dimensions of the basic component.

       **Parameters:**

         iLineCount
             Number of lines.

         iColumnCount
             Number of columns.

         iLayerCount
             Number of layers.

### Sub **SetReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  iValue)

     Sets the reference corresponding to the given component.

       **Parameters:**

         iLabel
             The label of the block containing the value.

         iLineIndex
             The line index of the value.

         iColumnIndex
             The column index of the value.

         iLayerIndex
             The layer index of the value.
     If the the component has a single value, assign 0 to the 3 parameters.

### Sub **SetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  iLabel,  long  iLineIndex,  long  iColumnIndex,  long  iLayerIndex,  [CATVariant](../System/typedef_CATVariant_20656.md)  iValue)

     Set the value corresponding to the given coordinates.

       **Parameters:**

         iLabel
            = Label of the block containing the value.

         iLineIndex
            = line index of the value.

         iColumnIndex
            = column index of the value.

         iLayerIndex
            = layer index of the value.
     If the the component has a single value, set these 3 parameters
     to 0.

---

# BasicComponents (Collection)

**_The collection of Basic Components defining and analysis object._**
These components are agregated by another basic component, an entity or a set.

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iVariant`) As [CATIABasicComponent](../CATAnalysisInterfaces/interface_BasicComponent_42336.md)

   Returns an Basic Component using its index or its name from the Basic Components collection.

**Parameters:**

` iIndex`      The index or the name of the Basic Component to retrieve from the collection of Basic Component. As a numerics, this index is the rank of the Basic Component. in the collection. The index of the first Basic Component in the collection is 1, and the index of the last Basic Component is Count. As a string, it is the name you assigned to the Basic Component using the
[AnyObject.Name](../System/interface_AnyObject_17321.htm#Name) property.  **Returns:**      The retrieved Basic Component