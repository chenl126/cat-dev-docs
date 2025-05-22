# ShapeFactory (Object)

**_Represents the factory for shapes to create all kinds of shapes that may be needed for part design._**

The Shapefactory mission is to build from scratch shapes that will be used within the design process of parts. Those shapes have a strong mechanical built-in knowledge, such as chamfer or hole, and in most cases apply contextually to the part being designed. When created, they become part of the definition of whichever _body_ or _shape_ that is current at that time. After they are created, they become in turn the current _body_ or _shape_. In most cases, shapes are created from a factory with a minimum number of parametersr. Other shapes parameters may be set further on by using methods offered by the shape itself.

## Methods

### Func **AddNewAdd**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBodyToAdd`) As [CATIAAdd](../PartInterfaces/interface_Add_1925.md)

Creates and returns a new add operation within the current body.

**Parameters:**

` iBodyToAdd`      The body to add to the current body
**Returns:**      The created add operation  
### Func **AddNewAffinity2**( double  `XRatio`,  double  `YRatio`,  double  `ZRatio`) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns a Affinity feature.

**Parameters:**

` XRatio`      Value for the XRatio.
` YRatio`      Value for the YRatio.
` ZRatio`      Value for the ZRatio.
**Returns:**      the created Affinity feature.  
### Func **AddNewAssemble**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBodyToAssemble`) As [CATIAAssemble](../PartInterfaces/interface_Assemble_13978.md)

Creates and returns a new assembly operation within the current body.

**Parameters:**

` iBodyToAssemble`      The body to assemble with the current body
**Returns:**      The created assembly operation  
### Func **AddNewAutoDraft**( double  `iDraftAngle`) As [CATIAAutoDraft](../PartInterfaces/interface_AutoDraft_17462.md)

Creates and returns a new solid autodraft.
Use this method to create autodraft by providing draft angle.

**Parameters:**

` iDraftAngle`      The draft angle.
**Returns:**      The created autodraft.  
### Func **AddNewAutoFillet**( double  `iFilletRadius`,  double  `iRoundRadius`) As [CATIAAutoFillet](../PartInterfaces/interface_AutoFillet_21690.md)

Creates and returns a new solid autofillet.
Use this method to create autofillet by providing fillet and round radius values.

**Parameters:**

` iFilletRadius`      The fillet radius
` iRoundRadius`      The round radius
**Returns:**      The created autofillet  
### Func **AddNewAxisToAxis2**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iReference`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iTarget`) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns an AxisToAxis transformation feature.

**Parameters:**

` iReference`      The refrence axis.
` iTarget`      The target axis.
**Returns:**      The created AxisToAxis transformation feature.  
### Func **AddNewBlend**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns a new Blend feature.

**Returns:**      The created Blend feature  
### Func **AddNewChamfer**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iObjectToChamfer`,  [CatChamferPropagation](../PartInterfaces/enum_CatChamferPropagation_93192.md)  `iPropagation`,  [CatChamferMode](../PartInterfaces/enum_CatChamferMode_40082.md)  `iMode`,  [CatChamferOrientation](../PartInterfaces/enum_CatChamferOrientation_93680.md)  `iOrientation`,  double  `iLength1`,  double  `iLength2OrAngle`) As [CATIAChamfer](../PartInterfaces/interface_Chamfer_10690.md)

Creates and returns a new chamfer within the current body.

**Parameters:**

` iObjectToChamfer`      The first edge or face to chamfer
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iPropagation`      Controls if and how the chamfering operation should propagate beyond the first chamfer element `iObjectToChamfer`, when it is an edge
` iMode`      Controls if the chamfer is defined by two lengthes, or by an angle and a length
The value of this argument changes the way the arguments `iLength1` and `iLength2OrAngle` should be interpreted.
` iOrientation`      Defines the relative meaning of arguments `iLength1` and `iLength2OrAngle` when defining a chamfer by two lengthes
` iLength1`      The first value for chamfer dimensioning. It represents the chamfer first length if the chamfer is defined by two lengthes, or the chamfer length if the chamfer is defined by a length and an angle.
` iLength2OrAngle`      The second value for chamfer dimensioning. It represents the chamfer second length if the chamfer is defined by two lengthes, or the chamfer angle if the chamfer is defined by a length and an angle.
**Returns:**      The created chamfer  
### Func **AddNewCircPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInRadialDir`,  long  `iNbOfCopiesInAngularDir`,  double  `iStepInRadialDir`,  double  `iStepInAngularDir`,  long  `iShapeToCopyPositionAlongRadialDir`,  long  `iShapeToCopyPositionAlongAngularDir`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationAxis`,  boolean  `iIsReversedRotationAxis`,  double  `iRotationAngle`,  boolean  `iIsRadiusAligned`) As [CATIACircPattern](../PartInterfaces/interface_CircPattern_26301.md)

Creates and returns a new circular pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the circular pattern
` iNbOfInstancesInRadialDir`      The number of times `iShapeToCopy` will be copied along pattern radial direction
` iNbOfInstancesInAngularDir`      The number of times `iShapeToCopy` will be copied along pattern angular direction
` iStepInRadialDir`      The distance that will separate two consecutive copies in the pattern along its radial direction
` iStepInAngularDir`      The angle that will separate two consecutive copies in the pattern along its angular direction
` iShapeToCopyPositionAlongRadialDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the radial direction
` iShapeToCopyPositionAlongAngularDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the angular direction
` iRotationCenter`      The point or vertex that specifies the pattern center of rotation
` iRotationAxis`      The line or linear edge that specifies the axis around which instances will be rotated relative to each other
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iIsReversedRotationAxis`      The boolean flag indicating wether the natural orientation of `iRotationAxis` should be used to orient the pattern operation. A value of true indicates that `iItemToDuplicate` are copied in the direction of the natural orientation of `iRotationAxis`.
` iRotationAngle`      The angle applied to the direction `iRotationAxis` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
` iIsRadiusAligned`      The boolean flag that specifies whether the instances of `iItemToDuplicate` copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
**Returns:**      The created circular pattern  
### Func **AddNewCircPatternofList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInRadialDir`,  long  `iNbOfCopiesInAngularDir`,  double  `iStepInRadialDir`,  double  `iStepInAngularDir`,  long  `iShapeToCopyPositionAlongRadialDir`,  long  `iShapeToCopyPositionAlongAngularDir`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationAxis`,  boolean  `iIsReversedRotationAxis`,  double  `iRotationAngle`,  boolean  `iIsRadiusAligned`) As [CATIACircPattern](../PartInterfaces/interface_CircPattern_26301.md)

