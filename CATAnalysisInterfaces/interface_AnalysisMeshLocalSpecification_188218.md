# AnalysisMeshLocalSpecification (Object)

**_The interface to access a CATIAAnalysisMeshLocalSpecification._**

## Properties

### Property **Type**(| ) As [CATBSTR](../System/typedef_CATBSTR_8129.md) (Read Only)

   Returns the type of the local specification.

**Returns:**      The string that represent the type of local specification.  Methods

### Sub **AddSupportFromPublication**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`)

   Defines the support of the local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iProduct`      the CATIA Product that represent the object to linked.
` iPublication`      the CATIA Publication that represent the geometry.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Defines the support of the local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iProduct`      the CATIA Product that represent the object to linked.
` iSupport`      the CATIA Reference that represent the geometry.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **SetAttribute**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets the value corresponding to the given local specification.

**Parameters:**

` iName`      The identifier of the attribute.
` iValue`      The value of the local specification.