# AnalysisMeshPart (Object)

**_The interface to access a CATIAAnalysisMeshPart._**

## Properties

### Property **Activity**(| ) As boolean

   Returns the activity of an meshpart.

**Parameters:**

` oActivity`

**Legal values** :

FALSE

    **Mesh Part** is not active. TRUE

    **Mesh Part** is active.

### Property **AnalysisMeshLocalSpecifications**( ) As [CATIAAnalysisMeshLocalSpecifications](../CATAnalysisInterfaces/interface_AnalysisMeshLocalSpecifications_201982.md) (Read Only)

   Returns the local specification collection from the meshpart analysis.  Methods

### Sub **AddSupportFromPublication**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`)

   Creates a new support and add it to the support description of the mesh part.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iPublication`      the CATIA Publication that represent the the geometry to meshed.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **AddSupportFromReference**( [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`)

   Creates a new support and add it to the support description of the mesh part.

**Parameters:**

` iProduct`      the CATIA Product that represent the object to linked.

` iSupport`      the CATIA Reference that represent the geometry to meshed.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) 
### Sub **SetGlobalSpecification**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATVariant](../System/typedef_CATVariant_20656.md)  `iValue`)

   Sets the value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iValue`      The value of the global specification.

### Sub **SetSpecificationFromPublication**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAPublication](../ProductStructureInterfaces/interface_Publication_26668.md)  `iSupport`,  long  `iMode`)

   Adds the geometric value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iProduct`      the CATIA Product that represent the object to linked.

` iPublication`      the CATIA Publication that represent the the geometry to meshed.

**See also:**      [Publication](../ProductStructureInterfaces/interface_Publication_26668.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) ` iMode`      The mode used to valuate the publication global specification.

**Legal values** :

0
    the global specification is defined as a single reference. 1
    the global specification is added to exising references.

### Sub **SetSpecificationFromReference**( [CATBSTR](../System/typedef_CATBSTR_8129.md)  `iName`,  [CATIAProduct](../ProductStructureInterfaces/interface_Product_11223.md)  `iProduct`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  long  `iMode`)

   Set the geometric value corresponding to the given global specification.

**Parameters:**

` iName`      The identifier if the global specification.

` iProduct`      the CATIA Product that represent the object to linked.

` iSupport`      the CATIA Reference that represent the geometry to meshed.

**See also:**      [Reference](../InfInterfaces/interface_Reference_17481.md), [Product](../ProductStructureInterfaces/interface_Product_11223.md) ` iMode`      The mode used to valuate the reference global specification.

**Legal values** :

0
    the global specification is defined as a single reference. 1
    the global specification is added to exising references.