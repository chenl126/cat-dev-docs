# SPAWorkbench (Object)

**_The object to manage all Space Analysis objects._**

This version allows you to manage inertia data, clashes, distances and sections.

## Properties

### Property **Clashes**(| ) As [CATIAClashes](../SpaceAnalysisInterfaces/interface_Clashes_10879.md) (Read Only)

   Returns the Clashes collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Clashes")` on the root product, to retrieve the `Clashes` collection.

**Example:**      This example retrieves the Clashes collection of the active document.

```VBScript
        Dim TheSPAWorkbench As Workbench
        Set TheSPAWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SPAWorkbench" )
        Dim TheClashesList As Clashes
        Set TheClashesList = TheSPAWorkbench.Clashes

```

### Property **Distances**( ) As [CATIADistances](../SpaceAnalysisInterfaces/interface_Distances_17870.md) (Read Only)

   Returns the Distances collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Distances")` on the root product, to retrieve the `Distances` collection.

**Example:**      This example retrieves the Distances collection of the active document.

```VBScript
        Dim TheSPAWorkbench As Workbench
        Set TheSPAWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SPAWorkbench" )
        Dim TheDistancesList As Distances
        Set TheDistancesList = TheSPAWorkbench.Distances

```

### Property **Inertias**( ) As [CATIAInertias](../SpaceAnalysisInterfaces/interface_Inertias_14370.md) (Read Only)

   Returns the Inertias collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Inertia")` on the product to analyze, to retrieve an `Inertia` object.

**Example:**      This example retrieves the Inertias collection of the active document.

```VBScript
        Dim TheSPAWorkbench As Workbench
        Set TheSPAWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SPAWorkbench" )
        Dim TheInertiasList As Inertias
        Set TheInertiasList = TheSPAWorkbench.Inertias

```

### Property **Sections**( ) As [CATIASections](../SpaceAnalysisInterfaces/interface_Sections_14574.md) (Read Only)

   Returns the Sections collection. WARNING: this method will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Sections")` on the root product, to retrieve the `Sections` collection.

**Example:**      This example retrieves the Sections collection of the active document.

```VBScript
        Dim TheSPAWorkbench As Workbench
        Set TheSPAWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SPAWorkbench" )
        Dim TheSectionsList As Sections
        Set TheSectionsList = TheSPAWorkbench.Sections

```

Methods

### Func **GetMeasurable**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iMeasuredItem`) As [CATIAMeasurable](../SpaceAnalysisInterfaces/interface_Measurable_21738.md)

   Returns the Measurable object.

**Example:**      This example get the Measurable from the SPAWorkBench.

```VBScript
        Dim referenceObject As referenceObject
        Set referenceObject = "GetReference"
        Dim TheSPAWorkbench As Workbench
        Set TheSPAWorkbench = CATIA.ActiveDocument.GetWorkbench ( "SPAWorkbench" )
        Dim TheMeasurable As Measurable
        Set TheMeasurable = TheSPAWorkbench.GetMeasurable(referenceObject)

```