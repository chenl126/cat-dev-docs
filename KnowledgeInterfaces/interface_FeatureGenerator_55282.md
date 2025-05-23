# FeatureGenerator (Object)

**_The interface to access a CATIAFeatureGenerator._**

## Properties

### Property **NbGeneratedFeatures**(| ) As long (Read Only)

   Number of generated features in last generation.  
### Property **Script**( ) As [CATBSTR](../System/typedef_CATBSTR_8129.md)

   Returns or sets the script that describes what is to be generated.  Methods

### Sub **Generate**( [CATIABase](../System/interface_AnyObject_17321.md)  `iContext`)

   Generates the features.  
### Sub **GenerateInContext**( [CATSafeArrayVariant](../System/typedef_CATSafeArrayVariant_73843.md)  `iInputsArray`)

   Generates the features.  
### Sub **LoadScriptFromFilePath**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iFilePath`)

   Sets a script from a document file.