V5R8 Only: Creates and returns a new circular pattern within the current body using a list of shapes.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the circular pattern. Others shapes will be add by put_ItemToCopy with CATIAPattern interface
` iNbOfInstancesInRadialDir`      The number of times `iShapeToCopy` will be copied along pattern radial direction
` iNbOfInstancesInAngularDir`      The number of times `iShapeToCopy` will be copied along pattern angular direction
` iStepInRadialDir`      The distance that will separate two consecutive copies in the pattern along its radial direction
` iStepInAngularDir`      The angle that will separate two consecutive copies in the pattern along its angular direction
` iShapeToCopyPositionAlongRadialDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the radial direction
` iShapeToCopyPositionAlongAngularDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the angular direction
` iRotationCenter`      The point or vertex that specifies the pattern center of rotation
` iRotationAxis`      The line or linear edge that specifies the axis around which instances will be rotated relative to each other
` iIsReversedRotationAxis`      The boolean flag indicating wether the natural orientation of `iRotationAxis` should be used to orient the pattern operation. A value of true indicates that `iItemToDuplicate` are copied in the direction of the natural orientation of `iRotationAxis`.
` iRotationAngle`      The angle applied to the direction `iRotationAxis` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
` iIsRadiusAligned`      The boolean flag that specifies whether the instances of `iItemToDuplicate` copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
**Returns:**      The created circular pattern  
### Func **AddNewCloseSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCloseElement`) As [CATIACloseSurface](../PartInterfaces/interface_CloseSurface_30578.md)

Creates and returns a new CloseSurface feature.

**Parameters:**

` iCloseElement`      The skin that will be closed and add with the current body
**Returns:**      The created CloseSurface feature  
### Func **AddNewDraft**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToDraft`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNeutral`,  [CatDraftNeutralPropagationMode](../PartInterfaces/enum_CatDraftNeutralPropagationMode_187684.md)  `iNeutralMode`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iParting`,  double  `iDirX`,  double  `iDirY`,  double  `iDirZ`,  [CatDraftMode](../PartInterfaces/enum_CatDraftMode_29572.md)  `iMode`,  double  `iAngle`,  [CatDraftMultiselectionMode](../PartInterfaces/enum_CatDraftMultiselectionMode_141932.md)  `iMultiselectionMode`) As [CATIADraft](../PartInterfaces/interface_Draft_5635.md)

Creates and returns a new draft within the current body.
The draft needs a reference face on the body. This face will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated by the draft angle.

**Parameters:**

` iFaceToDraft`      The first face to draft in the body. This face should be adjacent to the `iFaceToDraft` face. If several faces are to be drafted, only the first one is specified here, the others being inferred by propagating the draft operation onto faces adjacent to this first face. This is controlled by the `iNeutralMode` argument.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iNeutral`      The reference face for the draft. The draft needs a reference face on the body, that will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated according to the draft angle `iAngle`.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iNeutralMode`      Controls if and how the drafting operation should be propagated beyond the first face to draft `iFaceToDraft` to other adjacent faces.
` iParting`      The draft parting plane, face or surface. It specifies the element within the body to draft that represents the bottom of the mold. This element can be located either somewhere in the middle of the body or be one of its boundary faces. When located in the middle of the body, it crosses the faces to draft, and as a result, those faces are drafted with a positive angle on one side of the parting surface, and with a negative angle on the other side.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iDirX,iDirY,iDirZ`      The X, Y, and Z components of the absolute vector representing the drafting direction (i.e. the mold extraction direction).
` iMode`      The draft connecting mode to its reference face `iFaceToDraft`
` iAngle`      The draft angle
` iMultiselectionMode.`      The elements to be drafted can be selected explicitly or can implicitly selected as neighbors of the neutral face
**Returns:**      The created draft  
### Func **AddNewEdgeFilletWithConstantRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  double  `iRadius`) As [CATIAConstRadEdgeFillet](../PartInterfaces/interface_ConstRadEdgeFillet_66280.md)

**Deprecated:**      V5R14 #AddNewEdgeFilletWithConstantRadius use AddNewSolidEdgeFilletWithConstantRadius or AddNewSurfaceEdgeFilletWithConstantRadius depending on the type of fillet you want to create  
### Func **AddNewEdgeFilletWithVaryingRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  [CatFilletVariation](../PartInterfaces/enum_CatFilletVariation_68872.md)  `iVariationMode`,  double  `iDefaultRadius`) As [CATIAVarRadEdgeFillet](../PartInterfaces/interface_VarRadEdgeFillet_52056.md)

**Deprecated:**      V5R14 #AddNewEdgeFilletWithVaryingRadius use AddNewSolidEdgeFilletWithVaryingRadius or AddNewSurfaceEdgeFilletWithVaryingRadius depending on the type of fillet you want to create  
### Func **AddNewFaceFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  double  `iRadius`) As [CATIAFaceFillet](../PartInterfaces/interface_FaceFillet_21018.md)

**Deprecated:**      V5R14 #AddNewFaceFillet use AddNewSolidFaceFillet or AddNewSurfaceFaceFillet depending on the type of fillet you want to create  
### Func **AddNewGSDCircPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInRadialDir`,  long  `iNbOfCopiesInAngularDir`,  double  `iStepInRadialDir`,  double  `iStepInAngularDir`,  long  `iShapeToCopyPositionAlongRadialDir`,  long  `iShapeToCopyPositionAlongAngularDir`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationAxis`,  boolean  `iIsReversedRotationAxis`,  double  `iRotationAngle`,  boolean  `iIsRadiusAligned`,  boolean  `iCompleteCrown`,  double  `iType`) As [CATIACircPattern](../PartInterfaces/interface_CircPattern_26301.md)

**Deprecated:**      V5R15 #AddNewSurfacicCircPattern  
### Func **AddNewGSDRectPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInDir1`,  long  `iNbOfCopiesInDir2`,  double  `iStepInDir1`,  double  `iStepInDir2`,  long  `iShapeToCopyPositionAlongDir1`,  long  `iShapeToCopyPositionAlongDir2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir2`,  boolean  `iIsReversedDir1`,  boolean  `iIsReversedDir2`,  double  `iRotationAngle`,  double  `iType`) As [CATIARectPattern](../PartInterfaces/interface_RectPattern_26504.md)

