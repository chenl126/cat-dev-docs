# HybridShapeLoft (Object)

**_Represents the hybrid shape loft surface feature object._**

**Role** : To access the data of the hybrid shape loft surface feature object.
This data includes:

  * The spine
  * The tangent surfaces to the start and end sections
  * Guide curves, sections, and couplings

Use the CATIAHybridShapeFactory to create a HybridShapeLoft object.

LICENSING INFORMATION: Creation of volume result requires GSO License
if GSO License is not granted , settting of Volume context has not effect

Use the CATIAHybridShapeFactory to create a HybridShapeLoft object.

**See also:**      [HybridShapeFactory](../GSMInterfaces/interface_HybridShapeFactory_68680.md)

## Properties

### Property **BooleanOperation**(| ) As long

   Gets or sets the boolean operation for closed lofted surface. TO BE USED ONLY for Part Loft (closed loft). BooleanOperation = 1 : No boolean operation. = 2 : Union boolean operation. = 3 : Removal boolean operation. This example retrieves in `BoolOp` the type of boolean operation for the `Loft` hybrid shape feature.

```VBScript
     Dim BoolOp
     BoolOp = Loft.BooleanOperation

```

### Property **CanonicalDetection**( ) As long

   Returns or sets whether canonical surfaces of the lofted surface are detected.

**Legal values** :

0
    No detection of canonical surface is performed
1
    Detection of planar surfaces only is performed
2
    Detection of canonical surfaces is performed

### Property **CompEndSectionTangent**( ) As long

   Returns or sets whether the tangent surface to the end section of the lofted surface is computed.

**Legal values** :

1
    The tangent to the end section is computed
2
    The tangent to the end section is not computed

### Property **CompStartSectionTangent**( ) As long

   Returns or sets whether the tangent surface to the start section of the lofted surface is computed.

**Legal values** :

1
    The tangent to the start section is computed
2
    The tangent to the start section is not computed

### Property **Context**( ) As long

   Returns or sets the context on Loft feature.

**Legal values** :

  * **0** This option creates Lofted surface.
  * **1** This option creates Lofted volume.

Note: Setting volume result requires GSO License.

**Example** :      This example retrieves in `oContext` the context for the `Loft` hybrid shape feature.

```VBScript
     Dim oContext
     Set oContext = Loft.Context

```

### Property **Relimitation**( ) As long

   Returns or sets the relimitation type between sections of the loft.
NOT YET IMPLEMENTED.

**Legal values** :

1
    The loft will be swept along the spine, then relimited by the start section and the end section
2
    The loft will be swept along the spine.

  * If the spine is a user spine, then the loft is limited by the spine extremities
  * If the spine is a computed spine, then the loft is limited:
    * By the start section and the end section, if there is no guide
    * By the guides extremities, if there are guides

3
    The loft will be swept along the spine, then relimited by the first section,

  * If the spine is a user spine, then the loft is limited by the spine extremity opposite to the first section
  * If the spine is a computed spine, then the loft is limited:
    * By the last section, if there is no guide
    * By the guides extremities opposite to the first section, if there are guides

4
    The loft will be swept along the spine, then relimited by the last section,

  * If the spine is a user spine, then the loft is limited by the spine extremity opposite to the last section
  * If the spine is a computed spine, then the loft is limited:
    * By the first section, if there is no guide
    * By the guides extremities opposite to the last section, if there are guides

### Property **SectionCoupling**( ) As long

   Returns or sets the type of coupling between sections of the loft.

**Legal values** :

1
    The curves will be coupled according to the curvilinear abscissa ratio
2
    if each curve has the same number of tangency discontinuity points, then these points will be coupled, otherwise an error message is displayed
3
    if each curve has the same number of tangency and curvature discontinuity points, then tangency discontinuity points will be coupled, and after curvature discontinuity points will be coupled, otherwise an error message is displayed
4
    if each curve has the same number of vertices, then these points will be coupled, otherwise an error message is displayed

### Property **SmoothAngleThreshold**( ) As double

   Returns or sets the angular threshold under which discontinuities (moving frame, tangency net on reference surface) will be smoothed.  
