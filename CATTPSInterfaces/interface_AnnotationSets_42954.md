# AnnotationSets (Collection)

**_Interface for collection of Annotations' Set_**

## Methods

### Func **AddInAProduct**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iStandard`) As [CATIAAnnotationSet](../CATTPSInterfaces/interface_AnnotationSet_36773.md)

Add a set in the product.  
### Func **Item**( [CATVariant](../System/typedef_CATVariant_20656.md)  `iIndex`) As [CATIABase](../System/interface_AnyObject_17321.md)

Retrieve a set.  
### Sub **LoadAnnotationSetsList**( )

Loads the Annotation Sets list. This method is very useful when a cgr document containing Annotation Set is inserted in the product, because the Annotation Set is not automatically loaded If the Annotation Set is already loaded nothing happens.