**Deprecated:**      V5R15 #AddNewSurfacicRectPattern  
### Func **AddNewGroove**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`) As [CATIAGroove](../PartInterfaces/interface_Groove_8300.md)

Creates and returns a new groove within the current body.
The [Revolution](../PartInterfaces/interface_Revolution_22940.md), as a supertype for grooves, provides starting and ending angles for the groove definition.

**Parameters:**

` iSketch`      The sketch defining the groove section. The sketch must contain a contour and an axis that will be used to rotate the contour in the space, thus defining the groove. The contour has to penetrate in 3D space the current shape.
**Returns:**      The created groove  
### Func **AddNewGrooveFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElt`) As [CATIAGroove](../PartInterfaces/interface_Groove_8300.md)

Creates and returns a new groove within the current body.

**Parameters:**

` iProfileElt`      The reference on the element defining the groove base
**Returns:**      The created groove  
### Func **AddNewHole**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iSupport`      The support defining the hole reference plane.
Anchor point is located at the barycenter of the support. The hole axis in 3D passes through that point and is normal to the plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewHoleFromPoint**( double  `iX`,  double  `iY`,  double  `iZ`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iX`      Origin point x absolute coordinate
` iY`      Origin point y absolute coordinate
` iZ`      Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
` iSupport`      The support defining the hole reference plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewHoleFromRefPoint**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOrigin`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iOrigin`      The origin point which the hole is anchored to.
` iSupport`      The support defining the hole reference plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewHoleFromSketch**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iSketch`      The sketch defining the hole reference plane and anchor point.
This sketch must contain a single point that defines the hole axis: the hole axis in 3D passes through that point and is normal to the sketch plane.
` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewHoleWith2Constraints**( double  `iX`,  double  `iY`,  double  `iZ`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iX`      Origin point x absolute coordinate
` iY`      Origin point y absolute coordinate
` iZ`      Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
` iEdge`      The edge which the hole is constrained to.
The origin of the hole will have a length constraint with each edge.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iSupport`      The support defining the hole reference plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewHoleWithConstraint**( double  `iX`,  double  `iY`,  double  `iZ`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdge`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupport`,  double  `iDepth`) As [CATIAHole](../PartInterfaces/interface_Hole_3612.md)

Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.

**Parameters:**

` iX`      Origin point x absolute coordinate
` iY`      Origin point y absolute coordinate
` iZ`      Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
` iEdge`      The edge which the hole is constrained to.
If edge is circular, the origin of the hole will be concentric to the edge (iX, iY, iZ will be overridden). if not, the origin of the hole will have a length constraint with the edge.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iSupport`      The support defining the hole reference plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iDepth`      The hole depth.
**Returns:**      The created hole  
### Func **AddNewIntersect**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBodyToIntersect`) As [CATIAIntersect](../PartInterfaces/interface_Intersect_18201.md)

Creates and returns a new intersect operation within the current body.

**Parameters:**

` iBodyToIntersect`      The body to intersect with the current body
**Returns:**      The created intersect operation  
### Func **AddNewLoft**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns a new Loft feature.

**Returns:**      The created Loft feature  
### Func **AddNewMirror**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iMirroringElement`) As [CATIAMirror](../PartInterfaces/interface_Mirror_8458.md)

Creates and returns a new mirror within the current body.
A mirror allows for transforming existing shapes by a symmetry with respect to an existing plane.

**Parameters:**

` iMirroringElement`      The plane used by the mirror as the symmetry plane.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  **Returns:**      The created mirror  
### Func **AddNewPad**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  double  `iHeight`) As [CATIAPad](../PartInterfaces/interface_Pad_1979.md)

Creates and returns a new pad within the current body.

**Parameters:**

` iSketch`      The sketch defining the pad base
` iHeight`      The pad height
**Returns:**      The created pad  
### Func **AddNewPadFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElt`,  double  `iHeight`) As [CATIAPad](../PartInterfaces/interface_Pad_1979.md)

Creates and returns a new pad within the current body.

**Parameters:**

` iProfileElt`      The reference on the element defining the pad base
` iHeight`      The pad height
**Returns:**      The created pad  
### Func **AddNewPocket**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  double  `iHeight`) As [CATIAPocket](../PartInterfaces/interface_Pocket_8140.md)

Creates and returns a new pocket within the current shape.

**Parameters:**

` iSketch`      The sketch defining the pocket base
` iDepth`      The pocket depth
**Returns:**      The created pocket  
### Func **AddNewPocketFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElt`,  double  `iHeight`) As [CATIAPocket](../PartInterfaces/interface_Pocket_8140.md)

Creates and returns a new pocket within the current shape.

**Parameters:**

` iProfileElt`      The reference on the element defining the pocket base
` iDepth`      The pocket depth
**Returns:**      The created pocket  
### Func **AddNewRectPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInDir1`,  long  `iNbOfCopiesInDir2`,  double  `iStepInDir1`,  double  `iStepInDir2`,  long  `iShapeToCopyPositionAlongDir1`,  long  `iShapeToCopyPositionAlongDir2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir2`,  boolean  `iIsReversedDir1`,  boolean  `iIsReversedDir2`,  double  `iRotationAngle`) As [CATIARectPattern](../PartInterfaces/interface_RectPattern_26504.md)

