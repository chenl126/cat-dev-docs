# AnalysisLocalEntity (Object)

**_Represent the analysis local entity object._**
This class provides services to describe a analysis entity. It represents some local preprocessing activities.

## Properties

### Property **AnalysisImages**(| ) As [CATIAAnalysisImages](../CATAnalysisInterfaces/interface_AnalysisImages_41938.md) (Read Only)

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