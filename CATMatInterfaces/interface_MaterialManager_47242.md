# MaterialManager (Object)

**_Interface to manage material manager object._**

**Role** : A material manager is used to manage materials application on geometrical objects.

## Methods

### Sub **ApplyMaterialOnBody**(| [CATIABody](../MecModInterfaces/interface_Body_3736.md) | `iBody`,| | [CATIAMaterial](../CATMatInterfaces/interface_Material_14052.md) | `iMaterial`,| | short | `iLinkMode`)

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