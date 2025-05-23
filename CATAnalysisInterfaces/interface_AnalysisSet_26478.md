# AnalysisSet (Object)

**_Represent the analysis set object._**
In the Analysis Model, an **Analysis Set** is the data dedicated to manage the **Analysis Entities** for specific preprocessing data.
For example, LoadSet will manage loading conditions...

## Properties

### Property **AnalysisEntities**(| ) As [CATIAAnalysisEntities](../CATAnalysisInterfaces/interface_AnalysisEntities_55864.md) (Read Only)

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