### Property **SmoothAngleThresholdActivity**( ) As boolean

   Returns or sets whether a angular threshold is allowed or not during lofting operation in order to smooth it.

**Legal values** :

TRUE
    The angular threshold value is used during the lofting operation
FALSE
    The angular threshold value is not used during the lofting operation

### Property **SmoothDeviation**( ) As double

   Returns or sets the deviation value (length) allowed during lofting operation in order to smooth it.  
### Property **SmoothDeviationActivity**( ) As boolean

   Returns or sets whether a deviation is allowed or not during lofting operation in order to smooth it.

**Legal values** :

TRUE
    The deviation value is used during the lofting operation
FALSE
    The deviation value is not used during the lofting operation
Methods

### Sub **AddGuide**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`)

   Adds a guide curve to the lofted surface.

**Parameters:**

` iGuide`      The guide curve to be added

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Sub **AddGuideWithTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTangent`)

   Adds a guide curve and a tangent surface to the lofted surface.

**Parameters:**

` iGuide`      The guide curve to be added

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md). ` iTangent`      The tangent surface to be added. The guide curve must be layed on the tangent

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Sub **AddSectionToLoft**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  long  `iOri`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Retrieves a loft section.

**Parameters:**

` iCrv`      Reference to the curve
` iOri`      Orientation
` iPoint`      Reference to the Closing Point

### Sub **GetFacesForClosing**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oStartFace`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oEndFace`)

   Gets start and end faces if the tangent is a computed tangent surface to the start section or end section, from the lofted surface. The section must have been set as a face.

**Parameters:**

` oStartFace`      start face used to close the loft.
` oEndFace`      end face used to close the loft.

### Sub **GetGuide**( long  `iPos`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oGuide`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oGuideTangent`)

   Gets informations about the guide at a specified position in the list of the lofted surface.

**Parameters:**

` iPos`      position of the guide in the list where the information is retrieved.
` oGuide`      the guide curve.
` oGuideTangent`      the tangent corresponding to the guide curve.

### Func **GetNbOfGuides**( ) As long

   Returns the number of guides in the loft object.

**Parameters:**

` oSize`      Number of guides in the loft.

**Example** :      This example retrieves the number of guides in the `hybShpLoft` hybrid shape Loft.

```VBScript
     Dim oSize As  long
     oSize = hybShpLoft.GetNbOfGuides

```

### Sub **GetSectionFromLoft**( long  `iRank`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oCrv`,  long  `oOri`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oPoint`)

   Retrieves a loft section information.

**Parameters:**

` iRank`      The index of the section
` oCrv`      The reference to the curve
` oOri`      The orientation value
` oPoint`      The reference to the point

### Sub **GetSpine**( long  `oSpineType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oSpine`)

   Gets the spine of the lofted surface.

**Parameters:**

` oSpineType`      type of spine = 1 : User defined spine. = 2 : Automatically computed spine.
` oSpine`      curve used as a spine, if the spine is user defined one.

### Sub **GetStartAndEndSectionTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oStartSectionTangent`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oEndSectionTangent`)

   Gets the start and end section tangents of the lofted surface.

**Parameters:**

` oStartSectionTangent`      tangent surface at start section.
` oEndSectionTangent`      tangent surface at end section.

### Sub **InsertCoupling**( long  `iPosition`)

   Inserts a coupling to the loft.

**Parameters:**

` iPosition`      The position of the coupling in the list of couplings. If 0 is specified, the coupling is inserted at the end of the list.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Vertex](../MecModInterfaces/interface_Vertex_8466.md).  
### Sub **InsertCouplingPoint**( long  `iCouplingIndex`,  long  `iPosition`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`)

   Inserts a coupling point to a coupling of the lofted surface.

**Parameters:**

` iCouplingIndex`      The index of the coupling in the list of coupling where the point wil be inserted.
` iPosition`      The position of the coupling point in the list of coupling points. If 0 is specified, the coupling point is inserted at the end of the list.
` iPoint`      The point to be inserted. The point must be layed on the section with the same position.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): ScVertex.  
### Sub **InsertSectionToLoft**( boolean  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCrv`,  long  `iOri`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iPoint`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSectionRef`)

   Inserts a loft section.

