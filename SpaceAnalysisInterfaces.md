# SpaceAnalysisInterfaces Framework

## Object Index

  * [Clash](SpaceAnalysisInterfaces/interface_Clash_5563.md)
  * [ClashResult](SpaceAnalysisInterfaces/interface_ClashResult_26594.md)
  * [ClashResults](SpaceAnalysisInterfaces/interface_ClashResults_31864.md)
  * [Clashes](SpaceAnalysisInterfaces/interface_Clashes_10879.md)
  * [Conflict](SpaceAnalysisInterfaces/interface_Conflict_14180.md)
  * [Conflicts](SpaceAnalysisInterfaces/interface_Conflicts_18103.md)
  * [Distance](SpaceAnalysisInterfaces/interface_Distance_13954.md)
  * [Distances](SpaceAnalysisInterfaces/interface_Distances_17870.md)
  * [Inertia](SpaceAnalysisInterfaces/interface_Inertia_10894.md)
  * [Inertias](SpaceAnalysisInterfaces/interface_Inertias_14370.md)
  * [Measurable](SpaceAnalysisInterfaces/interface_Measurable_21738.md)
  * [MeasureSettingAtt](SpaceAnalysisInterfaces/interface_MeasureSettingAtt_61701.md)
  * [SPAWorkbench](SpaceAnalysisInterfaces/interface_SPAWorkbench_29716.md)
  * [Section](SpaceAnalysisInterfaces/interface_Section_11089.md)
  * [SectioningSettingAtt](SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md)
  * [Sections](SpaceAnalysisInterfaces/interface_Sections_14574.md)

## Enumerated Types Index

  * [CatClashComputationType](SpaceAnalysisInterfaces/enum_CatClashComputationType_112738.md)
  * [CatClashExportType](SpaceAnalysisInterfaces/enum_CatClashExportType_69048.md)
  * [CatClashImportType](SpaceAnalysisInterfaces/enum_CatClashImportType_68774.md)
  * [CatClashInterferenceType](SpaceAnalysisInterfaces/enum_CatClashInterferenceType_120652.md)
  * [CatConflictComparison](SpaceAnalysisInterfaces/enum_CatConflictComparison_93987.md)
  * [CatConflictStatus](SpaceAnalysisInterfaces/enum_CatConflictStatus_62234.md)
  * [CatConflictType](SpaceAnalysisInterfaces/enum_CatConflictType_47830.md)
  * [CatDistanceComputationType](SpaceAnalysisInterfaces/enum_CatDistanceComputationType_143950.md)
  * [CatDistanceMeasureType](SpaceAnalysisInterfaces/enum_CatDistanceMeasureType_101708.md)
  * [CatGridPositionMode](SpaceAnalysisInterfaces/enum_CatGridPositionMode_75400.md)
  * [CatMeasurableName](SpaceAnalysisInterfaces/enum_CatMeasurableName_59602.md)
  * [CatSecWindowOpenMode](SpaceAnalysisInterfaces/enum_CatSecWindowOpenMode_82170.md)
  * [CatSectionBehavior](SpaceAnalysisInterfaces/enum_CatSectionBehavior_68434.md)
  * [CatSectionClippingMode](SpaceAnalysisInterfaces/enum_CatSectionClippingMode_100444.md)
  * [CatSectionGridStyle](SpaceAnalysisInterfaces/enum_CatSectionGridStyle_76008.md)
  * [CatSectionPlaneNormal](SpaceAnalysisInterfaces/enum_CatSectionPlaneNormal_91976.md)
  * [CatSectionPlaneOrigin](SpaceAnalysisInterfaces/enum_CatSectionPlaneOrigin_91941.md)
  * [CatSectionType](SpaceAnalysisInterfaces/enum_CatSectionType_41996.md)

---

# CatClashComputationType (Enumeration)

**_The different types of clash computation._**
It is used by the [Clash](../SpaceAnalysisInterfaces/interface_Clash_5563.md) object to specify the computation type.

**Values:**

` catClashComputationTypeBetweenAll`      The computation tests each product in the document against all other products.
` catClashComputationTypeInsideOne`      The computation tests each product of the selection/group against all other products in the same selection.
` catClashComputationTypeAgainstAll`      The computation tests each product in the defined selection/group against all other products in the document.
` catClashComputationTypeBetweenTwo`      The computation tests each product in the first selection/group against all products in the second group.

---

# CatClashExportType (Enumeration)

**_The different types of clash export._**
It is used by the [Clash](../SpaceAnalysisInterfaces/interface_Clash_5563.md) and [ClashResult](../SpaceAnalysisInterfaces/interface_ClashResult_26594.md) objects to specify the export type.

**Values:**

` CatClashExportTypeXMLResultOnly`      The export is done using XML format with only the result data

---

# CatClashImportType (Enumeration)

**_The different types of clash import._**
It is used by the [ClashResults](../SpaceAnalysisInterfaces/interface_ClashResults_31864.md) object to specify the Import type.

**Values:**

` CatClashImportTypeClashOnly`      Only the clash data are imported
` CatClashImportTypeStructureAndClash`      Product structure data are inserted then clash data are imported

---

# CatClashInterferenceType (Enumeration)

**_The different types of clash interference._**
It is used by the [Clash](../SpaceAnalysisInterfaces/interface_Clash_5563.md) object to specify the interference type.

**Values:**

` catClashInterferenceTypeContact`      The computation tests penetration or contact between two products
` catClashInterferenceTypeClearance`      The computation tests penetration, contact or violation of clearance between two products
` catClashInterferenceAuthorizedPenetration`      The computation is ran with an authorized penetration taken into account
` catClashInterferenceCaseRule`      The computation is ran with the specification computed by the knowledge rules

---

# CatConflictComparison (Enumeration)

**_The different cases of comparison of conflicts._**
It is used by the [Conflict](../SpaceAnalysisInterfaces/interface_Conflict_14180.md) object to inform on a comparison with a previous computation on the same Clash object.

**Values:**

` catConflictComparisonNew`      The conflict is a new one.
` catConflictComparisonOld`      The conflict is an old one.
` catConflictComparisonNo`      There is no information on the conflict.

---

# CatConflictStatus (Enumeration)

**_The different statuses of conflicts._**
It is used by the [Conflict](../SpaceAnalysisInterfaces/interface_Conflict_14180.md) object to specify the conflict status.

**Values:**

` catConflictStatusNotInspected`      The conflict was not inspected since it was discovered.
` catConflictStatusRelevant`      The conflict was inspected and declared relevant by the user.
` catConflictStatusIrrelevant`      The conflict was inspected and declared irrelevant by the user.
` catConflictStatusSolved`      The conflict has been computed as SOLVED by the comparison soft

---

# CatConflictType (Enumeration)

**_The different types of conflicts._**
It is used by the [Conflict](../SpaceAnalysisInterfaces/interface_Conflict_14180.md) object to specify the result type.

**Values:**

` catConflictTypeClash`      The two products are in clash.
` catConflictTypeContact`      The two products are in contact.
` catConflictTypeClearance`      The two products are too close.

---

# CatDistanceComputationType (Enumeration)

**_The different types of clash computation._**
It is used by the [Distance](../SpaceAnalysisInterfaces/interface_Distance_13954.md) object to specify the computation type.

**Values:**