Creates and returns a new rectangular pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the rectangular pattern
` iNbOfCopiesInDir1`      The number of times `iShapeToCopy` will be copied along the pattern first direction
` iNbOfCopiesInDir2`      The number of times `iShapeToCopy` will be copied along the pattern second direction
` iStepInDir1`      The distance that will separate two consecutive copies in the pattern along its first direction
` iStepInDir2`      The distance that will separate two consecutive copies in the pattern along its second direction
` iShapeToCopyPositionAlongDir1`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir1`
` iShapeToCopyPositionAlongDir2`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir2`
` iDir1`      The line or linear edge that specifies the pattern first repartition direction
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iDir2`      The line or linear edge that specifies the pattern second repartition direction
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iIsReversedDir1`      The boolean flag indicating whether the natural orientation of `iDir1` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir1`.
` iIsReversedDir2`      The boolean flag indicating whether the natural orientation of `iDir2` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir2`.
` iRotationAngle`      The angle applied to both directions `iDir1` and `iDir2` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
**Returns:**      The created rectangular pattern  
### Func **AddNewRectPatternofList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInDir1`,  long  `iNbOfCopiesInDir2`,  double  `iStepInDir1`,  double  `iStepInDir2`,  long  `iShapeToCopyPositionAlongDir1`,  long  `iShapeToCopyPositionAlongDir2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir2`,  boolean  `iIsReversedDir1`,  boolean  `iIsReversedDir2`,  double  `iRotationAngle`) As [CATIARectPattern](../PartInterfaces/interface_RectPattern_26504.md)

V5R8 Only: Creates and returns a new rectangular pattern within the current body using a list of shapes.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the rectangular pattern Others shapes will be add by put_ItemToCopy with CATIAPattern interface
` iNbOfCopiesInDir1`      The number of times `iShapeToCopy` will be copied along the pattern first direction
` iNbOfCopiesInDir2`      The number of times `iShapeToCopy` will be copied along the pattern second direction
` iStepInDir1`      The distance that will separate two consecutive copies in the pattern along its first direction
` iStepInDir2`      The distance that will separate two consecutive copies in the pattern along its second direction
` iShapeToCopyPositionAlongDir1`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir1`
` iShapeToCopyPositionAlongDir2`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir2`
` iDir1`      The line or linear edge that specifies the pattern first repartition direction
` iDir2`      The line or linear edge that specifies the pattern second repartition direction
` iIsReversedDir1`      The boolean flag indicating whether the natural orientation of `iDir1` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir1`.
` iIsReversedDir2`      The boolean flag indicating whether the natural orientation of `iDir2` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir2`.
` iRotationAngle`      The angle applied to both directions `iDir1` and `iDir2` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
**Returns:**      The created rectangular pattern  
### Func **AddNewRemove**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBodyToRemove`) As [CATIARemove](../PartInterfaces/interface_Remove_8234.md)

Creates and returns a new remove operation within the current body.

**Parameters:**

` iBodyToRemove`      The body to remove from the current body
**Returns:**      The created remove operation  
### Func **AddNewRemoveFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iKeepFaces`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFaces`) As [CATIARemoveFace](../PartInterfaces/interface_RemoveFace_20726.md)

Creates and returns a new RemoveFace feature.

**Parameters:**

` iKeepFaces`      The reference of the face to Keep.
` iRemoveFaces`      The reference of the face to Remove.
**Returns:**      The created RemoveFace feature.  
### Func **AddNewRemovedBlend**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns a new Removed Blend feature.

**Returns:**      The created Removed Blend feature  
### Func **AddNewRemovedLoft**( ) As [CATIABase](../System/interface_AnyObject_17321.md)

Creates and returns a new Removed Loft feature.

**Returns:**      The created Removed Loft feature  
### Func **AddNewReplaceFace**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplitPlane`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemoveFace`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSplittingSide`) As [CATIAReplaceFace](../PartInterfaces/interface_ReplaceFace_24481.md)

Creates and returns a new Align/ ReplaceFace feature.

**Parameters:**

` iSplitPlane`      The reference of the element defining the Splitting Plane.
` iRemoveFace`      The reference of the Face to Remove.
` iSplittingSide`      The specification for which side of the current body should be Align
**Returns:**      The created Align/ ReplaceFace feature.  
### Func **AddNewRib**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iCenterCurve`) As [CATIARib](../PartInterfaces/interface_Rib_2027.md)

Creates and returns a new rib within the current body.

**Parameters:**

` iSketch`      The sketch defining the rib section
` iCenterCurve`      The sketched curve that defines the rib center curve. It must cross the section definition sketch `iSketch` within the inner part of its contour.
**Returns:**      The created rib  
### Func **AddNewRibFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfile`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenterCurve`) As [CATIARib](../PartInterfaces/interface_Rib_2027.md)

Creates and returns a new rib within the current body.

**Parameters:**

` iProfile`      The Profile defining the rib section
` iCenterCurve`      The curve that defines the rib center curve.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Returns:**      The created rib  
### Func **AddNewScaling**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iScalingReference`,  double  `iFactor`) As [CATIAScaling](../PartInterfaces/interface_Scaling_10755.md)

Creates and returns a new scaling within the current body.

**Parameters:**

` iScalingReference`      The point, plane or face of the current body that will remain fixed during the scaling process: even if the face itself shrinks or expands during the scaling, its supporting plane will remain unchanged after the scaling.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) and [Vertex](../MecModInterfaces/interface_Vertex_8466.md). ` iFactor`      The scaling factor
**Returns:**      The created scaling  
### Func **AddNewSewSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSewingElement`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSewingSide`) As [CATIASewing](../PartInterfaces/interface_SewSurface_21428.md)

Creates and returns a new sewing operation within the current body.

**Parameters:**

` iSewingElement`      The face or skin or surface that will be sewn on the current body
` iSewingSide`      The specification for which side of the current body should be kept at the end of the sewing operation
**Returns:**      The created sewing operation  
### Func **AddNewShaft**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`) As [CATIAShaft](../PartInterfaces/interface_Shaft_5650.md)

Creates and returns a new shaft within the current body.
The [Revolution](../PartInterfaces/interface_Revolution_22940.md), as a supertype for shafts, provides starting and ending angles for the shaft definition.

**Parameters:**