**Parameters:**

` iType`      iType if set to true section is added After and iType if set to false section is added Before iSectionRef
` iCrv`      Reference to the curve
` iOri`      Orientation
` iPoint`      Reference to the Closing Point
` iSectionRef`      iSectionRef is the section before and after which section is added.

### Sub **ModifyGuideCurve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewGuide`)

   Modifies the curve of a guide from the lofted surface.

**Parameters:**

` iGuide`      guide curve to be replaced.
` iNewGuide`      new guide curve, will replace iGuide.

### Sub **ModifySectionCurve**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNewSection`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oCurveSection`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `oClosingPoint`,  long  `oPtDiag`)

   Modifies the curve of section from the lofted surface.

**Parameters:**

` iSection`      section curve to be replaced.
` iNewSection`      section will replace iSection, can be a curve or a face
` oCurveSection`      if iSection is a face, oCurveSection is the boundary of the face. oCurveSection is used as section curve. if Part design, the face is used to close the Loft.
` oClosingPoint`      if iSection is a closed curve, oClosingPoint is a new closing point of iSection. if iSection is a face, oClosingPoint is a new closing point the boundary of iSection.
` oPtDiag`      Information on closing point = 0 : No closing point has been created nor retrieved. = 1 : A closing point has been created as a vertex. = 2 : A closing point has been created as an extremum. = 3 : A closing point has been retrieved as an extremum.

### Sub **ModifySectionOrient**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`,  long  `iOrient`)

   Modifies the orientation of the curve of a section from the lofted surface.

**Parameters:**

` iSection`      section curve to be modified.
` iOrient`      orientation of the section curve = 1 : same orientation. = -1 : inverted orientation. = 2 : ko orientation.

### Sub **RemoveFaceForClosing**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Removes face used to close the lofted surface.

**Parameters:**

` iSection`      section curve.

### Sub **RemoveGuide**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`)

   Removes a guide curve from the lofted surface.

**Parameters:**

` iGuide`      The guide curve to be removed

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Sub **RemoveGuideTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iGuide`)

   Removes a tangent surface of a guide from the lofted surface.

**Parameters:**

` iGuide`      guide curve of the guide from which the tangent will be removed.

### Sub **RemoveSection**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Removes a loft section from the lofted surface.

**Parameters:**

` iSection`      The loft section to remove

Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Sub **RemoveSectionPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Removes a closing point of a section from the lofted surface. The curve section must be closed curve.

**Parameters:**

` iSection`      section curve of the section from which the point will be removed.

### Sub **RemoveSectionTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSection`)

   Removes the tangent surface of a section from the lofted surface. The section must be the start section or the end section of the loft.

**Parameters:**

` iSection`      section curve of the section from which the tangent will be removed.

### Sub **SetEndFaceForClosing**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

   Sets a face to the end section from the lofted surface.

**Parameters:**

` iFace`      The face to close the loft (Part design only).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Sub **SetEndSectionTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTangentSection`)

   Sets a tangent surface to the end section from the lofted surface.

**Parameters:**

` iTangentSection`      The tangent surface to be added. The end curve section must lay on the surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Sub **SetSpine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSpine`)

   Sets the spine to the lofted surface.

**Parameters:**

` iSpine`      The curve to be added as a spine.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md) and [BiDimFeatEdge](../MecModInterfaces/interface_BiDimFeatEdge_33192.md).  
### Sub **SetStartFaceForClosing**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFace`)

   Sets a face to the start section from the lofted surface.

**Parameters:**

` iFace`      The face to close the loft (Part design only).
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).  
### Sub **SetStartSectionTangent**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTangentSection`)

   Sets a tangent surface to the start section from the lofted surface.

**Parameters:**

` iTangentSection`      The tangent surface to be added. The start curve section must lay on the surface.
Sub-element(s) supported (see
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object): [Face](../MecModInterfaces/interface_Face_3398.md).