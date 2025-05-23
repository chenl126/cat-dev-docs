# BasicComponent (Object)

**_Interface designed to manage**Analysis Basic Components**._**

A **Basic Component** is the low level of physical descriptive data. It is a "brick" dedicated to build the **Analysis Entity** or an **Analysis Set** .

A **Basic Components** can contain several **Blocks**. A **Block** is identified by a label. It contains entity data of the same type, organized in superimposed tables.

To create **Analysis Entities** with a complex structure, we have also created a particular **Basic Component** dedicated to encapsulate other **Basic Components**.

## Properties

### Property **BasicComponents**(| ) As [CATIABasicComponents](../CATAnalysisInterfaces/interface_BasicComponents_48940.md) (Read Only)

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