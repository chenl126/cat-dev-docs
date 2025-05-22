# HybridShapeExtrapol (Object)

**_Represents the hybrid shape extrapolation feature object._**
**Role** : To access the data of the hybrid shape affinity feature object. The hybrid shape extrapolation feature object is created by using an element (a curve or a surface), a boundary of this element (a point in case of curve extrapolation or a curve in case of surface extrapolation), and a limit (which can be specified by a length or a limit element).
The continuity between the extrapolated element and the extrapolation can be either tangent continuity or curvature continuity.
The extrapolation can be assembled or not with the extrapolated curve or surface. In case of surface extrapolation, extrapolation borders can be:

  * Normal to the boundary of the extrapolated surface
  * Tangent to the edges of the extrapolated surface, that are adjacent to the boundary

Use the CATIAHybridShapeFactory to create a HybridShapeExtrapol object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BorderType**( ) As long

Returns or sets the border type of extrapolation.
This applies for surface extrapolation only.
**Legal values** : the border type is either normal to the boundary of the extrapolated surface (CATGSMNormalBorder(=0)), or tangent to the edges of the extrapolated surface that are adjacent to the boundary CATGSMTangentBorder(=1)).  
### Property **Boundary**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the boundary of an extrapolated curve or surface from which extrapolation begins.
The boudary is a point for an extrapolated curve, or a curve for an extrapolated surface.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md) , [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Property **ConstantLengthMode**( ) As boolean

Returns or sets the constant distance mode in case of Length extrapolation limit.
This applies in case of Length extrapolation limit.  
### Property **ContinuityType**( ) As long

Returns or sets the continuity type between extrapolated element and extrapolation.
**Legal values** : the continuity type is either CATGSMTangentContinuity (=0) or CATGSMCurvatureContinuity (=1).  
### Property **ElemToExtrapol**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the curve or surface to extrapolate.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md) , [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) or [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Property **ElemUntil**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the surface or volume specifying the extrapolation limit.
This applies when the limit type is CATGSMUpToElementLimit (=1).  
### Property **ExtendEdgesMode**( ) As boolean

Returns or sets the extension of extrapolated edges mode.
This applies in case of tangent continuity mode, tangent border mode and assembled result.  
### Property **Length**( ) As [CATIALength](../KnowledgeInterfaces/interface_Length_8108.md) (Read Only)

Returns the length specifying the extrapolation limit.
This applies when the limit type is CATGSMLengthLimit (=0).  
### Property **LimitType**( ) As long

Returns or sets the limit type of extrapolation.
The limit can be a length, a surface, or a volume.
**Legal values** : the limit type is either CATGSMLengthLimit(0) or CATGSMUpToElementLimit(1).  
### Property **PropagationMode**( ) As long

Returns or sets the propagation mode.
This applies in case of curvature extrapolation of a shell.  
### Property **Support**( ) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Returns or sets the support surface.
This applies in case of tangent extrapolation of a wire. If a support surface is given, the extrapolation will lie on it.
Sub-element(s) supported (see [Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): see [Face](../MecModInterfaces/interface_Face_3398.md).  Methods

### Func **GetInternalEdgesElement**( long  `iPos`) As [CATIAReference](../InfInterfaces/interface_Reference_17481.md)

Gets an element in the list of internal elements (vertex or edges).

**Parameters:**

` oInternalElement`      internal element
` iPos`      position of internal element to be retrieved.

### Func **IsAssemble**( ) As boolean

Retrieves whether extrapolation is assembled with extrapolated curve or surface.

**Parameters:**

` oAssemble`      The assemble option
**True** when the extrapolation is assembled with extrapolated curve or surface, and **False** otherwise

### Sub **RemoveAllInternalEdgesElement**( )

Removes all internal elements.  
### Sub **SetAssemble**( boolean  `iAssemble`)

Sets whether extrapolation is to be assembled with extrapolated curve or surface.

**Parameters:**

` iAssemble`      The assemble option
**True** when the extrapolation is to be assembled with extrapolated curve or surface, and **False** otherwise.