` iSketch`      The sketch defining the shaft section.

  * If the shaft applies to the current body, then the sketch must contain a contour and an axis that will be used to rotate the contour in the space, thus defining the shaft.
  * If the shaft is the first shape defined, there is not current body to apply to. In such a case, the sketch must contain a curve whose end points are linked by an axis. By rotating the curve in the space around the axis, the shaft operation will define a revolution shape. This also works if the sketch contains a closed contour and an axis outside of this contour: in that case a revolution shape will be created, for example a torus.

**Returns:**      The created shaft  
### Func **AddNewShaftFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElt`) As [CATIAShaft](../PartInterfaces/interface_Shaft_5650.md)

Creates and returns a new shaft within the current body.

**Parameters:**

` iProfileElt`      The reference on the element defining the shaft base
**Returns:**      The created shaft  
### Func **AddNewShell**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`,  double  `iInternalThickness`,  double  `iExternalThickness`) As [CATIAShell](../PartInterfaces/interface_Shell_5652.md)

Creates and returns a new shell within the current body.

**Parameters:**

` iFaceToRemove`      The first face to be removed in the shell process.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iInternalThickness`      The thickness of material to be added on the internal side of all the faces during the shell process, except for those to be removed
` iExternaThickness`      The thickness of material to be added on the external side of all the faces during the shell process, except for those to be removed
**Returns:**      The created shell  
### Func **AddNewSlot**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`,  [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iCenterCurve`) As [CATIASlot](../PartInterfaces/interface_Slot_3864.md)

Creates and returns a new slot within the current shape.

**Parameters:**

` iSketch`      The sketch defining the slot section
` iCenterCurve`      The sketched curve that defines the slot center curve. It must cross the section definition sketch `iSketch` within the inner part of its contour.
**Returns:**      The created slot  
### Func **AddNewSlotFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfile`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCenterCurve`) As [CATIASlot](../PartInterfaces/interface_Slot_3864.md)

Creates and returns a new slot within the current shape.

**Parameters:**

` iProfile`      The sketch defining the slot section
` iCenterCurve`      The curve that defines the slot center curve.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md).  **Returns:**      The created slot  
### Func **AddNewSolidCombine**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileEltFirst`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileEltSecond`) As [CATIASolidCombine](../PartInterfaces/interface_SolidCombine_30404.md)

Creates and returns a new SolidCombine feature.

**Parameters:**

` iProfileEltFirst`      The reference of the element defining the profile for first component.
` iProfileEltSecond`      The reference of the element defining the profile for second component.
**Returns:**      The created SolidCombine feature.  
### Func **AddNewSolidEdgeFilletWithConstantRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  double  `iRadius`) As [CATIAConstRadEdgeFillet](../PartInterfaces/interface_ConstRadEdgeFillet_66280.md)

Creates and returns a new solid edge fillet with a constant radius. within the current body.

**Parameters:**

` iEdgeToFillet`      The edge that will be filleted first
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iPropagMode`      Controls whether other edges found adjacent to the first one should also be filleted in the same operation
` iRadius`      The fillet radius
**Returns:**      The created edge fillet  
### Func **AddNewSolidEdgeFilletWithVaryingRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  [CatFilletVariation](../PartInterfaces/enum_CatFilletVariation_68872.md)  `iVariationMode`,  double  `iDefaultRadius`) As [CATIAVarRadEdgeFillet](../PartInterfaces/interface_VarRadEdgeFillet_52056.md)

Creates and returns a new solid edge fillet with a varying radius. within the current body.

**Parameters:**

` iEdgeToFillet`      The edge that will be filleted first
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iPropagMode`      Controls whether other edges found adjacent to the first one should also be filleted in the same operation
` iVariationMode`      Controls the law of evolution for the fillet radius between specified control points, such as edges extremities
` iDefaultRadius`      The fillet default radius, that will apply when no other radius can be inferred from the `iVariationMode` parameter
**Returns:**      The created edge fillet  
### Func **AddNewSolidFaceFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  double  `iRadius`) As [CATIAFaceFillet](../PartInterfaces/interface_FaceFillet_21018.md)

Creates and returns a new solid face-to-face fillet.
Use this method to created face-to-face fillets with varying fillet radii, by editing fillet attributes driving its radius after its creation.

**Parameters:**

` iF1`      The first face that will support the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iF2`      The second face that will support the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iRadius`      The fillet radius
**Returns:**      The created face-to-face fillet  
### Func **AddNewSolidTritangentFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemovedFace`) As [CATIATritangentFillet](../PartInterfaces/interface_TritangentFillet_55088.md)

Creates and returns a new solid tritangent fillet within the current body.
This kind of fillet begins with tangency on a first face `iF1`, gets tangent to a second one `iRemovedFace` and ends with tangency to a third one `iF2`. During the process the second face `iRemovedFace` is removed.

**Parameters:**

` iF1`      The starting face for the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iF2`      The ending face for the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iRemovedFace`      The face used as an intermediate tangent support for the fillet during its course from `iF1` to `iF2`. This face will be removed at the end of the filleting operation.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md) **Returns:**      The created tritangent fillet  
### Func **AddNewSplit**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSplittingElement`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSplitSide`) As [CATIASplit](../PartInterfaces/interface_Split_5882.md)

Creates and returns a new split operation within the current body.

**Parameters:**

` iSplittingElement`      The face or plane that will split the current body
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iSplitSide`      The specification for which side of the current body should be kept at the end of the split operation
**Returns:**      The created split operation  
### Func **AddNewStiffener**( [CATIASketch](../SketcherInterfaces/interface_Sketch_8026.md)  `iSketch`) As [CATIAStiffener](../PartInterfaces/interface_Stiffener_17922.md)

Creates and returns a new stiffener within the current body.
A stiffener is made up of a sketch used as the stiffener profile, that is extruded (offset) and that fills the nearest shape.

**Parameters:**

` iSketch`      The sketch defining the stiffener border. It must contain a line or a curve that does not cross in 3D space the face(s) to stiffen.
**Returns:**      The created stiffener  
### Func **AddNewStiffenerFromRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iProfileElt`) As [CATIAStiffener](../PartInterfaces/interface_Stiffener_17922.md)

Creates and returns a new stiffener within the current body.

**Parameters:**

` iProfileElt`      The reference on the element defining the stiffener profile
**Returns:**      The created stiffener  
### Func **AddNewSurfaceEdgeFilletWithConstantRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  double  `iRadius`) As [CATIAConstRadEdgeFillet](../PartInterfaces/interface_ConstRadEdgeFillet_66280.md)

