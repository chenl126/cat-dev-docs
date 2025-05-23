# AnalysisCase (Object)

**_Represent the analysis case object._**

**Role:** Interface designed to manage **Analysis Case behavior**.
In the Analysis document, an **Analysis Case** is the object dedicated to define and manage the environment data necessary to run a computation. This environment is made of sets.

## Properties

### Property **AnalysisSets**(| ) As [CATIAAnalysisSets](../CATAnalysisInterfaces/interface_AnalysisSets_31754.md) (Read Only)

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