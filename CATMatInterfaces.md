# CATMatInterfaces Framework

## Object Index

  * [AnalysisMaterial](CATMatInterfaces/interface_AnalysisMaterial_54904.md)
  * [Material](CATMatInterfaces/interface_Material_14052.md)
  * [MaterialDocument](CATMatInterfaces/interface_MaterialDocument_54972.md)
  * [MaterialFamilies](CATMatInterfaces/interface_MaterialFamilies_54108.md)
  * [MaterialFamily](CATMatInterfaces/interface_MaterialFamily_41796.md)
  * [MaterialManager](CATMatInterfaces/interface_MaterialManager_47242.md)
  * [Materials](CATMatInterfaces/interface_Materials_17972.md)
  * [PositionedMaterial](CATMatInterfaces/interface_PositionedMaterial_69160.md)

---

# AnalysisMaterial (Object)

**_Represents an AnalysisMaterial object._**
This object is used to manage the Analysis properties of a material.

## Methods

### Func **GetType**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the analysis type (Ex: MATERIAL_ORTHOTROPIC, MATERIAL_ISOTROPIC).  
### Func **GetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Returns an analysis value of the material. The name of the parameter is needed  
### Sub **PutValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets an analysis value of the material. The name of the parameter is needed

---

# Material (Object)

**_Represents a Material object._**

## Properties

### Property **AnalysisMaterial**( ) As [CATIAAnalysisMaterial](../CATMatInterfaces/interface_AnalysisMaterial_54904.md) (Read Only)

   Returns the analysis material object from the current material.  
### Property **RenderingMaterial**( ) As [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md) (Read Only)

   Returns the rendering material object from the current material.  Methods

### Sub **CopyRenderingDataFrom**( [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md)  `iRenderingMaterial`)

   Copy rendering data from a material to the current material.  
### Func **CreateAnalysisData**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATIAAnalysisMaterial](../CATMatInterfaces/interface_AnalysisMaterial_54904.md)

   Create a default analysis material on the current material.  
### Func **CreateRenderingData**( ) As [CATIARenderingMaterial](../CATRmaInterfaces/interface_RenderingMaterial_61289.md)

   Create a default rendering material on the current material.  
### Func **ExistAnalysisData**( ) As short

   Returns true if a analysis material exists on the current material.  
### Func **ExistRenderingData**( ) As short

   Returns true if a rendering material exists on the current material.  
### Sub **GetIcon**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

   Write the icon of a material to disc. The parameter is the path of the folder where the JPEG is going to be written Ex : E:\folder\  
### Sub **PutIcon**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iPath`)

   Read the icon of a material from JPEG file. The parameter is the path of the folder where the JPEG is going to be read Ex : E:\folder\

---

# MaterialDocument (Object)

**_Represents the Document object for materials._**
When a MaterialDocument object is created, a MaterialFamily object is created. A Material object is also created inside this MaterialFamily object.

## Properties

### Property **Families**( ) As [CATIAMaterialFamilies](../CATMatInterfaces/interface_MaterialFamilies_54108.md) (Read Only)

   Returns the Family collection object from the current material document.

---

# MaterialFamilies (Collection)

**_A collection of all the MaterialFamily objects._**
This collection is currently managed by a CATIAMaterialDocument object.

## Methods

### Func **Add**( ) As [CATIAMaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md)

   Adds a new material family to the MaterialFamilies collection.  **Example:**      The following adds a material family to the collection attached to a document. This document must be a [MaterialDocument](../CATMatInterfaces/interface_MaterialDocument_54972.md) object.

```VBScript
     FileToOpen = "e:\users\ast\materials\Catalog.CATMaterial"
     Dim MyDocument As MaterialDocument
     Set MyDocument = Documents.Open(FileToOpen)
     Dim MyMaterialFamily As MaterialFamily
     Set MyMaterialFamily = MyDocument.MaterialFamilies.Add

```

### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md)

   Returns a material family from its index in the MaterialFamilies collection.

**Parameters:**

` iIndex`      The index of the material family to retrieve in the collection of material families. Compared with other collections, you cannot use the name of the material family as argument.

**Returns:**      The retrieved material family  **Example:**      The following example returns in `MyMaterialFamily` the sixth material family in the collection.

```VBScript
     Dim MyMaterialFamily As MaterialFamily
     Set MyMaterialFamily = MaterialFamilies.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a material family from the MaterialFamilies collection.

**Parameters:**

` iIndex`      The index of the material family to remove. Compared with other collections, you cannot use the name of the material family as argument.  **Example:**      The following example removes the second material family in the collection attached to the active document. This document must be a
[MaterialDocument](../CATMatInterfaces/interface_MaterialDocument_54972.md) object.

```VBScript
     FileToOpen = "e:\users\ast\materials\Catalog.CATMaterial"
     Dim MyDocument As MaterialDocument
     Set MyDocument = Documents.Open(FileToOpen)
     MyDocument.MaterialFamilies.Remove(2)

