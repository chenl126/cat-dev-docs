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