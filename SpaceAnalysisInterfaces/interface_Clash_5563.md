# Clash (Object)

**_Represents the Clash object._**
The Clash object is a specification of a collision detection of products.

## Properties

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

Returns the AnnotatedViews collection of the clash.

**Example:**      This example retrieves the AnnotatedViews collection of `NewClash` Clash.

```VBScript
   Dim TheAnnotatedViewsList As AnnotatedViews
   Set TheAnnotatedViewsList = NewClash.AnnotatedViews

```

### Property **Clearance**( ) As double

Returns or sets the clearance value for the computation. The clearance value must be greater than 0. Units are Millimeter.

**Example:**      The first example retrieves the clearance value of `NewClash` Clash.

```VBScript
   Dim Value As double
   Value = NewClash.Clearance

```

The second example sets the clearance value of `NewClash` Clash.

```VBScript
   NewClash.Clearance = 10.

```

### Property **ComputationType**( ) As [CatClashComputationType](../SpaceAnalysisInterfaces/enum_CatClashComputationType_112738.md)

Returns or sets the computation type.

**Example:**      The first example retrieves the computation type of `NewClash` Clash.

```VBScript
   Dim ComputationType As CatClashComputationType
   ComputationType = NewClash.ComputationType

```

The second example sets the computation type of `NewClash` Clash.

```VBScript
   NewClash.ComputationType = catClashComputationTypeBetweenAll

```

### Property **Conflicts**( ) As [CATIAConflicts](../SpaceAnalysisInterfaces/interface_Conflicts_18103.md) (Read Only)

Returns the collection of computed Conflicts.

**Example:**      This example retrieves the conflicts of `NewClash` Clash.

```VBScript
   Dim NewConflicts As Conflicts
   Set NewConflicts = NewClash.Conflicts

```

### Property **FirstGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

Returns or sets the first group used by the computation.

**Example:**      The first example retrieves the first group of `NewClash` Clash.

```VBScript
   Dim FirstGroup As Group
   Set FirstGroup = NewClash.FirstGroup

```

The second example sets the first group of `NewClash` Clash.

```VBScript
   Dim FirstGroup As Group
   NewClash.FirstGroup = FirstGroup

```

### Property **InterferenceType**( ) As [CatClashInterferenceType](../SpaceAnalysisInterfaces/enum_CatClashInterferenceType_120652.md)

Returns or sets the interference type for the computation.

**Example:**      The first example retrieves the interference type of `NewClash` Clash.

```VBScript
   Dim InterferenceType As CatClashInterferenceType
   InterferenceType = NewClash.InterferenceType

```

The second example sets the interference Type of `NewClash` Clash.

```VBScript
   NewClash.InterferenceType = CatClashInterferenceTypeContact

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

Returns the Marker3Ds collection of the clash.

**Example:**      This example retrieves the Marker3Ds collection of `NewClash` Clash.

```VBScript
   Dim TheMarker3DsList As Marker3Ds
   Set TheMarker3DsList = NewClash.Marker3Ds

```

### Property **SecondGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

Returns or sets the second group used by the computation.

**Example:**      The first example retrieves the second group of `NewClash` Clash.

```VBScript
   Dim SecondGroup As Group
   Set SecondGroup = NewClash.SecondGroup

```

The second example sets the second group of `NewClash` Clash.

```VBScript
   Dim SecondGroup As Group
   NewClash.SecondGroup = SecondGroup

```

Methods

### Sub **Compute**( )

Computes the conflicts.

**Example:**      This example computes the conflicts of `NewClash` Clash.

```VBScript
   NewClash.Compute

```

### Sub **Export**( [CatClashExportType](../SpaceAnalysisInterfaces/enum_CatClashExportType_69048.md)  `iType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

Exports the results in a XML file.

**Parameters:**

` iType`      The type of export.
` iPath`      The path of the file.
**Example:**      This example exports the results of `NewClash` Clash.

```VBScript
   Dim ThePath As String
   NewClash.Export CatClashExportTypeXMLResultOnly, "c:\tmp\sample.xml"

```