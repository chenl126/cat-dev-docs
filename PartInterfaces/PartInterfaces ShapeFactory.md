# ShapeFactory (Object)
**_Represents the factory for shapes to create all kinds of shapes that may be needed for part design._**
The Shapefactory mission is to build from scratch shapes that will be used within the design process of parts. Those shapes have a strong mechanical built-in knowledge, such as chamfer or hole, and in most cases apply contextually to the part being designed. When created, they become part of the definition of whichever body or shape that is current at that time. After they are created, they become in turn the current body or shape. In most cases, shapes are created from a factory with a minimum number of parametersr. Other shapes parameters may be set further on by using methods offered by the shape itself.
## Method Index
### AddNewAdd
Creates and returns a new add operation within the current body.
AddNewAffinity2
Creates and returns a Affinity feature.
### AddNewAssemble
Creates and returns a new assembly operation within the current body.
### AddNewAutoDraft
Creates and returns a new solid autodraft.
AddNewAutoFillet
Creates and returns a new solid autofillet.
### AddNewAxisToAxis2
Creates and returns an AxisToAxis transformation feature.
### AddNewBlend
Creates and returns a new Blend feature.
### AddNewChamfer
Creates and returns a new chamfer within the current body.
AddNewCircPattern
Creates and returns a new circular pattern within the current body.
AddNewCircPatternofList
V5R8 Only: Creates and returns a new circular pattern within the current body using a list of shapes.
AddNewCloseSurface
Creates and returns a new CloseSurface feature.
### AddNewDraft
Creates and returns a new draft within the current body.
AddNewEdgeFilletWithConstantRadius
AddNewEdgeFilletWithVaryingRadius
AddNewFaceFillet
AddNewGSDCircPattern
AddNewGSDRectPattern
AddNewGroove
Creates and returns a new groove within the current body.
### AddNewGrooveFromRef
Creates and returns a new groove within the current body.
#### AddNewHole
Creates and returns a new hole within the current shape. AddNewHoleFromPoint
Creates and returns a new hole within the current shape.
#### AddNewHoleFromRefPoint
Creates and returns a new hole within the current shape. AddNewHoleFromSketch
Creates and returns a new hole within the current shape. AddNewHoleWith2Constraints
Creates and returns a new hole within the current shape.
AddNewHoleWithConstraint
Creates and returns a new hole within the current shape.
#### AddNewIntersect
Creates and returns a new intersect operation within the current body.
AddNewLoft
Creates and returns a new Loft feature.
AddNewMirror
Creates and returns a new mirror within the current body.
#### AddNewPad
Creates and returns a new pad within the current body.
#### AddNewPadFromRef
Creates and returns a new pad within the current body.
#### AddNewPocket
Creates and returns a new pocket within the current shape.
#### AddNewPocketFromRef
Creates and returns a new pocket within the current shape.
#### AddNewRectPattern
Creates and returns a new rectangular pattern within the current body.
#### AddNewRectPatternofList
V5R8 Only: Creates and returns a new rectangular pattern within the current body using a list of shapes.
#### AddNewRemove
Creates and returns a new remove operation within the current body.
#### AddNewRemoveFace
Creates and returns a new RemoveFace feature.
#### AddNewRemovedBlend
Creates and returns a new Removed Blend feature.
AddNewRemovedLoft
Creates and returns a new Removed Loft feature.
#### AddNewReplaceFace
Creates and returns a new Align/ ReplaceFace feature.
#### AddNewRib
Creates and returns a new rib within the current body.
#### AddNewRibFromRef
Creates and returns a new rib within the current body.
#### AddNewScaling
Creates and returns a new scaling within the current body.
#### AddNewSewSurface
Creates and returns a new sewing operation within the current body.
#### AddNewShaft
Creates and returns a new shaft within the current body.
#### AddNewShaftFromRef
Creates and returns a new shaft within the current body.
#### AddNewShell
Creates and returns a new shell within the current body.
#### AddNewSlot
Creates and returns a new slot within the current shape.
#### AddNewSlotFromRef
Creates and returns a new slot within the current shape.
AddNewSolidCombine
Creates and returns a new SolidCombine feature.
AddNewSolidEdgeFilletWithConstantRadius
Creates and returns a new solid edge fillet with a constant radius.
#### AddNewSolidEdgeFilletWithVaryingRadius
Creates and returns a new solid edge fillet with a varying radius.
#### AddNewSolidFaceFillet
#### Creates and returns a new solid face-to-face fillet. AddNewSolidTritangentFillet
Creates and returns a new solid tritangent fillet within the current body.
#### AddNewSplit
Creates and returns a new split operation within the current body.
#### AddNewStiffener
Creates and returns a new stiffener within the current body. AddNewStiffenerFromRef
Creates and returns a new stiffener within the current body.
#### AddNewSurfaceEdgeFilletWithConstantRadius
Creates and returns a new surface edge fillet with a constant radius.
#### AddNewSurfaceEdgeFilletWithVaryingRadius
Creates and returns a new surface edge fillet with a varying radius.
#### AddNewSurfaceFaceFillet
Creates and returns a new surface face-to-face fillet.
#### AddNewSurfaceTritangentFillet
Creates and returns a new surface tritangent fillet within the current body.
AddNewSurfacicAutoFillet
#### Creates and returns a new Surfacic autofillet. AddNewSurfacicCircPattern
Creates and returns a new gsd circular pattern within the current body.
#### AddNewSurfacicRectPattern
Creates and returns a new GSD rectangular pattern within the current body. AddNewSurfacicUserPattern
Creates and returns a new GSD user pattern within the current body.
#### AddNewThickSurface
Creates and returns a new ThickSurface feature.
#### AddNewThickness
Creates and returns a new thickness within the current body.
#### AddNewThreadWithOutRef
Creates and returns a new thread\tap within the current body.
#### AddNewThreadWithRef
Creates and returns a new thread\tap within the current body.
#### AddNewTrim
Creates and returns a new Trim operation within the current body.
#### AddNewTritangentFillet
#### AddNewUserPattern
Creates and returns a new user pattern within the current body.
#### AddNewUserPatternofList
### AddNewGrooveFromRef
V5R8 Only: Creates and returns a new user pattern within the current body using a list of shapes.
#### AddNewVolumeAdd
Creates and returns a Volumic Add feature.
#### AddNewVolumeCloseSurface
Creates and returns a new VolumeCloseSurface feature.
#### AddNewVolumeIntersect
Creates and returns a Volumic Intersect feature.
#### AddNewVolumeRemove
Creates and returns a Volumic Remove feature.
#### AddNewVolumeSewSurface
Creates and returns a new volume sewing operation within the current OGS/GS.
#### AddNewVolumeShell
Creates and returns a Volumic Shell feature.
#### AddNewVolumeThickSurface
Creates and returns a new VolumeThickSurface feature.
#### AddNewVolumeThickness
Creates and returns a volume new thickness within the current GS or OGS.
#### AddNewVolumeTrim
Creates and returns a new Volume Trim operation within the GS/OGS.
#### AddNewVolumicDraft
Creates and returns a new volume draft within the current body.
#### o Func AddNewAdd(CATIABodyiBodyToAdd) As CATIAAdd
Creates and returns a new add operation within the current body.
Parameters:
#### iBodyToAdd
#### The body to add to the current body
Returns:
#### The created add operation
#### o Func AddNewAffinity2(doubleXRatio, doubleYRatio, doubleZRatio) As CATIABase
Creates and returns a Affinity feature.
Parameters:
XRatio
Value for the XRatio.
YRatio
Value for the YRatio.
ZRatio
Value for the ZRatio.
Returns:
the created Affinity feature.
#### o Func AddNewAssemble(CATIABodyiBodyToAssemble) As CATIAAssemble
Creates and returns a new assembly operation within the current body.
Parameters:
#### iBodyToAssemble
The body to assemble with the current body
Returns:
#### The created assembly operation
o Func AddNewAutoDraft(doubleiDraftAngle) As CATIAAutoDraft
#### Creates and returns a new solid autodraft.
Use this method to create autodraft by providing draft angle.
Parameters:
#### iDraftAngle
The draft angle.
Returns:
The created autodraft.
o Func AddNewAutoFillet(doubleiFilletRadius, doubleiRoundRadius) As CATIAAutoFillet
Creates and returns a new solid autofillet. Use this method to create autofillet by providing fillet and round radius values.
Parameters:
#### iFilletRadius
The fillet radius iRoundRadius The round radius
Returns:
The created autofillet o Func AddNewAxisToAxis2(CATIAReferenceiReference, CATIAReferenceiTarget) As CATIABase
Creates and returns an AxisToAxis transformation feature.
Parameters:
#### iReference
The refrence axis.
#### iTarget
The target axis.
Returns:
The created AxisToAxis transformation feature.
#### o Func AddNewBlend( ) As CATIABase
Creates and returns a new Blend feature.
Returns:
#### The created Blend feature
o Func AddNewChamfer(CATIAReference
iObjectToChamfer,
CatChamferPropagationiPropagation,
CatChamferMode
#### iMode,
CatChamferOrientation iOrientation,
double
iLength1,
double
#### iLength2OrAngle) As CATIAChamfer
Creates and returns a new chamfer within the current body.
Parameters:
#### iObjectToChamfer
The first edge or face to chamfer The following
Boundary object is supported: TriDimFeatEdge.
#### iPropagation
Controls if and how the chamfering operation should propagate beyond the first chamfer element iObjectToChamfer, when it is an edge
#### iMode
Controls if the chamfer is defined by two lengthes, or by an angle and a length The value of this argument changes the way the arguments iLength1 and iLength2OrAngle should be interpreted.
#### iOrientation
Defines the relative meaning of arguments iLength1 and iLength2OrAngle when defining a chamfer by two lengthes
iLength1
The first value for chamfer dimensioning. It represents the chamfer first length if the chamfer is defined by two lengthes, or the chamfer length if the chamfer is defined by a length and an angle.
### AddNewGrooveFromRef
#### iLength2OrAngle
The second value for chamfer dimensioning. It represents the chamfer second length if the chamfer is defined by two lengthes, or the chamfer angle if the chamfer is defined by a length and an angle.
Returns:
The created chamfer
o Func AddNewCircPattern(CATIABase iShapeToCopy,
long
iNbOfCopiesInRadialDir,
long
iNbOfCopiesInAngularDir,
double
iStepInRadialDir,
**以下是一个markdown表格**
| double | iStepInAngularDir, |
| --- | --- |
| long | iShapeToCopyPositionAlongRadialDir, |
| long | iShapeToCopyPositionAlongAngularDir, |
| - | CATIAReferenceiRotationCenter, |
| - | CATIAReferenceiRotationAxis, |
| boolean | iIsReversedRotationAxis, |
| double | iRotationAngle, |
| boolean | iIsRadiusAligned) As CATIACircPattern |
Creates and returns a new circular pattern within the current body.
Parameters:
#### iShapeToCopy
The shape to be copied by the circular pattern
#### iNbOfInstancesInRadialDir
The number of times iShapeToCopy will be copied along pattern radial direction iNbOfInstancesInAngularDir
The number of times iShapeToCopy will be copied along pattern angular direction iStepInRadialDir
The distance that will separate two consecutive copies in the pattern along its radial direction
#### iStepInAngularDir
The angle that will separate two consecutive copies in the pattern along its angular direction
#### iShapeToCopyPositionAlongRadialDir
Specifies the position of the original shape iShapeToCopy among its copies along the radial direction
#### iShapeToCopyPositionAlongAngularDir
Specifies the position of the original shape iShapeToCopy among its copies along the angular direction
#### iRotationCenter
The point or vertex that specifies the pattern center of rotation iRotationAxis
The line or linear edge that specifies the axis around which instances will be rotated relative to each other The following
Boundary objects are supported: PlanarFace , CylindricalFace , RectilinearTriDimFeatEdge and RectilinearBiDimFeatEdge.
#### iIsReversedRotationAxis
The boolean flag indicating wether the natural orientation of iRotationAxis should be used to orient the pattern operation. A value of true indicates that iItemToDuplicate are copied in the direction of the natural orientation of iRotationAxis.
#### iRotationAngle
The angle applied to the direction iRotationAxis prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
#### iIsRadiusAligned
The boolean flag that specifies whether the instances of iItemToDuplicate copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
Returns:
The created circular pattern
**以下是一个markdown表格**
| o Func AddNewCircPatternofList(CATIABase | - | iShapeToCopy, |
| --- | --- | --- |
| long | - | iNbOfCopiesInRadialDir, |
| long | - | iNbOfCopiesInAngularDir, |
| double | - | iStepInRadialDir, |
| double | - | iStepInAngularDir, |
| long | - | iShapeToCopyPositionAlongRadialDir, |
| long | - | iShapeToCopyPositionAlongAngularDir, |
CATIAReferenceiRotationCenter,
#### CATIAReferenceiRotationAxis,
**以下是一个markdown表格**
| boolean | iIsReversedRotationAxis, |
| --- | --- |
| double | iRotationAngle, |
| boolean | iIsRadiusAligned) As CATIACircPattern |
V5R8 Only: Creates and returns a new circular pattern within the current body using a list of shapes.
Parameters:
#### iShapeToCopy
The shape to be copied by the circular pattern. Others shapes will be add by put_ItemToCopy with CATIAPattern interface
#### iNbOfInstancesInRadialDir
The number of times iShapeToCopy will be copied along pattern radial direction iNbOfInstancesInAngularDir
The number of times iShapeToCopy will be copied along pattern angular direction iStepInRadialDir
The distance that will separate two consecutive copies in the pattern along its radial direction
### AddNewGrooveFromRef
#### iStepInAngularDir
The angle that will separate two consecutive copies in the pattern along its angular direction
#### iShapeToCopyPositionAlongRadialDir
Specifies the position of the original shape iShapeToCopy among its copies along the radial direction
#### iShapeToCopyPositionAlongAngularDir
Specifies the position of the original shape iShapeToCopy among its copies along the angular direction
#### iRotationCenter
The point or vertex that specifies the pattern center of rotation
#### iRotationAxis
The line or linear edge that specifies the axis around which instances will be rotated relative to each other
#### iIsReversedRotationAxis
The boolean flag indicating wether the natural orientation of iRotationAxis should be used to orient the pattern operation. A value of true indicates that iItemToDuplicate are copied in the direction of the natural orientation of iRotationAxis.
#### iRotationAngle
The angle applied to the direction iRotationAxis prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
#### iIsRadiusAligned
The boolean flag that specifies whether the instances of iItemToDuplicate copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
Returns:
The created circular pattern
o Func AddNewCloseSurface(CATIAReferenceiCloseElement) As CATIACloseSurface
Creates and returns a new CloseSurface feature.
Parameters:
#### iCloseElement
The skin that will be closed and add with the current body
Returns:
#### The created CloseSurface feature
#### o Func AddNewDraft(CATIAReference
CATIAReference
iFaceToDraft,
iNeutral,
#### CatDraftNeutralPropagationModeiNeutralMode,
**以下是一个markdown表格**
| CATIAReference | iParting, |
| --- | --- |
| double | iDirX, |
| double | iDirY, |
| double | iDirZ, |
| CatDraftMode | iMode, |
| double | iAngle, |
| CatDraftMultiselectionMode | iMultiselectionMode) As CATIADraft |
Creates and returns a new draft within the current body.
The draft needs a reference face on the body. This face will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated by the draft angle.
Parameters:
#### iFaceToDraft
The first face to draft in the body. This face should be adjacent to the iFaceToDraft face. If several faces are to be drafted, only the first one is specified here, the others being inferred by propagating the draft operation onto faces adjacent to this first face. This is controlled by the iNeutralMode argument. The following
#### Boundary object is supported: Face.
#### iNeutral
The reference face for the draft. The draft needs a reference face on the body, that will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated according to the draft angle iAngle.
The following
Boundary object is supported: PlanarFace.
#### iNeutralMode
Controls if and how the drafting operation should be propagated beyond the first face to draft iFaceToDraft to other adjacent faces.
#### iParting
The draft parting plane, face or surface. It specifies the element within the body to draft that represents the bottom of the mold. This element can be located either somewhere in the middle of the body or be one of its boundary faces. When located in the middle of the body, it crosses the faces to draft, and as a result, those faces are drafted with a positive angle on one side of the parting surface, and with a negative angle on the other side.
The following
Boundary object is supported: PlanarFace.
iDirX,iDirY,iDirZ
The X, Y, and Z components of the absolute vector representing the drafting direction (i.e. the mold extraction direction).
#### iMode
The draft connecting mode to its reference face iFaceToDraft
iAngle
#### The draft angle
#### iMultiselectionMode.
The elements to be drafted can be selected explicitly or can implicitly selected as neighbors of the neutral face
Returns:
#### The created draft
#### o Func AddNewEdgeFilletWithConstantRadius(
CATIAReference
iEdgeToFillet,
CatFilletEdgePropagationiPropagMode,
double
iRadius) As
CATIAConstRadEdgeFillet
#### Deprecated:
### AddNewGrooveFromRef
V5R14 #AddNewEdgeFilletWithConstantRadius use AddNewSolidEdgeFilletWithConstantRadius or AddNewSurfaceEdgeFilletWithConstantRadius depending on the type of fillet you want to create
**以下是一个markdown表格**
| AddNewEdgeFilletWithVaryingRadius( | CATIAReference | iEdgeToFillet, |
| --- | --- | --- |
| AddNewEdgeFilletWithVaryingRadius( | CatFilletEdgePropagationiPropagMode, | CatFilletEdgePropagationiPropagMode, |
| AddNewEdgeFilletWithVaryingRadius( | CatFilletVariation | iVariationMode, |
| AddNewEdgeFilletWithVaryingRadius( | double | iDefaultRadius) As |
| - | - | CATIAVarRadEdgeFillet |
#### o Func
#### Deprecated:
V5R14 #AddNewEdgeFilletWithVaryingRadius use AddNewSolidEdgeFilletWithVaryingRadius or AddNewSurfaceEdgeFilletWithVaryingRadius depending on the type of fillet you want to create
o Func AddNewFaceFillet(CATIAReferenceiF1,
CATIAReferenceiF2,
#### double iRadius) As CATIAFaceFillet
#### Deprecated:
V5R14 #AddNewFaceFillet use AddNewSolidFaceFillet or AddNewSurfaceFaceFillet depending on the type of fillet you want to create
**以下是一个markdown表格**
| AddNewGSDCircPattern(CATIABase | AddNewGSDCircPattern(CATIABase | iShapeToCopy, |
| --- | --- | --- |
| - | long | iNbOfCopiesInRadialDir, |
| - | long | iNbOfCopiesInAngularDir, |
| - | double | iStepInRadialDir, |
| - | double | iStepInAngularDir, |
| - | long | iShapeToCopyPositionAlongRadialDir, |
| - | long | iShapeToCopyPositionAlongAngularDir, |
| - | - | CATIAReferenceiRotationCenter, |
| - | - | CATIAReferenceiRotationAxis, |
| - | boolean | iIsReversedRotationAxis, |
| - | double | iRotationAngle, |
| - | boolean | iIsRadiusAligned, |
| - | boolean | iCompleteCrown, |
| - | double | iType) As CATIACircPattern |
#### Deprecated:
#### V5R15 #AddNewSurfacicCircPattern
**以下是一个markdown表格**
| o Func AddNewGSDRectPattern(CATIABase | - | iShapeToCopy, |
| --- | --- | --- |
| long | - | iNbOfCopiesInDir1, |
| long | - | iNbOfCopiesInDir2, |
| double | - | iStepInDir1, |
| double | - | iStepInDir2, |
| long | - | iShapeToCopyPositionAlongDir1, |
| long | - | iShapeToCopyPositionAlongDir2, |
| - | CATIAReferenceiDir1, | - |
| - | CATIAReferenceiDir2, | - |
| boolean | - | iIsReversedDir1, |
| boolean | - | iIsReversedDir2, |
| double | - | iRotationAngle, |
| double | - | iType) As CATIARectPattern |
#### Deprecated:
#### V5R15 #AddNewSurfacicRectPattern
#### o Func AddNewGroove(CATIASketchiSketch) As CATIAGroove
Creates and returns a new groove within the current body.
The Revolution, as a supertype for grooves, provides starting and ending angles for the groove definition.
Parameters:
iSketch
The sketch defining the groove section. The sketch must contain a contour and an axis that will be used to rotate the contour in the space, thus defining the groove. The contour has to penetrate in 3D space the current shape.
Returns:
#### The created groove
o Func AddNewGrooveFromRef(CATIAReferenceiProfileElt) As CATIAGroove
Creates and returns a new groove within the current body.
Parameters:
#### iProfileElt
The reference on the element defining the groove base
Returns:
### AddNewGrooveFromRef
#### The created groove
o Func AddNewHole(CATIAReferenceiSupport,
double iDepth) As CATIAHole
Creates and returns a new hole within the current shape. Actual hole shape is defined by editing hole properties after its creation.
Parameters:
#### iSupport
The support defining the hole reference plane. Anchor point is located at the barycenter of the support. The hole axis in 3D passes through that point and is normal to the plane. The following
Boundary object is supported: Face.
iDepth
The hole depth.
Returns:
The created hole
#### o Func AddNewHoleFromPoint(double iX,
double iY,
double iZ,
CATIAReferenceiSupport,
double iDepth) As CATIAHole
Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.
Parameters:
iX
Origin point x absolute coordinate
iY
Origin point y absolute coordinate
iZ
Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
#### iSupport
The support defining the hole reference plane.
The following
Boundary object is supported: Face.
#### iDepth
The hole depth.
Returns:
The created hole
o Func AddNewHoleFromRefPoint(CATIAReferenceiOrigin,
CATIAReferenceiSupport,
double iDepth) As CATIAHole
Creates and returns a new hole within the current shape. Actual hole shape is defined by editing hole properties after its creation.
Parameters:
#### iOrigin
The origin point which the hole is anchored to. iSupport
The support defining the hole reference plane. The following
Boundary object is supported: Face.
#### iDepth
The hole depth.
Returns:
The created hole
o Func AddNewHoleFromSketch(CATIASketchiSketch,
#### double iDepth) As CATIAHole
Creates and returns a new hole within the current shape. Actual hole shape is defined by editing hole properties after its creation.
Parameters:
iSketch
The sketch defining the hole reference plane and anchor point. This sketch must contain a single point that defines the hole axis: the hole axis in 3D passes through that point and is normal to the sketch plane.
#### iDepth
The hole depth.
Returns:
The created hole
#### o Func AddNewHoleWith2Constraints(double iX,
double iY, double iZ, CATIAReferenceiEdge1, CATIAReferenceiEdge2, CATIAReferenceiSupport, double iDepth) As CATIAHole
Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.
Parameters:
iX
Origin point x absolute coordinate
iY
Origin point y absolute coordinate
iZ
Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
iEdge
The edge which the hole is constrained to.
The origin of the hole will have a length constraint with each edge.
The following
Boundary object is supported: TriDimFeatEdge.
#### iSupport
The support defining the hole reference plane.
The following
Boundary object is supported: Face.
#### iDepth
The hole depth.
Returns:
The created hole
o Func AddNewHoleWithConstraint(double iX,
double iY,
double iZ,
CATIAReferenceiEdge,
CATIAReferenceiSupport,
double iDepth) As CATIAHole
Creates and returns a new hole within the current shape.
Actual hole shape is defined by editing hole properties after its creation.
Parameters:
#### iX Origin point x absolute coordinate
iY
Origin point y absolute coordinate
iZ
Origin point z absolute coordinate
Sets the origin point which the hole is anchored to.
If mandatory, the entry point will be projected onto a tangent plane.
iEdge
The edge which the hole is constrained to.
If edge is circular, the origin of the hole will be concentric to the edge (iX, iY, iZ will be overridden). if not, the origin of the hole will have a length constraint with the edge. The following
Boundary object is supported: TriDimFeatEdge.
#### iSupport
The support defining the hole reference plane.
The following
Boundary object is supported: Face.
#### iDepth
The hole depth.
Returns:
The created hole
o Func AddNewIntersect(CATIABodyiBodyToIntersect) As CATIAIntersect
Creates and returns a new intersect operation within the current body.
Parameters:
#### iBodyToIntersect
The body to intersect with the current body
Returns:
The created intersect operation
#### o Func AddNewLoft( ) As CATIABase
Creates and returns a new Loft feature.
Returns:
#### The created Loft feature
o Func AddNewMirror(CATIAReferenceiMirroringElement) As CATIAMirror
Creates and returns a new mirror within the current body.
A mirror allows for transforming existing shapes by a symmetry with respect to an existing plane.
Parameters:
#### iMirroringElement
The plane used by the mirror as the symmetry plane. The following
Boundary object is supported: PlanarFace.
Returns:
#### The created mirror
### AddNewGrooveFromRef
#### o Func AddNewPad(CATIASketchiSketch,
double iHeight) As CATIAPad
Creates and returns a new pad within the current body.
Parameters:
iSketch
The sketch defining the pad base iHeight
#### The pad height
Returns:
#### The created pad
o Func AddNewPadFromRef(CATIAReferenceiProfileElt, double iHeight) As CATIAPad
Creates and returns a new pad within the current body.
Parameters:
iProfileElt The reference on the element defining the pad base iHeight The pad height
Returns:
#### The created pad
o Func AddNewPocket(CATIASketchiSketch, double iHeight) As CATIAPocket
Creates and returns a new pocket within the current shape.
Parameters:
iSketch
The sketch defining the pocket base
#### iDepth
The pocket depth
Returns:
#### The created pocket
#### o Func AddNewPocketFromRef(CATIAReferenceiProfileElt,
double
iHeight) As CATIAPocket
Creates and returns a new pocket within the current shape.
Parameters:
#### iProfileElt
The reference on the element defining the pocket base iDepth
The pocket depth
Returns:
#### The created pocket
o Func AddNewRectPattern(CATIABase iShapeToCopy, long iNbOfCopiesInDir1, long iNbOfCopiesInDir2, double iStepInDir1, double iStepInDir2, long iShapeToCopyPositionAlongDir1, long iShapeToCopyPositionAlongDir2, CATIAReferenceiDir1, CATIAReferenceiDir2, boolean iIsReversedDir1, boolean iIsReversedDir2, double iRotationAngle) As CATIARectPattern
Creates and returns a new rectangular pattern within the current body.
Parameters:
#### iShapeToCopy
The shape to be copied by the rectangular pattern iNbOfCopiesInDir1
The number of times iShapeToCopy will be copied along the pattern first direction iNbOfCopiesInDir2
The number of times iShapeToCopy will be copied along the pattern second direction iStepInDir1
The distance that will separate two consecutive copies in the pattern along its first direction
#### iStepInDir2
The distance that will separate two consecutive copies in the pattern along its second direction
#### iShapeToCopyPositionAlongDir1
Specifies the position of the original shape iShapeToCopy among its copies along iDir1 iShapeToCopyPositionAlongDir2
Specifies the position of the original shape iShapeToCopy among its copies along iDir2 iDir1
The line or linear edge that specifies the pattern first repartition direction The following
Boundary objects are supported: PlanarFace, RectilinearTriDimFeatEdge,
RectilinearBiDimFeatEdge.
iDir2
The line or linear edge that specifies the pattern second repartition direction
The following
Boundary objects are supported: PlanarFace, RectilinearTriDimFeatEdge, RectilinearBiDimFeatEdge. iIsReversedDir1
The boolean flag indicating whether the natural orientation of iDir1 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir1.
iIsReversedDir2
The boolean flag indicating whether the natural orientation of iDir2 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir2.
#### iRotationAngle
The angle applied to both directions iDir1 and iDir2 prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
Returns:
The created rectangular pattern
o Func AddNewRectPatternofList(CATIABase iShapeToCopy,
long iNbOfCopiesInDir1, long iNbOfCopiesInDir2, double iStepInDir1, double iStepInDir2, long iShapeToCopyPositionAlongDir1, long iShapeToCopyPositionAlongDir2, CATIAReferenceiDir1, CATIAReferenceiDir2, boolean iIsReversedDir1, boolean iIsReversedDir2, double iRotationAngle) As CATIARectPattern
V5R8 Only: Creates and returns a new rectangular pattern within the current body using a list of shapes.
Parameters:
#### iShapeToCopy
The shape to be copied by the rectangular pattern Others shapes will be add by put_ItemToCopy with CATIAPattern interface
#### iNbOfCopiesInDir1
The number of times iShapeToCopy will be copied along the pattern first direction iNbOfCopiesInDir2
The number of times iShapeToCopy will be copied along the pattern second direction iStepInDir1
The distance that will separate two consecutive copies in the pattern along its first direction
#### iStepInDir2
The distance that will separate two consecutive copies in the pattern along its second direction
### AddNewGrooveFromRef
#### iShapeToCopyPositionAlongDir1
Specifies the position of the original shape iShapeToCopy among its copies along iDir1 iShapeToCopyPositionAlongDir2
Specifies the position of the original shape iShapeToCopy among its copies along iDir2 iDir1
The line or linear edge that specifies the pattern first repartition direction iDir2
The line or linear edge that specifies the pattern second repartition direction iIsReversedDir1
The boolean flag indicating whether the natural orientation of iDir1 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir1.
iIsReversedDir2
The boolean flag indicating whether the natural orientation of iDir2 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir2.
#### iRotationAngle
The angle applied to both directions iDir1 and iDir2 prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
Returns:
The created rectangular pattern o Func AddNewRemove(CATIABodyiBodyToRemove) As CATIARemove
Creates and returns a new remove operation within the current body.
Parameters:
#### iBodyToRemove
The body to remove from the current body
Returns:
#### The created remove operation
o Func AddNewRemoveFace(CATIAReferenceiKeepFaces, CATIAReferenceiRemoveFaces) As CATIARemoveFace
Creates and returns a new RemoveFace feature.
Parameters:
#### iKeepFaces
The reference of the face to Keep. iRemoveFaces
The reference of the face to Remove.
Returns:
The created RemoveFace feature.
#### o Func AddNewRemovedBlend( ) As CATIABase
Creates and returns a new Removed Blend feature.
Returns:
The created Removed Blend feature
#### o Func AddNewRemovedLoft( ) As CATIABase
Creates and returns a new Removed Loft feature.
Returns:
#### The created Removed Loft feature
o Func AddNewReplaceFace(CATIAReferenceiSplitPlane, CATIAReferenceiRemoveFace, CatSplitSide iSplittingSide) As CATIAReplaceFace
Creates and returns a new Align/ ReplaceFace feature.
Parameters:
#### iSplitPlane
The reference of the element defining the Splitting Plane. iRemoveFace The reference of the Face to Remove. iSplittingSide The specification for which side of the current body should be Align
Returns:
The created Align/ ReplaceFace feature.
o Func AddNewRib(CATIASketchiSketch, CATIASketchiCenterCurve) As CATIARib
Creates and returns a new rib within the current body.
Parameters:
iSketch
The sketch defining the rib section
#### iCenterCurve
The sketched curve that defines the rib center curve. It must cross the section definition sketch iSketch within the inner part of its contour.
Returns:
#### The created rib
o Func AddNewRibFromRef(CATIAReferenceiProfile, CATIAReferenceiCenterCurve) As CATIARib
Creates and returns a new rib within the current body.
Parameters:
#### iProfile
The Profile defining the rib section
#### iCenterCurve
The curve that defines the rib center curve. The following
Boundary object is supported: TriDimFeatEdge.
Returns:
#### The created rib
o Func AddNewScaling(CATIAReferenceiScalingReference, double iFactor) As CATIAScaling
Creates and returns a new scaling within the current body.
Parameters:
#### iScalingReference
The point, plane or face of the current body that will remain fixed during the scaling process: even if the face itself shrinks or expands during the scaling, its supporting plane will remain unchanged after the scaling. The following
Boundary objects are supported: PlanarFace and Vertex.
#### iFactor
#### The scaling factor
Returns:
The created scaling
o Func AddNewSewSurface(CATIAReferenceiSewingElement,
CatSplitSide iSewingSide) As CATIASewing
Creates and returns a new sewing operation within the current body.
Parameters:
#### iSewingElement
The face or skin or surface that will be sewn on the current body iSewingSide
The specification for which side of the current body should be kept at the end of the sewing operation
Returns:
### AddNewGrooveFromRef
#### The created sewing operation
o Func AddNewShaft(CATIASketchiSketch) As CATIAShaft
Creates and returns a new shaft within the current body. The Revolution, as a supertype for shafts, provides starting and ending angles for the shaft definition.
Parameters:
iSketch
The sketch defining the shaft section.
If the shaft applies to the current body, then the sketch must contain a contour and an axis that will be used to rotate the contour in the space, thus defining the shaft.
If the shaft is the first shape defined, there is not current body to apply to. In such a case, the sketch must contain a curve whose end points are linked by an axis. By rotating the curve in the space around the axis, the shaft operation will define a revolution shape. This also works if the sketch contains a closed contour and an axis outside of this contour: in that case a revolution shape will be created, for example a torus.
Returns:
The created shaft
#### o Func AddNewShaftFromRef(CATIAReferenceiProfileElt) As CATIAShaft
Creates and returns a new shaft within the current body.
Parameters:
#### iProfileElt
#### The reference on the element defining the shaft base
Returns:
The created shaft
o Func AddNewShell(CATIAReferenceiFaceToRemove,
**以下是一个markdown表格**
| double iInternalThickness, | double iInternalThickness, | double iInternalThickness, |
| --- | --- | --- |
| double | iExternalThickness) As CATIAShell | - |
Creates and returns a new shell within the current body.
Parameters:
#### iFaceToRemove
The first face to be removed in the shell process. The following
Boundary object is supported: Face.
#### iInternalThickness
The thickness of material to be added on the internal side of all the faces during the shell process, except for those to be removed
#### iExternaThickness
The thickness of material to be added on the external side of all the faces during the shell process, except for those to be removed
Returns:
#### The created shell
#### o Func AddNewSlot(CATIASketchiSketch, CATIASketchiCenterCurve) As CATIASlot
Creates and returns a new slot within the current shape.
Parameters:
iSketch
#### The sketch defining the slot section
#### iCenterCurve
The sketched curve that defines the slot center curve. It must cross the section definition sketch iSketch within the inner part of its contour.
Returns:
#### The created slot
o Func AddNewSlotFromRef(CATIAReferenceiProfile, CATIAReferenceiCenterCurve) As CATIASlot
Creates and returns a new slot within the current shape.
Parameters:
#### iProfile
The sketch defining the slot section iCenterCurve The curve that defines the slot center curve. The following
Boundary object is supported: TriDimFeatEdge.
Returns:
#### The created slot
#### o Func AddNewSolidCombine(CATIAReferenceiProfileEltFirst, CATIAReferenceiProfileEltSecond) As CATIASolidCombine
#### Creates and returns a new SolidCombine feature.
Parameters:
#### iProfileEltFirst
The reference of the element defining the profile for first component.
#### iProfileEltSecond
The reference of the element defining the profile for second component.
Returns:
The created SolidCombine feature.
**以下是一个markdown表格**
| 0runIC AddNewSolidEdgeFilletWithConstantRadius( | CATIAReference | iEdgeToFillet |
| --- | --- | --- |
| 0runIC AddNewSolidEdgeFilletWithConstantRadius( | CatFilletEdgePropagation iPropagMode, | CatFilletEdgePropagation iPropagMode, |
| 0runIC AddNewSolidEdgeFilletWithConstantRadius( | double | iRadius) As |
| - | - | CATIAConstRadEdgeFillet |
o Func
Creates and returns a new solid edge fillet with a constant radius. within the current body.
Parameters:
#### iEdgeToFillet
The edge that will be filleted first The following
Boundary object is supported: TriDimFeatEdge.
#### iPropagMode
Controls whether other edges found adjacent to the first one should also be filleted in the same operation
iRadius
The fillet radius
### AddNewGrooveFromRef
Returns:
The created edge fillet
**以下是一个markdown表格**
| AddNewSolidEdgeFilletWithVaryingRadius( | CATIAReference | iEdgeToFillet, |
| --- | --- | --- |
| AddNewSolidEdgeFilletWithVaryingRadius( | CatFilletEdgePropagationiPropagMode, | CatFilletEdgePropagationiPropagMode, |
| AddNewSolidEdgeFilletWithVaryingRadius( | CatFilletVariation | iVariationMode, |
| AddNewSolidEdgeFilletWithVaryingRadius( | double | iDefaultRadius) As |
| - | - | CATIAVarRadEdgeFillet |
o Func
Creates and returns a new solid edge fillet with a varying radius. within the current body.
Parameters:
#### iEdgeToFillet
The edge that will be filleted first The following
Boundary object is supported: TriDimFeatEdge.
#### iPropagMode
Controls whether other edges found adjacent to the first one should also be filleted in the same operation
#### iVariationMode
Controls the law of evolution for the fillet radius between specified control points, such as edges extremities
#### iDefaultRadius
The fillet default radius, that will apply when no other radius can be inferred from the iVariationMode parameter
Returns:
The created edge fillet
o Func AddNewSolidFaceFillet(CATIAReferenceiF1,
CATIAReferenceiF2,
double iRadius) As CATIAFaceFillet
Creates and returns a new solid face-to-face fillet.
Use this method to created face-to-face fillets with varying fillet radii, by editing fillet attributes driving its radius after its creation.
Parameters:
iF1
The first face that will support the fillet The following
Boundary object is supported: Face.
iF2
The second face that will support the fillet
The following
Boundary object is supported: Face.
iRadius
The fillet radius
Returns:
#### The created face-to-face fillet
o Func AddNewSolidTritangentFillet(CATIAReferenceiF1,
CATIAReferenceiF2,
CATIAReferenceiRemovedFace) As CATIATritangentFillet
Creates and returns a new solid tritangent fillet within the current body.
This kind of fillet begins with tangency on a first face iF1, gets tangent to a second one iRemovedFace and ends with tangency to a third one iF2. During the process the second face iRemovedFace is removed.
Parameters:
iF1
The starting face for the fillet The following
Boundary object is supported: Face.
iF2
#### The ending face for the fillet
The following
Boundary object is supported: Face.
#### iRemovedFace
The face used as an intermediate tangent support for the fillet during its course from iF1 to iF2. This face will be removed at the end of the filleting operation.
The following
Boundary object is supported: Face
Returns:
The created tritangent fillet
o Func AddNewSplit(CATIAReferenceiSplittingElement, CatSplitSide iSplitSide) As CATIASplit
Creates and returns a new split operation within the current body.
Parameters:
iSplittingElement The face or plane that will split the current body The following
Boundary object is supported: Face.
#### iSplitSide
The specification for which side of the current body should be kept at the end of the split operation
Returns:
#### The created split operation
o Func AddNewStiffener(CATIASketchiSketch) As CATIAStiffener
Creates and returns a new stiffener within the current body.
A stiffener is made up of a sketch used as the stiffener profile, that is extruded (offset) and that fills the nearest shape.
Parameters:
iSketch
The sketch defining the stiffener border. It must contain a line or a curve that does not cross in 3D space the face(s) to stiffen.
Returns:
The created stiffener
o Func AddNewStiffenerFromRef(CATIAReferenceiProfileElt) As CATIAStiffener
Creates and returns a new stiffener within the current body.
Parameters:
#### iProfileElt
The reference on the element defining the stiffener profile
Returns:
The created stiffener
**以下是一个markdown表格**
| 0 Func AddNewSurfaceEdgeFilletWithConstantRadius( | CATIAReference | iEdgeToFillet, |
| --- | --- | --- |
| 0 Func AddNewSurfaceEdgeFilletWithConstantRadius( | CatFilletEdgePropagation iPropagMode, | CatFilletEdgePropagation iPropagMode, |
| 0 Func AddNewSurfaceEdgeFilletWithConstantRadius( | double | iRadius) As |
| - | - | CATIAConstRadEdgeFillet |
#### o Func
Creates and returns a new surface edge fillet with a constant radius. within the current body.
Parameters:
#### iEdgeToFillet
The edge that will be filleted first The following
Boundary object is supported: TriDimFeatEdge.
### AddNewGrooveFromRef
#### iPropagMode
Controls whether other edges found adjacent to the first one should also be filleted in the same operation
iRadius
The fillet radius
Returns:
The created edge fillet
**以下是一个markdown表格**
| AddNewSurfaceEdgeFilletWithVaryingRadius( | CATIAReference | iEdgeToFillet, |
| --- | --- | --- |
| AddNewSurfaceEdgeFilletWithVaryingRadius( | CatFilletEdgePropagationiPropagMode, | CatFilletEdgePropagationiPropagMode, |
| AddNewSurfaceEdgeFilletWithVaryingRadius( | CatFilletVariation | iVariationMode, |
| - | double | iDefaultRadius) As |
| - | - | CATIAVarRadEdgeFillet |
#### o Func
Creates and returns a new surface edge fillet with a varying radius. within the current body.
Parameters:
iEdgeToFillet The edge that will be filleted first The following
Boundary object is supported: TriDimFeatEdge.
#### iPropagMode
Controls whether other edges found adjacent to the first one should also be filleted in the same operation
#### iVariationMode
Controls the law of evolution for the fillet radius between specified control points, such as edges extremities
#### iDefaultRadius
The fillet default radius, that will apply when no other radius can be inferred from the iVariationMode parameter
Returns:
The created edge fillet
o Func AddNewSurfaceFaceFillet(CATIAReferenceiF1,
CATIAReferenceiF2,
double iRadius) As CATIAFaceFillet
Creates and returns a new surface face-to-face fillet.
Use this method to created face-to-face fillets with varying fillet radii, by editing fillet attributes driving its radius after its creation.
Parameters:
iF1
The first face that will support the fillet
The following
Boundary object is supported: Face.
iF2
The second face that will support the fillet
The following
Boundary object is supported: Face.
iRadius
The fillet radius
Returns:
#### The created face-to-face fillet
o Func AddNewSurfaceTritangentFillet(CATIAReferenceiF1,
CATIAReferenceiF2,
CATIAReferenceiRemovedFace) As CATIATritangentFillet
Creates and returns a new surface tritangent fillet within the current body.
This kind of fillet begins with tangency on a first face iF1, gets tangent to a second one iRemovedFace and ends with tangency to a third one iF2. During the process the second face iRemovedFace is removed.
Parameters:
iF1
The starting face for the fillet The following
Boundary object is supported: Face.
iF2
The ending face for the fillet
The following
Boundary object is supported: Face.
iRemovedFace
The face used as an intermediate tangent support for the fillet during its course from iF1 to iF2. This face will be removed at the end of the filleting operation.
The following
Boundary object is supported: Face
Returns:
The created tritangent fillet
o Func AddNewSurfacicAutoFillet(doubleiFilletRadius) As CATIAAutoFillet
Creates and returns a new Surfacic autofillet. Use this method to create autofillet by providing fillet radius value.
Parameters:
#### iFilletRadius The fillet radius
Returns:
#### The created autofillet
**以下是一个markdown表格**
| o Func AddNewSurfacicCircPattern(CATIABase | - | iShapeToCopy, |
| --- | --- | --- |
| long | - | iNbOfCopiesInRadialDir, |
| long | - | iNbOfCopiesInAngularDir, |
| double | - | iStepInRadialDir, |
| double | - | iStepInAngularDir, |
| long | - | iShapeToCopyPositionAlongRadialDir, |
| long | - | iShapeToCopyPositionAlongAngularDir, |
| - | - | CATIAReferenceiRotationCenter, |
| - | - | CATIAReferenceiRotationAxis, |
| boolean | - | iIsReversedRotationAxis, |
| double | - | iRotationAngle, |
| boolean | - | iIsRadiusAligned, |
| boolean | - | iCompleteCrown) As CATIACircPattern |
Creates and returns a new gsd circular pattern within the current body.
Parameters:
#### iShapeToCopy
The shape to be copied by the circular pattern
### AddNewGrooveFromRef
#### iNbOfInstancesInRadialDir
The number of times iShapeToCopy will be copied along pattern radial direction iNbOfInstancesInAngularDir
The number of times iShapeToCopy will be copied along pattern angular direction iStepInRadialDir
The distance that will separate two consecutive copies in the pattern along its radial direction
#### iStepInAngularDir
The angle that will separate two consecutive copies in the pattern along its angular direction
#### iShapeToCopyPositionAlongRadialDir
Specifies the position of the original shape iShapeToCopy among its copies along the radial direction
#### iShapeToCopyPositionAlongAngularDir
Specifies the position of the original shape iShapeToCopy among its copies along the angular direction
#### iRotationCenter
The point or vertex that specifies the pattern center of rotation
#### iRotationAxis
The line or linear edge that specifies the axis around which instances will be rotated relative to each other
The following
Boundary objects are supported: PlanarFace , CylindricalFace , RectilinearTriDimFeatEdge and RectilinearBiDimFeatEdge. iIsReversedRotationAxis
The boolean flag indicating wether the natural orientation of iRotationAxis should be used to orient the pattern operation. A value of true indicates that iItemToDuplicate are copied in
the direction of the natural orientation of iRotationAxis.
#### iRotationAngle
The angle applied to the direction iRotationAxis prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a circular pattern relatively to existing geometry, but not necessarily parallel to it.
#### iIsRadiusAligned
The boolean flag that specifies whether the instances of iItemToDuplicate copied by the pattern should be kept parallel to each other (True) or if they should be aligned with the radial direction they lie upon (False).
#### iCompleteCrown
The boolean flag specifies the mode of angular distribution. True indicates that the angular step will be equal to 360 degrees iNba.
Returns:
The created circular pattern
**以下是一个markdown表格**
| Func AddNewSurfacicRectPattern(CATIABase | - | iShapeToCopy, |
| --- | --- | --- |
| - | long | iNbOfCopiesInDir1, |
| - | long | iNbOfCopiesInDir2, |
| - | double | iStepInDir1, |
| - | double | iStepInDir2, |
| - | long | iShapeToCopyPositionAlongDir1, |
| - | long | iShapeToCopyPositionAlongDir2, |
| - | CATIAReferenceiDir1, | CATIAReferenceiDir1, |
| - | CATIAReferenceiDir2, | CATIAReferenceiDir2, |
| - | boolean | iIsReversedDir1, |
| - | boolean | iIsReversedDir2, |
| - | double | iRotationAngle) As CATIARectPattern |
Creates and returns a new GSD rectangular pattern within the current body.
Parameters:
#### iShapeToCopy
The shape to be copied by the rectangular pattern iNbOfCopiesInDir1
The number of times iShapeToCopy will be copied along the pattern first direction iNbOfCopiesInDir2
The number of times iShapeToCopy will be copied along the pattern second direction iStepInDir1
The distance that will separate two consecutive copies in the pattern along its first direction
#### iStepInDir2
The distance that will separate two consecutive copies in the pattern along its second direction
#### iShapeToCopyPositionAlongDir1
Specifies the position of the original shape iShapeToCopy among its copies along iDir1 iShapeToCopyPositionAlongDir2
Specifies the position of the original shape iShapeToCopy among its copies along iDir2 iDir1
The line or linear edge that specifies the pattern first repartition direction The following
Boundary objects are supported: PlanarFace, RectilinearTriDimFeatEdge,
RectilinearBiDimFeatEdge.
iDir2
The line or linear edge that specifies the pattern second repartition direction
The following
Boundary objects are supported: PlanarFace, RectilinearTriDimFeatEdge, RectilinearBiDimFeatEdge.
### AddNewGrooveFromRef
#### iIsReversedDir1
The boolean flag indicating whether the natural orientation of iDir1 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir1.
iIsReversedDir2
The boolean flag indicating whether the natural orientation of iDir2 should be used to orient the pattern operation. True indicates that iShapeToCopy is copied in the direction of the natural orientation of iDir2.
#### iRotationAngle
The angle applied to both directions iDir1 and iDir2 prior to applying the pattern. The original shape iShapeToCopy is used as the rotation center. Nevertheless, the copied shapes themselves are not rotated. This allows the definition of a rectangular pattern relatively to existing geometry, but not necessarily parallel to it.
Returns:
The created rectangular pattern
#### o Func AddNewSurfacicUserPattern(CATIABaseiShapeToCopy, long iNbOfCopies) As CATIAUserPattern
Creates and returns a new GSD user pattern within the current body.
Parameters:
#### iShapeToCopy
The shape to be copied by the user pattern iNbOfCopies
#### The number of times iShapeToCopy will be copied
Returns:
#### The created user pattern
o Func AddNewThickSurface(CATIAReferenceiOffsetElement,
**以下是一个markdown表格**
| long | - | iIsensOffset, |
| --- | --- | --- |
| double | - | iTopoffset, |
| double | - | iBotoffset) As CATIAThickSurface |
Creates and returns a new ThickSurface feature.
Parameters:
#### iOffsetElement
The skin that will be thicken and added with the current body
iIsensOffset
#### The direction of the offset in regard to the direction of the normal iTopOffset
The Offset between the iOffsetElement and the upper skin of the resulting feature iBotOffset
The Offset between the iOffsetElement and the lower skin of the resulting feature
Returns:
#### The created ThickSurface feature
o Func AddNewThickness(CATIAReferenceiFaceToThicken, double iOffset) As CATIAThickness
Creates and returns a new thickness within the current body.
Parameters:
#### iFaceToThicken
The first face to thicken in the thickening process.
New faces to thicken can be added to the thickness afterwards by using methods offered by the created thickness
The following
Boundary object is supported: Face.
iOffset
The thickness of material to be added on the external side of the face iFaceToThicken during the thickening process
Returns:
The created thickness
#### o Func AddNewThreadWithOutRef( ) As CATIAThread
Creates and returns a new thread\tap within the current body.
Returns:
#### The created Thread
o Func AddNewThreadWithRef(CATIAReferenceiLateralFace, CATIAReferenceiLimitFace) As CATIAThread
Creates and returns a new thread\tap within the current body.
Parameters:
#### iLateralFace
The Face defining the support of thread\tap The following
Boundary object is supported: Face.
#### iLimitFacee
The Face defining the origin of the thread.
The following
Boundary object is supported: PlanarFace.
Returns:
#### The created Thread
o Func AddNewTrim(CATIABodyiBodyToTrim) As CATIATrim
Creates and returns a new Trim operation within the current body.
Parameters:
#### iBodyToTrim
The body to Trim with current body.
Returns:
#### The created Trim operation
o Func AddNewTritangentFillet(CATIAReferenceiF1,
CATIAReferenceiF2, CATIAReferenceiRemovedFace) As CATIATritangentFillet
#### Deprecated:
### AddNewGrooveFromRef
V5R14 #AddNewTritangentFillet use AddNewSolidTritangentFillet or AddNewSurfaceTritangentFillet depending on the type of fillet you want to create
o Func AddNewUserPattern(CATIABaseiShapeToCopy,
long
iNbOfCopies) As CATIAUserPattern
Creates and returns a new user pattern within the current body.
Parameters:
##### iShapeToCopy
The shape to be copied by the user pattern iNbOfCopies
The number of times iShapeToCopy will be copied
Returns:
##### The created user pattern
o Func AddNewUserPatternofList(CATIABaseiShapeToCopy,
long iNbOfCopies) As CATIAUserPattern
V5R8 Only: Creates and returns a new user pattern within the current body using a list of shapes.
Parameters:
##### iShapeToCopy
##### The shape to be copied by the user pattern Others shapes will be add by put_ItemToCopy with CATIAPattern interface iNbOfCopies
##### The number of times iShapeToCopy will be copied
Returns:
##### The created user pattern
o Func AddNewVolumeAdd(CATIAReferenceiBody1,
CATIAReferenceiBody2,
double
iType) As CATIAAdd
Creates and returns a Volumic Add feature.
Parameters:
##### iBody1
The volume or body to be modified. iBody2
The volume or body to be operated. iType
iType = 0 if Part Design, = 4 if GSD.
Returns:
The created Volumic Add feature.
o Func AddNewVolumeCloseSurface(CATIAReferenceiCloseElement) As CATIACloseSurface
Creates and returns a new VolumeCloseSurface feature.
Parameters:
##### iCloseElement
The skin that will be closed and add with the current body
Returns:
##### The created CloseSurface feature
o Func AddNewVolumeIntersect(CATIAReferenceiBody1, CATIAReferenceiBody2, double iType) As CATIAIntersect
Creates and returns a Volumic Intersect feature.
Parameters:
##### iBody1
The volume or body to be modified. iBody2
The volume or body to be operated.
##### iType
iType = 0 if Part Design, = 4 if GSD.
Returns:
The created Volumic Intersect feature.
o Func AddNewVolumeRemove(CATIAReferenceiBody1, CATIAReferenceiBody2, double iType) As CATIARemove
Creates and returns a Volumic Remove feature.
Parameters:
##### iBody1
The volume or body to be modified.
##### iBody2
The volume or body to be operated. iType
iType = 0 if Part Design, = 4 if GSD.
Returns:
The created Volumic Remove feature.
o Func AddNewVolumeSewSurface( long
iType,
CATIAReferenceiSupportVolume,
CATIAReferenceiSewingElement,
CatSplitSide iSewingSide) As CATIASewing
Creates and returns a new volume sewing operation within the current OGS/GS.
Parameters:
##### iType
Parameter to determine the sewing type. For Volume sewing Type = 4 iSupportVolume
The volume support on which sew operation will be performed iSewingElement
The face or skin or surface that will be sewn on the current volume support iSewingSide
The specification for which side of the current volume should be kept at the end of the sewing operation
Returns:
##### The created sewing operation
##### o Func AddNewVolumeShell(CATIAReferenceiFaceToRemove,
**以下是一个markdown表格**
| double | - | iInternalThickness, |
| --- | --- | --- |
| double | - | iExternalThickness, |
Creates and returns a Volumic Shell feature.
Parameters:
##### iFacesToRemove
##### The Faces of the Volume
##### iFacesToThicken
##### The Faces of the Volume
##### iInternalThickness
The thickness of material to be added on the internal side of all the faces during the shell process, except for those to be removed iExternaThickness
The thickness of material to be added on the external side of all the faces during the shell process, except for those to be removed
##### iVolumeSupport
The Volume related the faces to remove and faces to thicken
Returns:
The created Volumic Shell.
o Func AddNewVolumeThickSurface(CATIAReferenceiOffsetElement,
**以下是一个markdown表格**
| long | iIsensOffset, |
| --- | --- |
| double | iTopOffset, |
| double | iBotOffset) As CATIAThickSurface |
Creates and returns a new VolumeThickSurface feature.
Parameters:
### AddNewGrooveFromRef
##### iOffsetElement
The skin that will be thicken and added with the current OGS/GS
iIsensOffset
The direction of the offset in regard to the direction of the normal iTopOffset
The Offset between the iOffsetElement and the upper skin of the resulting feature iBotOffset
The Offset between the iOffsetElement and the lower skin of the resulting feature
Returns:
##### The created ThickSurface feature
o Func AddNewVolumeThickness(CATIAReferenceiFaceToThicken,
**以下是一个markdown表格**
| double | - | ioffset, |
| --- | --- | --- |
| long | - | iType, |
| - | - | CATIAReference iVol umeSupport) As CATIAThickness |
Creates and returns a volume new thickness within the current GS or OGS.
Parameters:
##### iFaceToThicken
The first face to thicken in the thickening process.
New faces to thicken can be added to the thickness afterwards by using methods offered by the created thickness
The following
Boundary object is supported: Face.
##### iOffset
The thickness of material to be added on the external side of the face iFaceToThicken during the thickening process
##### iType
The mode of thickness creation (4=Volume) iVolumeSupport
##### The support volume for volumic draft
Returns:
The created thickness
o Func AddNewVolumeTrim(CATIAReferenceiSupportVolume, CATIAReferenceiCuttingVolume) As CATIATrim
Creates and returns a new Volume Trim operation within the GS/OGS.
Parameters:
##### iSupportVolume
The Support Volume iCutttingVolume The trimming Volume
Returns:
##### The created Trim operation
**以下是一个markdown表格**
| o Func AddNewVolumicDraft(CATIAReference | - | iFaceToDraft, |
| --- | --- | --- |
| o Func AddNewVolumicDraft(CATIAReference | CATIAReference | iNeutral, |
| o Func AddNewVolumicDraft(CATIAReference | CatDraftNeutralPropagationModeiNeutralMode, | CatDraftNeutralPropagationModeiNeutralMode, |
| o Func AddNewVolumicDraft(CATIAReference | CATIAReference | iParting, |
| o Func AddNewVolumicDraft(CATIAReference | double | iDirX, |
| o Func AddNewVolumicDraft(CATIAReference | double | iDirY, |
| o Func AddNewVolumicDraft(CATIAReference | double | iDirZ, |
| o Func AddNewVolumicDraft(CATIAReference | CatDraftMode | iMode, |
| o Func AddNewVolumicDraft(CATIAReference | double | iAngle, |
| o Func AddNewVolumicDraft(CATIAReference | CatDraftMultiselectionMode | iMultiselectionMode, |
| o Func AddNewVolumicDraft(CATIAReference | long | iType, |
| o Func AddNewVolumicDraft(CATIAReference | CATIAReference | iVolumeSupport) As CATIADraft |
Creates and returns a new volume draft within the current body.
The draft needs a reference face on the body. This face will remain unchanged in the draft operation,
while faces adjacent to it and specified for drafting will be rotated by the draft angle.
Parameters:
##### iFaceToDraft
The first face to draft in the body. This face should be adjacent to the iFaceToDraft face. If several faces are to be drafted, only the first one is specified here, the others being inferred by propagating the draft operation onto faces adjacent to this first face. This is controlled by the iNeutralMode argument. The following
Boundary object is supported: Face.
##### iNeutral
The reference face for the draft. The draft needs a reference face on the body, that will remain unchanged in the draft operation, while faces adjacent to it and specified for drafting will be rotated according to the draft angle iAngle.
The following
Boundary object is supported: PlanarFace.
##### iNeutralMode
Controls if and how the drafting operation should be propagated beyond the first face to draft iFaceToDraft to other adjacent faces.
##### iParting
The draft parting plane, face or surface. It specifies the element within the body to draft that represents the bottom of the mold. This element can be located either somewhere in the middle of the body or be one of its boundary faces. When located in the middle of the body, it crosses the faces to draft, and as a result, those faces are drafted with a positive angle on one side of the parting surface, and with a negative angle on the other side.
The following
Boundary object is supported: PlanarFace.
### AddNewGrooveFromRef
iDirX,iDirY,iDirZ
The X, Y, and Z components of the absolute vector representing the drafting direction (i.e. the mold extraction direction).
##### iMode
The draft connecting mode to its reference face iFaceToDraft
iAngle
##### The draft angle
iMultiselectionMode.
The elements to be drafted can be selected explicitly or can implicitly selected as neighbors of the neutral face
##### iType
The mode of draft creation (4=Volume) iVolumeSupport
##### The support volume for volumic draft
Returns:
##### The created draft
