# HybridShapeSpine (Object)

**_Represents the hybrid spine curve feature object._**

**Role** :Use the CATIAHybridShapeFactory to create a HybridShapeSpine object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **Orientation**(| ) As long

   Gets or Sets the orientation. Orientation by reference with the normal to the first section/plane  
### Property **StartPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

   Retuns or sets the start point of the spine.  Methods

### Sub **AddSection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Adds a section or a plane to the spine curve.

**Parameters:**

` iSection`      The section curve or plane to be added

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  
### Sub **GetGuide**( long  `iIdx`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `opIAGuide`)

   Retrieves a guide .

**Parameters:**

` iIdx`      The index of the guide
` opIAGuide`      The guide retrieved

### Func **GetNumberOfGuides**( ) As long

   Retrieves number of guides in a spine curve.

**Parameters:**

` oNbGuides`      Number of guides in a spine curve

### Func **GetNumberOfSections**( ) As long

   Retrieves number of sections in a spine curve.

**Parameters:**

` oNbSections`      Number of sections in a spine curve

### Sub **GetSection**( long  `iIdx`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oSection`)

   Retrieves a section or a plane.

**Parameters:**

` iIdx`      The index of the section
` oSection`      The section retrieved

### Sub **ModifyGuideCurve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIAGuide`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIANewGuide`)

   Modifies a guide from the spine curve.

**Parameters:**

` ipIAGuide`      The guide curve to be replaced.
` ipIANewGuide`      The new guide curve or plane which replaces the old one.

### Sub **ModifySectionCurve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIASection`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `ipIANewSection`)

   Modifies a section or a plane from the spine curve.

**Parameters:**

` ipIASection`      The section curve or plane to be replaced.
` ipIANewSection`      The new section curve or plane which replaces the old one.

### Sub **RemoveSection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Removes a section or a plane from the spine curve.

**Parameters:**

` iSection`      The section curve or plane to be removed.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  
### Sub **SetStartPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Sets the start point of the spine curve.

**Parameters:**

` iPoint`      The point to be set as the spine curve start point.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).