Creates and returns a new surface edge fillet with a constant radius. within the current body.

**Parameters:**

` iEdgeToFillet`      The edge that will be filleted first
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iPropagMode`      Controls whether other edges found adjacent to the first one should also be filleted in the same operation
` iRadius`      The fillet radius
**Returns:**      The created edge fillet  
### Func **AddNewSurfaceEdgeFilletWithVaryingRadius**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iEdgeToFillet`,  [CatFilletEdgePropagation](../PartInterfaces/enum_CatFilletEdgePropagation_120210.md)  `iPropagMode`,  [CatFilletVariation](../PartInterfaces/enum_CatFilletVariation_68872.md)  `iVariationMode`,  double  `iDefaultRadius`) As [CATIAVarRadEdgeFillet](../PartInterfaces/interface_VarRadEdgeFillet_52056.md)

Creates and returns a new surface edge fillet with a varying radius. within the current body.

**Parameters:**

` iEdgeToFillet`      The edge that will be filleted first
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [TriDimFeatEdge](../MecModInterfaces/interface_TriDimFeatEdge_39030.md). ` iPropagMode`      Controls whether other edges found adjacent to the first one should also be filleted in the same operation
` iVariationMode`      Controls the law of evolution for the fillet radius between specified control points, such as edges extremities
` iDefaultRadius`      The fillet default radius, that will apply when no other radius can be inferred from the `iVariationMode` parameter
**Returns:**      The created edge fillet  
### Func **AddNewSurfaceFaceFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  double  `iRadius`) As [CATIAFaceFillet](../PartInterfaces/interface_FaceFillet_21018.md)

Creates and returns a new surface face-to-face fillet.
Use this method to created face-to-face fillets with varying fillet radii, by editing fillet attributes driving its radius after its creation.

**Parameters:**

` iF1`      The first face that will support the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iF2`      The second face that will support the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iRadius`      The fillet radius
**Returns:**      The created face-to-face fillet  
### Func **AddNewSurfaceTritangentFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemovedFace`) As [CATIATritangentFillet](../PartInterfaces/interface_TritangentFillet_55088.md)

Creates and returns a new surface tritangent fillet within the current body.
This kind of fillet begins with tangency on a first face `iF1`, gets tangent to a second one `iRemovedFace` and ends with tangency to a third one `iF2`. During the process the second face `iRemovedFace` is removed.

**Parameters:**

` iF1`      The starting face for the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iF2`      The ending face for the fillet
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iRemovedFace`      The face used as an intermediate tangent support for the fillet during its course from `iF1` to `iF2`. This face will be removed at the end of the filleting operation.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md) **Returns:**      The created tritangent fillet  
### Func **AddNewSurfacicAutoFillet**( double  `iFilletRadius`) As [CATIAAutoFillet](../PartInterfaces/interface_AutoFillet_21690.md)

Creates and returns a new Surfacic autofillet.
Use this method to create autofillet by providing fillet radius value.

**Parameters:**

` iFilletRadius`      The fillet radius
**Returns:**      The created autofillet  
### Func **AddNewSurfacicCircPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInRadialDir`,  long  `iNbOfCopiesInAngularDir`,  double  `iStepInRadialDir`,  double  `iStepInAngularDir`,  long  `iShapeToCopyPositionAlongRadialDir`,  long  `iShapeToCopyPositionAlongAngularDir`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationCenter`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRotationAxis`,  boolean  `iIsReversedRotationAxis`,  double  `iRotationAngle`,  boolean  `iIsRadiusAligned`,  boolean  `iCompleteCrown`) As [CATIACircPattern](../PartInterfaces/interface_CircPattern_26301.md)

Creates and returns a new gsd circular pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the circular pattern
` iNbOfInstancesInRadialDir`      The number of times `iShapeToCopy` will be copied along pattern radial direction
` iNbOfInstancesInAngularDir`      The number of times `iShapeToCopy` will be copied along pattern angular direction
` iStepInRadialDir`      The distance that will separate two consecutive copies in the pattern along its radial direction
` iStepInAngularDir`      The angle that will separate two consecutive copies in the pattern along its angular direction
` iShapeToCopyPositionAlongRadialDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the radial direction
` iShapeToCopyPositionAlongAngularDir`      Specifies the position of the original shape `iShapeToCopy` among its copies along the angular direction
` iRotationCenter`      The point or vertex that specifies the pattern center of rotation
` iRotationAxis`      The line or linear edge that specifies the axis around which instances will be rotated relative to each other
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md) , [CylindricalFace](../MecModInterfaces/interface_CylindricalFace_46299.md) , [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md) and [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iIsReversedRotationAxis`      The boolean flag indicating wether the natural orientation of `iRotationAxis` should be used to orient the pattern operation. A value of true indicates that `iItemToDuplicate` are copied in the direction of the natural orientation of `iRotationAxis`.
` iRotationAngle`      The angle applied to the direction `iRotationAxis` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
` iIsRadiusAligned`      The boolean flag that specifies whether the instances of `iItemToDuplicate` copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
` iCompleteCrown`      The boolean flag specifies the mode of angular distribution. True indicates that the angular step will be equal to 360 degrees `iNba`.
**Returns:**      The created circular pattern  
### Func **AddNewSurfacicRectPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopiesInDir1`,  long  `iNbOfCopiesInDir2`,  double  `iStepInDir1`,  double  `iStepInDir2`,  long  `iShapeToCopyPositionAlongDir1`,  long  `iShapeToCopyPositionAlongDir2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iDir2`,  boolean  `iIsReversedDir1`,  boolean  `iIsReversedDir2`,  double  `iRotationAngle`) As [CATIARectPattern](../PartInterfaces/interface_RectPattern_26504.md)