```

---

# MaterialFamily (Object)

**_Represents a Material Family object._**
This object is used to group Materials objects in a material document.

## Properties

### Property **Materials**( ) As [CATIAMaterials](../CATMatInterfaces/interface_Materials_17972.md) (Read Only)

   Returns the material collection object from the current material family.

---

# MaterialManager (Object)

**_Interface to manage material manager object._**

**Role** : A material manager is used to manage materials application on geometrical objects.

## Methods

### Sub **ApplyMaterialOnBody**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial`,  short  `iLinkMode`)

   Apply a Material on a Body. If Material is NULL, deletes the material already applied on the Body  
### Sub **ApplyMaterialOnHybridBody**( [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)  `iHybridBody`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial`,  short  `iLinkMode`)

   Apply a Material on a Hybrid Body. If Material is NULL, deletes the material already applied on the Hybrid Body  
### Sub **ApplyMaterialOnPart**( [CATIAPart](../MecModInterfaces/interface_Part_3788.md)  `iPart`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial`,  short  `iLinkMode`)

   Apply a Material on a Part. If Material is NULL, deletes the material already applied on the Part  
### Sub **ApplyMaterialOnProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial`,  short  `iLinkMode`)

   Apply a Material on a Product. If Material is NULL, deletes the material already applied on the Product  
### Sub **ApplyMaterialOnUserMaterial**( [CATIABase](../System/interface_AnyObject_17321.md)  `iUserMaterial`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial`,  short  `iLinkMode`)

   Apply a Material on a User Material (Analysis entity). Warning: iUserMaterial should be a CATIAAnalysisEntity object. If Material is NULL, deletes the material already applied on the User Material  
### Sub **GetMaterialOnBody**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBody`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `oMaterial`)

   Get a Material on a Body. Material returned is NULL if no material is applied on the Body  
### Sub **GetMaterialOnHybridBody**( [CATIAHybridBody](../MecModInterfaces/interface_HybridBody_21378.md)  `iHybridBody`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `oMaterial`)

   Get a Material on a Hybrid Body. Material returned is NULL if no material is applied on the Hybrid Body  
### Sub **GetMaterialOnPart**( [CATIAPart](../MecModInterfaces/interface_Part_3788.md)  `iPart`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `oMaterial`)

   Get a Material on a Part. Material returned is NULL if no material is applied on the Part  
### Sub **GetMaterialOnProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `oMaterial`)

   Get a Material on a Product. Material returned is NULL if no material is applied on the Product  
### Sub **GetMaterialOnUserMaterial**( [CATIABase](../System/interface_AnyObject_17321.md)  `iUserMaterial`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `oMaterial`)

   Get a Material on a User Material (Analysis entity). Warning: iUserMaterial should be a CATIAAnalysisEntity object. Material returned is NULL if no material is applied on the User Material  
### Sub **ReplaceMaterialLinks**( [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial1`,  [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)  `iMaterial2`)

   In current session, replace all links towards a material 1 with a link towards an other material 2. N.B. Both materials entered should be in a material library.

---

# Materials (Collection)

**_A collection of all the Material objects._**
This collection is currently managed by a [MaterialFamily](../CATMatInterfaces/interface_MaterialFamily_41796.md) object.

## Methods

### Func **Add**( ) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

   Adds a new material to the material collection.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

   Returns a material from its index in the Material collection.

**Parameters:**

` iIndex`      The index of the material to retrieve in the collection of materials. Compared with other collections, you cannot use the name of the material as argument.

**Returns:**      The retrieved material  **Example:**      The following example returns in `MyMaterial` the sixth material in a material collection.

```VBScript
     Dim MyMaterial As Material
     Set MyMaterial = Materials.Item(6)

```

### Sub **Remove**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`)

   Removes a material from the materials collection.  
### Func **SortedItem**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`,  short  `iMode`) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md)

   Returns a material from its index in the sorted Material collection.

**Parameters:**

` iIndex`      The index of the material to retrieve in the sorted collection of materials. Compared with other collections, you cannot use the name of the material as argument.
` iMode`      The sorted mode of material collection

Possible mode values are:
  * 0: Alphabetical order
  * 1: Inverse alphabetical order

**Returns:**      The retrieved material

---

# PositionedMaterial (Object)

**_Represents a Positioned Material object._**

## Properties

### Property **ApplicationMode**( ) As short (Read Only)

   Returns the application mode of the material.

Possible mode values are:
  * 0: Material has been applied as a copy on the geometrical object
  * 1: Material has been applied as a link on the geometrical object

### Property **InheritanceMode**( ) As short

   Returns or sets the inheritance mode of an applied material.

Possible inheritance mode values are:
  * 0: The material is propagated towards its children
  * 1: The material is not propagated towards its children
  * 2: The material do not accept material propagated by its father (forced mode)

### Property **Material**( ) As [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md) (Read Only)

   Returns the material object from the current positioned material.