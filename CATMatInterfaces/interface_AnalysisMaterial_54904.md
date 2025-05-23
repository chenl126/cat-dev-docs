# AnalysisMaterial (Object)

**_Represents an AnalysisMaterial object._**
This object is used to manage the Analysis properties of a material.

## Methods

### Func **GetType**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns the analysis type (Ex: MATERIAL_ORTHOTROPIC, MATERIAL_ISOTROPIC).  
### Func **GetValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`) As [CATVariant](../System/typedef_CATVariant_20656.md)

   Returns an analysis value of the material. The name of the parameter is needed  
### Sub **PutValue**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iLabel`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets an analysis value of the material. The name of the parameter is needed