Creates and returns a new GSD rectangular pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the rectangular pattern
` iNbOfCopiesInDir1`      The number of times `iShapeToCopy` will be copied along the pattern first direction
` iNbOfCopiesInDir2`      The number of times `iShapeToCopy` will be copied along the pattern second direction
` iStepInDir1`      The distance that will separate two consecutive copies in the pattern along its first direction
` iStepInDir2`      The distance that will separate two consecutive copies in the pattern along its second direction
` iShapeToCopyPositionAlongDir1`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir1`
` iShapeToCopyPositionAlongDir2`      Specifies the position of the original shape `iShapeToCopy` among its copies along `iDir2`
` iDir1`      The line or linear edge that specifies the pattern first repartition direction
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iDir2`      The line or linear edge that specifies the pattern second repartition direction
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) objects are supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md), [RectilinearTriDimFeatEdge](../MecModInterfaces/interface_RectilinearTriDimFeatEdge_125698.md), [RectilinearBiDimFeatEdge](../MecModInterfaces/interface_RectilinearBiDimFeatEdge_114366.md). ` iIsReversedDir1`      The boolean flag indicating whether the natural orientation of `iDir1` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir1`.
` iIsReversedDir2`      The boolean flag indicating whether the natural orientation of `iDir2` should be used to orient the pattern operation. True indicates that `iShapeToCopy` is copied in the direction of the natural orientation of `iDir2`.
` iRotationAngle`      The angle applied to both directions `iDir1` and `iDir2` prior to applying the pattern. The original shape `iShapeToCopy` is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
**Returns:**      The created rectangular pattern  
### Func **AddNewSurfacicUserPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopies`) As [CATIAUserPattern](../PartInterfaces/interface_UserPattern_26749.md)

Creates and returns a new GSD user pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the user pattern
` iNbOfCopies`      The number of times `iShapeToCopy` will be copied
**Returns:**      The created user pattern  
### Func **AddNewThickSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOffsetElement`,  long  `iIsensOffset`,  double  `iTopOffset`,  double  `iBotOffset`) As [CATIAThickSurface](../PartInterfaces/interface_ThickSurface_30456.md)

Creates and returns a new ThickSurface feature.

**Parameters:**

` iOffsetElement`      The skin that will be thicken and added with the current body
` iIsensOffset`      The direction of the offset in regard to the direction of the normal
` iTopOffset`      The Offset between the iOffsetElement and the upper skin of the resulting feature
` iBotOffset`      The Offset between the iOffsetElement and the lower skin of the resulting feature
**Returns:**      The created ThickSurface feature  
### Func **AddNewThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToThicken`,  double  `iOffset`) As [CATIAThickness](../PartInterfaces/interface_Thickness_18180.md)

Creates and returns a new thickness within the current body.

**Parameters:**

` iFaceToThicken`      The first face to thicken in the thickening process.
New faces to thicken can be added to the thickness afterwards by using methods offered by the created thickness
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iOffset`      The thickness of material to be added on the external side of the face `iFaceToThicken` during the thickening process
**Returns:**      The created thickness  
### Func **AddNewThreadWithOutRef**( ) As [CATIAThread](../PartInterfaces/interface_Thread_7846.md)

Creates and returns a new thread\tap within the current body.

**Returns:**      The created Thread  
### Func **AddNewThreadWithRef**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLateralFace`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iLimitFace`) As [CATIAThread](../PartInterfaces/interface_Thread_7846.md)

Creates and returns a new thread\tap within the current body.

**Parameters:**

` iLateralFace`      The Face defining the support of thread\tap
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iLimitFacee`      The Face defining the origin of the thread.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md).  **Returns:**      The created Thread  
### Func **AddNewTrim**( [CATIABody](../MecModInterfaces/interface_Body_3736.md)  `iBodyToTrim`) As [CATIATrim](../PartInterfaces/interface_Trim_3774.md)

Creates and returns a new Trim operation within the current body.

**Parameters:**

` iBodyToTrim`      The body to Trim with current body.
**Returns:**      The created Trim operation  
### Func **AddNewTritangentFillet**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iF2`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iRemovedFace`) As [CATIATritangentFillet](../PartInterfaces/interface_TritangentFillet_55088.md)

**Deprecated:**      V5R14 #AddNewTritangentFillet use AddNewSolidTritangentFillet or AddNewSurfaceTritangentFillet depending on the type of fillet you want to create  
### Func **AddNewUserPattern**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopies`) As [CATIAUserPattern](../PartInterfaces/interface_UserPattern_26749.md)

Creates and returns a new user pattern within the current body.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the user pattern
` iNbOfCopies`      The number of times `iShapeToCopy` will be copied
**Returns:**      The created user pattern  
### Func **AddNewUserPatternofList**( [CATIABase](../System/interface_AnyObject_17321.md)  `iShapeToCopy`,  long  `iNbOfCopies`) As [CATIAUserPattern](../PartInterfaces/interface_UserPattern_26749.md)

V5R8 Only: Creates and returns a new user pattern within the current body using a list of shapes.

**Parameters:**

` iShapeToCopy`      The shape to be copied by the user pattern Others shapes will be add by put_ItemToCopy with CATIAPattern interface
` iNbOfCopies`      The number of times `iShapeToCopy` will be copied
**Returns:**      The created user pattern  
### Func **AddNewVolumeAdd**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody2`,  double  `iType`) As [CATIAAdd](../PartInterfaces/interface_Add_1925.md)

Creates and returns a Volumic Add feature.

**Parameters:**

` iBody1`      The volume or body to be modified.
` iBody2`      The volume or body to be operated.
` iType`      iType = 0 if Part Design, = 4 if GSD.
**Returns:**      The created Volumic Add feature.  
### Func **AddNewVolumeCloseSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCloseElement`) As [CATIACloseSurface](../PartInterfaces/interface_CloseSurface_30578.md)

Creates and returns a new VolumeCloseSurface feature.

**Parameters:**

` iCloseElement`      The skin that will be closed and add with the current body
**Returns:**      The created CloseSurface feature  
### Func **AddNewVolumeIntersect**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody2`,  double  `iType`) As [CATIAIntersect](../PartInterfaces/interface_Intersect_18201.md)

Creates and returns a Volumic Intersect feature.

**Parameters:**

` iBody1`      The volume or body to be modified.
` iBody2`      The volume or body to be operated.
` iType`      iType = 0 if Part Design, = 4 if GSD.
**Returns:**      The created Volumic Intersect feature.  
### Func **AddNewVolumeRemove**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody1`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iBody2`,  double  `iType`) As [CATIARemove](../PartInterfaces/interface_Remove_8234.md)