` catDistanceComputationTypeInsideOne`      The computation tests each product of the selection/group against all other products in the same selection.
` catDistanceComputationTypeAgainstAll`      The computation tests each product in the defined selection/group against all other products in the document.
` catDistanceComputationTypeBetweenTwo`      The computation tests each product in the first selection/group against all products in the second group.

---

# CatDistanceMeasureType (Enumeration)

**_The different types of distance measure._**
It is used by the [Distance](../SpaceAnalysisInterfaces/interface_Distance_13954.md) object to specify the measure type.

**Values:**

` catDistanceMeasureTypeMinimum`      The computation measures the minimum distance between products
` catDistanceMeasureTypeAlongX`      The computation measures the minimum distance along X between products
` catDistanceMeasureTypeAlongY`      The computation measures the minimum distance along Y between products
` catDistanceMeasureTypeAlongZ`      The computation measures the minimum distance along Z between products
` catDistanceMeasureTypeBand`      The computation analyses the band between products

---

# CatGridPositionMode (Enumeration)

**_The different modes for section grid positioning._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the section grid's positioning mode in settings.

**Values:**

` catGridPositionMode_Absolute`      The grid's positioning is absolute.
` catGridPositionMode_Relative`      The grid's positioning is relative.

---

# CatMeasurableName (Enumeration)

**__**

---

# CatSectionBehavior (Enumeration)

**_The different types of a section._**
It is used by the [Section](../SpaceAnalysisInterfaces/interface_Section_11089.md) object to specify the section Behavior.

**Values:**

` catSectionBehaviorManual`      The update of the section has to be done manually. The icon is changing to show that the section result is not updated.
` catSectionBehaviorAutomatic`      The update of the section while a product is moving is done automatically.
` catSectionBehaviorFreeze`      The section result is freezed. No result will be recalculated untill the user unfreeze it.

---

# CatSectionClippingMode (Enumeration)

**_The different algorithmes used to computate the section result._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the section's computation mode.

**Values:**

` catSection_Software`      The section is software computed (the result is more precise but slower).
` catSection_OpenGL`      The section is computed by the graphic card (the result is faster but less precise).

---

# CatSectionGridStyle (Enumeration)

**_The different styles of the section grid._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the section grid's style in settings.

**Values:**

` catSectionGridStyle_Lines`      The grid's lines are displayed.
` catSectionGridStyle_Crosses`      Only the grid's intersections are displayed.

---

# CatSectionPlaneNormal (Enumeration)

**_The different default normals for the section plane._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the plane's normal in settings.

**Values:**

` catSectionNormal_X`      The normal of the section plane is along the X axis.
` catSectionNormal_Y`      The normal of the section plane is along the Y axis.
` catSectionNormal_Z`      The normal of the section plane is along the Z axis.

---

# CatSectionPlaneOrigin (Enumeration)

**_The different default origins for the section plane._**
It is used by the [SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the plane's origin in settings.

**Values:**

` catSectionOrigin_0`      The origin of the section plane is at coordinates (0,0,0).
` catSectionOrigin_Selection`      The origin of the section plane is on the selected point.

---

# CatSectionType (Enumeration)

**_The different types of a section._**
It is used by the [Section](../SpaceAnalysisInterfaces/interface_Section_11089.md) object to specify the section type.

**Values:**

` catSectionTypePlane`      The section is a plane.
` catSectionTypeSlice`      The section is made of two parallel planes separated by a thickness.
` catSectionTypeBox`      The section is a box.

---

# CatSecWindowOpenMode (Enumeration)

**_The different modes of opening the sectioning windows It is used by the_**
[SectioningSettingAtt](../SpaceAnalysisInterfaces/interface_SectioningSettingAtt_85288.md) object to specify the mode of opening the section window in settings.

**Values:**

` catSecWindow_DefaultSize`      Open the sectioning window with the default size specified in the Tools->Options.
` catSecWindow_TileVertically`      Tile the sectioning window vertically in the viewer

---

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

---

# Clashes (Collection)

**_A collection of all Clash objects currently managed by the application._**

The method `GetTechnologicalObject("Clashes")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**( ) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

   Creates a Clash object which takes all products into account and adds it to the Clashes collection.

**Returns:**      The created Clash  **Example:**      This example creates a new Clash in the `TheClashes` collection.

```VBScript
        Dim NewClash As Clash
        Set NewClash = TheClashes.Add

```

### Func **AddFromSel**( ) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

   Creates a Clash object which takes all products in the selection into account and adds it to the Clashes collection.

**Returns:**      The created Clash  **Example:**      This example creates a new Clash in the `TheClashes` collection.

```VBScript
        Dim NewClash As Clash
        Set NewClash = TheClashes.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAClash](../SpaceAnalysisInterfaces/interface_Clash_5563.md)

   Returns a Clash object using its index or its name from the Clashes collection.

**Parameters:**

` iIndex`      The index or the name of the Clash to retrieve from the collection of Clashes. As a numerics, this index is the rank of the Clash in the collection. The index of the first Clash in the collection is 1, and the index of the last Clash is Count. As a string, it is the name you assigned to the Clash.

**Example:**      This example retrieves in `ThisClash` the ninth Clash, and in `ThatClash` the Clash named `Clash Of MyProduct` from the `TheClashes` collection.

```VBScript
        Dim ThisClash As Clash
        Set ThisClash = TheClashes.Item(9)
        Dim ThatClash As Clash
        Set ThatClash = TheClashes.Item("Clash Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Clash object from the Clashes collection.

**Parameters:**

` iIndex`      The index or the name of the Clash to remove from the collection of Clashes. As a numerics, this index is the rank of the Clash in the collection. The index of the first Clash in the collection is 1, and the index of the last Clash is Count. As a string, it is the name you assigned to the Clash.

**Example:**      The following example removes the tenth Clash and the Clash named `Clash Of MyProduct` from the `TheClashes` collection.

```VBScript
        TheClashes.Remove(10)
        TheClashes.Remove("Clash Of MyProduct")

```

---

# ClashResult (Object)

**_Represents the ClashResult object._**
The ClashResult object is a set of conflicts resulting from a clash detection.

## Properties

### Property **Conflicts**( ) As [CATIAConflicts](../SpaceAnalysisInterfaces/interface_Conflicts_18103.md) (Read Only)

   Returns the collection of computed Conflicts.

**Example:**      This example retrieves the conflicts of `NewClashResult` ClashResult.

```VBScript
        Dim NewConflicts As Conflicts
        Set NewConflicts = NewClashResult.Conflicts

```

Methods

### Sub **Export**( [CatClashExportType](../SpaceAnalysisInterfaces/enum_CatClashExportType_69048.md)  `iType`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

   Exports the results in a XML file.

**Parameters:**

` iType`      The type of export.
` iPath`      The path of the file.

**Example:**      This example exports the results of `NewClashResult` ClashResult.

```VBScript
        Dim ThePath As String
        NewClashResult.Export CatClashExportTypeXMLResultOnly, "c:\tmp\sample.xml"

