# AnalysisModel (Object)

**_Represent the analysis model object._**

**Role** : In the analysis document, an analysis model is the object dedicated to set and manage all the required data for the discretization and idealization of a Finite Element model.
This object gives access to:

  * A collection of AnalysisCase.
  * A collection of AnalysisSets (All the input sets like properties, groups).
  * A AnalysisPostManager object for reporting.

## Properties

### Property **AdaptivityManager**(| ) As [CATIAAnalysisAdaptivityManager](../CATAnalysisInterfaces/interface_AnalysisAdaptivityManager_132794.md) (Read Only)

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