Creates and returns a Volumic Remove feature.

**Parameters:**

` iBody1`      The volume or body to be modified.
` iBody2`      The volume or body to be operated.
` iType`      iType = 0 if Part Design, = 4 if GSD.
**Returns:**      The created Volumic Remove feature.  
### Func **AddNewVolumeSewSurface**( long  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupportVolume`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSewingElement`,  [CatSplitSide](../PartInterfaces/enum_CatSplitSide_30158.md)  `iSewingSide`) As [CATIASewing](../PartInterfaces/interface_SewSurface_21428.md)

Creates and returns a new volume sewing operation within the current OGS/GS.

**Parameters:**

` iType`      Parameter to determine the sewing type. For Volume sewing Type = 4
` iSupportVolume`      The volume support on which sew operation will be performed
` iSewingElement`      The face or skin or surface that will be sewn on the current volume support
` iSewingSide`      The specification for which side of the current volume should be kept at the end of the sewing operation
**Returns:**      The created sewing operation  
### Func **AddNewVolumeShell**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToRemove`,  double  `iInternalThickness`,  double  `iExternalThickness`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`) As [CATIAShell](../PartInterfaces/interface_Shell_5652.md)

Creates and returns a Volumic Shell feature.

**Parameters:**

` iFacesToRemove`      The Faces of the Volume
` iFacesToThicken`      The Faces of the Volume
` iInternalThickness`      The thickness of material to be added on the internal side of all the faces during the shell process, except for those to be removed
` iExternaThickness`      The thickness of material to be added on the external side of all the faces during the shell process, except for those to be removed
` iVolumeSupport`      The Volume related the faces to remove and faces to thicken
**Returns:**      The created Volumic Shell.  
### Func **AddNewVolumeThickSurface**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iOffsetElement`,  long  `iIsensOffset`,  double  `iTopOffset`,  double  `iBotOffset`) As [CATIAThickSurface](../PartInterfaces/interface_ThickSurface_30456.md)

Creates and returns a new VolumeThickSurface feature.

**Parameters:**

` iOffsetElement`      The skin that will be thicken and added with the current OGS/GS
` iIsensOffset`      The direction of the offset in regard to the direction of the normal
` iTopOffset`      The Offset between the iOffsetElement and the upper skin of the resulting feature
` iBotOffset`      The Offset between the iOffsetElement and the lower skin of the resulting feature
**Returns:**      The created ThickSurface feature  
### Func **AddNewVolumeThickness**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToThicken`,  double  `iOffset`,  long  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`) As [CATIAThickness](../PartInterfaces/interface_Thickness_18180.md)

Creates and returns a volume new thickness within the current GS or OGS.

**Parameters:**

` iFaceToThicken`      The first face to thicken in the thickening process.
New faces to thicken can be added to the thickness afterwards by using methods offered by the created thickness
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iOffset`      The thickness of material to be added on the external side of the face `iFaceToThicken` during the thickening process
` iType`      The mode of thickness creation (4=Volume)
` iVolumeSupport`      The support volume for volumic draft
**Returns:**      The created thickness  
### Func **AddNewVolumeTrim**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iSupportVolume`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iCuttingVolume`) As [CATIATrim](../PartInterfaces/interface_Trim_3774.md)

Creates and returns a new Volume Trim operation within the GS/OGS.

**Parameters:**

` iSupportVolume`      The Support Volume
` iCutttingVolume`      The trimming Volume
**Returns:**      The created Trim operation  
### Func **AddNewVolumicDraft**( [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iFaceToDraft`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iNeutral`,  [CatDraftNeutralPropagationMode](../PartInterfaces/enum_CatDraftNeutralPropagationMode_187684.md)  `iNeutralMode`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iParting`,  double  `iDirX`,  double  `iDirY`,  double  `iDirZ`,  [CatDraftMode](../PartInterfaces/enum_CatDraftMode_29572.md)  `iMode`,  double  `iAngle`,  [CatDraftMultiselectionMode](../PartInterfaces/enum_CatDraftMultiselectionMode_141932.md)  `iMultiselectionMode`,  long  `iType`,  [CATIAReference](../InfInterfaces/interface_Reference_17481.md)  `iVolumeSupport`) As [CATIADraft](../PartInterfaces/interface_Draft_5635.md)

Creates and returns a new volume draft within the current body.
The draft needs a reference face on the body. This face will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated by the draft angle.

**Parameters:**

` iFaceToDraft`      The first face to draft in the body. This face should be adjacent to the `iFaceToDraft` face. If several faces are to be drafted, only the first one is specified here, the others being inferred by propagating the draft operation onto faces adjacent to this first face. This is controlled by the `iNeutralMode` argument.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [Face](../MecModInterfaces/interface_Face_3398.md). ` iNeutral`      The reference face for the draft. The draft needs a reference face on the body, that will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated according to the draft angle `iAngle`.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iNeutralMode`      Controls if and how the drafting operation should be propagated beyond the first face to draft `iFaceToDraft` to other adjacent faces.
` iParting`      The draft parting plane, face or surface. It specifies the element within the body to draft that represents the bottom of the mold. This element can be located either somewhere in the middle of the body or be one of its boundary faces. When located in the middle of the body, it crosses the faces to draft, and as a result, those faces are drafted with a positive angle on one side of the parting surface, and with a negative angle on the other side.
The following
[Boundary](../MecModInterfaces/interface_Boundary_14542.md) object is supported: [PlanarFace](../MecModInterfaces/interface_PlanarFace_20456.md). ` iDirX,iDirY,iDirZ`      The X, Y, and Z components of the absolute vector representing the drafting direction (i.e. the mold extraction direction).
` iMode`      The draft connecting mode to its reference face `iFaceToDraft`
` iAngle`      The draft angle
` iMultiselectionMode.`      The elements to be drafted can be selected explicitly or can implicitly selected as neighbors of the neutral face
` iType`      The mode of draft creation (4=Volume)
` iVolumeSupport`      The support volume for volumic draft
**Returns:**      The created draft