```

---

# ClashResults (Collection)

**_A collection of all ClashResult objects currently managed by the application._**

The results linked to a specification are not managed thru this collection (see [Clashes](../SpaceAnalysisInterfaces/interface_Clashes_10879.md) ).

The method `GetTechnologicalObject("ClashResults")` on the root product, allows you to retrieve this collection.

## Methods

### Func **AddFromXML**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`,  [CatClashImportType](../SpaceAnalysisInterfaces/enum_CatClashImportType_68774.md)  `iType`) As [CATIAClashResult](../SpaceAnalysisInterfaces/interface_ClashResult_26594.md)

   Creates a ClashResult object from a XML file and adds it to the ClashResults collection.

**Parameters:**

` iPath`      The path of the XML file.
` iType`      The type of import.

**Returns:**      The created ClashResult  **Example:**      This example creates a new ClashResult in the `TheClashResults` collection.

```VBScript
        Dim NewClashResult As ClashResult
        Set NewClashResult = TheClashResults.AddFromXML("c:\tmp\sample.xml", CatClashImportTypeClashOnly)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAClashResult](../SpaceAnalysisInterfaces/interface_ClashResult_26594.md)

   Returns a ClashResult object using its index or its name from the ClashResults collection.

**Parameters:**

` iIndex`      The index or the name of the ClashResult to retrieve from the collection of ClashResults. As a numerics, this index is the rank of the ClashResult in the collection. The index of the first ClashResult in the collection is 1, and the index of the last ClashResult is Count. As a string, it is the name you assigned to the ClashResult.

**Example:**      This example retrieves in `ThisClashResult` the ninth ClashResult, and in `ThatClashResult` the ClashResult named `ClashResult Of MyProduct` from the `TheClashResults` collection.

```VBScript
        Dim ThisClashResult As ClashResult
        Set ThisClashResult = TheClashResults.Item(9)
        Dim ThatClashResult As ClashResult
        Set ThatClashResult = TheClashResults.Item("ClashResult Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a ClashResult object from the ClashResults collection.

**Parameters:**

` iIndex`      The index or the name of the ClashResult to remove from the collection of ClashResults. As a numerics, this index is the rank of the ClashResult in the collection. The index of the first ClashResult in the collection is 1, and the index of the last ClashResult is Count. As a string, it is the name you assigned to the ClashResult.

**Example:**      The following example removes the tenth ClashResult and the ClashResult named `ClashResult Of MyProduct` from the `TheClashResults` collection.

```VBScript
        TheClashResults.Remove(10)
        TheClashResults.Remove("ClashResult Of MyProduct")

```

---

# Conflict (Object)

**_Represents the Conflict object._**

One Conflict object exists for each couple of products that are colliding.

## Properties

### Property **Comment**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets a comment on the conflict.

**Example:**      The first example gets the comment of `NewConflict` Conflict.

```VBScript
        Dim aComment As String
        aComment = NewConflict.Comment

```

   The second example sets a comment on the `NewConflict` Conflict.

```VBScript
        NewConflict.Comment = "OK : plastic part"

```

### Property **ComparisonInfo**( ) As [CatConflictComparison](../SpaceAnalysisInterfaces/enum_CatConflictComparison_93987.md) (Read Only)

   Returns the information on the comparison between the conflict and the previous one.

**Example:**      This example retrieves the comparison information of the `NewConflict` Conflict.

```VBScript
        Dim anInfo As CatConflictComparison
        anInfo = NewConflict.ComparisonInfo

```

### Property **FirstProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the first product involved in the conflict.

**Example:**      This example retrieves the first product involved in the `NewConflict` Conflict.

```VBScript
        Dim aProduct As Product
        Set aProduct = NewConflict.FirstProduct

```

### Property **SecondProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the second product involved in the conflict.

**Example:**      This example retrieves the second product involved in the `NewConflict` Conflict.

```VBScript
        Dim aProduct As Product
        Set aProduct = NewConflict.SecondProduct

```

### Property **Status**( ) As [CatConflictStatus](../SpaceAnalysisInterfaces/enum_CatConflictStatus_62234.md)

   Returns or sets the status of the conflict.

**Example:**      The first example gets the status of `NewConflict` Conflict.

```VBScript
        Dim aStatus As CatConflictStatus
        aStatus = NewConflict.Status

```

   The second example sets the status of `NewConflict` Conflict.

```VBScript
        NewConflict.Status = CatConflictStatusIrrelevant

```

### Property **Type**( ) As [CatConflictType](../SpaceAnalysisInterfaces/enum_CatConflictType_47830.md) (Read Only)

   Returns the type of the conflict.

**Example:**      This example retrieves the type of the `NewConflict` Conflict.

```VBScript
        Dim conflictType As CatConflictType
        conflictType = NewConflict.Type

```

### Property **Value**( ) As double (Read Only)

   Returns the conflict value. This value is the penetration lengh in case of a clash or the minimum distance in case of clearance violation.

**Example:**      This example retrieves the value of the `NewConflict` Conflict.

```VBScript
        Dim conflictValue As double
        conflictValue = NewConflict.Value

```

Methods

### Sub **GetFirstPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point on the first product which realizes the penetration or minimum distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the first product involved in the `NewConflict` Conflict.

```VBScript
        Dim Coordinates (2)
        NewConflict.GetFirstPointCoordinates Coordinates

```

### Sub **GetSecondPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point on the second product which realizes the penetration or minimum distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates in the `NewConflict` Conflict.

```VBScript
        Dim Coordinates (2)
        NewConflict.GetSecondPointCoordinates Coordinates

```

---

# Conflicts (Collection)

**_A collection of all Conflict objects currently detected by a Clash object._**

## Methods

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAConflict](../SpaceAnalysisInterfaces/interface_Conflict_14180.md)

   Returns a Conflict object using its index from the Conflicts collection.

**Parameters:**

` iIndex`      The index of the Conflict object to retrieve from the collection of Conflicts. As a numerics, this index is the rank of the Conflict in the collection. The index of the first Conflict in the collection is 1, and the index of the last Conflict is Count.

**Example:**      This example retrieves in `ThisConflict` the ninth Conflict from the `TheConflicts` collection.

```VBScript
        Dim ThisConflict As Conflict
        Set ThisConflict = TheConflicts.Item(9)

```

---

# Distance (Object)

**_Represents the Distance object._**
The Distance object is a specification of a distance computation between products or groups of products.

## Properties

### Property **Accuracy**( ) As double

   Returns or sets the accuracy value for the computation. The accuracy value must be greater than 0.

**Example:**      The first example retrieves the accuracy value of `NewDistance` Distance.

```VBScript
        Dim AccuracyValue As double
        AccuracyValue = NewDistance.Accuracy

```

   The second example sets the accuracy value of `NewDistance` Distance.

```VBScript
        NewDistance.Accuracy = 10.

```

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

   Returns the AnnotatedViews collection of the distance.

**Example:**      This example retrieves the AnnotatedViews collection of `NewDistance` Distance.

```VBScript
        Dim TheAnnotatedViewsList As AnnotatedViews
        Set TheAnnotatedViewsList = NewDistance.AnnotatedViews

```

### Property **ComputationType**( ) As [CatDistanceComputationType](../SpaceAnalysisInterfaces/enum_CatDistanceComputationType_143950.md)

   Returns or sets the computation type for the computation.

**Example:**      The first example retrieves the computation type of `NewDistance` Distance.

```VBScript
        Dim ComputationType As CatDistanceComputationType
        ComputationType = NewDistance.ComputationType

```

   The second example sets the computation type of `NewDistance` Distance.

