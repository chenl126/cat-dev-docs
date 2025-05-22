# HybridShapeLineBisecting (Object)

**_Represents the hybrid shape bisecting line feature object._**
**Role** : To access the data of the hybrid shape bisecting line feature object. This data includes:

  * The two lines used to create the bisecting line
  * The reference point
  * The support
  * The start and end offsets
  * The orientation
  * The solution type

Use the CATIAHybridShapeFactory to create a HybridShapeAffinity object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BeginOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the start offset of the line.  
### Property **Elem1**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the first line used to create the bisecting line.

Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) or [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  
### Property **Elem2**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the second line used to create the bisecting line.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) or [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md).  
### Property **EndOffset**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the end offset of the line.  
### Property **Orientation**( ) As long

Returns or sets the orientation used to compute the bisecting line.
**Role** : the orientation specifies bisecting line position
**Legal values** : The orientation can be the same(1) or the inverse(-1)  
### Property **RefPoint**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the reference point used to create the bisecting line.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Property **SolutionType**( ) As boolean

Returns or sets the solution type.
**Role** : The solution type allows you to know where is the bisecting line.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support used to create the bisecting line.

**Parameters:**

` oElem`      retrieve the support of the bisecting line.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md).  Methods

### Func **GetLengthType**( ) As long

Gets the length type Default is 0.

**Parameters:**

` oType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Func **GetSymmetricalExtension**( ) As boolean

Gets whether the symmetrical extension of the line is active.

**Parameters:**

` oSym`      Symetry flag

### Sub **SetLengthType**( long  `iType`)

Sets the length type Default is 0.

**Parameters:**

` iType`      The length type = 0 : length - the line is limited by its extremities = 1 : infinite - the line is infinite = 2 : infinite start point - the line is infinite on the side of the start point = 3 : infinite end point - the line is infinite on the side of the end point

### Sub **SetSymmetricalExtension**( boolean  `iSym`)

Sets the symmetrical extension of the line (start = -end).

**Parameters:**

` iSym`      Symetry flag