```VBScript
        NewDistance.ComputationType = CatDistanceComputationTypeInsideOne

```

### Property **FirstGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the first group used by the computation.

**Example:**      The first example retrieves the first group of `NewDistance` Distance.

```VBScript
        Dim FirstGroup As Group
        Set FirstGroup = NewDistance.FirstGroup

```

   The second example sets the first group of `NewDistance` Distance.

```VBScript
        Dim FirstGroup As Group
        NewDistance.FirstGroup = FirstGroup

```

### Property **FirstProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the product belonging to the first group that realizes the minimum distance.

**Example:**      This example retrieves the first product involved in the `NewDistance` Distance.

```VBScript
        Dim AProduct As Product
        Set AProduct = NewDistance.FirstProduct

```

### Property **IsDefined**( ) As long (Read Only)

   Returns a diagnosis on the distance. The diagnosis can take two values:

  * = 0: the distance is undefined (for example only one product) and the results are invalid.
  * = 1: the distance is defined and all results are valid.

**Example:**      This example retrieves the diagnosis on `NewDistance` Distance.

```VBScript
        If NewDistance.IsDefined = 1 Then

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

   Returns the Marker3Ds collection of the distance.

**Example:**      This example retrieves the Marker3Ds collection of `NewDistance` Distance.

```VBScript
        Dim TheMarker3DsList As Marker3Ds
        Set TheMarker3DsList = NewDistance.Marker3Ds

```

### Property **MaximumDistance**( ) As double

   Returns or sets the maximum distance value for the computation (valid only for band analysis). The maximum distance value must be greater than 0.

**Example:**      The first example retrieves the maximum distance value of `NewDistance` Distance.

```VBScript
        Dim MaximumValue As double
        MaximumValue = NewDistance.MaximumDistance

```

   The second example sets the maximum distance value of `NewDistance` Distance.

```VBScript
        NewDistance.MaximumDistance = 10.

```

### Property **MeasureType**( ) As [CatDistanceMeasureType](../SpaceAnalysisInterfaces/enum_CatDistanceMeasureType_101708.md)

   Returns or sets the type of distance that will be calculated.

**Example:**      The first example retrieves the type of `NewDistance` Distance.

```VBScript
        Dim MeasureType As CatDistanceMeasureType
        MeasureType = NewDistance.MeasureType

```

   The second example sets the Type of `NewDistance` Distance.

```VBScript
        NewDistance.MeasureType = CatDistanceMeasureTypeMinimum

```

### Property **MinimumDistance**( ) As double

   Returns or sets the minimum distance value for the computation (valid only for band analysis). The minimum distance value must be greater than 0.

**Example:**      The first example retrieves the minimum distance value of `NewDistance` Distance.

```VBScript
        Dim MinimumValue As double
        MinimumValue = NewDistance.MinimumDistance

```

   The second example sets the minimum distance value of `NewDistance` Distance.

```VBScript
        NewDistance.MinimumDistance = 10.

```

### Property **SecondGroup**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the second group used by the computation.

**Example:**      The first example retrieves the second group of `NewDistance` Distance.

```VBScript
        Dim SecondGroup As Group
        Set SecondGroup = NewDistance.SecondGroup

```

   The second example sets the second group of `NewDistance` Distance.

```VBScript
        Dim SecondGroup As Group
        NewDistance.SecondGroup = SecondGroup

```

### Property **SecondProduct**( ) As [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md) (Read Only)

   Returns the product belonging to the second group that realizes the minimum distance.

**Example:**      This example retrieves the coordinates in the `NewDistance` Distance.

```VBScript
        Dim AProduct As Product
        Set AProduct = NewDistance.SecondProduct

```

### Property **Value**( ) As double (Read Only)

   Returns the distance value.

**Example:**      This example retrieves the value of `NewDistance` Distance.

```VBScript
        Dim MinimumValue As double
        MinimumValue = NewDistance.Value

```

Methods

### Sub **Compute**( )

   Computes the distance.

**Example:**      This example computes the distance of `NewDistance` Distance.

```VBScript
        NewDistance.Compute

```

### Sub **GetFirstPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point belonging to the first product, which realizes the distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates of the first point in `NewDistance` Distance.

```VBScript
        Dim Coordinates (2)
        NewDistance.GetFirstPointCoordinates Coordinates

```

### Sub **GetSecondPointCoordinates**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the coordinates of the point belonging to the second product, which realizes the distance.

**Parameters:**

` oCoordinates`      The coordinates of the point

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the coordinates of the first point in `NewDistance` Distance.

```VBScript
        Dim Coordinates (2)
        NewDistance.GetSecondPointCoordinates Coordinates

```

---

# Distances (Collection)

**_A collection of all Distance objects currently managed by the application._**

The method `GetTechnologicalObject("Distances")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**( ) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Creates a Distance object which takes all products of the document into account and adds it to the Distances collection.

**Returns:**      The created Distance  **Example:**      This example creates a new Distance in the `TheDistances` collection.

```VBScript
        Dim NewDistance As Distance
        Set NewDistance = TheDistances.Add

```

### Func **AddFromSel**( ) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Creates a Distance object which takes all products in the selection into account and adds it to the Distances collection.

**Returns:**      The created Distance  **Example:**      This example creates a new Distance in the `TheDistances` collection.

```VBScript
        Dim NewDistance As Distance
        Set NewDistance = TheDistances.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIADistance](../SpaceAnalysisInterfaces/interface_Distance_13954.md)

   Returns a Distance object using its index or its name from the Distances collection.

**Parameters:**

` iIndex`      The index or the name of the Distance to retrieve from the collection of Distances. As a numerics, this index is the rank of the Distance in the collection. The index of the first Distance in the collection is 1, and the index of the last Distance is Count. As a string, it is the name you assigned to the Distance.

**Example:**      This example retrieves in `ThisDistance` the ninth Distance, and in `ThatDistance` the Distance named `Distance Of MyProduct` from the `TheDistances` collection.

```VBScript
        Dim ThisDistance As Distance
        Set ThisDistance = TheDistances.Item(9)
        Dim ThatDistance As Distance
        Set ThatDistance = TheDistances.Item("Distance Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Distance object from the Distances collection.

**Parameters:**

` iIndex`      The index or the name of the Distance to remove from the collection of Distances. As a numerics, this index is the rank of the Distance in the collection. The index of the first Distance in the collection is 1, and the index of the last Distance is Count. As a string, it is the name you assigned to the Distance.

**Example:**      The following example removes the tenth Distance and the Distance named `Distance Of MyProduct` from the `TheDistances` collection.

```VBScript
        TheDistances.Remove(10)
        TheDistances.Remove("Distance Of MyProduct")

```

---

# Inertia (Object)

**_Represents the Inertia object._**
The Inertia object can be associated with any relevant object of a document in order to get or compute its inertia data.

This version allows you to compute the following data:

  * mass
  * density
  * position of the center of gravity
  * inertia matrix
  * principal axes
  * principal moments
of a product.

The units are:

  * Kilogram (Kg) for Mass
  * Square meter (M^2) for Wet Area
  * Cubic meter (M^3) for Volume
  * Meter (M) for Position
  * Square Kilogram meter ((KgM)^2) for Inertia Matrix and Principal Moments
  * Kilogram per cubic meter (Kg/M^3) for Density

The method `GetTechnologicalObject("Inertia")` on the product to analyze, allows you to retrieve this object.

## Properties

### Property **Density**( ) As double

   Returns or sets the density for the computation. The density value is set to:

  * 0: the computation must use densities attached to each object.
  * any positive value: the computation has to use this value.
The density value is returned as:

  * 1: a default value is used (there is no density attached to objects).
  * -1: the density is not homogeneous for each object.
  * other positive values: the density attached to all objects.

**Example:**      The first example gets the density of `NewInertia` inertia.

```VBScript
        Dim ADensity As double
        ADensity = NewInertia.Density

```

   The second example sets the density of `NewInertia` inertia.

```VBScript
        NewInertia.Density = 10.

```

### Property **Mass**( ) As double (Read Only)

   Returns the mass.

**Example:**      This example retrieves the mass of `NewInertia` inertia.

```VBScript
        Dim AMass As double
        AMass = NewInertia.Mass

```

Methods

### Sub **GetCOGPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oCoordinates`)

   Retrieves the position of the center of gravity.

**Parameters:**

` oCoordinates`      The position of the center of gravity with respect to the product coordinate system:

  * oCoordinates(0) is the X coordinate
  * oCoordinates(1) is the Y coordinate
  * oCoordinates(2) is the Z coordinate

**Example:**      This example retrieves the position of the center of gravity of `NewInertia` inertia.

```VBScript
        Dim Coordinates (2)
        NewInertia.GetCOGPosition Coordinates

```

### Sub **GetInertiaMatrix**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oMatrix`)

   Retrieves the matrix of inertia.

**Parameters:**

` oMatrix`      The matrix of inertia array:

  * oMatrix(0) is the Ixx component
  * oMatrix(1) is the Ixy component
  * oMatrix(2) is the Ixz component
  * oMatrix(3) is the Iyx component
  * oMatrix(4) is the Iyy component
  * oMatrix(5) is the Iyz component
  * oMatrix(6) is the Izx component
  * oMatrix(7) is the Izy component
  * oMatrix(8) is the Izz component

**Example:**      This example retrieves the matrix of inertia of `NewInertia` inertia.

```VBScript
        Dim Matrix (8)
        NewInertia.GetInertiaMatrix Matrix

```

### Sub **GetPrincipalAxes**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oComponents`)

   Retrieves the the principal axes of inertia.

**Parameters:**

` oComponents`      The principal axes of inertia array (A1, A2 and A3 are the principal axes of inertia):

  * oComponents(0) is the A1x component
  * oComponents(1) is the A2x component
  * oComponents(2) is the A3x component
  * oComponents(3) is the A1y component
  * oComponents(4) is the A2y component
  * oComponents(5) is the A3y component
  * oComponents(6) is the A1z component
  * oComponents(7) is the A2z component
  * oComponents(8) is the A3z component

**Example:**      This example retrieves the principal axes of inertia of `NewInertia` inertia.

```VBScript
        Dim Components (8)
        NewInertia.GetPrincipalAxes Components

```

### Sub **GetPrincipalMoments**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oValues`)

   Retrieves the principal moments of inertia.

**Parameters:**

` oValues`      The principal moments of inertia array:

  * oValues(0) is the M1 value with respect to the first principal exes of inertia
  * oValues(1) is the M2 value with respect to the second principal exes of inertia
  * oValues(2) is the M3 value with respect to the third principal exes of inertia

**Example:**      This example retrieves principal moments of inertia of `NewInertia` inertia.

```VBScript
        Dim Values (2)
        NewInertia.GetPrincipalMoments Values

```

---

# Inertias (Collection)

**_A collection of all inertia objects currently managed by the application._**

WARNING: this collection will be DEPRECATED in the next release. It is recommended to use the method `GetTechnologicalObject("Inertia")` on the product to analyze, to retrieve an `Inertia` object.

## Methods

### Func **Add**( [CATIABase](../System/interface_AnyObject_17321.md)  `iObject`) As [CATIAInertia](../SpaceAnalysisInterfaces/interface_Inertia_10894.md)

   Creates an Inertia object from an object and adds it to the Inertias collection.

**Parameters:**

` iObject`      The Object

**Returns:**      The created Inertia  **Example:**      This example creates a new Inertia from a product `TheProduct` in the `TheInertias` collection.

```VBScript
        Dim NewInertia As Inertia
        Set NewInertia = TheInertias.Add(TheProduct)

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAInertia](../SpaceAnalysisInterfaces/interface_Inertia_10894.md)

   Returns an Inertia object using its index or its name from the Inertias collection.

**Parameters:**

` iIndex`      The index or the name of the Inertia to retrieve from the collection of inertias. As a numerics, this index is the rank of the Inertia in the collection. The index of the first Inertia in the collection is 1, and the index of the last Inertia is Count. As a string, it is the name you assigned to the Inertia.

**Example:**      This example retrieves in `ThisInertia` the ninth Inertia, and in `ThatInertia` the Inertia named `Inertia Of MyProduct` from the `TheInertias` collection.

```VBScript
        Dim ThisInertia As Inertia
        Set ThisInertia = TheInertias.Item(9)
        Dim ThatInertia As Inertia
        Set ThatInertia = TheInertias.Item("Inertia Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes an Inertia object from the Inertias collection.

**Parameters:**

` iIndex`      The index or the name of the Inertia to remove from the collection of inertias. As a numerics, this index is the rank of the Inertia in the collection. The index of the first Inertia in the collection is 1, and the index of the last Inertia is Count. As a string, it is the name you assigned to the Inertia.

**Example:**      The following example removes the tenth Inertia and the Inertia named `Inertia Of MyProduct` from the `TheInertias` collection.

```VBScript
        TheInertias.Remove(10)
        TheInertias.Remove("Inertia Of MyProduct")

```

---

# MeasureSettingAtt (Object)

**_The interface to access a CATIAMeasureSettingAtt._**

## Properties

### Property **BoxDisplay**( ) As boolean

   Returns or sets the BoxDisplay parameter .  Measure label background is filled if BoxDisplay is True ; there are only borders if BoxDisplay is False.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **LineWidth**( ) As short

   Returns or sets the LineWidth parameter.  The line width index, which ranges from 1 to 63.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PartUpdateStatus**( ) As boolean

   Returns or sets the PartUpdateStatus parameter .  Part is automatically updated if PartUpdateStatus is true.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ProductUpdateStatus**( ) As boolean

   Returns or sets the ProductUpdateStatus parameter .  Product is automatically updated if PartUpdateStatus is true.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **TildeDisplay**( ) As boolean

   Returns or sets the TildeDisplay parameter.  If TildeDisplay is TRUE, a tilde displayed for approximate measurement.  Ensure consistency with the C++ interface to which the work is delegated.  Methods

### Func **GetBoxDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the BoxDisplay parameter.

**Role** :Retrieves the state of the BoxDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetLabelColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the LabelColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Func **GetLabelColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LabelColor parameter.

**Role** :Retrieves the state of the LabelColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetLineWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the LineWidth parameter.

**Role** :Retrieves the state of the LineWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPartUpdateStatusInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PartUpdateStatus parameter.

**Role** :Retrieves the state of the PartUpdateStatus parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetProductUpdateStatusInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ProductUpdateStatus parameter.

**Role** :Retrieves the state of the ProductUpdateStatus parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetTextColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the TextColor parameter .  Ensure consistency with the C++ interface to which the work is delegated.  
### Func **GetTextColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TextColor parameter.

**Role** :Retrieves the state of the TextColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetTildeDisplayInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the TildeDisplay parameter.

**Role** :Retrieves the state of the TildeDisplay parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetBoxDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the BoxDisplay parameter.

**Role** :Locks or unlocks the BoxDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLabelColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the LabelColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Sub **SetLabelColorLock**( boolean  `iLocked`)

   Locks or unlocks the LabelColor parameter.

**Role** :Locks or unlocks the LabelColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetLineWidthLock**( boolean  `iLocked`)

   Locks or unlocks the LineWidth parameter.

**Role** :Locks or unlocks the LineWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPartUpdateStatusLock**( boolean  `iLocked`)

   Locks or unlocks the PartUpdateStatus parameter.

**Role** :Locks or unlocks the PartUpdateStatus parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetProductUpdateStatusLock**( boolean  `iLocked`)

   Locks or unlocks the ProductUpdateStatus parameter.

**Role** :Locks or unlocks the Xxx parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTextColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the TextColor parameter .  Ensure consistency with the C++ interface to which the work is delegated.  
### Sub **SetTextColorLock**( boolean  `iLocked`)

   Locks or unlocks the TextColor parameter.

**Role** :Locks or unlocks the TextColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetTildeDisplayLock**( boolean  `iLocked`)

   Locks or unlocks the TildeDisplay parameter.

**Role** :Locks or unlocks the TildeDisplay parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# Section (Object)

**_Represents the Section object._**
The Section object is a specification of a sectioning display and computationwith a section plane, section slice or section box.

## Properties

### Property **AnnotatedViews**( ) As [CATIAAnnotatedViews](../NavigatorInterfaces/interface_AnnotatedViews_42578.md) (Read Only)

   Returns the AnnotatedViews collection of the section.

**Example:**      This example retrieves the AnnotatedViews collection of `NewSection` Section.

```VBScript
        Dim TheAnnotatedViewsList As AnnotatedViews
        Set TheAnnotatedViewsList = NewSection.AnnotatedViews

```

### Property **Behavior**( ) As [CatSectionBehavior](../SpaceAnalysisInterfaces/enum_CatSectionBehavior_68434.md)

   Returns or sets the general behavior of the section: Freeze, Automatic update, manual update The behavior value are defined in [CatSectionBehavior](../SpaceAnalysisInterfaces/enum_CatSectionBehavior_68434.md).

**Example:**      The first example retrieves the behavior of `NewSection` Section.

```VBScript
        Dim SectionBehavior As CatSectionBehavior
        Behavior = NewSection.Behavior

```

   The second example sets the behavior of `NewSection` Section.

```VBScript
        NewSection.Behavior = catSectionBehaviorAutomatic

```

### Property **CutMode**( ) As long

   Returns or sets the cutting mode of the section. The cutting mode value is 1 for clipping or 0 without clipping.

**Example:**      The first example retrieves the cutting mode of `NewSection` Section.

```VBScript
        Dim SectionMode As Integer
        SectionMode = NewSection.CutMode

```

   The second example sets the cutting mode of `NewSection` Section.

```VBScript
        NewSection.CutMode = 1

```

### Property **Group**( ) As [CATIAGroup](../NavigatorInterfaces/interface_Group_5945.md)

   Returns or sets the sectionned group. By default, it is the all leaves group.

**Example:**      The first example retrieves the group of `NewSection` Section.

```VBScript
        Dim AGroup As Group
        AGroup = NewSection.Group

```

   The second example sets the group of `NewSection` Section.

```VBScript
        Dim AGroup As Group
        NewSection.Group = AGroup

```

### Property **Height**( ) As double

   Returns or sets the height of the section. The height value must be greater than 0.

**Example:**      The first example retrieves the height of `NewSection` Section.

```VBScript
        Dim SectionHeight As double
        SectionHeight = NewSection.Height

```

   The second example sets the height value of `NewSection` Section.

```VBScript
        NewSection.Height = 100.

```

### Property **Marker3Ds**( ) As [CATIAMarker3Ds](../NavigatorInterfaces/interface_Marker3Ds_15928.md) (Read Only)

   Returns the Marker3Ds collection of the section.

**Example:**      This example retrieves the Marker3Ds collection of `NewSection` Section.

```VBScript
        Dim TheMarker3DsList As Marker3Ds
        Set TheMarker3DsList = NewSection.Marker3Ds

```

### Property **Thickness**( ) As double

   Returns or sets the thickness of the section. The thickness value must be greater than 0.

**Example:**      The first example retrieves the thickness of `NewSection` Section.

```VBScript
        Dim SectionThickness As double
        SectionThickness = NewSection.Thickness

```

   The second example sets the thickness value of `NewSection` Section.

```VBScript
        NewSection.Thickness = 100.

```

### Property **Type**( ) As [CatSectionType](../SpaceAnalysisInterfaces/enum_CatSectionType_41996.md)

   Returns or sets the type of the section. The type value are defined in [CatSectionType](../SpaceAnalysisInterfaces/enum_CatSectionType_41996.md).

**Example:**      The first example retrieves the type of `NewSection` Section.

```VBScript
        Dim SectionType As CatSectionType
        SectionType = NewSection.Type

```

   The second example sets the type of `NewSection` Section.

```VBScript
        NewSection.Type = catSectionTypeSlice

```

### Property **Width**( ) As double

   Returns or sets the width of the section. The width value must be greater than 0.

**Example:**      The first example retrieves the width of `NewSection` Section.

```VBScript
        Dim SectionWidth As double
        SectionWidth = NewSection.Width

```

   The second example sets the width value of `NewSection` Section.

```VBScript
        NewSection.Width = 100.

```

Methods

### Func **Export**( ) As [CATIADocument](../InfInterfaces/interface_Document_14456.md)

   Exports the sections curves of the section in a document.

**Returns:**      The document  **Example:**      This example exports the section curves of `NewSection` Section in `PartDoc` document.

```VBScript
        Dim PartDoc As Document
        PartDoc = NewSection.Export

```

### Sub **GetPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `oComponents`)

   Retrieves the position of the section. The position of the section is made of a coordinate system whose origin is the center of the section, and X and Y axes lie on the section. It is retrieved in an array of the X, Y, Z axes components and the origin components with respect to the absolute coordinate system.

**Parameters:**

` oComponents`      The position of the section

  * oComponents( 0) is the X component of the X-axis
  * oComponents( 1) is the Y component of the X-axis
  * oComponents( 2) is the Z component of the X-axis
  * oComponents( 3) is the X component of the Y-axis
  * oComponents( 4) is the Y component of the Y-axis
  * oComponents( 5) is the Z component of the Y-axis
  * oComponents( 6) is the X component of the Z-axis
  * oComponents( 7) is the Y component of the Z-axis
  * oComponents( 8) is the Z component of the Z-axis
  * oComponents( 9) is the X component of the origin
  * oComponents(10) is the Y component of the origin
  * oComponents(11) is the Z component of the origin

**Example:**      This example retrieves the position of `NewSection` Section.

```VBScript
        Dim Components (11)
        NewSection.GetPosition Components

```

### Func **IsEmpty**( ) As long

   Indicates whether the section is empty. The indicator value is 0 if the section is empty or 1 if the section comprise at least one segment.

**Example:**      This example retrieves the information on `NewSection` Section.

```VBScript
        Dim Indicator
        Indicator = NewSection.IsEmpty

```

### Sub **SetPosition**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iComponents`)

   Sets the position of the section.

**Parameters:**

` oComponents`      The position of the section with respect to the absolute coordinate system

  * iComponents( 0) is the X component of the X-axis
  * iComponents( 1) is the Y component of the X-axis
  * iComponents( 2) is the Z component of the X-axis
  * iComponents( 3) is the X component of the Y-axis
  * iComponents( 4) is the Y component of the Y-axis
  * iComponents( 5) is the Z component of the Y-axis
  * iComponents( 6) is the X component of the Z-axis
  * iComponents( 7) is the Y component of the Z-axis
  * iComponents( 8) is the Z component of the Z-axis
  * iComponents( 9) is the X component of the origin
  * iComponents(10) is the Y component of the origin
  * iComponents(11) is the Z component of the origin

**Example:**      This example sets the position of `NewSection` Section.

```VBScript
        Dim MatrixPos (11) As Double
        MatrixPos( 0) = 1.0
        MatrixPos( 1) = 0.0
        MatrixPos( 2) = 0.0
        MatrixPos( 3) = 0.0
        MatrixPos( 4) = 1.0
        MatrixPos( 5) = 0.0
        MatrixPos( 6) = 0.0
        MatrixPos( 7) = 0.0
        MatrixPos( 8) = 1.0
        MatrixPos( 9) = 1000.0
        MatrixPos(10) = 0.0
        MatrixPos(11) = 0.0
        NewSection.SetPosition MatrixPos

```

---

# SectioningSettingAtt (Object)

**_The interface to access a CATIASectioningSettingAtt._**

## Properties

### Property **ClippingMode**( ) As [CatSectionClippingMode](../SpaceAnalysisInterfaces/enum_CatSectionClippingMode_100444.md)

   Returns or sets the ClippingMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **DisplayCutInWireframe**( ) As boolean

   Returns or sets the DisplayCutInWireframe parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridAutoFiltering**( ) As boolean

   Returns or sets the GridAutoFiltering parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridAutoResize**( ) As boolean

   Returns or sets the GridAutoResize parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridHeightStep**( ) As float

   Returns or sets the GridHeightStep parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridPositionMode**( ) As [CatGridPositionMode](../SpaceAnalysisInterfaces/enum_CatGridPositionMode_75400.md)

   Returns or sets the GridPositionMode parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridStyle**( ) As [CatSectionGridStyle](../SpaceAnalysisInterfaces/enum_CatSectionGridStyle_76008.md)

   Returns or sets the GridStyle parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **GridWidthStep**( ) As float

   Returns or sets the GridWidthStep parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **HidePlane**( ) As boolean

   Returns or sets the HidePlane parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **HideResult**( ) As boolean

   Returns or sets the HideResult parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlaneNormal**( ) As [CatSectionPlaneNormal](../SpaceAnalysisInterfaces/enum_CatSectionPlaneNormal_91976.md)

   Returns or sets the PlaneNormal parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **PlaneOrigin**( ) As [CatSectionPlaneOrigin](../SpaceAnalysisInterfaces/enum_CatSectionPlaneOrigin_91941.md)

   Returns or sets the PlaneOrigin parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **SectionFill**( ) As boolean

   Returns or sets the SectionFill parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **UpdateResult**( ) As boolean

   Returns or sets the UpdateResult parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerAutoOpen**( ) As boolean

   Returns or sets the ViewerAutoOpen parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerAutoReframe**( ) As boolean

   Returns or sets the ViewerAutoReframe parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **ViewerLock2D**( ) As boolean

   Returns or sets the ViewerLock2D parameter.  Ensure consistency with the C++ interface to which the work is delegated.  
### Property **WindowDefaultHeight**( ) As long

**Role** :Retrieve section window default height if the window open mode is catSecWindow_DefaultSize

**Parameters:**

` oWindowDefaultHeight`

**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  
### Property **WindowDefaultWidth**( ) As long

**Role** :Retrieve section window default width if the window open mode is catSecWindow_DefaultSize

**Parameters:**

` oWindowDefaultWidth`

**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  
### Property **WindowOpenMode**( ) As [CatSecWindowOpenMode](../SpaceAnalysisInterfaces/enum_CatSecWindowOpenMode_82170.md)

**Role** :Retrieve section window open mode

**Parameters:**

` oWindowOpenMode`      **Legal values** :
`catSecWindow_DefaultSize :`Opens the sectioning window(s) with the default size specified in the Tools->Options.
`catSecWindow_TileVertically :`Tiles the sectioning window(s) vertically in the viewer

**Returns:**      S_OK Successfully retieved the window open mode E_FAIL Failed to retrieved the window open mode  Methods

### Func **GetClippingModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ClippingMode parameter.

**Role** :Retrieves the state of the ClippingMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetDisplayCutInWireframeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the DisplayCutInWireframe parameter.

**Role** :Retrieves the state of the DisplayCutInWireframe parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridAutoFilteringInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridAutoFiltering parameter.

**Role** :Retrieves the state of the GridAutoFiltering parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridAutoResizeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridAutoResize parameter.

**Role** :Retrieves the state of the GridAutoResize parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridHeightStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridHeightStep parameter.

**Role** :Retrieves the state of the GridHeightStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridPositionModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridPositionMode parameter.

**Role** :Retrieves the state of the GridPositionMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridStyleInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridStyle parameter.

**Role** :Retrieves the state of the GridStyle parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetGridWidthStepInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the GridWidthStep parameter.

**Role** :Retrieves the state of the GridWidthStep parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHidePlaneInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the HidePlane parameter.

**Role** :Retrieves the state of the HidePlane parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetHideResultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the HideResult parameter.

**Role** :Retrieves the state of the HideResult parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **GetPlaneColor**( long  `oR`,  long  `oG`,  long  `oB`)

   Returns the PlaneColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Func **GetPlaneColorInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlaneColor parameter.

**Role** :Retrieves the state of the PlaneColor parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlaneNormalInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlaneNormal parameter.

**Role** :Retrieves the state of the PlaneNormal parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetPlaneOriginInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the PlaneOrigin parameter.

**Role** :Retrieves the state of the PlaneOrigin parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetSectionFillInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the SectionFill parameter.

**Role** :Retrieves the state of the SectionFill parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetUpdateResultInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the UpdateResult parameter.

**Role** :Retrieves the state of the UpdateResult parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerAutoOpenInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ViewerAutoOpen parameter.

**Role** :Retrieves the state of the ViewerAutoOpen parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerAutoReframeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ViewerAutoReframe parameter.

**Role** :Retrieves the state of the ViewerAutoReframe parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetViewerLock2DInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the ViewerLock2D parameter.

**Role** :Retrieves the state of the ViewerLock2D parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowDefaultHeightInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the WindowDefaultHeight parameter.

**Role** :Retrieves the state of the WindowDefaultHeight parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowDefaultWidthInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the WindowDefaultWidth parameter.

**Role** :Retrieves the state of the WindowDefaultWidth parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Func **GetWindowOpenModeInfo**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioAdminLevel`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `ioLocked`) As boolean

   Retrieves environment informations for the WindowOpenMode parameter.

**Role** :Retrieves the state of the WindowOpenMode parameter in the current environment.

**Parameters:**

` ioAdminLevel`
If the parameter is locked, AdminLevel gives the administration level that imposes the value of the parameter.
If the parameter is not locked, AdminLevel gives the administration level that will give the value of the parameter after a reset.
` ioLocked`      Indicates if the parameter has been locked.

**Returns:**      Indicates if the parameter has been explicitly modified or remain to the administrated value.  
### Sub **SetClippingModeLock**( boolean  `iLocked`)

   Locks or unlocks the ClippingMode parameter.

**Role** :Locks or unlocks the PlaneOrigin parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetDisplayCutInWireframeLock**( boolean  `iLocked`)

   Locks or unlocks the DisplayCutInWireframe parameter.

**Role** :Locks or unlocks the DisplayCutInWireframe parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridAutoFilteringLock**( boolean  `iLocked`)

   Locks or unlocks the GridAutoFiltering parameter.

**Role** :Locks or unlocks the GridAutoFiltering parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridAutoResizeLock**( boolean  `iLocked`)

   Locks or unlocks the GridAutoResize parameter.

**Role** :Locks or unlocks the GridAutoResize parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridHeightStepLock**( boolean  `iLocked`)

   Locks or unlocks the GridHeightStep parameter.

**Role** :Locks or unlocks the GridHeightStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridPositionModeLock**( boolean  `iLocked`)

   Locks or unlocks the GridPositionMode parameter.

**Role** :Locks or unlocks the GridPositionMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridStyleLock**( boolean  `iLocked`)

   Locks or unlocks the GridStyle parameter.

**Role** :Locks or unlocks the GridStyle parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetGridWidthStepLock**( boolean  `iLocked`)

   Locks or unlocks the GridWidthStep parameter.

**Role** :Locks or unlocks the GridWidthStep parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHidePlaneLock**( boolean  `iLocked`)

   Locks or unlocks the HidePlane parameter.

**Role** :Locks or unlocks the HidePlane parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetHideResultLock**( boolean  `iLocked`)

   Locks or unlocks the HideResult parameter.

**Role** :Locks or unlocks the HideResult parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneColor**( long  `iR`,  long  `iG`,  long  `iB`)

   Sets the PlaneColor parameter.

**Parameters:**

` oR`      the red component of the color.
` oG`      the green component of the color.
` oB`      the blue component of the color.  Ensure consistency with the C++ interface to which the work is delegated.

### Sub **SetPlaneColorLock**( boolean  `iLocked`)

   Locks or unlocks the PlaneColor parameter.

**Role** :Locks or unlocks the PlaneColor parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneNormalLock**( boolean  `iLocked`)

   Locks or unlocks the PlaneNormal parameter.

**Role** :Locks or unlocks the PlaneNormal parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetPlaneOriginLock**( boolean  `iLocked`)

   Locks or unlocks the PlaneOrigin parameter.

**Role** :Locks or unlocks the PlaneOrigin parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetSectionFillLock**( boolean  `iLocked`)

   Locks or unlocks the SectionFill parameter.

**Role** :Locks or unlocks the SectionFill parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetUpdateResultLock**( boolean  `iLocked`)

   Locks or unlocks the UpdateResult parameter.

**Role** :Locks or unlocks the UpdateResult parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerAutoOpenLock**( boolean  `iLocked`)

   Locks or unlocks the ViewerAutoOpen parameter.

**Role** :Locks or unlocks the ViewerAutoOpen parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerAutoReframeLock**( boolean  `iLocked`)

   Locks or unlocks the ViewerAutoReframe parameter.

**Role** :Locks or unlocks the ViewerAutoReframe parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetViewerLock2DLock**( boolean  `iLocked`)

   Locks or unlocks the ViewerLock2D parameter.

**Role** :Locks or unlocks the ViewerLock2D parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowDefaultHeightLock**( boolean  `iLocked`)

   Locks or unlocks the WindowDefaultHeight parameter.

**Role** :Locks or unlocks the WindowDefaultHeight parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowDefaultWidthLock**( boolean  `iLocked`)

   Locks or unlocks the WindowDefaultWidth parameter.

**Role** :Locks or unlocks the WindowDefaultWidth parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

### Sub **SetWindowOpenModeLock**( boolean  `iLocked`)

   Locks or unlocks the WindowOpenMode parameter.

**Role** :Locks or unlocks the WindowOpenMode parameter if it is possible in the current administrative context. In user mode this method will always return E_FAIL.

**Parameters:**

` iLocked`      the locking operation to be performed **Legal values** :
`TRUE :` to lock the parameter.
`FALSE:` to unlock the parameter.

---

# Sections (Collection)

**_A collection of all Section objects currently managed by the application._**

The method `GetTechnologicalObject("Sections")` on the root product, allows you to retrieve this collection.

## Methods

### Func **Add**( ) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

   Creates a Section object which takes all products of the documents into account and adds it to the Sections collection.

**Returns:**      The created Section  **Example:**      This example creates a new Section in the `TheSections` collection.

```VBScript
        Dim NewSection As Section
        Set NewSection = TheSections.Add

```

### Func **AddFromSel**( ) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

   Creates a Section object which takes all products in the selection into account and adds it to the Sections collection.

**Returns:**      The created Section  **Example:**      This example creates a new Section in the `TheSections` collection.

```VBScript
        Dim NewSection As Section
        Set NewSection = TheSections.AddFromSel

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIASection](../SpaceAnalysisInterfaces/interface_Section_11089.md)

   Returns a Section object using its index or its name from the Sections collection.

**Parameters:**

` iIndex`      The index or the name of the Section to retrieve from the collection of Sections. As a numerics, this index is the rank of the Section in the collection. The index of the first Section in the collection is 1, and the index of the last Section is Count. As a string, it is the name you assigned to the Section.

**Example:**      This example retrieves in `ThisSection` the ninth Section, and in `ThatSection` the Section named `Section Of MyProduct` from the `TheSections` collection.

```VBScript
        Dim ThisSection As Section
        Set ThisSection = TheSections.Item(9)
        Dim ThatSection As Section
        Set ThatSection = TheSections.Item("Section Of MyProduct")

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a Section object from the Sections collection.

**Parameters:**

` iIndex`      The index or the name of the Section to remove from the collection of Sections. As a numerics, this index is the rank of the Section in the collection. The index of the first Section in the collection is 1, and the index of the last Section is Count. As a string, it is the name you assigned to the Section.

**Example:**      The following example removes the tenth Section and the Section named `Section Of MyProduct` from the `TheSections` collection.

```VBScript
        TheSections.Remove(10)
        TheSections.Remove("Section Of MyProduct")

```

---

# SPAWorkbench (Object)

**_The object to manage all Space Analysis objects._**

This version allows you to manage inertia data, clashes, distances and sections.

## Properties

### Property **Clashes**( ) As [CATIAClashes](../SpaceAnalysisInterfaces/interface_Clashes_10879.md) (Read Only)

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